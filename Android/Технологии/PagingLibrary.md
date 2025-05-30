## dependencies
https://developer.android.com/topic/libraries/architecture/paging/v3-overview#setup
```
  val paging_version = "3.3.6"

  implementation("androidx.paging:paging-runtime:$paging_version")
  implementation("androidx.room:room-paging:$room_version")
```
## boilerplate
#### PagingSource
https://developer.android.com/topic/libraries/architecture/paging/v3-paged-data#pagingsource
Важно, что в типе LoadResult<Int, User> указывается единственное число, а при создании LoadResult.Page Указывается List\<User>

Обзор: https://developer.android.com/topic/libraries/architecture/paging/v3-overview

## LoadResult Value

## Query (PagingLibrary + Room)
[Paging and Room](https://commonsware.com/Room/pages/chap-paging-004.html)
## convert entity to domain
[pagination - How can I convert PagingSource type in the modular app in android? - Stack Overflow](https://stackoverflow.com/questions/71194604/how-can-i-convert-pagingsource-type-in-the-modular-app-in-android)
## Paging load calls multiple times on start
[Multiple APPEND calls after REFRESH in DB+Network case [183335970] - Issue Tracker](https://issuetracker.google.com/issues/183335970)
[Android Paging 3: LoadType.APPEND returns null remote keys - Stack Overflow](https://stackoverflow.com/questions/66813622/android-paging-3-loadtype-append-returns-null-remote-keys) - это работает
## Paging not load in first time

## refresh Paging Library
PagingDataAdapter.clear()
## PagingDataAdapter clear
[android - How to clear/remove all items in page list adapter - Stack Overflow](https://stackoverflow.com/questions/54856941/how-to-clear-remove-all-items-in-page-list-adapter)
```
searchAdapter.submitData(lifecycle, PagingData.empty())
```