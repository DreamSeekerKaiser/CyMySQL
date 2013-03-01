========
CyMySQL
========

What's CyMySQL
--------------

This package contains a python MySQL client library.

It is a fork project from PyMySQL http://www.pymysql.org/ .

PyMySQL is written by Yutaka Matsubara <yutaka.matsubara@gmail.com>
as a pure python database driver. CyMySQL is powered by Cython by
Hajime Nakagami <nakagami@gmail.com>.

It still can work without Cython as a pure python driver.

Documentation on the MySQL client/server protocol can be found here:
http://forge.mysql.com/wiki/MySQL_Internals_ClientServer_Protocol .

Requirements
-------------

- Python 2.6 or higher
- Cython 17.1 or higher
- MySQL 4.1 or higher
    
Installation & Example
-----------------------

Install cython (optional) ::

   # pip install cython

Install cymysql ::

   # pip install cymysql

Example ::

   import cymysql
   conn = cymysql.connect(host='127.0.0.1', user='root', passwd='', db='database_name', charset='utf8')
   cur = conn.cursor()
   cur.execute('select foo, bar from baz')
   for r in cur.fetchall():
      print r[0], r[1]

