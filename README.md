# ExportCSV
### What is it ?
A class that allows you to export all you database structure and datas into a CSV file

##### Example
```php
<?php
require 'class.CSV.php';
try
{
    $dbh = new PDO('mysql:host=localhost;dbname=chatbox', 'root', '');
}
catch (PDOException $e)
{
    print "Erreur !: " . $e->getMessage() . "<br/>";
    die();
}

$csv = new CSV($dbh, array('table' => 'chatbox_messages','name' => 'export_chatbox_messages', 'database' => 'chatbox', 'directory' => 'csv'));
```
