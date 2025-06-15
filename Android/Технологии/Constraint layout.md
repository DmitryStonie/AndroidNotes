# Constraint layout
## rounded corners
[android - How to make layout with rounded corners..? - Stack Overflow](https://stackoverflow.com/questions/16161448/how-to-make-layout-with-rounded-corners)
## Flow (layout)
[Flow  |  API reference  |  Android Developers](https://developer.android.com/reference/androidx/constraintlayout/helper/widget/Flow)
[Android Adventure: Constraint Views with Flow | by Hasina H. R. | Medium](https://medium.com/@hasina.anddev/android-adventure-constraint-views-with-flow-74b7d982e452)
[Flow and Layer - 2 new cool views in constraint layout 2.0 | DECODE](https://decode.agency/article/flow-and-layer-2-new-cool-views-in-constraint-layout-2-0-2/)
## Ignore height
0dp [Why is 0dp considered a performance enhancement? & Avoid wrap_content on ListView](https://gist.github.com/vxhviet/345dc70960d85047ab04)
[Flow layouts in Compose  |  Android Developers](https://developer.android.com/develop/ui/compose/layouts/flow)
Кажись, нельзя
## 2 constraint layouts max size
[android - constraint layout - Two views with largest width - Stack Overflow](https://stackoverflow.com/questions/59035011/constraint-layout-two-views-with-largest-width)
## Barrier horizontal
[ConstraintLayout](https://constraintlayout.com/basics/barriers.html)
## width and height 0dp - width percentage
[android - ConstraintLayout max width percentage - Stack Overflow](https://stackoverflow.com/questions/49255147/constraintlayout-max-width-percentage)
второй ответ, важны эти строки:
```
<com.google.android.material.imageview.ShapeableImageView  
    android:id="@+id/poster"  
    android:layout_width="0dp"  
    android:layout_height="0dp"  
    app:layout_constraintEnd_toEndOf="parent"  
    app:layout_constraintStart_toStartOf="parent"  
    app:layout_constraintTop_toTopOf="parent"  
    app:shapeAppearanceOverlay="@style/roundedImageView"  
    app:srcCompat="@drawable/photo_sample_2"  
    app:layout_constraintDimensionRatio="13:20"  
    app:layout_constraintWidth_max="wrap"  
    app:layout_constraintWidth_percent="0.35"/>
```
## Guideline
https://developer.android.com/develop/ui/views/layout/constraint-layout#constrain-to-a-guideline
[Guideline  |  API reference  |  Android Developers](https://developer.android.com/reference/androidx/constraintlayout/widget/Guideline)