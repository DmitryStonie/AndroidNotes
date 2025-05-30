# Android
[[Технологии]]
[[Лекции яндекса]]
[[Android/Технологии/Проблемы]]
## Toast
[Android: Toast - всплывающие сообщения (alexanderklimov.ru)](https://developer.alexanderklimov.ru/android/toast.php)
## Activity, Task, Backstack
[Tasks and the back stack  |  Android Developers](https://developer.android.com/guide/components/activities/tasks-and-back-stack)
(https://developer.android.com/guide/topics/manifest/activity-element#lmode)
[[Activity backstack]]
## Свои шрифты
[android - How to use specified weights for fonts in XML - Stack Overflow](https://stackoverflow.com/questions/46589519/how-to-use-specified-weights-for-fonts-in-xml)
[Add a font as an XML resource  |  Views  |  Android Developers](https://developer.android.com/develop/ui/views/text-and-emoji/fonts-in-xml)
## Подгон изображения по ширине
android:scaleType="centerCrop"
## Строковый ресурс
[String resources  |  Android Developers](https://developer.android.com/guide/topics/resources/string-resource)
## Базовый recycler view
[Kotlin: RecyclerView (alexanderklimov.ru)](https://developer.alexanderklimov.ru/android/views/recyclerview-kot.php)
## Recycler view с разными элементами
[A RecyclerView with multiple item types in Kotlin | by Ruud Jansen | Medium](https://medium.com/@ruut_j/a-recyclerview-with-multiple-item-types-in-kotlin-80e1e36d93e6)
## Расстояние между элементами
[A better way to set RecyclerView items margin | by Cesar Morigaki | Medium](https://cesarmorigaki.medium.com/a-better-way-to-set-recyclerview-items-margin-708ea9d3ac25)
## Конвертировать dp в пиксели
[Extension Function to convert dp to px and px to dp in Android | by Puria kazemieh | Medium](https://medium.com/@puriakazemieh/extension-function-to-convert-dp-to-px-and-px-to-dp-in-android-f4414a15651f)
## Сказать адаптеру обновить
[android - How to add Items to a recyclerview Kotlin - Stack Overflow](https://stackoverflow.com/questions/61754402/how-to-add-items-to-a-recyclerview-kotlin)
## DiffUtil для анимации:
[Пример использования Android DiffUtil (startandroid.ru)](https://startandroid.ru/ru/blog/504-primer-ispolzovanija-android-diffutil.html)
Но есть проблемы.
DiffUtil для 2-х типов: [android - Using RecyclerView with DiffUtil for multiple data types - Stack Overflow](https://stackoverflow.com/questions/63019699/using-recyclerview-with-diffutil-for-multiple-data-types)
## Click listener
[How to Apply OnClickListener to RecyclerView Items in Android? - GeeksforGeeks](https://www.geeksforgeeks.org/how-to-apply-onclicklistener-to-recyclerview-items-in-android/)
## RecyclerView item decoration
https://developer.android.com/reference/androidx/recyclerview/widget/RecyclerView#addItemDecoration(androidx.recyclerview.widget.RecyclerView.ItemDecoration)
[RecyclerView.ItemDecoration  |  Android Developers](https://developer.android.com/reference/androidx/recyclerview/widget/RecyclerView.ItemDecoration)
## DiffUtil
[DiffUtil  |  Android Developers](https://developer.android.com/reference/androidx/recyclerview/widget/DiffUtil)
[DiffUtil.DiffResult  |  Android Developers](https://developer.android.com/reference/androidx/recyclerview/widget/DiffUtil.DiffResult)
## Динамический список RecyclerView
[Create dynamic lists with RecyclerView  |  Views  |  Android Developers](https://developer.android.com/develop/ui/views/layout/recyclerview)
## Анимации
https://developer.android.com/develop/ui/views/animations/spring-animation#kts
https://www.youtube.com/watch?v=bhSqkeoC7yI&list=PLQC2_0cDcSKAVl_3u-3ZrEW2UFBUjDD97&index=16
[[Библиотеки для анимаций]]
## Про хранение фото и ImageUri
[How to Select an Image from Gallery in Android? - GeeksforGeeks](https://www.geeksforgeeks.org/how-to-select-an-image-from-gallery-in-android/)
## Использовать layout в другом layout
[android - How to include layout inside layout? - Stack Overflow](https://stackoverflow.com/questions/5632114/how-to-include-layout-inside-layout)
## Topbar menu
https://www.youtube.com/watch?v=Pu6GZ6RugM4
[Working with the AppBar  |  Android Developers](https://developer.android.com/guide/fragments/appbar)
[android - 'setHasOptionsMenu(Boolean): Unit' is deprecated. Deprecated in Java - Stack Overflow](https://stackoverflow.com/questions/71917856/sethasoptionsmenuboolean-unit-is-deprecated-deprecated-in-java)
все равно не получилось

[ToolBar in Android with Example - GeeksforGeeks](https://www.geeksforgeeks.org/toolbar-in-android-with-example/) - так получилось, но это для активити
## Bindings
[View binding  |  Android Developers](https://developer.android.com/topic/libraries/view-binding)
## Добавить toolbar в fragment
[android - how to use setSupportActionBar in fragment - Stack Overflow](https://stackoverflow.com/questions/38189198/how-to-use-setsupportactionbar-in-fragment)

## Передача парамтеров в транзакции
[android - Send data to fragment with FragmentTransaction - Stack Overflow](https://stackoverflow.com/questions/36041545/send-data-to-fragment-with-fragmenttransaction)
## Сохранение данных
[External Storage in Android with Example - GeeksforGeeks](https://www.geeksforgeeks.org/external-storage-in-android-with-example/) - в файл
[How to Create and Add Data to SQLite Database in Android? - GeeksforGeeks](https://www.geeksforgeeks.org/how-to-create-and-add-data-to-sqlite-database-in-android/) - в бд, уперлось все в то, что бдшке нужен КОНТЕКСТ. Может, DI поможет?
[Просто об архитектуре в Android / Хабр](https://habr.com/ru/companies/bsl/articles/788940/) - про андроид
## Clean architecture
[Clean Architecture / Хабр](https://habr.com/ru/companies/otus/articles/732178/)
[Чистая архитектура на примере / Хабр](https://habr.com/ru/articles/784922/)
## List
[Kotlin | List](https://metanit.com/kotlin/tutorial/7.2.php)
[Kotlin | Map](https://metanit.com/kotlin/tutorial/7.4.php)
## Порядок проектирования по clean
1. Domain layer
	1. Entity
	2. Interactor или UseCase
	3. Repository **Interface**
2. Data layer
	1. Repository Implementation
	2. Data Sources
	3. Data Models
	4. Mappers
3. Presentation
	1. View
	2. Presenter / ViewModel
## Hide an element
[Android: hide an element - Stack Overflow](https://stackoverflow.com/questions/42608060/android-hide-an-element)
## Diffutil криво работает с удалением
https://www.youtube.com/watch?v=cppys4VYyvA
1:30 DiffUtil не поддерживает удаление элементов
## RecyclerView max height
[RecyclerView — How to handle insertion and deletion | by Eric N | Medium](https://ericntd.medium.com/recyclerview-how-to-handle-insertion-and-deletion-334a38104de8)
Есть разные методы для вызова diffutil
проблема не решена
## Список контактов
[Retrieve a list of contacts  |  Identity  |  Android Developers](https://developer.android.com/identity/providers/contacts-provider/retrieve-names) - сложно, непонятно
[How to Get Saved Contacts in Android Application using Cursor? - GeeksforGeeks](https://www.geeksforgeeks.org/how-to-get-saved-contacts-in-android-application-using-cursor/) - startManagingCursor deprecated, не получится
[How can getContentResolver() be called in Android? - Stack Overflow](https://stackoverflow.com/questions/3750903/how-can-getcontentresolver-be-called-in-android)
[Android Contacts fetching using Kotlin Coroutines | Medium](https://medium.com/@kednaik/android-contacts-fetching-using-coroutines-aa0129bffdc4)
## Запрос permission
[How to Request Permissions in Android Application? - GeeksforGeeks](https://www.geeksforgeeks.org/android-how-to-request-permissions-in-android-application/)
[Request runtime permissions  |  Android Developers](https://developer.android.com/training/permissions/requesting)
[java - How to check permission in fragment - Stack Overflow](https://stackoverflow.com/questions/40760625/how-to-check-permission-in-fragment)
## android check if app got permission after dialog in FRAGMENT
[java - How to check permission in fragment - Stack Overflow](https://stackoverflow.com/questions/40760625/how-to-check-permission-in-fragment)
## update 1 view model from another
[Show hide fragment in android - Stack Overflow](https://stackoverflow.com/questions/14347588/show-hide-fragment-in-android)
## Подпись приложения
[Sign your app  |  Android Studio  |  Android Developers](https://developer.android.com/studio/publish/app-signing#sign_release)
## add mp4 to app
'C' is not a valid file-based resource name character: File-based resource names must contain only lowercase a-z, 0-9, or underscore
название файла должно быть с маленькой буквы

https://developer.android.com/build/build-variants#variant_aware
![[Pasted image 20241206193006.png]]
## how to create release dir
https://www.geeksforgeeks.org/how-to-detect-shake-event-in-android/
## add mp4 to project
https://stackoverflow.com/questions/77965781/video-function-in-r-video-package-doesnt-work-for-mp4-file-saved-on-local-drive
## Grid layout
https://www.geeksforgeeks.org/recyclerview-using-gridlayoutmanager-in-android-with-example/
## Change color on recyclerview click item
https://stackoverflow.com/questions/40692214/changing-background-color-of-selected-item-in-recyclerview
## Pull refresh
https://developer.android.com/develop/ui/views/touch-and-input/swipe/add-swipe-interface
https://developer.android.com/develop/ui/views/touch-and-input/swipe/respond-refresh-request
## Corners constarint
https://stackoverflow.com/questions/16161448/how-to-make-layout-with-rounded-corners
https://stackoverflow.com/questions/8930555/android-drawable-with-rounded-corners-at-the-top-only
## Time
https://stackoverflow.com/questions/47006254/how-to-get-current-local-date-and-time-in-kotlin
Date в Room сохранить нельзя, надо как-то конвертировать

[How to store “date” in Room database? - Betül Necanlı - Medium](https://betulnecanli.medium.com/how-to-store-date-in-room-database-d06dec3a2d7e)
## Обновление каждые 12 часов - service
https://khurramitdeveloper.blogspot.com/2013/06/android-alarm-manager-to-start-service.html\
## Иконки валют
[android - How to get currency symbol by currency name? - Stack Overflow](https://stackoverflow.com/questions/36258511/how-to-get-currency-symbol-by-currency-name)
## Как делать обновление 12 часов
сохранять время последнего обновления
## Как подключить bindings
https://developer.android.com/topic/libraries/view-binding
## EditText get current value
поле .text.toString()
## Как подключить kapt для DataBinding
#### build.gradle.kts (для модуля)
plugins {  
    kotlin("kapt")  
}
android {  
    buildFeatures {  
        dataBinding = true  
        // for view binding:  
        // viewBinding = true
    }
}
dependencies {  
    kapt("com.android.tools.build:gradle:8.5.1")  
}
#### settings.gradle.kts
pluginManagement {  
    plugins {  
        kotlin("kapt") version "2.0.20"  
    }
}
## android:ems
[What is meant by Ems? (Android TextView) - Stack Overflow](https://stackoverflow.com/questions/7053738/what-is-meant-by-ems-android-textview)
## Выпадающий список: Spinner
[Java и Android | Выпадающий список Spinner (metanit.com)](https://metanit.com/java/android/5.4.php)
## Как нормально из другого потока данные передавать
[Java и Android | Потоки, фрагменты и ViewModel (metanit.com)](https://metanit.com/java/android/10.2.php)
## Шринкинг, обфускация
[Shrink, obfuscate, and optimize your app  |  Android Studio  |  Android Developers](https://developer.android.com/build/shrink-code)
сейчас используется не ProGuard, а R8
## JWT где хранить токены
[android - Where to store a JWT token? - Stack Overflow](https://stackoverflow.com/questions/34191731/where-to-store-a-jwt-token)
Ответ: лучше в SharedPreferences. Но вообще, он устаревший. ЛУчше DataStore
## Получить текущее время
[How to get current time and date in Android - Stack Overflow](https://stackoverflow.com/questions/5369682/how-to-get-current-time-and-date-in-android)
[Calendar  |  Android Developers](https://developer.android.com/reference/java/util/Calendar.html)
Для хранения используется класс Date. Есть проблема: создание объекта Date из строчки/
https://stackoverflow.com/questions/30096749/the-constructor-datestring-is-deprecated
## Как сгенерировать fingerprint для jwt
[uniqueidentifier - Is there a unique Android device ID? - Stack Overflow](https://stackoverflow.com/questions/2785485/is-there-a-unique-android-device-id?page=1&tab=scoredesc#tab-top)
Можно этот идентификатор использовать, но не получилось
[Best practices for unique identifiers  |  Identity  |  Android Developers](https://developer.android.com/identity/user-data-ids)
var uniqueID = UUID.randomUUID().toString()
## Date как сравнивать?
[How to compare dates in Java? - Stack Overflow](https://stackoverflow.com/questions/2592501/how-to-compare-dates-in-java)
Сравнение по типу больше/меньше/равно. А надо на сколько больше
[How do I do calendar arithmetic with java.util.Date? - Stack Overflow](https://stackoverflow.com/questions/5894726/how-do-i-do-calendar-arithmetic-with-java-util-date)
можно сделать новый объект и прибавить к нему времени
## Писать логи

## Checkbox
[Add checkboxes to your app  |  Views  |  Android Developers](https://developer.android.com/develop/ui/views/components/checkbox)
#### Как отметить
[How to programatically check a Checkbox in Android? - Stack Overflow](https://stackoverflow.com/questions/34947145/how-to-programatically-check-a-checkbox-in-android)
status - чекбокс, task.executionStatus - boolean value
status.isChecked = task.executionStatus

#### Как поменять цвет

#### material checkbox
[material-components-android/docs/components/Checkbox.md at master · material-components/material-components-android](https://github.com/material-components/material-components-android/blob/master/docs/components/Checkbox.md)
оказывается, это и есть обычный чекбокс. но тут все свойства описаны
## Выключить полный экран
Проблема - с api35 edgetoedge включен автоматически
[Display content edge-to-edge in your app  |  Views  |  Android Developers](https://developer.android.com/develop/ui/views/layout/edge-to-edge)
решение - 
ViewCompat.setOnApplyWindowInsetsListener(fab)
но тогда надо покрасить statius bar и navigation bar
[How to change the status bar color in Android? - Stack Overflow](https://stackoverflow.com/questions/22192291/how-to-change-the-status-bar-color-in-android)
короче херня это все, лучше Edge to edge. проблема то в том, что я добавляю topbar через include в xml фрагмента. А надо как-то так:
активити [Set up the app bar  |  Views  |  Android Developers](https://developer.android.com/develop/ui/views/components/appbar/setting-up)

[android - Calling setSupportActionBar in a fragment - Stack Overflow](https://stackoverflow.com/questions/49781110/calling-setsupportactionbar-in-a-fragment)
https://www.youtube.com/watch?v=-z53q9j0YaM - неудача

## Верстка
## Текст по центру по вертикали
[android - How do I center text horizontally and vertically in a TextView? - Stack Overflow](https://stackoverflow.com/questions/432037/how-do-i-center-text-horizontally-and-vertically-in-a-textview)
если не получается (визуально), то скорее всего textLabel слишком маленький (внутри кнопки). 
## Прятать элементы
[Android- Hide or Show Specific Layout & Views Efficiently - GeeksforGeeks](https://www.geeksforgeeks.org/android-hide-or-show-specific-layout-views-efficiently/)
Не работает на include элементах. на них надо [java - How to set visibility for include layout in databinding? - Stack Overflow](https://stackoverflow.com/questions/56365215/how-to-set-visibility-for-include-layout-in-databinding)
## Показать keyboard
[android - How to show soft-keyboard when edittext is focused - Stack Overflow](https://stackoverflow.com/questions/5105354/how-to-show-soft-keyboard-when-edittext-is-focused)
## TextInputEditText значение
view.text

## get string resource
[Android: How do I get string from resources using its name? - Stack Overflow](https://stackoverflow.com/questions/7493287/android-how-do-i-get-string-from-resources-using-its-name)

## layout inspector
[Debug your layout with Layout Inspector  |  Android Studio  |  Android Developers](https://developer.android.com/studio/debug/layout-inspector)
## instantiate view

## include в разметке