# Dagger2
## Как подключить #гайд
#### 1. Добавить в libs.versions.toml
```
[versions]
ksp = "2.0.21-1.0.27"
dagger = "2.56.2"


[libraries]
dagger = { module = "com.google.dagger:dagger", version.ref = "dagger" }
dagger-compiler = { module = "com.google.dagger:dagger-compiler", version.ref = "dagger" }

[plugins]
google-devtools-ksp = { id = "com.google.devtools.ksp", version.ref = "ksp" }

```
#### 2. build.gradle (package)
```
plugins{
	alias(libs.plugins.google.devtools.ksp) apply false
}
```
#### 3. build.gradle (module)
```
plugins {
    alias(libs.plugins.google.devtools.ksp)
}

dependencies {   
	implementation(libs.dagger)
	ksp(libs.dagger.compiler)
}
```
## Dagger multimodule clean


## Как подключить dagger
[курс Dagger 2 (1)](https://www.youtube.com/watch?v=1dOsef2ZzQ8&list=PL0SwNXKJbuNkYFUda5rlA-odAVyWItRCP&index=2)
3:43
в gradle.build.kts (app):
plugins:
id("kotlin-kapt")
dependencies:
implementation(libs.dagger)  
kapt(libs.dagger.compiler)
## Dagger и KSP (alpha)
[Dagger KSP](https://dagger.dev/dev-guide/ksp.html)
[Migrate from kapt to KSP  |  Android Studio  |  Android Developers](https://developer.android.com/build/migrate-to-ksp)
[Android Kotlin KSP plugin with Gradle Catalogs - Stack Overflow](https://stackoverflow.com/questions/77375240/android-kotlin-ksp-plugin-with-gradle-catalogs)

| Источник                                                                                                               | Информация                                                                                                                                               |
| ---------------------------------------------------------------------------------------------------------------------- | -------------------------------------------------------------------------------------------------------------------------------------------------------- |
| [Dependency injection in Android  \|  Android Developers](https://developer.android.com/training/dependency-injection) | DI бывает разный. Руками или библиотекой. Dagger или Hilt(поверх dagger).                                                                                |
| [Перегрузка операторов](https://kotlinlang.ru/docs/operator-overloading.html)                                          | operator fun - переопределение оператора                                                                                                                 |
| [Изолированные классы](https://kotlinlang.ru/docs/sealed-classes.html)                                                 | sealed класс - клиенты класса из других библиотек не смогут отнаследоваться и расширить функциональность                                                 |
| [ссылка](https://stackoverflow.com/questions/2929562/register-application-class-in-manifest)                           | Указать класс Application в манифесте                                                                                                                    |
| [Dagger](https://dagger.dev/)                                                                                          |                                                                                                                                                          |
| [курс Dagger 2 (1)](https://www.youtube.com/watch?v=1dOsef2ZzQ8&list=PL0SwNXKJbuNkYFUda5rlA-odAVyWItRCP&index=2)       | Что такое DI. Технология процессинга аннотаций из java - генерит новый код на основе аннотаций. Dagger- библиотека + процессор аннотаций. kapt - плагин. |
| [курс Dagger 2 (2)](https://www.youtube.com/watch?v=xif-1cnSHxs&list=PL0SwNXKJbuNkYFUda5rlA-odAVyWItRCP&index=3)       |                                                                                                                                                          |
## DI контекста
[dependency injection - Dagger 2 injecting Android Application Context - Stack Overflow](https://stackoverflow.com/questions/30692501/dagger-2-injecting-android-application-context)
+идея про класс насл от Application, в котором и создается AppComponent
https://search.app?link=https%3A%2F%2Fhabr.com%2Fru%2Fcompanies%2Fwrike%2Farticles%2F569918%2F&utm_campaign=aga&utm_source=agsadl1%2Csh%2Fx%2Fgs%2Fm2%2F4 - 5 способ
[Assisted Injection](https://dagger.dev/dev-guide/assisted-injection.html)
## Inject в viewModel
-- [Dagger2 и архитектурный компонент «ViewModel» / Хабр](https://habr.com/ru/articles/337320/)-- старый код
[Dagger 2 and Jetpack Compose Integration | by Alexey Glukharev | ProAndroidDev](https://proandroiddev.com/dagger-2-and-jetpack-compose-integration-8a8d424ffdb4) - в composable
## Dagger retrofit network module
[android - How should I use Dagger2 with Retrofit? - Stack Overflow](https://stackoverflow.com/questions/56597042/how-should-i-use-dagger2-with-retrofit)
## Dagger module inside another
[java - Module depending on another module in Dagger - Stack Overflow](https://stackoverflow.com/questions/24668957/module-depending-on-another-module-in-dagger)

## Guide
[Dagger](https://dagger.dev/dev-guide/)
## Dagger and composable
[Injecting Composables with Dagger without losing it | by Costa Fotiadis | ProAndroidDev](https://proandroiddev.com/injecting-composables-with-dagger-without-losing-it-bcf5a6988229)
[Dagger 2 and Jetpack Compose Integration | by Alexey Glukharev | ProAndroidDev](https://proandroiddev.com/dagger-2-and-jetpack-compose-integration-8a8d424ffdb4) - годно
На самом деле все плохо, функция @Composable по нескольку раз вызывается
[Navigation Compose recreating ViewModel each time. : r/androiddev](https://www.reddit.com/r/androiddev/comments/1g9tpmx/navigation_compose_recreating_viewmodel_each_time/)
## Dagger room module