[material-components-android/docs/components/BottomNavigation.md at master · material-components/material-components-android](https://github.com/material-components/material-components-android/blob/master/docs/components/BottomNavigation.md)
[Navigation bar – Material Design 3](https://m3.material.io/components/navigation-bar/overview)
## Не хочет менять цвет активного элемента в навбаре. 
Решение: [android - Material Design 3 uses colorPrimary for actionBar, navBar and calendar background color. How do I disable this? - Stack Overflow](https://stackoverflow.com/questions/71929841/material-design-3-uses-colorprimary-for-actionbar-navbar-and-calendar-backgroun)
## Не хочет реагировать на нажатия
есть 3 решения - как в доке, deprecated и первое тут: [android - onItemSelectedListener for bottomnavigationbar - Stack Overflow](https://stackoverflow.com/questions/68515923/onitemselectedlistener-for-bottomnavigationbar)
работает только то, что на стэке
## при 4 элементах пропали названия
The `labelVisibilityMode` attribute can be used to adjust the behavior of the text labels for each navigation item. There are four visibility modes:

- `LABEL_VISIBILITY_AUTO` (default): The label behaves as “labeled” when there are 3 items or less, or “selected” when there are 4 items or more
- `LABEL_VISIBILITY_SELECTED`: The label is only shown on the selected navigation item
- `LABEL_VISIBILITY_LABELED`: The label is shown on all navigation items
- `LABEL_VISIBILITY_UNLABELED`: The label is hidden for all navigation items
