[material-components-android/docs/components/BottomSheet.md at master · material-components/material-components-android](https://github.com/material-components/material-components-android/blob/master/docs/components/BottomSheet.md)
## Неадекватное поведение frame layout внутри CoordinatorLayout
![[Pasted image 20250115173358.png]]
android:layout_height="match_parent" - не работает. вся проблема в 
com.google.android.material.bottomsheet.BottomSheetBehavior
я его убрал и вроде бы ничего не сломалось, кроме цвета