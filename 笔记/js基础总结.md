#js基础
**js几种外部不同的引用方式**
- **头部书写**:
- **头部写入**:
- **内部书写**:
- **内部引入**:

**js的变量**
- **变量命名的规则**: 
- 1.字母 数字 _ $;
- 2.不能以数字开头3.严格区分发小写;
- 4.不能使用关键字 保留字(name this new.......)
- 5.驼峰命名规则;
- 6.见名知意; 

-  var中间有空格
-  var age;
-  
-  age = 20;// = 是赋值操作 把左边的值赋值给右边
-  
-  var age1=18;// 声明了变量.ag1并且赋值18;声明变量的同时给一个初始值
- 
-  var age2 = 30,firstName="zhang",lastName="san"; // 声明多个变量
-  // 每一行代码结束都用分号结束 
-  **变量必须先声明在使用**

**数据类型**

- **基础数据类型**

- **1.字符串**
- 用引号或者双引号包裹;
- 单双引号不能嵌套,可以混用
```html
var str= '我是一个字符串';
        var str2='不凡学院';
        var str3=str+str2;
        console.log(str3);
```
- **2.number类型(整数.小数..浮点数)**
```html
  var number=20;
        var age=15;
        var floatNum=12.9;
        console.log(number);

        console.log(str-str2);
```
- 计算不出结果返回nan
- 无穷大infinity -infinty负无穷大

- **3.布尔值类型boolean**
- true(真/符合条件)flase(假/不符合条件)
- 条件判断常用   
```html
var sex=true;
console.log(sex);
console.log('true');
``` 
- **4.undefined类型**
- 当声明一个变量,没有初始化,默认也会给他初始化一个undefined值;
```html
    var a;
    console.log(a);
```

- **5.null类型 空值**
```html
        var timel=null;
        console.log(timel);
```

- **6.es6新增了Symbol类型**

**复杂数据类型**
- **object**
- **Array数组类型**
- **Function函数**

- 归根结底都是object
- key:value;
```html
var obj={
    name:'李四',
    age:6,
    sex:true,
    children:{
                 name='李四',
                 age=30
             }
}
```
**数组类型**
```html
var arr=[4,5,6,name:李四,age:8,true,'不凡学院']

```
- 数组元素 逗号隔开.

- 判断数据类型
```html
console.log(typeof str);//string
        console.log(typeof age);//number
        console.log(typeof sex); // boolean
        console.log(typeof firstName); // undefined
        console.log(typeof timer); // object
        console.log(typeof obj); // object
        console.log(typeof arr); // object
        console.log(typeof foo); // function
```

**数据类型的转换**

- **转换string类型**:
- console.log(''+null);
- toString()

```html
console.log('hello'+null)//
console.log(true.toString())//
```

- **转换为boolean类型**
-    数据0
-    // NaN
-    // ""空字符串
-    // false
-    //  undefined
-    // null
-    // 全是false
-    console.log(Boolean(0));
-    console.log(Boolean(NaN));
-    console.log(Boolean(""));
-    console.log(Boolean(false));
-    console.log(Boolean(undefined));
-    console.log(Boolean(null));

- **转换为number**

- **Number** 可以把数字类型的字符串转换为数字
- console.log(Number('123.123'))
  console.log(Number(true));//true 1 false 0
- **parseInt转换成整数,只取整数部分**
    console.log(parseInt('123.9'));//123
    console.log(parseInnt('123a3'));//123
    console.log(parseInt(''));//nan
- **parseFloat转换成小数**
    console.log(parseFloat('123.99.33'));//123.99
    console.log(parseFloat('123.9a9'));//123.9

##比较运算符

-   >大于 >=大于等于 <小于 <=小于等于 ==等于 ===严格等于 !=(==的反面) !==(===的反面)
-   比较运算符返回值 true false 

```html
console.log(5>3);//true
    console.log(3>5);//false
    console.log(5==5);//true
```
- // == 假如数据类型不一致 ,会将其它数据类型转换为number,再比较.

```html
console.log(5=='5');//true 隐式转换  将 '5'转换成了 5
```
- === 数据类型不一样直接false
- 比较的时候 一方是数字 一方不是数字,会把不是数字的 转换成数字
```html
    console.log('5'>2);//true
    console.log('ab' > 'ac'); // 97>98
        // 比较运算符 不能连用 a>b>c
         
```
##基础数据类型和复杂(引用)数据类型的区别
- var a=0;

- 基础数据类型存放在栈内存中

- 引用数据类型,(复杂数据类型存放在堆内存当中)(堆内存当中)
- 在堆内存开辟空间 存放了这个对象, 数据本身
- 同时在栈内存当中开辟空间 存放了变量obj(放的是 指针, 指向堆内存当中的这个对象) 并不是数据本身
```html
var obj = {
            name: '张三'
            // 属性名:属性值
        }
        var obj2 = obj; // 赋给它的 仅仅是一个 引用地址 指针变量(地址)

        obj.name = '李四';
        console.log(obj.name); // 李四
        console.log(obj2.name); // 李四  
```

##算数运算符

- 乘法  除法  取余  都会把 数字类型的字符串  转换成number (加法除外)

```html
var a=3;
var b=4;
var c='5';
console.log(b+c);//45 加 拼接
console.log(b-d);//-1  
        console.log(Infinity * 0); // NAN 
        console.log(b*d);//20
        console.log(d/b);//1.25
        console.log(d%b);//1求余
          // 括号  提升运算优先级
        // 有括号 先算括号里边的
```
##赋值运算

```html
var a =1;
         a=10;
         var b=a+10;//20
         a=a+3;
         console.log(a);
         var c=10;
        //  c=c+5;
        //  c+=5;
        c+=1;
        // 自加一
        var temp=c++;//先把c的值赋给a,然后自加1

        console.log(temp);//11
        var d=9;
        var temp2=++d;//先加一 再赋值
        console.log(d);//10
        console.log(temp2)//10
```
##Date对象
```html

    var obj={
        namme='张珊',
        age:14,
        say:function(){
            alert('你好')
        }
    }
    //获取对象的属性 对象.xxx 静态的 小狗的颜色身高
    //调用对象的方法 对象.xx() 动态的 小狗跑 小狗跳
    console.log(obj.name);
    console.log(obj.age);
    //obj.say();


    //创造构造函数(Date)的实例对象
    var date =new Date();
    console.log(date);
    console.log(new Date());
    // date实例对象 具有 很多方法和属性
    var year=date.getFullYear();//年份
    var month= date.getMonth()+1;//月份
    var day= date.getDate();//日期
    var weekDay=date.getDay();//周几
    var hour=date.getHours();//小时
    var min=date.getMinutes();//分钟
    var second=date.getSeconds();//秒
    var milliSecond=date.getMilisecond();//毫秒
    //常规拼接操作
    var timestr=year+'-'+month+'-'+day+'-'+hour+':'+min+':'+second;
    console.log(timester);
    //时间戳
    var stamp=date.getTime();
    //当前时间见距离1970年0分0秒的毫秒数
    console.log(stamp);
```



