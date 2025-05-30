# Retrofit
## dependencies
```
dependencies {
	val retrofit_version = "2.11.0" 
	implementation("com.squareup.retrofit2:retrofit:$retrofit_version")  
	implementation("com.squareup.retrofit2:converter-gson:$retrofit_version")  
}
```
dependencies {
	...
	val okHttp_version = "4.8.0"  
	val retrofit_version = "2.9.0"  
implementation("com.squareup.retrofit2:retrofit:$retrofit_version")  
implementation("com.squareup.retrofit2:converter-gson:$retrofit_version")  
implementation("com.squareup.retrofit2:adapter-rxjava3:$retrofit_version")  
implementation("com.squareup.okhttp3:okhttp:$okHttp_version")  
implementation("com.squareup.okhttp3:logging-interceptor:$okHttp_version")
	...
}
взято из видео https://youtu.be/mVx3_vSxbJU?si=sbwgwzsZxgA6a8jm
не рекомендую сразу использовать сокращенные - android Studio не всегда их понимает
Чуть подробнее: https://github.com/square/okhttp/tree/master/okhttp-logging-interceptor
## Boilerplate
``` Manifest
<uses-permission android:name="android.permission.INTERNET"/>
```

``` 
data class User(    
	val age : Int,    
	val name : String
)
```

```
interface MainService {    
	@GET("User/{userId}.json")
	suspend fun getUser(@Path("userId") userId : Int) : Response<User>
}
```

``` module in hilt
@Module@InstallIn(SingletonComponent::class)object AppModule {    @Provides    fun providesBaseUrl() : String = "https://example-hilt-retrofit-default-rtdb.firebaseio.com/"    @Provides    @Singleton    fun provideRetrofit(BASE_URL : String) : Retrofit = Retrofit.Builder()        .addConverterFactory(GsonConverterFactory.create())        .baseUrl(BASE_URL)        .build()    @Provides    @Singleton    fun provideMainService(retrofit : Retrofit) : MainService = retrofit.create(MainService::class.java)    @Provides    @Singleton    fun provideMainRemoteData(mainService : MainService) : MainRemoteData = MainRemoteData(mainService)}
```
<uses-permission android:name="android.permission.INTERNET"/>
## Retrofit
https://youtu.be/mVx3_vSxbJU?si=sbwgwzsZxgA6a8jm - подключение, пример get, singleton без di
https://youtu.be/Pous1Uyj-9M?si=yd0CsCDa47BvWYA0
https://habr.com/ru/articles/568792/ - retrofit + hilt
## Post, Headers
https://square.github.io/retrofit/
## parse array
[android - Parse JSON array response using Retrofit & Gson - Stack Overflow](https://stackoverflow.com/questions/42623437/parse-json-array-response-using-retrofit-gson)
[How to use Retrofit 2 for nameless JSON Arrays | by Chelsea Katsidzira | Medium](https://medium.com/@tafadzwachelsea/how-to-use-retrofit-2-for-nameless-json-arrays-45361e784b8)
## field name
[gson - Telling Retrofit to what variable it should map a certain json field? - Stack Overflow](https://stackoverflow.com/questions/23524331/telling-retrofit-to-what-variable-it-should-map-a-certain-json-field)
```kotlin
public class PagedResponse<T> {

    public PagingLinks _links;
    @SerializedName(value="RESPONSE_DATA_NAME")
    public List<T> _data;
}
```
## URL manipulation
[Declarations | Retrofit](https://square.github.io/retrofit/declarations/)
```
@GET("group/{id}/users")
Call<List<User>> groupList(@Path("id") int groupId);

@GET("/json")
    suspend fun getSunrise(@Query("lat") latitude: String, @Query("lng") longitude: String, @Query("date") date: String, @Query("time_format") timeFormat: Int = 24) : Response<SunriseApiResponse>
```
## Get image

## GEt empty annotation
[json - Retrofit GET without a value in Android - Stack Overflow](https://stackoverflow.com/questions/31962817/retrofit-get-without-a-value-in-android)
	