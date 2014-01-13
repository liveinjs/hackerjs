/**
 * 学习 Singleton 模式
 *
 * 直接创建对象
 * 创建有私有成员，私有方法的对象
 *
 * 创建唯一的一个对象.（单例）
 * 创建一个可定制的一个唯一的对象。(单例)
 * 单例模式，就是用用函数 返回一个单例。 
 */

var mySingleton = {
    property1:"something",
    property2:"something else",

    method1:function(){
        console.log("hello world");
    }
};

//私有成员与私有方法的实现。 定义一个闭包函数，返回值为一个对象。函数中定义的变量与函数，外部访问不了。
//每调用一次，都会生成一个对象。

var mySingleton2 = function() {
    var privateVariable = 'somethingg';
    function showPrivate() {
        console.log(privateVariable);
    }

    return {
        publicMethod:function(){
            showPrivate();
        },
        publicVar:'the public can see this'
    }
}

//3. 无论调用多少次，仅仅会生成一个对象！
var mySingleton = (function(){
    var instantiated;

    function init() {
        return {
            publicMethod:function(){
                console.log("hello world");
            },
            publicVar:'test'
        }
    }

    return {
        getInstance:function(){
            if(!instantiated) {
                instantiated = init();
            }
        return instantiated;
        }
    }
})();

//应用例子

var SingletonTester = (function () {

    function Singleton(options) {
        options = options || {};
        this.name = "SingletonTester";
        this.pointX = args.pointX || 6;
        this.pointY = args.pointY || 10;
    }

    var instance;

    var _static = {
        getIntance: function(options) {
            if(instance === undefined){
                instance = new Singleton(options);
            }
            return instance;
        }
    };

    return _static;
})();
