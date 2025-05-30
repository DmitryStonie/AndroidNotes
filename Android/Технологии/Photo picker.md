# Photo picker
https://developer.android.com/training/data-storage/shared/photopicker
## где взять registerForActivityResult
из activity. лучше в фрагменте это вызывать, нежели в viewModel
## Install backported version
[google play services - Automatic install of the backported version of the Android Photo Picker not playing nicely with Android Studio - Stack Overflow](https://stackoverflow.com/questions/75996256/automatic-install-of-the-backported-version-of-the-android-photo-picker-not-play)

```
<!--suppress AndroidDomInspection -->  
<service  
    android:name="com.google.android.gms.metadata.ModuleDependencies"  
    android:enabled="false"  
    android:exported="false"  
    tools:ignore="MissingClass">  
    <intent-filter>  
        <action android:name="com.google.android.gms.metadata.MODULE_DEPENDENCIES" />  
    </intent-filter>  
  
    <meta-data  
        android:name="photopicker_activity:0:required"  
        android:value="" />  
</service>
```
## Fragments must call registerForActivityResult() before they are created (i.e. initialization, onAttach(), or onCreate()).
[Get a result from an activity  |  App architecture  |  Android Developers](https://developer.android.com/training/basics/intents/result) - нужно делать callback, чтобы получить результат
а вообще, эту штуку нужно писать в onAttach или onCreate
