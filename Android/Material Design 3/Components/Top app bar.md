# Top app bar
[material-components-android/docs/components/TopAppBar.md at master · material-components/material-components-android](https://github.com/material-components/material-components-android/blob/master/docs/components/TopAppBar.md)

Проблем с ним много. Основная - не понятно, как его добавить, чтобы EdgeToEdge корректно работал. Я добавляю компонент через Include, и topbar наезжает на него.
[[EdgeToEdge]]

## Как поставить listeners на пункты выпадающего меню
[material-components-android/docs/components/TopAppBar.md at master · material-components/material-components-android](https://github.com/material-components/material-components-android/blob/master/docs/components/TopAppBar.md)
Там есть! 
```
topAppBar.setNavigationOnClickListener {
    // Handle navigation icon press
}

topAppBar.setOnMenuItemClickListener { menuItem ->
    when (menuItem.itemId) {
        R.id.edit -> {
            // Handle edit text press
            true
        }
        R.id.favorite -> {
            // Handle favorite icon press
            true
        }
        R.id.more -> {
            // Handle more item (inside overflow menu) press
            true
        }
        else -> false
    }
}
```
точно так же, обращаться к пунктам меню по R.id.menu_calendar к примеру.