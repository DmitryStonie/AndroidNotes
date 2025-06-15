# TextView
## dots if text too big
[android - Show three dots when TextView is too long - Stack Overflow](https://stackoverflow.com/questions/56357722/show-three-dots-when-textview-is-too-long)
## dp vs sp - разница для текста
[android - Should use "sp" instead of "dp" for text sizes - Stack Overflow](https://stackoverflow.com/questions/23981260/should-use-sp-instead-of-dp-for-text-sizes)
Есть изменение размера текста, есть масштаб интерфейса. Если использовать sp, размер будет меняться при изменении этих настроек, если dp - нет. Лучше использовать sp.
## How to handle text size option
[How do you deal with large font size across an app in xml layouts? : r/androiddev](https://www.reddit.com/r/androiddev/comments/103rtfl/how_do_you_deal_with_large_font_size_across_an/)
Не по теме: лучше использовать файл dimens для хранения размеров.
[How to use dimens.xml in Android? - Stack Overflow](https://stackoverflow.com/questions/29128178/how-to-use-dimens-xml-in-android)
Возможное решение - Flow (layout) - [[Constraint layout]]
## How to test different text size
[Accessible Text Scaling for Android - DEV Community](https://dev.to/sigute/accessible-text-scaling-for-android-1ham)
https://developer.android.com/about/versions/14/features#accessibility
## Как разрабатывать под разный размер текста
Не нашел настройки размера текста в редакторе layout
Можно просто изменять размеры экранов в редакторе
## Case - uppercase (каждая первая буква - большая)
[android - Is there a way to style a TextView to uppercase all of its letters? - Stack Overflow](https://stackoverflow.com/questions/4434588/is-there-a-way-to-style-a-textview-to-uppercase-all-of-its-letters) - все большие
[xml - How to capitalize the first letter of text in a TextView in an Android Application - Stack Overflow](https://stackoverflow.com/questions/3419521/how-to-capitalize-the-first-letter-of-text-in-a-textview-in-an-android-applicati) - только первые буквы
В общем, нельзя, только в коде
## Line height
[Line height в Android TextView: где не сходится с Figma, как мешает pixel-perfect, и как это решить / Хабр](https://habr.com/ru/companies/avito/articles/803865/)
Обходной путь:
```
<TextView    
...    
android:textSize="15sp"    
app:lineHeight="22sp"    
app:firstBaselineToTopHeight="17sp"    
app:lastBaselineToBottomHeight="5sp" />
```
## Свои шрифты - text weight
[android - How to use specified weights for fonts in XML - Stack Overflow](https://stackoverflow.com/questions/46589519/how-to-use-specified-weights-for-fonts-in-xml)
[Add a font as an XML resource  |  Views  |  Android Developers](https://developer.android.com/develop/ui/views/text-and-emoji/fonts-in-xml)
```scss
200    Extra Light (Ultra Light)
300    Light
400    Normal (Regular)
500    Medium
600    Semi Bold (Demi Bold)
700    Bold
800    Extra Bold (Ultra Bold)
900    Black (Heavy)
950    Extra Black (Ultra Black)
```
## Letter spasing in px/sp
https://developer.android.com/reference/android/widget/TextView#attr_android:letterSpacing
Но указывается в ems
[What is meant by Ems? (Android TextView) - Stack Overflow](https://stackoverflow.com/questions/7053738/what-is-meant-by-ems-android-textview)
#### Перевод px в em и в %
[PX to EM Conversion](https://www.w3schools.com/tags/ref_pxtoemconversion.asp)