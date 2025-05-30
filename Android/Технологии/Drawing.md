# Drawing
# Нарисовать Эллипс
## xml drawable shape
[How to draw a semi-oval shape using shape drawable in xml (Android) - Stack Overflow](https://stackoverflow.com/questions/44705444/how-to-draw-a-semi-oval-shape-using-shape-drawable-in-xml-android) - статично и не совсем то, что надо.
## custom view
[How Android draws views  |  Views  |  Android Developers](https://developer.android.com/guide/topics/ui/how-android-draws) - кажется сложно
## Open GL
[Draw shapes  |  Views  |  Android Developers](https://developer.android.com/develop/ui/views/graphics/opengl/draw)
## canvas
[Drawing Custom Shapes in Android | Kodeco](https://www.kodeco.com/9556022-drawing-custom-shapes-in-android) - path, на самом деле кастом view, супер
[how to draw a half circle in android - Stack Overflow](https://stackoverflow.com/questions/31705870/how-to-draw-a-half-circle-in-android)
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