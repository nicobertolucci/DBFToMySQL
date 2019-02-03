Nicolas Bertolucci 
https://www.devcognitio.com.ar
DBF To MySQL 
========================================================================================================================

This script imports DBASE/FoxPro files, located in a subdir, into a MySQL database. It can be used for reverse
engeneering of FoxPro applications. For OS/X and Linux, I didn't find any usefull and working tool to do this
automatically.

This script is based on: 

* https://github.com/doofpot/DBFToMySQL
* http://stackoverflow.com/questions/14270236/php-script-to-convert-dbf-files-to-mysql
* http://www.ostalks.com/2009/12/31/import-dbf-files-to-mysql-using-php/


Installation and use
------------------------------------------------------------------------------------------------------------------------
```bash
git clone https://github.com/nicobertolucci/DBFToMySQL.git

```
* Configure MySQL info and paths to directory where DBF/PFT files are located in configuration file **config.php**. Remember that you need to change it from config.sample.php to config.php

* Use it:
Open console in this folder and type:

```php
php dbf-import.php
```

Known-issues
------------------------------------------------------------------------------------------------------------------------

- if a date field is 0, then the the corresponding date with 0 is inserted (january first, 1970).
- the php-xbase thing is in the subdir "classes". As a ruby programmer, i didn't find how to make this separate whithin the day, I spent on solving this problem. If someone can help me with this problem.

License
------------------------------------------------------------------------------------------------------------------------

MIT
