# Room
## Dependencies
[Save data in a local database using Room  |  App data and files  |  Android Developers](https://developer.android.com/training/data-storage/room)
```
apply plugin: 'kotlin-kapt' 

dependencies {
    def room_version = '2.3.0'
    implementation 'androidx.room:room-runtime:$room_version'
    implementation "androidx.room:room-ktx:$room_version"
    kapt "androidx.room:room-compiler:$room_version"
}
```
## Room
[Урок 5. Room. Основы](https://startandroid.ru/ru/courses/architecture-components/27-course/architecture-components/529-urok-5-room-osnovy.html)
[Save data in a local database using Room  |  Android Developers](https://developer.android.com/training/data-storage/room)
[Migrate from kapt to KSP  |  Android Studio  |  Android Developers](https://developer.android.com/build/migrate-to-ksp)

## TypeConverter
[Урок 11. Room. Type converter](https://startandroid.ru/ru/courses/architecture-components/27-course/architecture-components/539-urok-11-room-type-converter.html)

## Foreign key
[Урок 6. Room. Entity](https://startandroid.ru/ru/courses/architecture-components/27-course/architecture-components/530-urok-6-room-entity.html) - чет устарело
[ForeignKey  |  Android Developers](https://developer.android.com/reference/androidx/room/ForeignKey) - тут лучше
## Table name
[Define data using Room entities  |  Android Developers](https://developer.android.com/training/data-storage/room/defining-data)
## error: To use RxJava3 features, you must add `rxjava3` artifact from Room as a dependency. androidx.room:room-rxjava3:\<version>


## error: Type of the parameter must be a class annotated with @Entity or a collection/array of it.


## после insert получить id
[Урок 7. Room. Insert, Update, Delete, Transaction](https://startandroid.ru/ru/courses/architecture-components/27-course/architecture-components/531-urok-7-room-insert-update-delete-transaction.html)

## getById несуществующего элемента
[android - Room - Delete executes after I insert new values - Stack Overflow](https://stackoverflow.com/questions/53344456/room-delete-executes-after-i-insert-new-values/53345937)
## FileLockInterruptionException

## не вызывается update
update может возвращать только void, int, Int. если вернуть Single\<Task>, компилятор будет ругаться. если вернуть Completable, компилятор не будет ругаться, но метод не вызовется (проверил, пока дебажил).
## после добавления сущностей бд перестала работать
удалить приложение и по новой поставить
## Room + hilt

## annotations
[Define data using Room entities  |  App data and files  |  Android Developers](https://developer.android.com/training/data-storage/room/defining-data)

## Информация по Room
#### Зачем, dependencies
https://developer.android.com/training/data-storage/room#setup - отсюда dependencies не работают
[android - Room cannot find implementation - Stack Overflow](https://stackoverflow.com/questions/47274677/room-cannot-find-implementation) - 3 коммент, dependencies работают
#### Database, dao, entity example, Database instanse
https://developer.android.com/training/data-storage/room#sample-implementation
## Обновление схемы базы данных в проде
меняешь версию, пишешь миграцию
[Migrate your Room database  |  App data and files  |  Android Developers](https://developer.android.com/training/data-storage/room/migrating-db-versions)