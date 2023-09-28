# regex-sql
Useful Regex Commands for editing SQL files.

## CREATE TABLE
### Add PRIMARY KEY to first id column
``(CREATE TABLE) (.*?)(\()(\n.* )\b(bigint|text|numeric|bollean|timestamp)\b``
In your ide, insert regex in find box then use replace all method with the following:
``$0 PRIMARY KEY``
