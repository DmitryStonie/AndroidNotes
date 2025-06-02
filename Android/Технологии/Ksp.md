# Ksp
## Kapt to Ksp migration
[Migrate from kapt to KSP  |  Android Studio  |  Android Developers](https://developer.android.com/build/migrate-to-ksp)
Пишут, что до 2 раз быстрее работает
## Dependencies
[Migrate from kapt to KSP  |  Android Studio  |  Android Developers](https://developer.android.com/build/migrate-to-ksp)
``` project-level build.gradle
id("com.google.devtools.ksp") version "2.0.21-1.0.27" apply false
```

``` module-level build.gradle
id("com.google.devtools.ksp")
```
