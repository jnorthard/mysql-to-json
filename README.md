# mysql-to-json
Write a MySQL Database to JSON using PHP
 
```
<?php
//Collect the data  
  $results = mysql_query("SELECT * FROM table");  
  $rows = array();
  while($r = mysql_fetch_assoc($results)) {
    $rows[] = $r;
  }
//Write the data to results.json
  $fp = fopen('results.json', 'w');
  fwrite($fp, json_encode($rows));
  fclose($fp);
?>
````
