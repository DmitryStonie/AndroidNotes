# ViewModel
## dependencies

## get activity

## создание ViewModel используя ViewModelProvider
в onCreate фрагмента или activity
```
val provider: ViewModelProvider = ViewModelProvider(this)  
val screenViewModel = provider.get(MainScreenViewModel::class.java)
```

## activityViewModels нет
[android - how to get viewModel by viewModels? (fragment-ktx) - Stack Overflow](https://stackoverflow.com/questions/56748334/how-to-get-viewmodel-by-viewmodels-fragment-ktx)
## return value from viewModelScope

## can't get viewModelScope
import androidx.lifecycle.viewModelScope не распознается
```
val lifecycle_version = "2.9.1"  
implementation("androidx.lifecycle:lifecycle-viewmodel-ktx:$lifecycle_version")
```
## can't get viewModels, activityViewModels
#### fragment
[android - how to get viewModel by viewModels? (fragment-ktx) - Stack Overflow](https://stackoverflow.com/questions/56748334/how-to-get-viewmodel-by-viewmodels-fragment-ktx)
```
val fragment_ktx_version = "1.8.6"  
implementation("androidx.fragment:fragment-ktx:$fragment_ktx_version")
```
#### activity

## Share data between viewModels
[Are there actually any guidelines on how to pass data between ViewModels? : r/androiddev](https://www.reddit.com/r/androiddev/comments/17alr8x/are_there_actually_any_guidelines_on_how_to_pass/)
[android - Sharing Data between ViewModels - Stack Overflow](https://stackoverflow.com/questions/54588201/sharing-data-between-viewmodels)
