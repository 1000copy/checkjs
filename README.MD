## Checkjs

Checkjs is a extremly simplize assert framework.talk in detail here :

1. one function `check()` vs. any condition of assert,such as equal,deepEqual,noEqual.
2. assert output is as simple as possible.It will not print any message if assert is ok.it will not print error stack unless you config it.

## Example code


        var check = require('check')
        check({a:1},{a:1},'object')
        var y = [1,2,3]
        check('1','1','string')
        check(1,1,'number')
        check([1],[1],'simple array')
        check([1,2,3],[1,2,3],'array')
        check([1,[2],3],[1,[2],3],'deep array')
        check(3,Object.keys(y).length,'len',true)//if trace:true then print stacktree

## Usage

Call this function to check if variable of value1 equal (or deep equal) to value1.if false then print `msg' message to console,if trace is true then print call stack.

        function prototype:check(value1,value2,msg,trace)
parameter value1 and value1 is required ,and `msg` and `trace' is  optional.

## License 

[gpl3.0](LICENSE)

