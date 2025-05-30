## круг
[How to define a circle shape in an Android XML drawable file? - Stack Overflow](https://stackoverflow.com/questions/3185103/how-to-define-a-circle-shape-in-an-android-xml-drawable-file)
## Скругленные углы
[android - How do I set the rounded corner radius of a color drawable using xml? - Stack Overflow](https://stackoverflow.com/questions/2122199/how-do-i-set-the-rounded-corner-radius-of-a-color-drawable-using-xml)
```
```xml
<?xml version="1.0" encoding="UTF-8"?> 
<shape xmlns:android="http://schemas.android.com/apk/res/android"> 
    <solid android:color="#ffffffff"/>    
             
    <stroke android:width="3dp"
            android:color="#ff000000" />

    <padding android:left="1dp"
             android:top="1dp"
             android:right="1dp"
             android:bottom="1dp" /> 
             
    <corners android:radius="7dp" /> 
</shape>
```
## add text
кажется никак, только в коде