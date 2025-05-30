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


