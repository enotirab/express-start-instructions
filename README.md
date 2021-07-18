# Hogwarts Bookstore

Hogwarts Books is a bookstore for upcoming wizards and witches. Recently they have decided to get with the times and provide
an only store where students can purchase books for their classes ahead of time. They have decided that you are the best
candidate to build this application for them. Eventually, they would like their store to all users to search/shop for books based on all manner of search criteria, place items in a shopping cart,
purchase their books and receive an invoice. For now, however, they are asking you for some minimal functionality to
allow them to start uploading their current inventory.

## Phase 1

To get the application started, the following functionality must be completed.

1. A page to view all books.
1. A page to view a specific book.
1. A page to add new books to the system.
1. A page to edit books that already exist.
1. A button on the edit book page that allows a user to delete that book.

### Initial setup.

1. First make a new express project in webstorm.
1. Install dependencies  `npm install pg pg-hstore nodemon sequelize`
1. Create a file called `nodemon.json` in the root of the project and fill it with the contents of the file of the same name
in this repository.
1. Add the nodemon watch script `"watch": "nodemon ./start.js --ignore public/"` to `package.json`.  


### Database Setup

1. In Datagrip create a database called `bookstore`.
1. In our `bookstore` database, create a table called `books`.
1. Add a fields called `id`  of type `biging` and select `Not null`, `Auto inc` and `Primary key`.
1. Add the fields `isbn`, `title`, `description` as `text` for type.  Also add `pages` with an `int` type.
   
### Sequelize Model Setup
1. Run `sequelize init`. This will create the folders `config`, `migrations` and `models`.
1. Open `config/config.json` and fill in the database values in the `development` section. 
1. Generate our `Book` model with the `sequelize` command `sequelize model:generate --name Book --attributes title:string`.
1. Open `model/book.js` and add our other attributes.  
1. In our `Book` model, also added the options `tableName: 'books'` and `timestamps: 'false'`.








