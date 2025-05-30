# ObjectAnimator
## перекрасить drawable
Как будто никак. В списке параметров нет такого (хотя, там и backgroundColor нет)

Когда использовать ObjectAnimator, ==ValueAnimator== и TransitionDrawable
[animation - Animate change of view background color on Android - Stack Overflow](https://stackoverflow.com/questions/2614545/animate-change-of-view-background-color-on-android)


## примеры анимаций
[ObjectAnimator | Jake Lee on Software](https://blog.jakelee.co.uk/programmatically-creating-and-scheduling-animations-for-android-drawable-layers-with-objectanimator/)

## список параметров для анимации
[Property Animation Overview  |  Views  |  Android Developers](https://developer.android.com/develop/ui/views/animations/prop-animation#views)
## stop ObjectAnimator
ObjectAnimator.cancel()
## get animated value
[getAnimatedValue](https://developer.android.com/reference/android/animation/ValueAnimator#getAnimatedValue\(\))()
## how to use Animator.AnimatorListene
[Android: How to run some code on animation end - Stack Overflow](https://stackoverflow.com/questions/49509516/android-how-to-run-some-code-on-animation-end)
# ValueAnimator
## перекрасить drawable


## repeat
```java
valueAnimator.setRepeatCount(ValueAnimator.INFINITE);
```