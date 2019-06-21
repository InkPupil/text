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
##Match对象
- 不需要new  封装了很多数学方法
- Math.ceil()天花板函数向上取整
```html
console.log(Math.ceil(4.9)); //5
console.log(Math.ceil(4.3)); //5
```
- Math.floor() 地板函数 向下取整
```html
console.log(Math(4.3));//4
console.log(Math(4.9));//4
```
- 求最大值/最小值

```html
console.log(Math.max(4,5,9));//求最大值
console.log(Math.min(2,3,4));//求最小值
```
- 返回0-1之间的任意数字 随机 不报括1

```html
console.log(Math.random());//返回0到1之间的不包括1
console.log(Math.floor(Math.random()*99));//0-99随机
console.log(Math.floor(Math.rendom()*99)+1);//1-99随机
console.log(Math.floor(Math.rendom()*8)+3);//3-10随机

//方法 Math.floor(Math.rendom()*个数)+最小值

console.log(Math.pow(2,3));//2的阶乘(2的3次方)

//Math.round()四舍五入

console.log(Math.round(4.9999999999));
//电脑存在舍入误差 2.9999999999999  3.0
//4.4999999999999999  4.5
```
##逻辑运算符

- **&&** 与 都真才真
- **||** 或 有一真便为真
- **!**  非 取反

```html
console.log(false&&true);//false
console.log(true||false);//true
consloe.log(!true);//false

//判断2 在不在 3和5之间
//console.log(2>3&&2<5);//false

//判断一个人是否能够考驾照,交通法规定18-70岁能够考驾照.
//var age=Number(proment('请输入你的年龄'));//string
//console.log(age);
//逻辑运算符返回的是操作数

var a5 ='Gat'&&'Dog';//遇到false就返回 Dog
//与 && 当第一个值为假时 直接返回操作数
//当第一个值为真时 直接返回第二个操作数

var a6='cat'&& false;//false

var a7=0 && 'gat';//false

var a8='cat' && '';//''

// ||遇到true就返回

var b1='cat' || 'dog';//cat
var b2='false' || 'cat';//cat
var b3='cat' || false;//cat
var n3=!'cat'//false
```
##if语句
- if....else....

```html
 // 用户输入自己的考试成绩，提示用户是否及格。如果及格了，弹出警告框“恭喜，你及格了”、“不要骄傲啊”。
        // 如果没有及格，
        // 那么弹出警告框“很遗憾，你没有及格”、“请继续努力啊”。 然后都弹出“么么哒”。
 var cj=Number(prompt('请输入你的成绩'));
        if(cj>=60){
            alert('成绩及格')
        }else{
            alert('恭喜你,成绩不及格')
        }
        alert('么么哒');
    
```
##多分支lf语句

```html
// 每一个 else if  都暗含了 不符和 上边的条件

        //         【分组探究作业】根据BMI（身体质量指数）显示一个人的体型。
        // BMI指数，就是体重、身高的一个计算公式。公式是：
        // BMI =体重÷身高的平方

        // 比如，老师的体重是81.6公斤，身高是1.71米。
        // 那么老师的BMI就是  81.6 ÷ 1.712     等于 27.906022365856163

        // 过轻：低于18.5
        // 正常：18.5-24.99999999
        // 过重：25-27.9999999
        // 肥胖：28-32
        // 非常肥胖, 高于32
        var height= parseFloat(prompt('身高:单位m'));

        var weight= parseFloat(prompt('体重:单位kg'));

        var BMI =weight/Math.pow(height,2);
        console.log(BMI);
        if(BMI>32){
            alert('非常肥胖')
        }else if(BIM<=32&&BIM>=28){
            alert('肥胖')
        }else if(BIM<28&&BIM>=25){
            alert('过重')
        }else if(BIM<25&&BIM>=18.5){
            alert('正常')
        }else{
            alert('过轻')
        }


```
##if语句的嵌套

```html
 //     小例子：
                // 一个加油站为了鼓励车主多加油，所以加的多有优惠。
                // 92号汽油，每升6元；如果大于等于20升，那么每升5.9；
                // 95号汽油，每升7元；如果大于等于30升，那么每升6.95
                // 编写JS程序，用户输入自己的汽油编号，然后输入自己加多少升，弹出价格。
                // var type = prompt('请输入油号(92或者95)');
                // var count = parseFloat(prompt('请输入油量(升)'));
                var type = '92';
                var count = 30;
                var price;
                var totalPrice;
                if (type == '92') {
                    // 判断加了多少油,修改价格
                    if (count >= 20) {
                        price = 5.9;
                    } else {
                        price = 6;
                    }
                    // alert(price * count)
                } else if (type == '95') {
                    if (count >= 30) {
                        price = 6.95;
                    } else {
                        price = 7;
                    }
                    // alert(count * price)
                } else {
                    alert('请输入正确的油号')
                }
                totalPrice = count * price;
                alert('您本次加了' + count + '升' + type + '号汽油,共' + totalPrice + '元');
                // 您本次加了30升92号汽油,共210元
        
        
                // if 语句 小知识点
                // else 部分 如果什么都不做  可以省略不写
```
##三元表达式

```html
if(3>5){
    a=5
}else{
    a=3
}
//三元表达式表达 
var a=3>5?5:3;
```
##for循环

```html

 // 遍历
        console.log(1);
        // 想在控制台打印 100  个  1
        // 自动循环执行
        for (var i = 0; i < 100; i = i + 2) {
            // 变量  i  循环变量
            // i<100  循环条件
            // 符合条件  执行里边的代码一次
            // 执行完之后
            // 执行i++  循环的 步长
            console.log(1);
        }

        // 打印  1---100  这些数字
        // 奇数
        for (var i = 1; i <= 100; i = i + 2) {
            console.log(i);
        }

        // 分析程序走向
        for (var j = 1; j < 13; j = j + 4) {
            console.log(j);
        }
        // 1    j==>5
        // 5    j===>9
        // 9    j==>13
        console.log(j); // 13



        for (var i = 1; i < 10; i = i + 3) {
            i = i + 1;
            console.log(i);
        }
        // 2   6   10 

        for (var i = 1; i < 10; i = i + 1) {
            if (i % 2 == 0) {
                i = i * 2;
            }
            console.log(i);
        }
        // 1  4   5  12

        // for (var i = 1; i > 0; i++) {
        //     console.log(i);
        // }
```

##枚举

```html
var num =prompt(''输入数字')
 switch(num){
     case'1';
      console.log('1');
      break;
      case'2';
      console.log('2');
      break;
      case'3';
      console.log('3');
      baeak
    default:
    console.log('不是预定的数字')
 }
 ```
 ##while语句与dowhile语句

 - while 语句页可以实现循环 
 ```html
 var num=0;
 while(num<10){
     console.log(num);
     num++;
 }

 //先执行 后判断

 var count=10;
 do{
     console.log(count);
     count++;
 }while(count<10);
  //年利率为5% 1000涨到5000需要多少年 
            var year=0;
            var money=1000;
            while(money<5000){
                money*=1.05;//money=money*1.5
                year++;
            }
            console.log(year);
```

##break与continue

- **break**:跳出循环
- **continue**:结束本次循环.

```html
//从1-99找到一个+5+7之后能被33整除的数
//在找到第一个后 没必要进行额外的运算 这时候就可以终止循环
for(var i= ;i<100;i++){
    if((i+5+7)%33===0){
        console.log('找到一个符合条件的一个数',i);
        break;跳出循环
    }
}
//需求 找到0-30中所有能被3整除的,或者能被7整除的数
for(var i=0;i<=30;i++){
    if(i%3===0){
        console.log('这个数能被3整除',i)
    }
    if(i%7===0){
        console.log('这个数能被7整除',i)
    }
}
```


##for的嵌套

```html
//打印9*9乘法表
for(var i=1;i<10;i++){
    var str='';
    //内置for循环 走完后 外层的for循环的i才会增加步长;

    for(var j=1;j<10;;j++){
        if(j<=i){
            str=str+''+i+'*'+j+'='+i*j+';'
        }
    }
    console.log(str);
}
```

##数组

```html
var arr=[30,29,24,22];
var arr1=[];
var newArr=new Array();
console.log(newArr);
console.log(arr1);
arr[2]=25;//修改arr数组下标为2的数值
console.log(arr[2]);//打印下标为2的数值
console.log(arr.length);//打印数组的长度
```
##数组的遍历

```html

var arr=[20,10,30,25,15];
for(var i=0;i<arr.length;i++){
    if(arr[i]<20){
        console.log(arr[i]);
    }
}
//for in 循环 多用于对象
//index
for(var index in arr){
    console.log(index);
    console.log(arr[index])
}
```

##数组的方法

- **concat**:合并数组 
```html
var arr=[2,5,3,4,1];
var arr1=[7,5,9];
var arr2=arr.concat(arr1)
console.log(arr2);
```
- **数组转为字符串**: xx.join;
```html
var arrstr=arr2.join('-');
var arrstr1=arr.join(' ');
console,log(arrstr);
connsole,log(arrstr1);
```
- **字符串转为数组**:语法.split(分割符,数组长度)
- 通过指定分隔符，如果省略，默认以逗号分隔，将字符串分割为字符串数组。
- 第二个参数，制定返回数组的最大长度。

```html
var emarr='abc@163.com;cc@126.com;frg@qq.com';
    var emarr1=emarr.split(';',3);
    console.log(emarr1);
    console.log(emarr);
```

- **添加元素**:

- push()从后加入元素

- unshft()从前加入元素
- 都会改变原数组
```html
var temp=arr.push('zhangshan');
        arr.unshift('王五');
        arr.push('李四');
        console.log(arr);
        console.log(temp);
```
- **删除元素**:

- pop() 删除数组最后一个元素
- shift() 删除数组第一个元素
- 改变了原数组 并且返回删除的元素
```html
var temp2=arr.pop();
       var temp3= arr.shift();
        console.log(temp2);
        console.log(temp3);
        console.log(arr);
        var temp4=arr.push();//没有添加任何元素
        console.log(temp4);//这个得出的就是字符串的长度
```

##数组求平均

```html
  var arr=[20,50,30,80,400];
    // var sum=0;
    // for(var i =0;i<arr.length;i++){
        
    //     sum=sum+arr[i];
       
    // }
    //  console.log(sum);
    // var avj=sum/arr.length;
    // console.log(avj);
    // var temp=arr.push();
    // console.log(temp);
    //第二种方法函数封装
    function avj(arr){
        var sum=0;
        for(var i=0;i<arr.length-1;i++){
            sum=sum+arr[i];
        }
        var avj1=sum/arr.length;
        console.log(avj1);
    }
    avj(arr);
```

##冒泡排序

```html
// 从小到大 排列
        // 它重复地走访过要排序的元素列，依次比较两个相邻的元素，
        // 如果他们的顺序（如从大到小、首字母从A到Z）错误就把他们交换过来。
        // 走访元素的工作是重复地进行直到没有相邻元素需要交换，也就是说该元素列已经排序完成。
        // 第一轮
        // var arr=[5,20,15,16,18];
        // for(var i=0;i<arr.length-1;i++){
        //     if(arr[i]>arr[i+1]){
        //         var temp=arr[i];
        //         arr[i]=arr[i+1];
        //         arr[i+1]=temp;

        //     }
        //     console.log(arr);
        // }
        // console.log(arr);
        


        //冒泡优化

        var arr =[30,20,29,22];
        for(var j=1; j<arr.length;i++){
            //控制比较的次数(轮数)
            for(var i=0;i<arr.length-j;i++){
                //两两比较 冒泡
                //第一轮 比较 3次 0 1 2
                //第二轮 比较2次 0 1
                //第三轮 比较1次 0
                if(arr[i]>arr[i+1]){
                    //交换位置
                    //保留arr[i]的位置
                    var temp=arr[i];
                    arr[i]=arr[i+1];
                    arr[i+1]=temp;

                }
                console.log(arr)
            }
            console.log(arr)
        }
```

##函数 

- 函数就是封装

```html

    //函数就是封装
    // function foo(){
    //     alert('我是一个foo函数')
    // }
    // foo();
    // function foo1(){
    //     alert('我是一个f001函数')
    // }
     var sing=function (){
         alert('hello');
     }
    sing();
```

##函数的参数

```html
 // 封装一个函数,求两个数的和
		// 参数 就是  函和外界的 一个桥梁
		//  形参  x , y, 并参与实际运算,仅仅是为了 给 实参占位置 
		//  实参  3, 5 ,真正参与运算
        function arr(x,y){
            console.log(x+y);
        }
        arr(1,5);
```

##函数的返回值

- 1.函数程序运行后的结果外部需要使用的时候，我们不能拿到，需要通过return返回。
- 2.函数使用return语句后，这个函数会在执行完 return 语句之后停止并立即退出，也就是说return后面的所有其他代码都不会再执行。
- 3.函数里面可以没有return。

```html
 var a=5;
    var b=6;
    function add(x,y){
        var sum=x+y;
        alert('执行');
        return sum;
    }
    var he=add(a,b)
    console.log(he);
```

##函数的封装案例

```html
var arr1 =[1,4,24,12,50];
function selectTion(arr){
    for(var i=0;i<arr.length;i++){
        var min=i
        for(var j=i+1;j<arr.length;j++){
            if(arr[min]>arr[j]){
                min=j
            }
        }
        var temp=arr[i];
        arr[i]=arr[min];
        arr[min]=temp;
    }
    retunt arr
}
var max=selectTion(arr1);
console.log(max);
```

##立即执行函数

- **具名函数**

- **匿名函数表达式**

- **自执行函数(立即执行函数)**: 方法:(function(){})
```html

(function(){alert('你好')})()


```

##对象

```html

var obj={
    name:'张珊',
    age:5,
    sex:'男',
    say:function(){
        alert('hello')
    }
}
```

    






