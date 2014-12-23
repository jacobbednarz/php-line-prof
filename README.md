# PHP line profiler

php-line-prof is designed to enable developers to break down line by line which part of the script execution is causing a bottle neck.

### Example output

```
$ php php-line-prof.php

         | <?php
         |
         | include 'some_script.php';
         |
  0.05ms | $a = 'my cheap variable';
  0.07ms | $my_array = array(
         |   'colour' => 'red',
         |   'name' => 'Jacob',
         | );
         |
         | foreach ($my_array as $item) {
   119ms |   usleep(100000);
  0.15ms |   echo $item;
         | }
         |
         | $result = array_merge($my_array, array('shape' => 'square'));
  0.88ms | var_dump($result);
```
