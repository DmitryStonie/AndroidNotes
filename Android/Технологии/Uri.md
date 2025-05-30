## get filetype by uri
https://stackoverflow.com/questions/12473851/how-i-can-get-the-mime-type-of-a-file-having-its-uri - устаревшее, код нерабочий
https://developer.android.com/training/secure-file-sharing/retrieve-info - норм
## get filename by uri
[Retrieving file information  |  App data and files  |  Android Developers](https://developer.android.com/training/secure-file-sharing/retrieve-info)
## This Cursor should be freed up after use with
[android - The cursor should be freed up after use with #close - Stack Overflow](https://stackoverflow.com/questions/34109463/the-cursor-should-be-freed-up-after-use-with-close)
## getColumnIndex not defined


## Uri, выданный photoPicker и Intent разные

## get video tumbnail
[Get a Video thumbnail from Content Uri on Android - Ngenge Senior - Medium](https://ngengesenior.medium.com/get-a-video-thumbnail-from-content-uri-on-android-3548df4dad47)
## create from string
[java - Turning a string into a Uri in Android - Stack Overflow](https://stackoverflow.com/questions/2709087/turning-a-string-into-a-uri-in-android)
```
Uri.parse(строчка)
```
## после перезапуска не работает получение типа
[Uri Access Lifetime: Still Shorter Than You Might Think](https://commonsware.com/blog/2020/08/08/uri-access-lifetime-still-shorter-than-you-might-think.html) - у него есть время жизни.
```
If you need durable access — such as being able to access the content tomorrow — you have two main options that I know of:

1. If you used `ACTION_OPEN_DOCUMENT`, `ACTION_CREATE_DOCUMENT`, or similar Storage Access Framework actions, you can try using `takePersistableUriPermissions()` on `ContentResolver` to get long-term access to the content.
    
2. Otherwise, before your component is destroyed, make a local copy of the content in your app’s portion of internal storage (e.g., `getCacheDir()`). This approach sucks, as it duplicates the content, and changes to the original edition of the content will not be reflected in the copy. Use appropriate UI terms (e.g., “import”) to help the user understand that this is what is going on.
```