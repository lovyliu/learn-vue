###多个script标签中引用同一个变量的问题###

JavaScript解释器在执行脚本时，是按块来执行的。通俗地说，就是浏览器在解析HTML文档流时，如果遇到一个&lt;script&gt;标签，则JavaScript解释器会等到这个代码块都加载完后，先对代码块进行预编译，然后再执行。执行完毕后，浏览器会继续解析下面的HTML文档流，同时JavaScript解释器也准备好处理下一个代码块。

```html
<script type="text/javascript">
  a(); //报错
</script>
<script type="text/javascript">
  function a(){
    console.log('doing a ...')
  }
</script>
<script type="text/javascript">
  a(); // 输出doing a ...
</script>
```

此时在多个代码块中，访问同一个全局作用域，所以第三个代码块可以访问到a变量。但此时变量提升只能提升到相应代码块最前面，所以第一个script中执行a()会报错。
