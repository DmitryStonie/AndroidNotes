# Navigation
## Как сделать навигацию #гайд
#### 1. Добавить в libs.versions.toml
``` kotlin
[versions]
navigationCompose = "2.8.0-beta03"
kotlinxSerialization = "1.6.3"


[libraries]
androidx-navigation-compose = { group = "androidx.navigation", name = "navigation-compose", version.ref = "navigationCompose"}
kotlinx-serialization-json = { module = "org.jetbrains.kotlinx:kotlinx-serialization-json", version.ref = "kotlinxSerialization"}

[plugins]
jetbrains-kotlin-serialization = { id = "org.jetbrains.kotlin.plugin.serialization", version.ref = "kotlin" }


```
#### 2. Добавить зависимости и плагин в build.gradle.kts (module)
В app module libs.androidx.navigation.compose, в остальных модулях без нее - только сериализация
```kotlin
plugins{
    alias(libs.plugins.jetbrains.kotlin.serialization)
}
dependencies{
	implementation(libs.androidx.navigation.compose)
	implementation(libs.kotlinx.serialization.json)
}
```

#### 3. Подключить плагин в build.gradle.kts (project)
```kotlin
plugins {
    alias(libs.plugins.jetbrains.kotlin.serialization) apply false
}
```
#### 3. Добавить Route для экрана
Обычно это отдельный файл в папке ui, там же где и экран. Если посредством route ничего не передается, нужно делать
``` kotlin
@Serializable
data object HistoryRoute
```
Если передается, то
``` kotlin
@Serializable
data class DetailsRoute(
	val loanId: Long,
)
```
#### 4. Добавить навигацию на главный экран
MainScreen.kt
```kotlin
@Composable
fun MainScreen() {
	val navController = rememberNavController()

	Scaffold { paddingValues: PaddingValues ->
		NavHost(
			modifier = Modifier.padding(paddingValues),
			navController = navController,
			startDestination = HistoryRoute,
		) {
			composable<HistoryRoute> {
				LoanHistoryScreen(
					onItemClick = { loanId ->
						navController.navigate(DetailsRoute(loanId))
					}
				)
			}
			composable<DetailsRoute> {
				val destination = it.toRoute<DetailsRoute>()

				DetailsScreen(
					loanId = destination.loanId,
					onBackClick = {
						navController.navigateUp()
					}
				)
			}
		}
	}
}
```