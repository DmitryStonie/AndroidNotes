# Testing
[Test apps on Android  |  Android Developers](https://developer.android.com/training/testing) - очень полезно, несколько статей

## JUnit 4
[Заметки программистера: Шпаргалка по JUnit 4](https://www.dokwork.ru/2012/04/junit-4.html)

## BeforeClass
[junit - How do I manage unit test resources in Kotlin, such as starting/stopping a database connection or an embedded elasticsearch server? - Stack Overflow](https://stackoverflow.com/questions/35554076/how-do-i-manage-unit-test-resources-in-kotlin-such-as-starting-stopping-a-datab)
## Unit test Room
[Урок 13. Room. Тестирование](https://startandroid.ru/ru/courses/architecture-components/27-course/architecture-components/541-urok-13-room-testirovanie.html)
## ApplicationProvider не находит
[Android. Where did ApplicationProvider go? - Stack Overflow](https://stackoverflow.com/questions/56571764/android-where-did-applicationprovider-go)
androidTestImplementation (libs.androidx.core) все равно не помогло
## fail test
[java - JUnit4 fail() is here, but where is pass()? - Stack Overflow](https://stackoverflow.com/questions/4036144/junit4-fail-is-here-but-where-is-pass)
## No instrumentation registered! Must run under a registering instrumentation.
нужно нормально писать тесты
## JUnit
[Test and debug your database  |  Android Developers](https://developer.android.com/training/data-storage/room/testing-db)
#### Delegate runner androidx.test.internal.runner.junit4.AndroidJUnit4ClassRunner for AndroidJUnit4 could not be found.
instrumented тест должен лежать в папке androidTest
## JUnit rxjava
[How to Test RxJava? | Baeldung](https://www.baeldung.com/rxjava-testing) - приятный TestSubscriber, но он не работает
## Overload resolution ambiguity. All these functions match

## run tests from command line
[Test from the command line  |  Android Studio  |  Android Developers](https://developer.android.com/studio/test/command-line)
## Testing android apps
#### Unit tests
[Build local unit tests  |  Test your app on Android  |  Android Developers](https://developer.android.com/training/testing/local-tests)
#### UI tests
[Automate UI tests  |  Test your app on Android  |  Android Developers](https://developer.android.com/training/testing/ui-tests)
Виды тестов:
1. Behaviour tests [Behavior UI Tests  |  Test your app on Android  |  Android Developers](https://developer.android.com/training/testing/ui-tests/behavior)
2. Screenshot tests [Screenshot testing  |  Test your app on Android  |  Android Developers](https://developer.android.com/training/testing/ui-tests/screenshot)
#### UI test example
https://proandroiddev.com/testing-android-ui-with-pleasure-e7d795308821
https://github.com/mitrejcevski/ui-testing
## Espresso
[Espresso  |  Test your app on Android  |  Android Developers](https://developer.android.com/training/testing/espresso)
#### Samples
[Additional Resources for Espresso  |  Test your app on Android  |  Android Developers](https://developer.android.com/training/testing/espresso/additional-resources#samples)
#### Hamcrest matchers
[Writing and using Hamcrest Matchers | PPT](https://www.slideshare.net/slideshow/hamcrest-matchers/10387142)
#### RecyclerView testing
https://developer.android.com/training/testing/espresso/lists#recycler-view-list-items
[testing-samples/ui/espresso/RecyclerViewSample/app/src/androidTest/java/com/example/android/testing/espresso/RecyclerViewSample/RecyclerViewSampleTest.java at main · android/testing-samples](https://github.com/android/testing-samples/blob/main/ui/espresso/RecyclerViewSample/app/src/androidTest/java/com/example/android/testing/espresso/RecyclerViewSample/RecyclerViewSampleTest.java)
#### Didn't find class "org.hamcrest.Matchers
[android - Test Error - NoClassDefFoundError: Failed resolution of: Lorg/hamcrest/Matchers - Stack Overflow](https://stackoverflow.com/questions/66915068/test-error-noclassdeffounderror-failed-resolution-of-lorg-hamcrest-matchers)
```
./gradlew :app:dependencies
```
#### start ui tests automatically
[Espresso tests not running in android studio - Stack Overflow](https://stackoverflow.com/questions/70622183/espresso-tests-not-running-in-android-studio)
downgrading not working
https://stackoverflow.com/questions/21406246/google-espresso-java-lang-runtimeexception-could-not-launch-intent-intent-act
проблема в ActivityScenarioRule. Это штука, которая запускает activity перед тестом.
[Better tests with AndroidX’s ActivityScenario in Kotlin — Part 1 | by Piotr Zawadzki | the-stepstone-group-tech-blog | Medium](https://medium.com/stepstone-tech/better-tests-with-androidxs-activityscenario-in-kotlin-part-1-6a6376b713ea)
при замене на ActivityTestRule получил Could not launch intent Intent within 45000 milliseconds. Perhaps the main thread has not gone idle 
[Espresso driver : Could not launch intent Intent · Issue #805 · appium/appium-espresso-driver](https://github.com/appium/appium-espresso-driver/issues/805#issuecomment-1197768092)
Скорее всего, приложение просто занято, поэтому не может запуститься
https://github.com/android/android-test/issues/1875
Необходимо включить разрешение на телефоне xiaomi. И все заработает. До следующей переустановки (а она будет при следующем запуске тестов)
[java - Displaying popup windows while running in the background? - Stack Overflow](https://stackoverflow.com/questions/59645936/displaying-popup-windows-while-running-in-the-background)START_FOREGROUND_SERVICES_FROM_BACKGROUND
#### espresso view overlapping
isVisible() не то
isCompletelyDisplayed проверяет ожидаемые и реальные размеры, т.е. с пересечением не справляется
[android - How to test that views are overlapping? - Stack Overflow](https://stackoverflow.com/questions/50396456/how-to-test-that-views-are-overlapping)
#### espresso idling resourses - wait activity before test
[Espresso idling resources  |  Test your app on Android  |  Android Developers](https://developer.android.com/training/testing/espresso/idling-resource)
3 способа, все отстой. Но я выбрал первый
[testing-samples/ui/espresso/IdlingResourceSample at main · android/testing-samples](https://github.com/android/testing-samples/tree/main/ui/espresso/IdlingResourceSample)
[Android testing with Espresso’s Idling Resources and testing fidelity | by Jose Alcérreca | Android Developers | Medium](https://medium.com/androiddevelopers/android-testing-with-espressos-idling-resources-and-testing-fidelity-8b8647ed57f4)
#### androidx.test.core.app.ActivityScenario.ActivityAction<CapturedType(*)!>!' was expected.
https://developer.android.com/guide/components/activities/testing#determine-current-state
``` not works
@Before  
fun registerIdlingResource() {  
    val activityScenario: ActivityScenario<*> =  
        ActivityScenario.launch<MainActivity>(MainActivity::class.java)  
    activityScenario.onActivity { activity ->  
        mIdlingResource = (activity as MainActivity).getIdlingResource();  
        // To prove that the test fails, omit this call:  
        IdlingRegistry.getInstance().register(mIdlingResource);  
    }  
}
```
