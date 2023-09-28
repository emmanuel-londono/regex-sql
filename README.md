# regex-sql
Useful Regex patterns for editing SQL files.

## CREATE TABLE
### Add PRIMARY KEY to first id column

``(CREATE TABLE) (.*?)(\()(\n.* )\b(bigint|text|n|numeric|boolean|timestamp)\b``

<br/>
In your IDE, insert regex in find box then use replace all method with the following:
``$0 PRIMARY KEY``
<br/>
You may add more data types in regex in between the ``\b()\b`` section. 
