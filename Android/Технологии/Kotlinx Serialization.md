# Kotlinx Serialization
## string and int at the same time
[Force Int convert to string in Kotlinx Serialization : r/Kotlin](https://www.reddit.com/r/Kotlin/comments/17eudwn/force_int_convert_to_string_in_kotlinx/)
[json - How to configure ignoreUnknownKeys for Kotlin Retrofit2 deserialization converter - Stack Overflow](https://stackoverflow.com/questions/78920882/how-to-configure-ignoreunknownkeys-for-kotlin-retrofit2-deserialization-converte)
```
val json = Json { isLenient = true }  
return json.asConverterFactory(  
    "application/json; charset=UTF8;".toMediaType()  
)
```