## Как подключить rxjava
https://github.com/ReactiveX/RxAndroid
## ReactiveX
[ReactiveX/RxAndroid: RxJava bindings for Android](https://github.com/ReactiveX/RxAndroid)
## Completable
[Completable (RxJava Javadoc 3.1.9)](https://reactivex.io/RxJava/3.x/javadoc/io/reactivex/rxjava3/core/Completable.html)
## Maybe
[Maybe (RxJava Javadoc 3.1.9)](https://reactivex.io/RxJava/3.x/javadoc/io/reactivex/rxjava3/core/Maybe.html)

## Что подтолкнуло на последние 3 задания с установкой listener
[RxJava: Wrapping Listener Callback with Observable Examples](https://www.couchbase.com/blog/exploring-rxjava-wrapping-listener-callback/)
```
/**  
 * Установить слушателя инициализации чата. * При успешной инициализации успешно завершать поток с передачей имени чата. * При фатальной ошибке инициализации завершать поток с ошибкой. */

fun solve(chat: Chat): Single<String> {  
    return Single.create { emitter ->  
        chat.setInitListener(MessageListener({ item ->  
            run {  
                emitter.onSuccess(item)  
            }  
        }, { err ->  
            run {  
                emitter.onError(err)  
            }  
        }))  
    }  
}  
interface Chat {  
  
    fun setInitListener(listener: MessageListener)  
}  
  
class MessageListener(  
    val onSuccess: (name: String) -> Unit,  
    val onFatalError: (Throwable) -> Unit,  
)

```

```
/**  
 * Преобразовать результат получаемый из [worker] в Maybe поток. */fun solve(worker: Worker): Maybe<String> {  
    return Maybe.create { emitter ->  
        worker.setResultListener { item ->  
            run {  
                if (item != null) {  
                    emitter.onSuccess(item)  
                } else{  
                    emitter.onComplete()  
                }  
            }  
        }    }}  
  
interface Worker {  
    fun setResultListener(listener: (String?) -> Unit)  
}
```
## Пример проекта с rxJava
https://youtu.be/23sm4HSdDfI?si=E-nf5vFfXa0wsbhV
https://github.com/AlexGladkov/TransportApp/blob/master/presentation/src/main/java/com/agladkov/presentation/screens/cities/CitiesViewModel.kt
## Add rxjava to project
[ReactiveX/RxAndroid: RxJava bindings for Android](https://github.com/ReactiveX/RxAndroid)
[java - Android-RxJava: Update UI from background thread using observable - Stack Overflow](https://stackoverflow.com/questions/60688724/android-rxjava-update-ui-from-background-thread-using-observable)
## RxJava как я хочу
https://www.baeldung.com/rxjava-completable
## Single to Completable
[android - RxJava Single to Completable to Single - how to pass the result of the first Single to the second Single - Stack Overflow](https://stackoverflow.com/questions/50807932/rxjava-single-to-completable-to-single-how-to-pass-the-result-of-the-first-sin)
## Chaining - выполнение по цепочке.

## Объединение двух Single
https://ru.stackoverflow.com/questions/969222/%D0%9A%D0%B0%D0%BA-%D0%BE%D0%B1%D1%8A%D0%B5%D0%B4%D0%B8%D0%BD%D0%B8%D1%82%D1%8C-%D0%B4%D0%B2%D0%B0-single-%D0%B2-rxjava
## Объединение двух Completable
Completable.merge(listof(compl1, compl2))

## if else
https://stackoverflow.com/questions/43382603/how-to-use-if-else-in-rx-java-chain
Используют flatMap, но это java. Как применить на Kotlin?
## flatMap не может вернуть Completable
он возвращает single. надо использовать flatMapCompletable

## иногда dispose все ломает. он не дожидается данных и завершает