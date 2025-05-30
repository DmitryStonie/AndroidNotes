## Как подключить dagger
[курс Dagger 2 (1)](https://www.youtube.com/watch?v=1dOsef2ZzQ8&list=PL0SwNXKJbuNkYFUda5rlA-odAVyWItRCP&index=2)
3:43
в gradle.build.kts (app):
plugins:
id("kotlin-kapt")
dependencies:
implementation(libs.dagger)  
kapt(libs.dagger.compiler)

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