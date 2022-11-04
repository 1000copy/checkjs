## Checkjs

极简的断言框架，表现在：

1. 一个函数搞定assert的各种情况。
2. 输出内容极简。仅仅显示当前的check结果。如果assert是对的，那么什么也不输出
3. 默认不打印错误堆栈

## 调用案例

        var check = require('../lib/check.js')
        check({a:1},{a:1},'object')
        // t([1]===[1])
        var y = [1,2,3]
        check('1','1','string')
        check(1,1,'number')
        check([1],[1],'simple array')
        check([1,2,3],[1,2,3],'array')
        check([1,[2],3],[1,[2],3],'deep array')
        check(3,Object.keys(y).length,'len',true)//if trace:true then print stacktree


说明 ： check(value1,value2,msg,trace)

判断value1和value2是否相等，可以输入数字字符串数组对象，如果不等就打印msg消息，如果trace为true，就打印错误堆栈。

## TODO



## 工作日志


## 更多场景


## License 

[gpl3.0](LICENSE)