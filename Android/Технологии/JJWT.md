[jwtk/jjwt: Java JWT: JSON Web Token for Java and Android](https://github.com/jwtk/jjwt)
## Как подключить
[jwtk/jjwt: Java JWT: JSON Web Token for Java and Android](https://github.com/jwtk/jjwt?tab=readme-ov-file#android-projects)
dependencies {
	val jjwt_version = "0.12.6"  
	api("io.jsonwebtoken:jjwt-api:$jjwt_version")  
	runtimeOnly("io.jsonwebtoken:jjwt-impl:$jjwt_version")  
	runtimeOnly("io.jsonwebtoken:jjwt-orgjson:$jjwt_version") {  
	    exclude(group = "org.json", module = "json")  
	}
}
## Структура пакета, отправляемого с токеном
[javascript - Каким образом отправлять JWT токен при авторизации на сервер? - Stack Overflow на русском](https://ru.stackoverflow.com/questions/881832/%D0%9A%D0%B0%D0%BA%D0%B8%D0%BC-%D0%BE%D0%B1%D1%80%D0%B0%D0%B7%D0%BE%D0%BC-%D0%BE%D1%82%D0%BF%D1%80%D0%B0%D0%B2%D0%BB%D1%8F%D1%82%D1%8C-jwt-%D1%82%D0%BE%D0%BA%D0%B5%D0%BD-%D0%BF%D1%80%D0%B8-%D0%B0%D0%B2%D1%82%D0%BE%D1%80%D0%B8%D0%B7%D0%B0%D1%86%D0%B8%D0%B8-%D0%BD%D0%B0-%D1%81%D0%B5%D1%80%D0%B2%D0%B5%D1%80)
[JSON Web Token Introduction - jwt.io](https://jwt.io/introduction)
