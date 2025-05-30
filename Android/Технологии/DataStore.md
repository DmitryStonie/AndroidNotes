# DataStore
## Как добавить в проект
[App Architecture: Data Layer - DataStore - Android Developers](https://developer.android.com/topic/libraries/architecture/datastore)
## Как это подружить с DI
проблема: в [App Architecture: Data Layer - DataStore - Android Developers](https://developer.android.com/topic/libraries/architecture/datastore) предлагают в верх файла писать. оно работает на функции-расширении. внутри di-модуля такое не прокатает.
Решение:
[DataStore and dependency injection | by Simona Milanović | Android Developers | Medium](https://medium.com/androiddevelopers/datastore-and-dependency-injection-ea32b95704e3)
## DataStore + RxJava
Проблема: по умолчанию DataStore работает на corutines, а хочется rxJava. Поддержка есть.
## Как этим пользоваться
[App Architecture: Data Layer - DataStore - Android Developers](https://developer.android.com/topic/libraries/architecture/datastore)
[Обзор DataStore Library. Прощаемся с SharedPreference? / Хабр](https://habr.com/ru/companies/tbank/articles/525010/)
[DataStore and synchronous work. In the following posts from our Jetpack… | by Simona Milanović | Android Developers | Medium](https://medium.com/androiddevelopers/datastore-and-synchronous-work-576f3869ec4c)
## Синхронное использование
ну не знаю я пока корутины
[DataStore and synchronous work. In the following posts from our Jetpack… | by Simona Milanović | Android Developers | Medium](https://medium.com/androiddevelopers/datastore-and-synchronous-work-576f3869ec4c)
## Как сохранять время
