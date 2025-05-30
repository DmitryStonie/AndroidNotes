[Permissions в Android: как не допустить ошибок при разработке / Хабр](https://habr.com/ru/companies/swordfish_security/articles/741574/) - сложные советы
[Manifest.permission  |  API reference  |  Android Developers](https://developer.android.com/reference/android/Manifest.permission#ACCEPT_HANDOVER) - Список всех permissions
[Android permissions](https://startandroid.ru/ru/blog/508-android-permissions.html) - просто и понятно
В итоге схема получения разрешения состоит из трех действий:  
- проверка текущего состояния разрешения  
- запрос на получение разрешения, если оно еще не было получено  
- обработка ответа на запрос
[Permissions on Android  |  Privacy  |  Android Developers](https://developer.android.com/guide/topics/permissions/overview#normal-dangerous) - базовый оф док
[Declare app permissions  |  Privacy  |  Android Developers](https://developer.android.com/training/permissions/declaring) - как объявлять в манифесте
[Request runtime permissions  |  Privacy  |  Android Developers](https://developer.android.com/training/permissions/requesting) - запрос runtime permissions
## не отображается request permission dialog
проблема в том, что запрашивается READ_EXTERNAL_STORAGE, который работает до maxSdk=32, на новых надо просить 
https://developer.android.com/about/versions/13/behavior-changes-13#granular-media-permissions