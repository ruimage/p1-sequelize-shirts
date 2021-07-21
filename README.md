# T-shirts

## General information

In this assignment, you will practice constructing Mongoose relationships. Though the following approach is usually for relational databases, you can use it for Mongo as well. You'll need [`ObjectId`][ObjectId] and [`populate`][populate] (especially for the tests).

![database schema](shirts-schema.png)

*Figure 1*. Normalized schema for this assignment (SQL version).

The above image shows a normalized database (scan the Internet for more information on normalization). Normalization: the division of data into atomic units,  which reference each other via ids, allowing no data duplication. This approach is perfect for SQL relational databases, but MongoDB prefers the opposite: denormalization. This type of database management system (DBMS) constantly queries from one place (usually one collection), leading to data duplication and entity nesting.

Though this assignment is for writing relationships, imagine you're making a complete create-your-own-T-shirt website: the designув T-shirts should be available for purchase. What interface does this website need? It'll be easier if you sketch your database's design on paper.


After creating the relationships, write model methods, which will give you answers to the following questions:

*For a T-shirt...*

1. Which user created this T-shirt?
2. Which purchases include this T-shirt?
3. Which users bought this t-shirt?


*For a user...*

1. Which T-shirts did this user create?
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

Make sure you installed mongoose. For this task, you must have `User` and `Shirt` models, but the `Purchase` model is optional.

### Release 0: Declaring Relationships

We provided you with tests and comments describing desired model relationships (see files in `spec/models/`). Though the tests help ensure desired relationships, they confirm only one specific structure, so if you're confident in yours, but the tests don't agree, consult with one of the instructors.

*P.S. You'll need to utilize [`ObjectId`][ObjectId] to create the desired relationships.*

### Release 1: More options
How else would you design your database? Take a piece of paper and sketch different types of models and their relationships. When is your version optimal? When is it not? Keep in mind that the MongoDB structure is highly dependent on the specific assignment (easy retrieval of all data is very important).

## Conclusion
In this assignment, you learned how to connect models. You also learned the importance of considering several database structure options and selecting a reasonable one based on inferences, Internet information, etc. You now know how to make requests and understand when and why you need `.populate()` and `ObjectId`.

[ObjectId]: https://mongoosejs.com/docs/schematypes.html#objectids
[populate]: https://mongoosejs.com/docs/populate.html
