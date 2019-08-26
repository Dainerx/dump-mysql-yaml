# dump-mysql-yaml

## Introduction

  Script to generate YAML (http://www.yaml.org/) from
  a MySQL database. Will generate YAML for either all
  tables in the specified database, only the specified
  tables in the specified database or only the given
  SQL query.

## Options

- -h <host>         MySQL database host
- -u <user>         MySQL username
- -d <database>     Name of the MySQL database to dump
- -t <table(s)>     Comma delimited list of tables to dump from database
- -p <pass>         MySQL password
- -f <file>         File to dump to
- -q \"<query>\"    SQL query to dump
- -qn <query name>  Name of the \"table\" when using the -q option
- -n                Convert table names to class names

## Usage

        main.php [options] -d <database>
        main.php [options] -d <database> -t table1,table2
        main.php [options] -d <database> -q \"SELECT * FROM `mytable`\" -qn custom_name

## Example

        main.php -h localhost -u root -p pass -d test -f dump.yaml
