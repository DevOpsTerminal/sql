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

### Usage

    const db = require('better-sqlite3')('foobar.db', options);

    const row = db.prepare('SELECT * FROM users WHERE id=?').get(userId);
    console.log(row.firstName, row.lastName, row.email);
