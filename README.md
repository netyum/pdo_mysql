pdo_mysql
=========

add read/write timeout

# INSTALLATION

Copy the file to the corresponding versions of php source code ext/pdo_mysql

# Constants

* PDO::MYSQL_ATTR_READ_TIMEOUT   //int second  default 60
* PDO::MYSQL_ATTR_WRITE_TIMEOUT  //int second  default 60
* PDO::MYSQL_ATTR_RW_TIMEOUT_ENV //int value range  default PDO::MYSQL_RW_ENV_CLI
  * PDO::MYSQL_RW_ENV_ALL  // all env
  * PDO::MYSQL_RW_ENV_CLI  // cli env
  * PDO::MYSQL_RW_ENV_WEB  // web env
  * PDO::MYSQL_RW_ENV_NONE // not use 

# QUICK TEST

```
$attribute = array(
        PDO::MYSQL_ATTR_READ_TIMEOUT=>10,
        PDO::MYSQL_ATTR_WRITE_TIMEOUT=>10,
);
$db = new PDO('mysql:host=localhost;dbname=test', 'root', '', $attribute);
$rs = $db->query("SELECT SLEEP(5)");
var_dump($rs);
$rs = $db->query("SELECT SLEEP(20)");
var_dump($rs);
```


