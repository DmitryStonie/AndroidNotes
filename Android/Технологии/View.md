# View
## change view position
[layout - How can I dynamically set the position of view in Android? - Stack Overflow](https://stackoverflow.com/questions/6535648/how-can-i-dynamically-set-the-position-of-view-in-android)
## where in activity legal to get view height

## color of GradientDrawable

## get lifecycleowner
[android - Easy way to get current Activity, Fragment, LifeCycleOwner from within View? - Stack Overflow](https://stackoverflow.com/questions/49075413/easy-way-to-get-current-activity-fragment-lifecycleowner-from-within-view)

[Maven Repository: androidx.lifecycle » lifecycle-runtime-ktx](https://mvnrepository.com/artifact/androidx.lifecycle/lifecycle-runtime-ktx)
Да отстой все это, не гарантировано, что найдет
## Что это
[View  |  Android Developers](https://developer.android.com/reference/android/view/View)
[Основы View и ViewGroup. Создаём интерфейсы в Android-приложениях / Хабр](https://habr.com/ru/articles/853348/)
[Custom View в Android — краткое руководство / Хабр](https://habr.com/ru/articles/727744/)
они образуют дерево
есть padding
нет margin
## Иерархия
![[Pasted image 20250209132215.png]]
## Жизненный цикл
![[Pasted image 20250209133136.png]]
## как посмотреть дерево?
В Layout Inspector
## Почему view не находится
findViewById возвращает null
потому-что он вызывается от текущей view, у нее нет ничего
## Как findViewByid ищет
от view, от которого вызвали и по дереву ниже
## The specified child already has a parent. You must call removeView() on the child's parent first.
с attachToRoot = false работает
[java - The specified child already has a parent. You must call removeView() on the child's parent first (Android) - Stack Overflow](https://stackoverflow.com/questions/28071349/the-specified-child-already-has-a-parent-you-must-call-removeview-on-the-chil)
```
val view = LayoutInflater.from(context).inflate(R.layout.calendar, layout, true)  
  

setContentView(view)
```
первый метод дает parent для view, и второй.
## attachToRoot в layoutInflater
это чтобы папку в дереве view Назначить

## достать view без root
![[Pasted image 20250209142812.png]]
## handle long click
https://stackoverflow.com/questions/9589895/how-to-handle-long-click-in-android