# Activity
## почему нельзя блокировать activity recreation
[Handle configuration changes  |  App architecture  |  Android Developers](https://developer.android.com/guide/topics/resources/runtime-changes)
## Activity backstack
Активити в стеке никогда не меняют порядок, только кладутся/снимаются.
У определении в Intent приоритет по сравнении с манифестом
launchMode атрибут у activity  в манифесте, значения:
+ standard - создается новый instance активити на вершине стека, из которой эта активити создается. Несколько инстансов в одной таске, несколько инстансов в разных тасках.
+ singleTop - если активити есть на вершине текущего стека таски, то вызов intent перенаправляется в метод onNewIntent этой таски. Если активити нет на вершине стека - поведение как у standard. Несколько инстансов в одной таске, несколько инстансов в разных тасках.
+ singleTask - активити нет - создает новую активити на дне стека новой таски (то есть в ней одна активити - новая), либо располагает активити в таске с такой же affinity. остальные активити завершает. Если есть активити выше - чистит их, а сама помещается на дно.
+ singleInstance - как singleTask, только в одной таске только 1 activity. (нет расположения в таске одной affinity). Но может быть несколько тасок, в каждой по 1 инстансу activity.
+ singleInstancePerTask - активити всегда на дне стека и только 1 в этом стеке.
standard и singleTop могут быть инстанцированы несколько раз, остальные - нет
singleInstancePerTask всегда в корне