# Hilt
## Dependencies
[Dependency injection with Hilt in Android development | by Tomáš Repčík | Medium](https://tomas-repcik.medium.com/dependency-injection-with-hilt-in-android-development-e23fc636d65c)
``` project-level build.gradle
plugins {  
	id("com.google.dagger.hilt.android") version "2.56.1" apply false
}
```

``` app-level build.gradle
plugins {  
	id("kotlin-kapt")  
	id("com.google.dagger.hilt.android")  
}  
  
android {  
	compileOptions {  
		sourceCompatibility JavaVersion.VERSION_1_8  
		targetCompatibility JavaVersion.VERSION_1_8  
	}  
}  
  
dependencies {  
	// For hilt Implementation  
	val hilt_version = "2.56.1"  
	implementation("com.google.dagger:hilt-android:$hilt_version")  
	kapt("com.google.dagger:hilt-android-compiler:$hilt_version") 
	  
	// For instrumentation tests  
	androidTestImplementation "com.google.dagger:hilt-android-testing:2.51.1"  
	kaptAndroidTest "com.google.dagger:hilt-android-compiler:2.51.1"  
	  
	// For local unit tests  
	testImplementation 'com.google.dagger:hilt-android-testing:2.51.1'  
	kaptTest 'com.google.dagger:hilt-compiler:2.51.1'  
}  
  
kapt {  
	correctErrorTypes = true  
}
```
## Boilerplate
#### Application class 
https://developer.android.com/training/dependency-injection/hilt-android#application-class
```
@HiltAndroidApp
class ExampleApplication : Application() { ... }
```

``` Manifest
<application
...
android:name=".ExampleApplication"
/>
```

## Inject into
#### Activity
https://developer.android.com/training/dependency-injection/hilt-android#android-classes
```
@AndroidEntryPoint
class ExampleActivity : AppCompatActivity() { ... }
```
#### constructor
```
class PokeApiRemoteRepositoryImpl @Inject constructor(private val pokeApiDatasource: PokeApiDatasource)
```
## Как подключить hilt
https://developer.android.com/training/dependency-injection/hilt-android - не работает
[Dependency injection with Hilt in Android development | by Tomáš Repčík | Medium](https://tomas-repcik.medium.com/dependency-injection-with-hilt-in-android-development-e23fc636d65c)
## Пример проекта с di
https://youtu.be/23sm4HSdDfI?si=E-nf5vFfXa0wsbhV
https://github.com/AlexGladkov/TransportApp/blob/master/presentation/src/main/java/com/agladkov/presentation/screens/cities/CitiesViewModel.kt
## Hilt
https://www.youtube.com/watch?v=WzqHHTks1NE
## Как добавить в проект
https://developer.android.com/training/dependency-injection/hilt-android

## Hilt visible empty constructor
https://stackoverflow.com/questions/70661944/modules-that-need-to-be-instantiated-by-hilt-must-have-a-visible-empty-construc
## Hilt context
https://stackoverflow.com/questions/63072927/how-to-inject-application-context-in-a-repository-with-hilt
## Hilt viewModel
https://stackoverflow.com/questions/68167211/hilt-how-to-inject-viewmodel-interface
## Hilt singleton viewmodel
[android - Hilt creating different instances of view model inside same activity - Stack Overflow](https://stackoverflow.com/questions/62560019/hilt-creating-different-instances-of-view-model-inside-same-activity)
## Plugin [id: 'com.google.devtools.ksp'] was not found in any of the following sources:
Более того, ksp не поддерживает hilt
[Kotlin Symbol Processing API | Kotlin Documentation](https://kotlinlang.org/docs/ksp-overview.html#supported-libraries)
## hilt deal with duplicate bindings
[android - Hilt dependency injection Duplicate Bindings Error - Stack Overflow](https://stackoverflow.com/questions/74005162/hilt-dependency-injection-duplicate-bindings-error)

```kotlin
@Provides
@Singleton
@Named("products") // 👈
fun provideProductsRef(db: FirebaseFirestore) = db.collection("products")

@Provides
@Singleton
@Named("categories") // 👈
fun provideCategoriesRef(db: FirebaseFirestore) = db.collection("categories")

```
как такие потом использовать
```kotlin
@Provides
@Singleton
fun provideProductRepository(
  @Named("products") // 👈
  productsRef: CollectionReference,
  @Named("categories") // 👈
  categoriesRef: CollectionReference,
  @Named("cart") // 👈
  cartRef: CollectionReference
): ProductRepository = ProductRepositoryImpl(productsRef, categoriesRef, cartRef)
```