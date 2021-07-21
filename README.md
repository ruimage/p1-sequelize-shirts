# T-shirts

## General information

In this assignment, you will practice constructing Mongoose connections. Though the following approach is usually for relational databases, it can be used for Mongo as well. You'll need [`ObjectId`][ObjectId] and [`populate`][populate] (especially for the tests).

![database schema](shirts-schema.png)

*Figure 1*. Normalized schema for this assignment (SQL version).

The above image shows a normalized database (scan the Internet for more information on normalization). Normalization is the division of data into atomic units with reference to one other via ids, allowing no data duplication. This is perfect for SQL relational databases, but MongoDB prefers the opposite: denormalization. This type of database management system (DBMS) constantly queries from one place (usually one collection), leading to data duplication and entity nesting.

Though this assignment is for writing connections, imagine you're making a complete create-your-own-T-shirt website: the designув T-shirts should be available for purchase. What interface does this website need? It'll be easier if you sketch your database's design on paper.


After creating the connections, write model methods, which will give you answers to the following questions:

*For a T-shirt...*

1. Which user created this T-shirt?
2. Which purchases includes this T-shirt?
3. Which users bought this t-shirt?


*For a user...*

1. Which T-shirts did this user create ?
2. What purchases did the user make?
3. What T-shirts did the user buy?
4. Which users designed the T-shirts bought by this user?


*The purchases in your code should be `Purchase` models...*

*For a purchase...*

1. Which user made the purchase?
2. Which T-shirt was bought?


You may find [.populate()](https://mongoosejs.com/docs/populate.html) helpful.

## Releases

### Prerelease: Customization
Убедись, что mongoose установлен. Тебе предоставили необходимые модели. Без моделей `User` и `Shirt` не обойтись, а `Purchase` является опциональной.


### Release 0: Declaring Relationships
Для отношений каждой модели написаны тесты, предоставляющие комментарии по написанным отношениям (см. файлы в `spec/models/`). Если все тесты пройдены, то твои отношения написаны верно. Однако тесты заточены под определенную структуру, которая не является единственно верной. Поэтому если ты считаешь, что твоя структура подходит для решения данной задачи, но тесты не проходят, тогда можешь проконсультироваться с кем-нибудь из инструкторов.

*P.S. Чтобы написать желаемые отношения (связи/ассоциации), необходимо ознакомиться с [`ObjectId`][ObjectId]*

### Release 1: More options
Подумай, как можно было спроектировать твою базу данных по-другому? Порисуй на листе бумаги варианты моделей, их взаимоотношений, подумай в каких случаях твой вариант работает хорошо, а в каких нужно сделать по-другому? Не забывай, что структура в случае с MongoDB сильно зависит от конкретной задачи. Важно, чтобы вы могли легко получать все необходимые данные из вашей БД.


## Conclusion
В рамках этой задачи стояла цель поработать со связыванием нескольких моделей между собой. Также важными частями задания являются: рассмотрение нескольких различных вариантов структуры БД, обоснованный выбор одной из них на основании каких-либо определенных умозаключений, информации из интернета и т.д. После завершения задания ты должен понимать, как составлять запросы, что такое `.populate()`, зачем нужен `ObjectId`, а также когда именно он нужен, в каких случаях можно обойтись без него.


[ObjectId]: https://mongoosejs.com/docs/schematypes.html#objectids
[populate]: https://mongoosejs.com/docs/populate.html
