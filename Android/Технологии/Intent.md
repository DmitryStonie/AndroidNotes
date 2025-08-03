# Intent
## не работает (открывает просто приложение, а не конкретный элемент)
https://stackoverflow.com/questions/3114471/android-launching-music-player-using-intent 
```
intent.addFlags(Intent.FLAG_GRANT_READ_URI_PERMISSION);
```

## черный экран при открытии image
Проблема в PhotoPicker
```
AttachedFileItem.Type.Image.value -> {  
    val chooser: Intent = Intent.createChooser(  
        Intent(Intent.ACTION_VIEW).setDataAndType(  
            (model as ImageItem).file.uri,  
            "image/*"  
        ).addFlags(Intent.FLAG_GRANT_READ_URI_PERMISSION), context.getString(  
            R.string.choose_app_to_open_attached_file  
        )  
    )  
    context.startActivity(chooser)  
}
```
## Get started
[Intent  |  API reference  |  Android Developers](https://developer.android.com/reference/android/content/Intent)
Как это устроено [Intents and intent filters  |  App architecture  |  Android Developers](https://developer.android.com/guide/components/intents-filters)
Тема тесно связана с Manifest
#### посмотреть intent-фильтры всех приложений на телефоне

## Phone
[How to make a phone call using intent in Android? - Stack Overflow](https://stackoverflow.com/questions/4275678/how-to-make-a-phone-call-using-intent-in-android)

## Email
[Common intents  |  App architecture  |  Android Developers](https://developer.android.com/guide/components/intents-common#Email)

## SMS

## Maps

## startActivity deprecated
context.startActivity(it)