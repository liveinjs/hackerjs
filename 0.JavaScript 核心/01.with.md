with ( object )
      statement
      
with 把 object 添加到作用域链的顶部，然后执行 statement, 最后把作用域链复原。


不要忘记，只有在查找标识符的时候，才用到作用域链，创建新的变量的时候不使用作用域链。

with ( o ) x = 1;

with 语句提供了一种访问 o 属性的快捷方式 ，但它不能给 o 创建新属性。
