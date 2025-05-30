[android - Disable default animation from Portrait to Landscape - Stack Overflow](https://stackoverflow.com/questions/11957772/disable-default-animation-from-portrait-to-landscape)
2 ответ что-то делает
WindowManager.LayoutParams.ROTATION_ANIMATION_CROSSFADE - есть несколько анимаций
```
public static final int ROTATION_ANIMATION_CHANGED = 4096;
public static final int ROTATION_ANIMATION_CROSSFADE = 1;  
public static final int ROTATION_ANIMATION_JUMPCUT = 2;  
public static final int ROTATION_ANIMATION_ROTATE = 0;  
public static final int ROTATION_ANIMATION_SEAMLESS = 3;
```
[How to detect orientation change in layout in Android? - Stack Overflow](https://stackoverflow.com/questions/5726657/how-to-detect-orientation-change-in-layout-in-android)
посмотреть ориентацию в config