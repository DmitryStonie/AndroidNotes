# Coroutines
## Как подключить #гайд 
#### 1. Добавить в libs.versions.toml
```
[versions]
coroutines = "1.8.1"

[libraries]
kotlinx-coroutines-android = { module = "org.jetbrains.kotlinx:kotlinx-coroutines-android", version.ref = "coroutines"}

```
#### 2. build.gradle (module)
```
dependencies {   
	implementation(libs.kotlinx.coroutines.android)
}
```
## coroutine + liveData
https://developer.android.com/topic/libraries/architecture/coroutines#livedata
## dependency
[Lifecycle  |  Jetpack  |  Android Developers](https://developer.android.com/jetpack/androidx/releases/lifecycle)
## not resolving liveData
add dependency
## coroutine save data structures
