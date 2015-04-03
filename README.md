    
## Authors & contact


Al-Fallouji Bashar 
    - bashar@alfallouji.com

    
## Documentation and download


Latest version is available on github at :
    - http://github.com/alfallouji/PHP-Multithread/


## License


This Code is released under the GNU LGPL

Please do not change the header of the file(s).

This library is free software; you can redistribute it and/or modify it 
under the terms of the GNU Lesser General Public License as published 
by the Free Software Foundation; either version 2 of the License, or 
(at your option) any later version.

This library is distributed in the hope that it will be useful, but 
WITHOUT ANY WARRANTY; without even the implied warranty of MERCHANTABILITY 
or FITNESS FOR A PARTICULAR PURPOSE.

See the GNU Lesser General Public License for more details.


## Description


This library provides a lightweight / simple PHP Oriented Object classe to handle multi-threading. Check the sample folder for examples on how to use it. This library requires to have the pcntl (http://php.net/pcntl) extension installed and it will only work with unix distributions.

## Setup 

You can use composer to use this library.

```
{
    "require": {
		"alfallouji/php_multithread": "*"
    }
}
```


## Usage

This client does not rely or depend on any framework and it should be fairly easy to integrate with your own code. You can use composer or your own custom autoloader.

The sample folder contains example on how to use this library.

## Example

### Multi-threading a simple task
```
require(__DIR__ . '/../vendor/autoload.php');

$maxThreads = 5;
echo 'Example of the multi-thread manager with ' . $maxThreads . ' threads' . PHP_EOL . PHP_EOL;
$params = array();
$exampleTask = new Threading\Task\Example($params);
$multithreadManager = new Threading\Multiple();

$cpt = 0;
while (++$cpt <= 30)
{
    $multithreadManager->start($exampleTask);
}
```

Will provide following output : 
```
Example of the multi-thread manager with 5 threads

[Pid:23447] Task executed at 2015-04-03 14:49:18
[Pid:23448] Task executed at 2015-04-03 14:49:18
[Pid:23449] Task executed at 2015-04-03 14:49:18
[Pid:23450] Task executed at 2015-04-03 14:49:18
[Pid:23451] Task executed at 2015-04-03 14:49:18
[Pid:23452] Task executed at 2015-04-03 14:49:19
[Pid:23454] Task executed at 2015-04-03 14:49:19
[Pid:23453] Task executed at 2015-04-03 14:49:19
[Pid:23455] Task executed at 2015-04-03 14:49:19
[Pid:23456] Task executed at 2015-04-03 14:49:19
[Pid:23457] Task executed at 2015-04-03 14:49:20
[Pid:23458] Task executed at 2015-04-03 14:49:20
[Pid:23459] Task executed at 2015-04-03 14:49:20
[Pid:23460] Task executed at 2015-04-03 14:49:20
[Pid:23461] Task executed at 2015-04-03 14:49:20
[Pid:23463] Task executed at 2015-04-03 14:49:21
[Pid:23462] Task executed at 2015-04-03 14:49:21
[Pid:23464] Task executed at 2015-04-03 14:49:21
[Pid:23465] Task executed at 2015-04-03 14:49:21
[Pid:23466] Task executed at 2015-04-03 14:49:21
[Pid:23467] Task executed at 2015-04-03 14:49:22
[Pid:23468] Task executed at 2015-04-03 14:49:22
[Pid:23470] Task executed at 2015-04-03 14:49:22
[Pid:23469] Task executed at 2015-04-03 14:49:22
[Pid:23471] Task executed at 2015-04-03 14:49:22
[Pid:23472] Task executed at 2015-04-03 14:49:23
[Pid:23473] Task executed at 2015-04-03 14:49:23
[Pid:23474] Task executed at 2015-04-03 14:49:23
[Pid:23475] Task executed at 2015-04-03 14:49:23
[Pid:23476] Task executed at 2015-04-03 14:49:23
```
