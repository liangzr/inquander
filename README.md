inquander
=========

Inquirer for commander.
This module takes two awesome modules and connects them.

If no arguments and options are passed to your [commander](https://github.com/visionmedia/commander.js) app, it runs [inquirer](https://github.com/SBoudrias/Inquirer.js). For all commands, arguments and options defined in your commander app.


Usage
-----

Instead of calling programm.parse you need to call inquander.parse.

```Javascript
var program = require('commander'),
    inquander = require('inquander');

program
    .command('hello [name]')
    .action(function(name) {
        console.log('Hello', name);
    });
program
    .command('pay [creditcard]')
    .action(function(creditcard) {
        console.log('Please come again.');
        console.log(creditcard);
    });

inquander.parse(program, process.argv);
```

![call with arguments]()
![call without arguments]()
