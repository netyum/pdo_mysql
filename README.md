pdo_mysql
=========

add read/write timeout

# INSTALLATION

Copy the file to the corresponding versions of php source code ext/pdo_mysql

# USED

* PDO::MYSQL_ATTR_READ_TIMEOUT   //int second
* PDO::MYSQL_ATTR_WRITE_TIMEOUT  //int second
* PDO::MYSQL_ATTR_RW_TIMEOUT_ENV //int value range
  * PDO::MYSQL_RW_ENV_ALL  // all env
  * PDO::MYSQL_RW_ENV_CLI  // cli env
  * PDO::MYSQL_RW_ENV_WEB  // web env
  * PDO::MYSQL_RW_ENV_NONE // not use 
