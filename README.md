# sql
DB Structure


Which solution for:
- sqlite nodejs api swagger


## better-sqlite3
https://github.com/JoshuaWise/better-sqlite3


    Full transaction support
    High performance, efficiency, and safety
    Easy-to-use synchronous API (faster than an asynchronous API... yes, you read that correctly)
    Support for user-defined functions, aggregates, and extensions
    64-bit integers (invisible until you need them)


### Installation

    npm install --save better-sqlite3

If you have trouble installing, check the troubleshooting guide.


### Install example electronjs desktop application
https://github.com/electron/electron-api-demos
This is a desktop app that interactively and with sample code demonstrates core features of the Electron API. It's built with Electron, too, of course. This app works on Windows, macOS and Linux operating systems.

    .\apicra\electron\install.bat
    .\apicra\electron\start.bat
    

### Install example statement
https://github.com/lvivier/better-sqlite3-statements

    .\apicra\statement\install.bat
    .\apicra\statement\start.bat
    
    
## Better-SQLite-Pool, *python  
https://github.com/hyurl/better-sqlite-pool
A connection pool for the module better-sqlite3.
Using this module to open pools and acquire connections, and release the connection once it has done its work.    
    
## better-sqlite3-helper, *python
https://github.com/Kauto/better-sqlite3-helper

    .\apicra\helper\install.bat
    .\apicra\helper\start.bat
                
        How to install
        
        Like always
        
        npm i better-sqlite3-helper
        
        How to use
        
        In every file you want access to a sqlite3 database simply require the library and use it right away.
        anyServerFile.js
        
        const DB = require('better-sqlite3-helper');
        
        let row = DB().queryFirstRow('SELECT * FROM users WHERE id=?', userId);
        console.log(row.firstName, row.lastName, row.email);
        
        To setup your database, create a sql-file named 001-init.sql in a migrations-directory in the root-directory of your program.
        ~/migrations/001-init.sql
        
        -- Up
        CREATE TABLE `users` (
          id INTEGER PRIMARY KEY, 
          firstName TEXT NOT NULL, 
          lastName TEXT NOT NULL, 
          email TEXT NOT NULL
        );
        
        -- Down
        DROP TABLE IF EXISTS `users`;
        

https://loopback.io/doc/en/lb3/SQLite3.html#model-definition-for-sqlite3
        
Model definition for SQLite3

The model definition consists of the following properties:

    name: Name of the model, by default, it’s the camel case of the table
    properties: Property definitions, including default value mapping


    {"name": "Inventory", "options": {
      "idInjection": false,
    }, "properties": {
      "id": {
        "type": "String",
        "required": false,
        "length": 64,
        "precision": null,
        "scale": null
      },
      "productId": {
        "type": "String",
        "required": false,
        "length": 20,
        "precision": null,
        "scale": null,
        "id": 1
      },
      "locationId": {
        "type": "String",
        "required": false,
        "length": 20,
        "precision": null,
        "scale": null,
        "id": 1
      },
      "available": {
        "type": "Number",
        "required": false,
        "length": null,
        "precision": 32,
        "scale": 0
      },
      "total": {
        "type": "Number",
        "required": false,
        "length": null,
        "precision": 32,
        "scale": 0
      },
      "createdOn": {
       "type": "Date",
        "required": false,
        "sqlite3": {
          "dbDefault": "now"
        }
      }
    }}
            
### Usage

    const db = require('better-sqlite3')('foobar.db', options);

    const row = db.prepare('SELECT * FROM users WHERE id=?').get(userId);
    console.log(row.firstName, row.lastName, row.email);
