---
class: webd 2008
module: module three
date: 2022-02-09
tags: webd-2008, web-development, php, pdo, term-2
---

# CRUD
localhost:xxxx/phpmyadmin

**CODE FOR MYSQL SERVER IN PHP**

- DB_DSN - data source name
    - define(’DB_DSN’, ‘mysql.....
- The rest defines the user and password

### ***PDO: PHP Data Objects***

**require('db_connect.php');**

- When using include and there is a problem, the page would continue loading
- With require, none of the code will execute if there is a problem

**$query = "INSERT INTO quotes (author, content) VALUES (:author, :content)";**

- Creating parameters for the the SQL query

**$statement = $db->prepare($query);**

- Caches the statement

**PDO::PARAM_INT**

- Integer, throws an error if the datatypes don’t match

**<input type="hidden" name="id" value="<?= $quote['id'] ?>">**

- Common to use hidden types when you are doing updates
- The user should never be able to update the primary key