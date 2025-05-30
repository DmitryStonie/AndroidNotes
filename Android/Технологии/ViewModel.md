## dependencies

## get activity

## создание ViewModel используя ViewModelProvider
в onCreate фрагмента или activity
```
val provider: ViewModelProvider = ViewModelProvider(this)  
val screenViewModel = provider.get(MainScreenViewModel::class.java)
```
## fragment viewModels

## activityViewModels нет
[android - how to get viewModel by viewModels? (fragment-ktx) - Stack Overflow](https://stackoverflow.com/questions/56748334/how-to-get-viewmodel-by-viewmodels-fragment-ktx)
## return value from viewModelScope