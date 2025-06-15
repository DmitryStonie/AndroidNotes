# RecyclerView
## Examples
[views-widgets-samples/RecyclerViewKotlin at main · android/views-widgets-samples](https://github.com/android/views-widgets-samples/tree/main/RecyclerViewKotlin/)
## Dependencies

## Базовый RecyclerView
[Create dynamic lists with RecyclerView  |  Views  |  Android Developers](https://developer.android.com/develop/ui/views/layout/recyclerview)
## DiffUtil

## беды - вылет при удалении
elements = ArrayList(newElements)

elements = newElements  // проблема, они на одно и то же ссылаются, recycler не может убрать удаленный элемент, т.к. его уже нет

## фигово анимируется добавление/удаление
надо корректно написать diffutilcallback,
```

override fun areItemsTheSame(  
    oldItemPosition: Int,  
    newItemPosition: Int,  
): Boolean {  
    val oldItem: ListItem = oldList[oldItemPosition]  
    val newItem: ListItem = newList[newItemPosition]  
    //хорошо
    return oldItem == newItem  
}
```
```
override fun areItemsTheSame(  
    oldItemPosition: Int,  
    newItemPosition: Int,  
): Boolean {  
    val oldItem: ListItem = oldList[oldItemPosition]  
    val newItem: ListItem = newList[newItemPosition]  
    //плохо
    return when {  
        oldItem is TaskItem && newItem is TaskItem -> {  
            true  
        }  
  
        else -> false  
    }  
}
```

items разные, но тип один. второй код говорит, что они одинаковые если тип одинаковый, что не так. тогда получается что все одинаковые и алгоритм считает, что дешевле в начало запихнуть.
## No adapter attached; skipping layout

## Layouts для recyclerView

## Как сделать свой recyclerView - гайд

добавить в imageView фото tools
src
## изменять размер в зависимости от числа элементво
[android - How to make RecyclerView item size dynamic based on number of items - Stack Overflow](https://stackoverflow.com/questions/75577182/how-to-make-recyclerview-item-size-dynamic-based-on-number-of-items)
## screen width (не про recycler)
https://stackoverflow.com/questions/4743116/get-screen-width-and-height-in-android
## color bottom

## square items

## PagingDataAdapter blinking 
[android - RecyclerView blinking after notifyDatasetChanged() - Stack Overflow](https://stackoverflow.com/questions/29331075/recyclerview-blinking-after-notifydatasetchanged)
## Обновление части viewHolder (когда он сложный)
[Update recycler view content without refreshing the data. | by Miguel Sesma | Medium](https://medium.com/@MiguelSesma/update-recycler-view-content-without-refreshing-the-data-bb79d768bde8)
## viewholder + livedata
[android - How to use livedata and viewmodel with a viewholder as Lifecycle Owner? - Stack Overflow](https://stackoverflow.com/questions/54825613/how-to-use-livedata-and-viewmodel-with-a-viewholder-as-lifecycle-owner)
## высота viewHolder
[android - How to set RecyclerView item max height relative to parent - Stack Overflow](https://stackoverflow.com/questions/64789096/how-to-set-recyclerview-item-max-height-relative-to-parent)
можно переделать так:
```
val view = LayoutInflater.from(parent.context).inflate(R.layout.recycler_ground_day_info_element, parent, false)  
val holder = DayInfoViewHolder(view)  
val params = holder.view.findViewById<ConstraintLayout>(R.id.element).layoutParams as RecyclerView.LayoutParams  
params.height = (parent.height * 0.2).toInt()  
holder.view.layoutParams = params
```
## ItemDecoration
[Кастомный ItemDecoration для RecyclerView / Хабр](https://habr.com/ru/articles/532552/)
#### Для GridLayoutManager
[gridview - Android Recyclerview GridLayoutManager column spacing - Stack Overflow](https://stackoverflow.com/questions/28531996/android-recyclerview-gridlayoutmanager-column-spacing)
[Советы для профессионального использования RecyclerView. Часть 2 / Хабр](https://habr.com/ru/articles/426773/) - четные, нечетные элементы
[Android RecyclerView finding out first and last view on ItemDecoration - Stack Overflow](https://stackoverflow.com/questions/29666598/android-recyclerview-finding-out-first-and-last-view-on-itemdecoration) - как узнать первый и последний элемент
#### ItemDecoration applies multiple times

## RecyclerView element height
[android - How to handle variable height image in RecyclerView? - Stack Overflow](https://stackoverflow.com/questions/55767695/how-to-handle-variable-height-image-in-recyclerview)
