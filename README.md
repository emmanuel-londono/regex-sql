# regex-sql
Useful Regex patterns for editing SQL files.

## CREATE TABLE
### Add PRIMARY KEY to first id column

``(CREATE TABLE) (.*?)(\()(\n.* )\b(bigint|text|n|numeric|boolean|timestamp)\b``

<br/>
In your IDE, insert regex in find box then use replace all method with the following:
<br/>
``$0 PRIMARY KEY``
<br/>
<br/>
You may add more data types in regex in between the ``\b()\b`` section. 

### Remove tbl in front of table name and then lowercase following text.

``(\b(CREATE TABLE|INSERT INTO|ALTER TABLE)\b) (\b(tbl([a-zA-Z]*)\b))``

<br/>
In your IDE, insert regex in find box then use replace all method with the following:
<br/>
``$1 \L$5,``
<br/>
<br/>
