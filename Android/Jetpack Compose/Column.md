# column
## Vertically scrollable component was measured with an infinity maximum height constraints

## Scrollable
[android - How do I create a Jetpack Compose Column where a middle child is scrollable but all of the other children are always visible? - Stack Overflow](https://stackoverflow.com/questions/68164883/how-do-i-create-a-jetpack-compose-column-where-a-middle-child-is-scrollable-but)
```kotlin
Column(
    modifier = Modifier
        .verticalScroll(rememberScrollState())
        .weight(weight = 1f, fill = false)
) {
     Text("Your text here")
}
```