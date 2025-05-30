# DialogFragment
[Display dialogs with DialogFragment  |  Android Developers](https://developer.android.com/guide/fragments/dialogs)
[Dialogs  |  Views  |  Android Developers](https://developer.android.com/develop/ui/views/components/dialogs)
## DialogFragment with custom view (like RecyclerView)
https://developer.android.com/develop/ui/views/components/dialogs#FullscreenDialog
Вот тут збс, работает. запихиваем в этот же фрагмент все, что надо (например, recycler), и он рисует его.
## Transparent background
[android - Can't make the custom DialogFragment transparent over the Fragment - Stack Overflow](https://stackoverflow.com/questions/8045556/cant-make-the-custom-dialogfragment-transparent-over-the-fragment)
```
getDialog().getWindow().setBackgroundDrawable(new ColorDrawable(Color.TRANSPARENT));
```
## set width

## Ширина не такая, как надо

## Как выйти из него
[android - How to correctly dismiss a DialogFragment? - Stack Overflow](https://stackoverflow.com/questions/11201022/how-to-correctly-dismiss-a-dialogfragment)
## callback
https://stackoverflow.com/questions/17708397/run-a-method-after-a-dialog-is-dismissed-android