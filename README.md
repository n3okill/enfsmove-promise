[![Build Status](https://travis-ci.org/n3okill/enfsmove-promise.svg)](https://travis-ci.org/n3okill/enfsmove-promise)
[![AppVeyor status](https://ci.appveyor.com/api/projects/status/7xg7sskffp2w49bc?svg=true)](https://ci.appveyor.com/project/n3okill/enfsmove-promise)
[![Codacy Badge](https://api.codacy.com/project/badge/Grade/f35b96facc764831999fb8fe30c8dafd)](https://www.codacy.com/app/n3okill/enfsmove-promise)
[![Donate](https://www.paypalobjects.com/en_US/i/btn/btn_donate_SM.gif)](https://www.paypal.com/cgi-bin/webscr?cmd=_s-xclick&hosted_button_id=64PYTCDH5UNZ6)

[![NPM](https://nodei.co/npm/enfsmove-promise.png)](https://nodei.co/npm/enfsmove-promise/)

enfsmove-promise
================
Module that add move functionality to node fs module with promises

**enfs** stands for [E]asy [N]ode [fs]

This module is intended to work as a sub-module of [enfs](https://www.npmjs.com/package/enfs)


Description
-----------
This module will add a method that allows moving files and directories in the file system.

- This module will add following methods to node fs module:
  * move
  
Usage
-----
`enfsmove-promise`

```js
    const enfsmove = require("enfsmove-promise");
```


Additional Methods
------------------
- [moveP](#moveP)


### moveP
  - **moveP(srcPath, dstPatch, [options])**

> Move files and directories in the file system

[options]:
  * fs (Object): an alternative fs module to use (default will be [enfspatch](https://www.npmjs.com/package/enfspatch))
  * mkdirp (Boolean): if true will create new directories instead of copying the old ones (default: false)
  * overwrite (Boolean): if true will overwrite items at destination if they exist (Default: false)
  * limit (Number): the maximum number of items being moved at a moment (Default: 512)
  

```js
    enfsmove.moveP("/home/myHome","/home/myOtherHome").then(function(){
        console.log("Everything moved correctly");
    }).catch(function(){
        console.log("Error occurred while moving.");
    });
```


License
-------

Creative Commons Attribution 4.0 International License

Copyright (c) 2017 Joao Parreira <joaofrparreira@gmail.com> [GitHub](https://github.com/n3okill)

This work is licensed under the Creative Commons Attribution 4.0 International License. 
To view a copy of this license, visit [CC-BY-4.0](http://creativecommons.org/licenses/by/4.0/).


