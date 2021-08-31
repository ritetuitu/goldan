<h3>1.JS写法

```html
·<!-- 1.行内式JS -->
<input type="button" value="蜡笔小新" onclick="alert('夏日') ">
·//2. 内嵌式
·<script>
    alert('哪吒')
</script>
·<!-- 3.外部js 双标签 -->
<script src="./js/my.js"></script>
```


    方法
    alert(msg)  浏览器弹出警示框，输出的结果展示给用户    浏览器
    console.log(msg)    浏览器控制台打印输出信息，程序员看到的    浏览器console
    prompt(info)    浏览器弹出输入框，用户可以输入  浏览器

<h1>1.变量

<h3>1.1什么是变量</h3>用于存放数据的容器

<h3>1.2变量在内存中的存储</h3>变量是程序在内存中申请的一块用来存放数据的空间

<h3>2.变量的使用</h3>
1.**声明变量** 

·var	js的关键字，用来声明变量(variable 变量的意思)。使用该关键字声明变量后，计算机会自动为变量分配内存空间

·age	是程序员定义的变量名，通过变量名来访问内存中分配的空间

2.**赋值**

age = 10; 	//age 变量赋值为10

·= 用来把右边的赋值给左边的变量空间中

·变量值是程序员保存到变量空间里的值

```js
				// 1. 声明一个age 变量
        var age;
        // 2. 赋值  把值存入这个变量中
        age = 18;
        // 3. 输出结果
        console.log(age)
        // 4. 变量初始化
        var myname = 'leezheyi'
        console.log(myname)
```

<h3>1.4更新变量</h3>
1.变量被重新赋值后，原有的值会被覆盖，以最后一次的值为准

```js
var age = 26;
        age = 100; //结果是100
console.log(age);
```

2.声明多个变量

```js
        var myname = 'lizheyi';
        age = '81',
        address='foshan';
```

3.1只声明 不赋值

```js
var sex;

console.log(sex); //undefined
```

3.2不声明不赋值 直接使用某个变量会报错，js就此停止

```
console.log(sex); 
```

3.3不声明 直接赋值使用	可以正常输出 不建议使用

```js
name = lzheyi;
console.log(name)
```

<h3>1.5变量命名规范</h3>

<img src="/Users/aoki/Library/Application Support/typora-user-images/image-20210813140524148.png" alt="image-20210813140524148" style="zoom:33%;" />

**不要使用name作为变量名**

<img src="/Users/aoki/Library/Application Support/typora-user-images/image-20210813140707738.png" alt="image-20210813140707738" style="zoom:33%;" />

<h3>交换变量</h3>

使用临时变量用来做中间存储

```js
<script>
        // 1.需要一个临时变量
        // 2.apple1 给临时变量 temp
        // 3.apple2 里面的苹果给 apple1
        // 4.临时变量里面的值给apple2
        var temp; // 临时变量为空
        var apple1 = '青苹果';
        var apple2 = '红苹果';
        temp = apple1;
        apple1 = apple2;
        apple2 = temp;
        console.log(apple1);
        console.log(apple2)
    </script>
```

<img src="/Users/aoki/Library/Application Support/typora-user-images/image-20210813144151512.png" alt="image-20210813144151512" style="zoom:50%;" />输出结果

1.5**小结**

·为什么需要变量	：一些数据需要保存

·变量是什么	：变量就是一个容器，用来存放数据，方便以后使用里面的数据

·变量的本质	：变量是内存里的一块空间，用来存储数据

·变量的使用	：声明变量(去内存申请空间)➡️然后赋值

·声明变量并赋值我们称之为变量的初始化



<h1>数据类型</h1>

<h3>1.1为什么需要数据类型</h3>在计算机中，不同的数据所需占用的存储空间不同，为了便于把数据分成所需内存大小不同的数据，充分利用存储空间。“李四”“年龄18”，数据不同的类型

<h3>1.2变量的数据类型</h3>JavaScript是弱类型/动态语言

```js
        var num;    //这里的num 不确定属于哪种数据类型
        // 1.js的变量数据类型是只有程序在运行过程中，根据等号右边的值来确定
        // 2.js是动态语言 变量的数据类型可以变化，变量可用作不同类型
        var x = 10;  //x是数字型
        x = 'lee'; //x是字符型
```



<h3>1.2数据类型的分类</h3>

·简单数据类型——number	boolean	string	undefined	null

·复杂数据类型——object

<h3>2.1 简单数据类型（基础数据类型）</h3>

Number	数字型，包含整型值和浮点型值，如21/0.21	默认值：0

Boolean	布尔值类型，如true/false，等价于1和0	默认值：false

String	字符串类型，字符串类型里面都带引号，“李四”	默认：“”

Undefined	var a;	a = undefined 声明了变量a但是没有给值	默认：undefined

Null	var a = null; 声明了变量a为空值	默认：null

<h3>2.2 Number 数字型</h3>

1.数字型进制

八进制OCT，以数字0开始表明该数字是八进制：

```js
        // 1.八进制 最小是0～最大是7 程序里面数字前面加0 表示八进制，逢8进1	
        var num1 = 010
        console.log(num1);	//	010 八进制转换为10进制就是8
```

<img src="/Users/aoki/Library/Application Support/typora-user-images/image-20210813151002522.png" alt="image-20210813151002522" style="zoom:50%;" />



十六进制HEX，以0x开始表示该数字是十六进制：0～9	a～f	#ffffff	| 0123456789abcded

<h5>2.数字型范围</h5>

JS中最大值 最小值

```js
        alert(Number.MAX_VALUE); // 1.7976931348623157e+308 最大值
        alert(Number.MIN_VALUE); // 5e-324 最小值
```

<h5>3.数字型三个特殊值</h5>

·infinity 无穷大∞，大于任何数值

·- infinity 无穷小，小于任何数值

·NaN，Not a number，代表一个非数值

```js
        console.log(Number.MAX_VALUE * 2);  //无穷大
        console.log(-Number.MAX_VALUE * 2); //无穷小
        console.log('lzheyi' + 100);    // 非数字，NAN
```

<img src="/Users/aoki/Library/Application Support/typora-user-images/image-20210813160348101.png" alt="image-20210813160348101" style="zoom:50%;" />

<h5>4.isNaN()</h5>判断一个变量是否为非数字类型，返回true/false

```js
        console.log(isNaN(12)); //返回结果是：false
        console.log(isNaN('lee')); //返回结果是：true
```



<h3>2.3字符串型 String</h3>	单引号嵌套双引号/双引号嵌套单引号（外双内单，外单内双）

```js
        var myname = 'lee"ritetuitu"zheyi'  //外单内双
```

字符串转移字符 “\”写在引号里

\n	换行符号，n=newline

\	斜杠\

\'	单引号\

\"	双引号

\t	tab缩进

\b	空格，b=blank

<h5>3.字符串长度</h5>检测获取字符串的长度 length

```js
        var myname = 'my name is lee'
        console.log(myname.length); //14字符
```

<h5>4.字符串拼接</h5> 数值相加，字符相联

·多个字符串之间可以使用+进行拼接：字符串+任何类型=拼接之后的新字符串

·拼接前会把与字符串相加的任何类型转成字符串，在拼接成一个新的字符串

```js
        console.log('小李' + '小王');   //小李小王
        console.log('blue' + 21);   //blue21
        console.log(12 + 12);   //24
        console.log('12' + 12);   //1212
```

<img src="/Users/aoki/Library/Application Support/typora-user-images/image-20210813163118133.png" alt="image-20210813163118133" style="zoom:50%;" />

<h5>5.字符串拼接</h5> 引引加加

```js
        //变量不写在字符串里面，通过和字符串相联的方式实现
        var age = 25;
        console.log('lee' + age + '岁');
```

**案例**：

1.弹出输入框(prompt)，让用户输入名字(你是谁)

2.用户输入的值用变量保存 var name = prompt，把输入的名字与所要输出的字符串拼接(程序内部处理)

3.使用alert弹出警示框(输出结果)

```js
        var name = prompt('你是谁')	//输入框prompt，变量保存
        var str = '我是' + name + '大爷';	//程序内部处理 输入的名字和输出的字符串拼接
        var age = prompt('输入年龄')
        var vv = '今天' + age + '岁';
        alert(str) //输出结果
        alert(vv)
```



<img src="/Users/aoki/Library/Application Support/typora-user-images/image-20210813164536091.png" alt="image-20210813164536091" style="zoom:50%;" /><img src="/Users/aoki/Library/Application Support/typora-user-images/image-20210813164546641.png" alt="image-20210813164546641" style="zoom:50%;" />

<h3>2.5布尔型 Boolean</h3>两个值 true(真 对) ｜ false(假 错)

```js
        // 加法运算 true=1  false=0
        var flag = true; //flag布尔型 
        var flag1 = false; //flag布尔型 
        console.log(flag + 1);  //1
        console.log(flag + 1);  //0

```

<h3>2.6 Undefined Null</h3>
·一个声明没有被赋值的变量会有一个默认值Undefined（相联/相加时注意结果）

·一个声明变量给null值，里面的值为空

```js
        //如果一个变量声明没有赋值  就是 undefined未定义数据类型
        var str;
        console.log(str);
        var variable = undefined;
        console.log(variable + 'lee');  //undefinedlee字符串
        console.log(variable + 1);  //NaN   underfined+数字 结果是not a number
        console.log(true + variable);   //NaN
        //null  空值
        var space = null;
        console.log(space + 'lee'); //nunlee
        console.log(space + 1); //1 空值+数字 结果是数字
        console.log(true + space);  //1
```

<img src="/Users/aoki/Library/Application Support/typora-user-images/image-20210814111103858.png" alt="image-20210814111103858" style="zoom:50%;" />

<h2>3.获取变量数据类型</h2>
<h3>3.1获取检测变量的数据类型</h3>typeof可用来获取检测变量的数据类型

```js
        var num = 10;
        console.log(typeof num);    //number
        var str = 'lee';
        console.log(typeof str);    //string
        var flag = true;
        console.log(typeof flag);   //boolean
        var vari = undefined;
        console.log(typeof vari);   //undefined
        var timer = null;
        console.log(typeof timer);  //object对象

        //prompt的值是字符型 string
        var age = prompt('年龄')
        console.log(age);
        console.log(typeof age);
```

```js
        console.log(18);	//数字型
        console.log('18');	//字符串
        console.log(true);	//boolean
        console.log(undefined);	//undefined
        console.log(null);	//null 空值
```

<img src="/Users/aoki/Library/Application Support/typora-user-images/image-20210814113123205.png" alt="image-20210814113123205" style="zoom:50%;" />根据控制台的颜色来判断

<h3>3.2字面量</h3>源代码中一个固定值的表示法，字面量表示如何表达这个值

·数字字面量：8 9 10

·字符串字面量：‘lee’ “lee”

·布尔字面量：true false



<h2>4.数据类型转换</h2>

<h3>4.1什么是数据类型转换</h3>
使用表单，prompt获取过来的数据默认是**字符串类型**，此时不能直接简单的进行加法运算，而需要转换变量的数据类型。把一种数据类型转换为另一种数据类型

·转换为string

·转换为Number

·转换为Boolean

<h3>4.2转换为字符串</h3>

·toString()	转换成字符串

·String()强制转换	转换成字符串

·加号拼接字符串	和字符串拼接的结果都是字符串(隐式转换)<img src="/Users/aoki/Library/Application Support/typora-user-images/image-20210814114732142.png" alt="image-20210814114732142" style="zoom:50%;" />

```js
        //1.把数字型转换为字符串型 toString()
        var num = 10;
        var str = num.toString();
        console.log(str);
        console.log(typeof str); //string
        //2.String()
        console.log(String(num));
        //3.利用+拼接字符串的方法实现效果
        console.log(num + '');
```

<h3>4.3转换为数字型(重点)</h3>

parseInt 整数 | parseFloat小数，注意单词大小写

```js
        //1. parseInt(变量) 字符型转换为数字型 结果是整数
        var age = prompt('age')
        console.log(parseInt(age));
        console.log(parseInt('6.3')); //6取整
        console.log(parseInt('120px')); //120 去掉px单位
        console.log(parseInt('rem120px')); //NaN
        console.log(typeof age);
        //2.parseFloat(变量) 字符型转换为数字型 结果是小数 浮点数
        console.log(parseFloat('3.14')); //3.14
        console.log(parseFloat('120px')); //120 去掉px单位
        console.log(parseFloat('rem120px')); //NaN
        //3.Number(变量)
        var str = '123'
        console.log(Number(str));   //12 数字
        console.log(Number('123')); //12 数字
        //4.算数运算 - * / 隐式转换
        console.log('12' - 0);  //数字型
        console.log('12' - '10');   //2 数字型
        console.log('12' + 0);  //120 字符型
```

<img src="/Users/aoki/Library/Application Support/typora-user-images/image-20210814120301013.png" alt="image-20210814120301013" style="zoom:50%;" />

<h3>4.4转换为布尔型</h3>

Boolean()函数	其他类型转换成布尔型	Boolean(‘true’);

·空、否定的值会被转换为false，0/‘’/NaN/null/undefined

·其余值都会被转换为true

```js
      	console.log(Boolean(''));   //false
        console.log(Boolean(0));    //false
        console.log(Boolean(NaN));  //false
        console.log(Boolean(null)); //false
        console.log(Boolean(undefined));    //false
        console.log(Boolean('lee'));    //true
        console.log(Boolean(2021)); //true
```


<h1>解释型语言和编译型语言
<img src="/Users/aoki/Library/Application Support/typora-user-images/image-20210816141150266.png" alt="image-20210816141150266" style="zoom:50%;" />



<h1>2.标识符、关键字、保留字</h1>

<h3>1.标识符</h3>开发人员为变量/属性/函数/参数取得名字。标识符不能是关键字/保留字

<h3>2.关键字</h3>JS本身已经使用的字，不能再用充当变量名/方法名。

包括：break/case/catch/continue/default/delete/do/else/finally/for/…

<h3>3.保留字</h3>实际上就是预留的“关键字”，现在虽然不是关键字，但是未来可能会成为关键字。不能当变量名/方法名。

包括：boolean/byte/char/class/const/debugger/doouble/enum/export/extends/fimal/float/goto/implements/import/int/interface/log/mative/

package/private/protected/public/…



<h1>1.运算符operator</h1> 也被称为操作符，用于实现赋值、比较和执行算术运算等功能的符号

<h3>2.1~3算数运算符</h3>

***=赋值***	 ***==判断两边是否相等***

+ 加 +

+ 减 -

+ 乘 *

+ 除 /

+ 取余 %

  ```js
          console.log(1 + 1); // 2
          console.log(1 - 1); // 0
          console.log(2 * 2); // 4
          console.log(2 / 2); // 1
          //1.% 取余
          console.log(4 % 2); // 0
          console.log(5 % 2); // 1
          console.log(2 % 5); // 2
          //2.浮点数 算数运算里会有问题
          console.log(0.1 + 0.2); // 0.30000000000000004
          console.log(0.07 * 100); // 7.000000000000001
          var num = 0.1 + 0.2;
          console.log(num == 0.3); // false 
  ```

+ 浮点数最高精度是17位小数，运算时其精确度不如整数。**不要判断两个浮点数是否相等**

？怎么判断一个数能够被整除：余数是0说明这个数能被整除，%取余运算符的主要用途

？1+2*3= 7：算数运算符优先级

<h3>2.4表达式 返回值</h3>表达式：数字、运算符、变量等组成的公式，表达式都会有结果，称为返回值

```js
        console.log(1 + 1); // 2是返回值
        // 1 + 1 = 2
        //在程序里 2 = 1 + 1 把右边表达式计算完毕 返回值给左边
        var num = 1 + 1;
```

<h2>3.递增和递减运算符</h2>

<h3>3.1递增和递减运算符概述</h3>

如果需要反复给数字变量添加/减去1，可以使用递增(++)递减(- -)运算符来完成

递增(++)递减(- -)放在变量前后都可以。放在变量前面是，称为前置递增/递减运算符。放在变量后面，称为后置递增/递减运算符。

**递增和递减运算符必须和变量配合使用** 

<h3>3.2递增运算符</h3>

**1.前置递增运算符( ++num )**

++num 前置递增，自加1，**先自加，后返回原值**

```js
        var age = 10;
        ++age;  // age = age + 1
        console.log(age); // 11
        // 先加1 后返回10
        var p = 10;
        console.log(++p + 10); //21 ++p=11
```

**2.后置递增运算符( num++ )**

**先返回原值，后自加**

```js
        // 1.前置自增和后置自增单独使用时效果一样
        // 2.后置自增 先运算，后自加
        var age = 10;
        console.log(age++ + 10); // 20 	age++ = 10 age =11
        console.log(age); // 11
```

```js
        var a = 10;
        ++a;    // ++a 11   a = 11
        var b = ++a + 2;    // ++a = 12
        console.log(b);     // 14

        var c = 10;
        c++;    // c++ = 11 c = 11
        var d = c++ + 2; // c++ = 11 C = 12
        console.log(d); // 13

        var e = 10;
        var f = e++ + ++e  // 1.e++ = 10  e = 11  2.e = 12 ++e = 12
        console.log(f); // 22
				//后置递增 先表达式返回值 后面变量在自加1	表达式结果和变量结果
```

+ 前置递增和后置递增运算符可以简化代码的编写，让变量的值+1

+ 单独使用时运行结果相同

+ 与其他代码联用时，结果不同

+ 开发时大多使用 后置递增/减，代码独占一行，例如：num++;或者num- -;

  **e++ = 表达式结果   e = 变量结果**

  

### 4.1比较运算符：(关系运算符) 两个数据进行比较时使用的运算符，比较运算后，会返回一个布尔值(true/ false)作为运算结果

+ 小于 < 1<2 true
+ 大于 >  1>2 false
+ 大于等于 >=  2>=2 true
+ 小于等于 <= 3<=2  false
+ 判断号(会转型) ==  37 == 37  true
+ 不等号 != 37!=37  false
+ 全等 要求值和数据类型一致 全等=== / 不全等!== 37 === ‘37’ false

```js
        console.log(3 >= 5); // false
        console.log(2 <= 4); //true
        //1.程序里等于符号：==  默认转换数据类型 会把string数据转换为Number 只要求值相等就可以
        console.log(3 == 5); //false
        console.log('lee' == 'wang'); // false
        console.log(18 == 18); //true
        console.log(18 == '18'); //true 隐式转换
        console.log(18 != 18); //false
        // 2. 全等时 要求两侧的值和数据类型完全一致 才可以true
        console.log(18 === 18); //true
        console.log(18 !== '18'); //true Number String
        console.log(18 === '18'); // false
```

> = 赋值	把右边给左边
>
> == 判断	判断两边值是否相等（注意此时有隐式转换）
>
> === 全等(判断)	判断两遍值和数据类型是否完全相同

练习：

```js
        var num1 = 10;
        var num2 = 100;
        var res1 = num1 > num2; 
        var res2 = num1 = 11; 
        var res3 = num1 != num2; 
        console.log(num1 > num2); //false
        console.log(num1); // 11
        console.log(num1 != num2); //true
```



## 5.逻辑运算符

### 5.1逻辑运算符

+ &&	逻辑与/ and	两边都是true结果为true 否则返回false

+ ｜｜ 逻辑或/or   两边都是false结果为false 否则返回true

+ ！ 逻辑非/ not   取反值，用来取一个布尔值相反的值，true的相反值是false

  ```js
          //1.逻辑与 && and 两侧都为true 结果是true 只要一侧为false 结果为false
          console.log(3 > 5 && 3 > 2); //false
          console.log(3 < 5 && 3 > 2); //true
          //2.逻辑或 ｜｜ or 两侧都为false 结果是false 只要有一侧为true 结果为true
          console.log(3 > 5 || 3 > 2); //true
          console.log(3 > 5 || 3 < 2); //false
          // 3.逻辑非 ！ not
          console.log(!true); //fasle
          console.log(!false); //true
  ```

  <img src="/Users/aoki/Library/Application Support/typora-user-images/image-20210816171807709.png" alt="image-20210816171807709" style="zoom:50%;" />

<img src="/Users/aoki/Library/Application Support/typora-user-images/image-20210816171943710.png" alt="image-20210816171943710" style="zoom:50%;" />



### 5.4短路运算（逻辑中断）

短路运算：当有多个表达式(值)时，左边的表达式值可以确定结果时，就不再继续运算右边表达式的值

##### 1.逻辑与 && （短路运算）

+ 表达式1 && 表达式2
+ 如果表达式1的值为真，则返回表达式2
+ 如果表达式1的值为假，则返回表达式1

```js
        // 1.布尔值参与逻辑运算 true&&false == false
        // 2. 123 && 456 值/表达式参与逻辑计算
        // 3.逻辑与短路运算 如果表达式1 结果为真 则返回表达式2。如果表达式1为假 返回表达式1
        console.log(123 && 456); // 456
        console.log(0 && 456); // 0
        console.log(0 && 1 + 2 && 4 * 5); // 0
        console.log('' && 123); // 空
        // 如果有空的/否定的为假，其余是真的 0 '' null undefined NaN
```

<img src="/Users/aoki/Library/Application Support/typora-user-images/image-20210817105631833.png" alt="image-20210817105631833" style="zoom:33%;" />

##### 2.逻辑或 ｜｜（短路操作）

+ 表达式1 || 表达式2
+ 如果表达式1的值为真，则返回表达式1
+ 如果表达式1的值为假，则返回表达式2

```js
        // 4.逻辑或短路运算 ｜｜ 如果表达式1结果为真 则返回表达式1。 如果表达式1结果为假 则返回表达式2
        console.log(123 || 456); // 123
        console.log(123 || 456 || 789); //123
        console.log(0 || 123 || 456); //123

				//案例：逻辑中断很重要 会影响我们程序运行结果
        var num = 0;
        console.log(123 || num++); // 123结果为真 不执行num++
        console.log(num); // 0 
```



### 6.赋值运算符

用来把数据赋值给变量的运算符

=	直接赋值	var usrName=‘我是值’；

+=、-=	加、减一个数 后在赋值	var age = 10; age + 5; // 15

*=、/=、%=	乘、除、取余后在赋值	var age = 2;	age *= 5; // 10

```js
        var num = 10;
        num += 2;
        console.log(num); // 12
        num += 5;
        console.log(num); // 15
        var age = 2;
        age *= 3
        console.log(age); // 6
```



### 7.运算符优先级

1	小括号	（）

2	一元运算符	++  - - ！

3	算数运算符	先* / % 后+ -

4	关系运算符	> >= < <=

5	相等运算符	==	!=	===	!==

6	逻辑运算符	**先&& 后｜｜**

7	赋值运算符	=

8	逗号运算符	,

+ 一元运算符里面的逻辑非 ！优先级很高
+ 逻辑与&& 比 逻辑或｜｜ 优先级高

```js
// 练习1：
// true: (4 >= 6) f,('people' != '阿凡达') t, (!(12 * 2 == 144)) t, false|| true && true && true && true        
console.log(4 >= 6 || 'people' != '阿凡达' && !(12 * 2 == 144) && true); 
var num = 10;
console.log(5 === num / 2 && (2 + 2 * num).toString() === '22'); // true

// 练习2:
        var a = 3 > 5 && 2 < 7 && 3 == 4; // false
        console.log(a);
        var b = 3 <= 4 || 3 > 1 || 3 != 2; // true
        console.log(b);
        var c = 2 === '2'; // false
        console.log(c);
        var d = !c || b && a;
        console.log(d); // true
```



# 1.流程控制

在一个程序执行的过程中，各条代码的执行顺序对程序的结果是有直接影响的。很多时候我们要通过控制代码的执行顺序来实现我们要完成的功能。**控制代码按照什么结构顺序来执行**

顺序结构、分支结构、循环结构

<img src="/Users/aoki/Library/Application Support/typora-user-images/image-20210817115013239.png" alt="image-20210817115013239" style="zoom:30%;" />

## 2.顺序流程控制：代码的先后顺序，依次执行，大多数代码都是这样执行

## 3.分支流程控制 if语句

### 3.1分支结构

由上到下执行代码的过程中，根据不同的条件，执行不同的路径代码(执行代码多选一的过程)从而得到不同的结果

+ if语句

+ switch语句

  

### 3.2 if语句

##### 1.语法结构

语句可以理解为一个行为

```js
        // 1. if语法结构 
        if (条件表达式) {
            // 执行语句
        }

        // 2. 执行思路 如果if里面条件表达式为真 true，则执行{}里面的执行语句。如果if里面条件表达式为假 false，不执行{}里面的执行语句，则执行if语句后面的代码
        if (3 < 5) {
            // 执行
            alert('lee');
        } 
```

<img src="/Users/aoki/Library/Application Support/typora-user-images/image-20210817115911217.png" alt="image-20210817115911217" style="zoom:25%;" />

### 3.3 if else 语句(双分支语句)

##### 1.语法结构

```js
        // 1. 语法结构 if：如果  else：否则
        if (条件表达式) {
            // 执行语句1
        }
        else {
            // 执行语句2
        }
        // 2. 执行思路 如果表达式结果为真，则执行语句1，否则执行语句2
        // 3.代码执行
        var age = prompt('请输入年龄：');
        if (age >= 18) {
            alert('hello');
        }
        else {
            alert('byebye');
        }
        // 4. if里的语句1和else里的语句2，最终只能有一个语句执行，2选1
        // 5.else后面直接跟大括号{} 没有小括号
```

<img src="/Users/aoki/Library/Application Support/typora-user-images/image-20210817121243954.png" alt="image-20210817121243954" style="zoom:29%;" />

案例：

```js
        // 能被4整除且不能整除100的为闰年/能够被400整除的就是闰年
        // 1. 弹出prompt输入框，让用户输入年份，把这个值取过来保存到变量中
        // 2.使用if语句来判断是否是闰年，如果是闰年，就执行if打括号里面的输出语句，否则执行else里面的输出语句
        // 3. 一定要注意里面的逻辑和&& 还有逻辑或｜｜的写法，同时注意半段整除的方法是取余为0
        var year = prompt('请你输入年份：');
        if (year % 4 == 0 && year % 100 != 0 || year % 400 == 0) {
            alert('你输入的年份是闰年')
        } else {
            alert('你输入的年份是平年')
        }
//练习：
        var name = prompt('请输入名字：');
        if (name === '小王') {
            alert('奖励抱抱');
        } else {
            alert('再来一次');
        }
```



### 3.4 if else if 语句(多分支语句)

```js
        // 1.多分支语句 利用多个条件来选择不同的语句执行得到不同的结果 多选1的过程
        // 2. if else if 多分支语句
        // 3.语法规范
        if (条件表达式1) {
            // 语句1；
        } else if (条件表达式2) {
            // 语句2；
        } else if (条件表达式3) {
            // 语句3；
        } else {
            // 最后的语句；（上述表达都不成立时执行此处代码）
        }
        // 4.执行思路
        // 如果条件表达式1满足就执行，语句1执行完后，退出整个if分支语句
        // 如果条件表达式1 不满足，则判断条件表达式2，满足的就执行条件语句2，以此类推
        // 5.注意⚠️
        // ·多分支语句还是多选1 最后只能有一个语句执行
        // ·else if 里面的条件理论上是可以任意多个的
        // ·else if 中间有空格隔开
```

<img src="/Users/aoki/Library/Application Support/typora-user-images/image-20210817134416253.png" alt="image-20210817134416253" style="zoom:25%;" />

```js
//案例：
        // 中文——伪代码
        // 1.按照从大到小判断
        // 2.弹出prompt输入框，让用户输入分数(score)，把这个值取过来保存到变量中
        // 3.使用多分支 if else if语句来分别√判断输出不同的值
        var score = prompt('请输入分数：');
        if (score >= 90) {
            alert('A');
        } else if (score >= 80) {
            alert('B');
        } else if (score >= 70) {
            alert('C');
        } else if (score >= 60) {
            alert('D');
        } else {
            alert('E');
```



## 4.三元表达式

```js
        // 1.有三元运算符组成的式子称为三元表达式
        // 2. ++num(一元)  3 + 5(二元)  ? :(三元)  
        // 3.语法结构
        // 表达式 ？ 表达式1 ：表达式2
        // 如果条件表达式结果为真，则返回表达式1的值。如果条件表达式结果为假，则返回表达式2的值。
        var num = 10;
        var result = num > 5 ? 'yes' : 'no'; // 表达式有返回值
        console.log(result);

        // 同if else相同
        if (num > 5) {
            result = 'yes';
        } else {
            result = 'no';
        }
```

<img src="/Users/aoki/Library/Application Support/typora-user-images/image-20210817143527924.png" alt="image-20210817143527924" style="zoom:40%;" />

```js
// 案例
        // 1.用户输入0～59之间的数字
        // 2.数字小于10.则这个数字前面补0，（加0）否则不做操作
        // 3.用一个变量接受这个返回值，输出
				var time = prompt('输入0～59之间的数字');
        // 三元表达式  表达式？ 表达式1 ：表达式2
        var result = time < 10 ? '0' + time : time; // 把返回值赋值给一个变量
        alert(result);

```



## 5.分支流程控制switch语句

### 5.1 switch语法结构

switch语句是多分支语句，用于给予不同的条件来执行不同的代码。当要针对变量设置一系列的**特定值**的选项时用switch。

```js
        // 1.switch语句是多分支语句，也可以实现多选1
        // 2.语法结构 switch 转换、开关。case 小例/选项
        // 3.执行思路⬇️
        // 利用表达式的值，和case后面选项值匹配上，就执行改case里面的语句。如果都没有匹配上，则之心default里面的语句。
        switch (表达式) {
            case value1:
                执行语句1;
                break;
            case value2:
                执行语句2;
                break;
            ...
            default:
                执行最后的语句;
        }
        // 4.代码验证   switch表达式的值直接跳转与case的值匹配
        switch (2) {
            case 1:
                console.log('这是1');
                break;
            case 2:
                console.log('这是2');
                break;
            case 3:
                console.log('这是3');
                break;
            default:
                console.log('没有匹配结果');
        }
```

<img src="/Users/aoki/Library/Application Support/typora-user-images/image-20210817144916161.png" alt="image-20210817144916161" style="zoom:50%;" />

```js
        // switch 注意事项⚠️
        var num = 3;
        switch (num) {
            case 1:
                console.log(1);
                break;
            case 2:
                console.log(2);
                break;
            case 3:
                console.log(3);
                break;
        }
        // 1.开发里面表达式经常写为变量
        // 2.num的值和case的值相匹配的时候是全等 ===，必须是值和数据类型一致才可以 num === 1
        // 3.break 如果当前的case里面没有break，则不会退出switch，会继续执行下一个case。
```

```js
        //案例：
        // 弹出prompt输入框，让用户输入水果名称，把这个值取过来保存在变量中
        // 将这个变量作为switch 括号里面的表达式
        // case后面的值些几个不同的水果名称，注意一定要加引号，因为必须全等匹配
        // 弹出不同价格即可，注意每个case之后加上break，以便退出switch语句
        // default设置为没有此水果
        var fruit = prompt('请输入查询的水果：');
        switch (fruit) {
            case '芒果':
                alert('9.99/斤');
                break;
            case '桃子':
                alert('2.99/斤');
                break;
            default:
                alert('没有此水果');
        }
```

### 5.2 switch语句和 if else if语句区别

+ 一般情况下两个语句可以互换
+ switch…case语句通常处理case为比较确定值的情况，而if…else…语句更加灵活，常用于范围判断(大于、等于某个范围)
+ switch语句进行条件判断后直接执行到程序的条件语句，效率更高。if…else语句逐行判断，有几种条件，就要判断多少次
+ 当分支比较少时，if…else语句的执行效率更高
+ 当分支比较多时，switch…case语句的执行效率更高，而且结构清晰

```js
作业1:	
				//判断时间阶段。比如用户输入12弹出中午好，用户输入18点弹出傍晚好
        var time = prompt('请输入时间：');
        if (time == '12') {
            alert('中午好');
        } else if (time == '18') {
            alert('傍晚好');
        } else if (time == '23') {
            alert('深夜好');
        }
        else {
            alert('早上好');
        }

作业2:   
				// 比较两个数的最大值(用户依次输入2个值，最后弹出最大的那个值)
				var num1 = prompt('请输入第一个数字：')
        var num2 = prompt('请输入第二个数字：')
        // var定义的变量是字符串，单纯比较字符串会出现错误，需要先转化数字类型再做比较
        if (parseInt(num1) > parseInt(num2)) {
            alert('最大的数是' + num1)
        } else {
            alert('最大的数是' + num2)
        }

作业3:
				// 用户输入一个数判断是奇数偶数
        var num = prompt('请输入数字：');
        //判定条件余数为0时为偶数
        if (num % 2 == 0) {
            alert('偶数');
        } else {
            alert('奇数');
        }

作业4:
        // 根据用户输入的数值(数字1～数字7)，返回星期几
        var num = prompt('请输入数字1～7：');
        switch (num) {
            case '1':
                alert('星期一');
                break;
            case '2':
                alert('星期二');
                break;
            case '3':
                alert('星期三');
                break;
            case '4':
                alert('星期四');
                break;
            case '5':
                alert('星期五');
                break;
            case '6':
                alert('星期六');
                break;
            case '7':
                alert('星期日');
                break;
            default:
                alert('输入数字超出范围');
        }

作业5:
        // 口袋里的钱，大于等于2000吃西餐。小于2000，大于等于1500吃快餐。小于1500大于等于1000喝饮料。小于1000大于等于500吃棒棒糖。否则提醒把钱带够
        var money = prompt('兜里有多少钱');
        if (money >= 2000) {
            alert('吃西餐')
        } else if (money >= 1500) {
            alert('吃快餐')
        } else if (money >= 1000) {
            alert('喝饮料')
        } else if (money >= 500) {
            alert('吃糖')
        } else {
            alert('吃土')
        }

作业6:
        // 分数转换，给一个分数判断等级。大于等于90 A，大于等于80小于90 B，大于等于70小于80 C，大于等于60小于70 D，小于60 E
        // 方法一 switch case语句
				var value = prompt('请输入数字');
        var value = parseInt(value / 10);
        switch (value) {
            case 9:
                alert('A');
                break;
            case 8:
                alert('B');
                break;
            case 7:
                alert('C');
                break;
            case 6:
                alert('D');
                break;
            case 5:
            case 4:
            case 3:
            case 2:
            case 1:
                alert('E');
                break;
            default:
                alert('error')
        }

				//方法2 if else语句
        var value = prompt('请输入数字');
        // var value = parseInt(value / 10);
        if (value > 100 || value < 0) {
            alert('error')
        } else if (value >= 90) {
            alert('A');
        } else if (value >= 80) {
            alert('B');
        } else if (value >= 70) {
            alert('C');
        } else if (value >= 60) {
            alert('D');
        } else {
            alert('E')
        } 
```

# 循环

### 1.循环

有规律性的重复操作，完成这类操作就需要重复执行某些语句

### 2. for 循环

一组被重复执行的语句被称之为循环体，能否继续重复执行，取决于循环的终止条件。由循环体及循环的终止条件组成的语句，被称为循环语句。

### 2.1语法结构

for循环主要用于把某些代码循环若干次，通常跟计数有关系。

```js
        // 1.for 重复执行某些代码，通常跟计数有关系
        // 2.语法结构
        for (初始化变量; 条件表达式; 操作表达式) {
            // 循环体；
        }
        // 3. 初始化变量 就是用var声明的普通变量，通常用于作为计数器使用
        // 4.条件表达式 用来决定每一次循环是否继续执行，即终止条件
        // 5.操作表达式 每次循环最后执行的代码 经常用于计数器变量更新(递增/递减)
        // 6.代码体验
        for (var i = 1; i <= 100; i++) {
            console.log('hello');
        }

				// 1.首先执行计数器变量 var i = 1， 但是这里在for里面只执行一次 index
        // 2.然后到 i <= 100来判断是否满足条件，如果满足条件就执行循环体。不满足条件退出循环        // 3.最后执行i++，i++是单独写的代码递增。第一轮结束
        // 4.接着执行：i++去判断 i<=100 如果满足条件就执行循环体。不满足条件退出循环。第二轮
				// 5.第三轮... 执行操作表达式➡️条件表达式判断➡️满足执行/不满足退出➡️执行操作表达式
```

<img src="/Users/aoki/Library/Application Support/typora-user-images/image-20210818150234001.png" alt="image-20210818150234001" style="zoom:30%;" />

<img src="/Users/aoki/Library/Application Support/typora-user-images/image-20210818150518482.png" alt="image-20210818150518482" style="zoom:30%;" />

<img src="/Users/aoki/Library/Application Support/typora-user-images/image-20210818150543771.png" alt="image-20210818150543771" style="zoom:30%;" />



##### 断点调试：

断点调试是指自己在程序的某一行设置一个断点，调试时程序运行到这一行就会停住，然后可以一步一步往下调试，调试过程中可以看各个变量当前的值，出错的话，调试到出错的代码行即消失错误停下。

断点调试可以帮助观察程序的运行过程：

F12–>sources–>找到需要调试的文件–>在程序的某一行设置断点

Watch：监视，通过watch件事变量的值变化

F11：程序单步执行，让程序一行一行的执行，观察watch中变量的值的变化

### 2.2 for循环重复相同的代码

```js
        // 让用户控制输出的次数
        var num = prompt('请输入次数：');
        for (var=i; i <= num; i++) {
            console.log('ohayo');
        }
```

### 2.3 for 循环重复不同的代码

for循环还可以重复不同的代码，这主要是因为使用了计数器，计数器在每次循环过程中都会有变化

```js
        // for 循环可以重复执行不同的代码，有计数器变量i的存在，i每次循环值都会变化
        // 输出1个人 1～100岁for (var i = 1; i <= 100; i++) {
            if (i == 1) {
                console.log('今年1岁 出生了');
            } else if (i == 100) {
                console.log('今年100岁 去世了');
            } else {
                console.log('今年' + i + '岁了');
            }
        }
```

### 2.4 for循环重复某些相同操作

```js
        // 案例：
        // 1～100之间所有整数的累加和
        // 1.需要循环100次，需要一个计数器i
        // 存储结果变量sum，初始值一定是0
        // 核心算法：1+2+3+4... sum = sum + i;
        var sum = 0; // 求和的变量
        for (var i = 1; i <= 100; i++) {
            // sum = sum + i;
            sum += i;
        }
        console.log(sum);
```

<img src="/Users/aoki/Library/Application Support/typora-user-images/image-20210818154433451.png" alt="image-20210818154433451" style="zoom:50%;" />

```js
//案例1：
        // 1.求1～100之间所有数的平均值
        // 2.需要sum和的变量
        // 3.还需要一个平均值average变量
        var sum = 0;
        var average = 0;
        for (var i = 1; i <= 100; i++) {
            sum += i;
        }
        average = sum / 100;
        console.log(average);

//案例2：
        // 1.分别算出1~100之间所有偶数的和以及奇数的和 一个even 一个odd
        var even = 0;
        var odd = 0;
        for (var i = 1; i <= 100; i++) {
            if (i % 2 == 0) {
                even += i
            } else {
                odd += i
            }
        }
        console.log('1~100之间所有的偶数和是' + even);
        console.log('1~100之间所有的奇数和是' + odd);

//案例3：        // 1~100之间所有能被3整除的数字之和
        var result = 0;
        for (var i = 1; i <= 100; i++) {
            if (i % 3 == 0) {
                result += i
            }
        }
        console.log('1~00之间能被3整除的数字的和' + result);

```

<img src="/Users/aoki/Library/Application Support/typora-user-images/image-20210818155531677.png" alt="image-20210818155531677" style="zoom:50%;" />

<img src="/Users/aoki/Library/Application Support/typora-user-images/image-20210818155758611.png" alt="image-20210818155758611" style="zoom:50%;" />

```js
//案例：
        // 求学生成绩
        // 用户输入班级人数，之后一次输入每个学生的成绩，最后打印出班级总的成绩以及平均成绩
        // 1.弹出prompt输入框，请输入班级总人数
        // 2.一次输入学生的成绩(score) 需要用到for循环，弹出的次数跟班级总人数有关系 条件表达式：i<=num
        // 3.进行业务处理：计算成绩。先求总成绩(sum)，之后求平均成绩(average)
        // 4.弹出结果
        var num = prompt('请输入班级总人数:');
        var sum = 0; // 求和的变量
        var average = 0; //求平均值的变量
        for (var i = 1; i <= num; i++) {
            var score = prompt('请输入第' + i + '成绩'); // var score 保存学生成绩
            // 因为从prompt取过来的数据是字符串型的 需要转换为数字型
            sum += parseFloat(score);
        }
        average = sum / num;
        alert('班级总成绩' + sum);
        alert('班级平均分' + average)
```

<img src="/Users/aoki/Library/Application Support/typora-user-images/image-20210818171434003.png" alt="image-20210818171434003" style="zoom:50%;" />

```js
        // 一行打印五颗星星 采用字符串的方式
        var str = '';
        for (var i = 1; i <= 5; i++) {
            str = str + '🪐';
        }
        console.log(str);
				
				//用户输入
        var num = prompt('请输入星星个数：');
        var str = '';
        for (var i = 1; i <= num; i++) {
            str = str + '🌟';
        }
        alert(str);
```

<img src="/Users/aoki/Library/Application Support/typora-user-images/image-20210818172554463.png" alt="image-20210818172554463" style="zoom:25%;" />

## 3. 双重 for 循环

### 3.1 双重for 循环概述

循环嵌套是指在一个循环语句中在定义一个循环语句的语法结构，例如在for循环语句中，可以嵌套一个for循环，这样的for循环语句被称为双重for循环。

```js
        // 双重for循环 语法结构
        for (外层的初始化变量; 外层的条件表达式; 外层的操作表达式) {
            for (里层的初始化变量; 里层的条件表达式; 里层的操作表达式) {
                // 执行语句;
            }
        }
        // 2.里面的循环看做是外层循环的语句
        // 3.外层循环，循环一次，里面的循环执行全部
        // 、4.代码验证
        for (var i = 1; i <= 3; i++) {
            console.log('这是外循环的第' + i + '次');
            for (var j = 1; j <= 3; j++) {
                console.log('这是里层循环的第' + j + '次');
            }
        }
```

<img src="/Users/aoki/Library/Application Support/typora-user-images/image-20210819092124396.png" alt="image-20210819092124396" style="zoom: 33%;" />

### 3.4 五行五列星星案例

```js
        // 1.内层循环负责一行打印五个星星
        // 2.外层循环负责打印五行
        var str = '';
        for (var i = 1; i <= 5; i++) { //外层循环负责打印五行
            for (var j = 1; j <= 5; j++) { //内层循环负责一行打印五个星星
                str = str + '⭐️'
            }
            // 一行打印完毕5个星星要另起一行 加\n
            str = str + '\n';
        }
        console.log(str);
```

```js
        // 打印n行n列星星
        var rows = prompt('请输入行数：');
        var cols = prompt('请输入列数：');
        var str = '';
        for (var i = 1; i <= rows; i++) {
            for (var j = 1; j <= cols; j++) {
                str = str + '❤️';
            }
            str = str + '\n';
        }
        console.log(str);
```

```js
        // 打印倒三角
        var rows = prompt('请输入行数：');
        var str = '';
        for (var i = 1; i <= rows; i++) {
            for (var j = i; j <= rows; j++) {
                str = str + '⚛';
            }
            str = str + '\n';
        }
        console.log(str);

        // 打印正三角
        var rows = prompt('请输入行数：');
        var str = '';
        for (var i = 1; i <= rows; i++) {
            for (var j = 1; j <= i; j++) {
                str = str + '⚛';
            }
            str = str + '\n';
        }
        console.log(str);
```

<img src="/Users/aoki/Library/Application Support/typora-user-images/image-20210819102720177.png" alt="image-20210819102720177" style="zoom:33%;" />

##### JS基础运用循环三角形 菱形：https://juejin.cn/post/6844903748087578631



<img src="/Users/aoki/Library/Application Support/typora-user-images/image-20210819105055161.png" alt="image-20210819105055161" style="zoom:50%;" />

```js
        // 九九乘法表
        // 1.一共有9行，每行个数不一样，双重for循环
        // 2.外层的for循环控制行数i，循环9次，
        // 3.内层的for循环控制每行公式j
        // 4.核心算法：每一行公示的个数正好和行数一致，j <= i;
        // 5.每行打印完毕都重新换行
        var str = '';
        for (var i = 1; i <= 9; i++) { // 外层循环控制行数
            for (var j = 1; j <= i; j++) { // 里层循环控制每行个数
                // 1x2=2
                // str += '🌀';
                // str = i + 'x' + j '=' + i * j;
                str += j + 'x' + i + '=' + i * j + '\t';
            }
            str += '\n';
        }
        console.log(str);
```

+ for循环可以重复执行某些相同的代码
+ for循环可以重复执行不同的代码，因为有计数器
+ for循环可以重复执行某些操作，比如技术运算符加法操作
+ 双重for循环，外层循环一次，内层for循环全部执行
+ for循环式循环条件和数字直接相关的循环



### 4.while循环

while循环可以在条件表达式为真的前提下，循环执行制定的一段代码，直到表达式不为真时结束循环。

```js
        // 1.while循环语法结构  while 当...时候
        while (条件表达式) {
            // 循环体;
        }
        // 2.执行思路   当条件表达式结果为true则执行循环体，否则退出循环
        // 3.代码验证
        var num = 1; //计数器
        while (num <= 100) {
            console.log('hello');
            num++; //操作表达式防止死循环
        }
        // 4.有计数器 初始化变量
        // 5.也有操作表达式 完成计数器的更新防止死循环
```

```js
       //案例：
       
       // 1.打印人的一生，从1~100岁
        var age = 0;
        while (age <= 100) {
            console.log('这个人今年' + age + '岁了');
            age++;
        }
        // 2.计算1~100之间所有整数的和
        var sum = 0;
        var num = 1;
        while (num <= 100) {
            sum += num;
            num++;
        }
        console.log(sum);
        // 3.弹出一个提示框，你好吗？   如果输入我很好提示结束，否则一直询问
        // 1.弹出输入框
        // 2.判断条件比较复杂用while
        // while循环语句条件表达式输入的不是我很好 就一直循环
        var i = prompt('你好吗？');
        while (i !== '我很好') {
            i = prompt('你好吗？');
        }
        alert('我也很好');
```

<img src="/Users/aoki/Library/Application Support/typora-user-images/image-20210819114320282.png" alt="image-20210819114320282" style="zoom:33%;" />

### 5. do while循环

该循环会执行一次代码块，然后对条件式进行判断，如果条件为真，就会重复执行循环体，否则退出循环

```js
        // 1.do while循环 语法结构
        do {
            // 循环体；
        } while (条件表达式)
        // 2.执行思路 跟while不同的地方在于 do while限制性一次循环体 再判断条件，条件表达式结果为真，则继续执行循环体，否则退出循环
        // 3.代码验证
        var i = 1;
        do {
            console.log('hellow');
            i++;
        } while (i <= 100)
        // 4.do while 循环体至少循环一次
```

```js
//案例：
        // 人的一生 1~100岁
        var i = 1;
        do {
            console.log('这个人今年' + i + '岁了');
            i++;
        } while (i <= 100)
          
				// 1~100之间所有整数的和
        var num = 0;
        var sum = 1;
        do {
            num = num + sum;
            sum++;
        } while (sum <= 100)
        console.log(num);

        // 3.弹出提示框
        do {
            var message = prompt('hello?');
        } while (message !== 'hi')
        alert('how are you')
```

+ for	while	do…while
+ 三个循环很多情况下都可以相互替代使用
+ 记次数，和数字相关，三者使用基本相同，更喜欢用for
+ while和do…while可以做更负责的判断条件，比for循环更灵活
+ while和do…while执行顺序不一样。while先判断后执行，do…while先执行一次，再判断执行
+ while和do…while执行次数不一样，do…while至少会执行一次循环体，而while可能一次也不执行
+ 更常用for循环语句，写法简洁直观

## 6. continue break

### 6.1 continue关键字

continue关键字用于立即**跳出本次循环，继续下一次循环**（本次循环中continue之后的代码就会少执行一次）

```js
        // continue关键字   退出当前次的循环 继续执行剩余次数的循环
        for (var i = 1; i <= 5; i++) {
            if (i == 3) {
                continue; // continue退出本次循环 直接到i++
            }
            console.log(i);
        }
//案例：
        // 1.求1~100之间，除了能被7整除之外的整数和
        var num = 0;
        for (var i = 1; i <= 100; i++) {
            if (i % 7 == 0) {
                continue;
            }
            num += i;
        }
        console.log(num);
```

<img src="/Users/aoki/Library/Application Support/typora-user-images/image-20210819140725426.png" alt="image-20210819140725426" style="zoom:50%;" />

### 6.2 break关键字

break关键字用于立即跳出整个循环（循环结束）

```js
        // break退出整个循环
        for (var i = 1; i <= 5; i++) {
            if (i == 3) {
                break;
            }
            console.log(i);
        }
```

# 命名规范

### 1.标识符命名规范

+ 变量、函数的命名必须要有意义
+ 变量的名称一般用名词
+ 函数的名称一般用动词

### 2.操作符规范

```js
        // 操作符左右两侧各保留一个空格
        for (var i = 1; i <= 5; i++) {
            if (i == 3) {
                break; // 直接退出整个for循环，跳到整个for循环下面的语句
            }
            console.log(i);
        }
```

### 3.单行注释

单行注释前面注意有个空格

### 4.其他规范

<img src="/Users/aoki/Library/Application Support/typora-user-images/image-20210819141444708.png" alt="image-20210819141444708" style="zoom:50%;" />

```js
        // 作业1：
        // 1.求1~100之间所有数的总和与平均值
        var num = 0;
        var sum = 0;
        for (var i = 1; i <= 100; i++) {
            num = num + i;
            sum = num / i;
        }
        console.log('1~100之间所有数的总和：' + num);
        console.log('1~100之间所有数的平均数：' + sum);

```

<img src="/Users/aoki/Library/Application Support/typora-user-images/image-20210819142314204.png" alt="image-20210819142314204" style="zoom:30%;" />

```js
        // 作业2：
        // 2.求1~100之间所有偶数的和
        var num = 0;
        for (var i = 1; i <= 100; i++) {
            if (i % 2 == 0) {
                num += i;
            }
        }
        console.log('1~100之间所有数的总和：' + num);
        console.log('1~100之间所有数的平均数：' + sum);
```

<img src="/Users/aoki/Library/Application Support/typora-user-images/image-20210819142534033.png" alt="image-20210819142534033" style="zoom:50%;" />

```js
        // 作业3：
        // 3.求100以内7的倍数的总和
        var num = 0;
        for (var i = 1; i <= 100; i++) {
            if (i % 7 == 0) {
                num = num + i;
            }
        }
        console.log(num);
```

<img src="/Users/aoki/Library/Application Support/typora-user-images/image-20210819143514876.png" alt="image-20210819143514876" style="zoom:50%;" />

```js
        // 作业4：
        // 使用for循环打印三角形，要求每次只输出一个⭐️
        var rows = prompt('请输入矩形高度：');
        var num = '';
        for (var i = 1; i <= rows; i++) {
            for (var a = 1; a <= i; a++) {
                num += '⭐️';
            }
            num = num + '\n';
        }
        console.log(num);
```

<img src="/Users/aoki/Library/Application Support/typora-user-images/image-20210819144353037.png" alt="image-20210819144353037" style="zoom:50%;" />

```js
        // 作业5：
        // 使用for循环打印矩形 每次只能输出一个⭐️
        var num = '';
        for (var i = 1; i <= 5; i++) {
            for (var b = 1; b <= 5; b++) {
                num = num + '⭐️';
            }
            num += '\n';
        }
        console.log(num);
```

<img src="/Users/aoki/Library/Application Support/typora-user-images/image-20210819144716147.png" alt="image-20210819144716147" style="zoom:50%;" />

# 数组Array

### 1.数组的概念

把一组相关数据一起存放，并提供方便的访问（获取）方式。

数组是指一组数据的集合，其中每个数据被称为元素，在数组中可以存放任意类型的元素。数组是一种将一组数据存储在单个变量名下的方式。

### 2.1 数组的创建方式

+ 利用new创建数组
+ 利用数组字面量创建数组

### 2.2利用new创建数组

```js
        var 数组名 = new Array();
        var arr = new Array(); // 创建一个新数组
```

### 2.3利用数组字面量创建数组

```js
        // 1.利用数组字面量
        var arr = []; // 创建了一个空的数组
        var arr1 = [1, 2, 3, 'love', true]; // 数组中可以存放任意类型数据
        // 2.数组里面的数据一定要用逗号隔开
        // 3.数组里面的数据 1,2 true...称为数组元素
```

+ 数字的字面量时方括号
+ 声明数组并赋值称为数组的初始化
+ 这种字面量方式使用最多

### 2.4数组元素类型

数组中可以存放任意类型数据，例如字符串，数字，布尔值等等。

## 3.获取数组元素

### 3.1数组的索引

**索引（下标）**：用来访问数组元素的序号（数组下标从0开始）

数组可以通过索引来访问、设置、修改对应的数组元素，通过“数组名[索引]”的形式来获取数组中的元素。访问时获取得到的意思。

```js
        var arr1 = [1, 2, 3, 'love', true];
        // 2.数组里面的数据一定要用逗号隔开
        // 3.数组里面的数据 1,2 true...称为数组元素
        console.log(arr1);
        console.log(arr1[3]);
        console.log(arr1[4]);
        console.log(arr1[5]); // 没有这个数组元素 输出结果时undefined

//练习：
        var xq = ['星期一', '星期二', '星期三', '星期四', '星期五', '星期六', '星期日'];
        console.log(xq[6]);
```

<img src="/Users/aoki/Library/Application Support/typora-user-images/image-20210819163314611.png" alt="image-20210819163314611" style="zoom:33%;" />

## 4.遍历数组

**规律：**数组中取出每一个元素时，代码是重复的，不一样的时索引值在递增。通过循环

**遍历：**把数组中每个元素从头到尾都访问一遍

索引号从0开始，数组长度是元素个数

```js
        var arr = ['green', 'blue', 'yellow'];
        for (var i = 0; i < 3; i++) {
            console.log(arr[i]);
        }
        // 1.数组索引号从0开始，所以i必须从0开始，i<3
        // 2.输出的时候 arr[i] , i是计数器当索引号来使用，arr[i]是数组元素第i个数组元素
```

<img src="/Users/aoki/Library/Application Support/typora-user-images/image-20210819164316221.png" alt="image-20210819164316221" style="zoom:30%;" />

### 4.1数组的长度

**数组名.length**可以访问数组元素的数量（数组长度）

```js
        // 数组长度 数组名.length
        var arr = ['关羽', '张飞', '马超', '赵云', '黄忠', '刘备', 'lee'];
        for (var i = 0; i < 6; i++) {
            console.log(arr[i]);
        }
        console.log(arr.length);
        for (var i = 0; i < arr.length; i++) {
            console.log(arr[i]);
        }
        // 1.数组的长度时元素个数 不要跟索引号混淆
        // 2.arr.length 动态检测数组元素的个数

//练习：
        var arr = ['关羽', '张飞', '马超', '赵云', '黄忠', '刘备', 'lee'];
        console.log(arr.length);
        for (var i = 0; i < arr.length; i++) {
            console.log(arr[i]);
        }

//案例：
        // 数组元素【2，6，1，7，4】里面所有元素的和，及平均值
        // 1.求和变量sum
        // 遍历这个数组，把里面每个数组元素加到sum里面
        // 3.用求和变量sum除以数组的长度就可以得到数组的平均值
        var arr = [2, 6, 1, 7, 4];
        var sum = 0;
        var average = 0;
        for (var i = 0; i < arr.length; i++) {
            sum += arr[i];  // 加的数组元素arr[i]，不是计数器i
        }
        average = sum / arr.length;
        console.log(sum, average); // 想要输出多个变量，用逗号隔开

// 案例：
        // 求数[2,6,1,77,52,25,7]中的最大值
        // 1.声明一个保存最大元素的变量 max
        // 2.默认最大值可以取数组中的第一个元素
        // 3.遍历这个数组，把里面每个数组元素和max相比较
        // 4.如果这个数组元素大于max，就把这个数组元素存到max里面，否则继续下一轮比较
        // 5.最后输出这个max
        var arr = [1, 20, 33, 444, 5555, 66666];
        var max = arr[0];
        for (var i = 1; i <= arr.length; i++) {
            if (max < arr[i]) {
                max = arr[i];
            }
        }
        console.log('数组中最大值是：' + max);


// 数组中最小值
        var arr = [1, 20, 33, 444, 5555, 66666];
        var min = arr[0];
        for (var i = 1; i >= arr.length; i++) {
            if (min > arr[i]) {
                min = arr[i];
            }
        }
        console.log('数组中最小值是：' + min);

// 案例4：数组转换为分割字符串
        // 要求：将数组['red','green','blue','pink']转换为字符串，并且用|或其他符号分割
        // 输出：'red|green|blue|pink'
        // 1.需要一个新变量用于存放转换完的字符串，str
        // 2.遍历原来的数组，分别把里面数据取出来，加到字符串里面
        // 3.同时在后面多加一个分隔符
        var arr = ['red', 'green', 'blue', 'pink'];
        var str = '';
        var sep = '🍩';
        for (var i = 0; i <= arr.length; i++) {
            str += arr[i] + sep;
        }
        console.log(str);
```

<img src="/Users/aoki/Library/Application Support/typora-user-images/image-20210820115813825.png" alt="image-20210820115813825" style="zoom:33%;" />

## 数组中新增元素

通过修改length长度以及索引号增加数组元素

### 5.1通过修改length长度新增数组元素

+ 可以通过修改length长度来实现数组扩容的目的
+ length属性是可读写的

```js
        // 1.新增数组元素 修改length
        var arr = ['red', 'blue', 'green'];
        console.log(arr.length);
        arr.length = 5;
        console.log(arr);
        console.log(arr[3]); // undefined
        console.log(arr[4]); // undefined
        // 索引号3，4的空间没有给值，也就是声明变量没有给值，默认值是undefined
```

### 5.2通过修改数组索引新增数组元素

+ 通过修改数组索引的方式追加数组元素
+ 不能直接给数组名赋值，否则会覆盖掉以前的数据

```js
        // 2.新增数组元素 修改索引号 追加数组元素
        var arr1 = ['red', 'blue', 'green'];
        arr1[3] = 'lee';
        console.log(arr1);
        arr1[4] = 'vv';
        console.log(arr1);
        arr1[0] = 'color'; // 替换原来的数组元素
        console.log(arr1);
        arr1 = '是李'; // 不要直接给数组名赋值，否则里面的数组元素都会消失
        console.log(arr1);
```

<img src="/Users/aoki/Library/Application Support/typora-user-images/image-20210820121848333.png" alt="image-20210820121848333" style="zoom:40%;" />

```js
        // 案例：
        // 新建一个数组，里面存放10个整数(1~10)
        // 1.使用循环来追加数组
        // 2.声明一个空数组arr
        // 3.循环中的计数器i 可以作为数组元素存入
        // 4.有余数组的索引号是从0开始，因此计数器从0开始更合适，存入的数组元素要+1
        var arr = [];
        for (var i = 0; i < 10; i++) {
            arr[i] = i + 1;
        }
        console.log(arr);
```

<img src="/Users/aoki/Library/Application Support/typora-user-images/image-20210820121820793.png" alt="image-20210820121820793" style="zoom:40%;" />

```js
        // 将数组[2,4,6,8,10,0,20,0,40,50]中大于等于10的元素选出来放入数组
        // 1.声明一个新的数组用于存放新数据newArr
        // 2.遍历原来的旧数组 找出大于等于10的元素
        // 3.依次追加给新数组

				// 方法1
        var arr = [2, 4, 6, 8, 10, 0, 20, 0, 30, 40];
        var newArr = [];
        var a = 0;
        for (var i = 0; i <= arr.length; i++) {
            if (arr[i] >= 10) {
                // 新数组从0开始依次递增
                newArr[a] = arr[i];
                a++; // 0-->1-->2-->3...
            }
        }
        console.log(newArr);

        // 方法2
        var arr = [2, 4, 6, 8, 10, 0, 20, 0, 30, 40];
        var newArr = [];
        // newArr.length 一开始就是0
        for (var i = 0; i <= arr.length; i++) {
            if (arr[i] >= 10) {
                // 新数组从0开始依次递增
                newArr[newArr.length] = arr[i];
            }
        }
        console.log(newArr);
```

<img src="/Users/aoki/Library/Application Support/typora-user-images/image-20210820132737629.png" alt="image-20210820132737629" style="zoom:40%;" />

```js
        // 案例1：删除指定数组元素
        // 要求：将数组[2, 0,6,1,77,0,52,0,25,7]中的0去掉后，形成一个不包含0的新数组
        // 1.需要一个新数组用于存放筛选之后的数据
        // 2.遍历原来的数组，把不是0的数据添加到新数组里面(此时要注意采用数组名+索引的格式接收数据)
        // 3.新数组里面的个数，用length不断累加
        var arr = [2, 0, 6, 1, 77, 0, 52, 0, 25, 7];
        var newArr = [];
        for (var i = 0; i < arr.length; i++) {
            if (arr[i] != 0) {
                newArr[newArr.length] = arr[i];
            }
        }
        console.log(newArr);
```

<img src="/Users/aoki/Library/Application Support/typora-user-images/image-20210820134058369.png" alt="image-20210820134058369" style="zoom:50%;" />

```js
        // 案例2：翻转数组
        // 要求：将数组['red', 'green','blue','pink','purple']的内容反过来存放 输出：
        // 1.声明一个新数组
        // 2.把旧数组索引号第4个取过来(arr.length-1)，给新数组索引号第0个元素(newArr.length)
        // 3.采取递减的方式
        // 方法1
        var arr = ['red', 'green', 'blue', 'pink', 'purple'];
        var newArr = [];
        for (var i = arr.length - 1; i >= 0; i--) {
            newArr[newArr.length] = arr[i];
        }
        console.log(newArr);

        // 方法2
        var arr = ['red', 'green', 'blue', 'pink', 'purple'];
        var newArr = [];
        var a = 0;
        for (var i = arr.length - 1; i >= 0; i--) {
            newArr[a] = arr[i];
            a++;
        }
        console.log(newArr);

        // 方法3：利用函数翻转数组
        // 翻转数组 reverse翻转
        function reverse(arr) {
            var newArr = []; // 新的空数组
            for (var i = arr.length - 1; i >= 0; i--) { // arr.length - 1相当于(5)-1 第四个-->第三个
                newArr[newArr.length] = arr[i]; // newArr.length 相当于 把第4个-->新数组第0个
            }
            return newArr;
        }
        console.log(reverse([1, 2, 3, 4, 5]));

```

<img src="/Users/aoki/Library/Application Support/typora-user-images/image-20210820134356999.png" alt="image-20210820134356999" style="zoom:50%;" />

<img src="/Users/aoki/Library/Application Support/typora-user-images/image-20210820135633749.png" alt="image-20210820135633749" style="zoom:40%;" /><img src="/Users/aoki/Library/Application Support/typora-user-images/image-20210825104942527.png" alt="image-20210825104942527" style="zoom:50%;" />

<img src="/Users/aoki/Library/Application Support/typora-user-images/image-20210820142001710.png" alt="image-20210820142001710" style="zoom: 40%;" />

<img src="/Users/aoki/Library/Application Support/typora-user-images/image-20210820142713173.png" alt="image-20210820142713173" style="zoom:50%;" />

```js
        // 案例3：数组排序（冒泡排序）一定的顺序进行排列显示（从小到大/从大到小）
        // 冒泡排序
        var arr = [4, 1, 2, 3, 5];
        for (var i = 0; i <= arr.length - 1; i++) {
            for (var j = 0; j <= arr.length - i - 1; j++) {
                if (arr[j] > arr[j + 1]) {
                    var temp = arr[j];
                    arr[j] = arr[j + 1];
                    arr[j + 1] = temp;
                }
            }
        }
        console.log(arr);
        var arr = [4, 1, 2, 3, 5];
        for (var i = 0; i <= arr.length - 1; i++) { // 外层循环管趟数 
            for (var j = 0; j <= arr.length - i - 1; j++) { // 里面的循环管 每一趟的交换次数
                // 内部交换2个变量的值 前一个和后面一个数组元素相比较
                if (arr[j] < arr[j + 1]) {
                    var temp = arr[j];
                    arr[j] = arr[j + 1];
                    arr[j + 1] = temp;
                }
            }
        }
        console.log(arr);
```

# 函数

### 1.函数的概念

函数：封装一段可以被重复执行调用的代码块，目的：让大量代码重复使用

## 2.函数的使用

```js
        // 1.声明函数
        // function 函数名() {
        //     // 函数体;
        // }
        function sayHi() {
            console.log('hellow');
        }
        // (1) function声明函数的关键字 全部小写
        // (2) 函数是做某件事情（实现某个功能才定义的），函数名一般是动词 sayHi、getSum
        // (3) 函数不调用自己不执行
        // 2.调用函数
        // 函数名();
        sayHi();
        // 调用函数的时候千万不要忘记小括号
```

**函数本身并不会执行代码，只有调用函数时才会执行函数体代码**

### 2.3函数的封装

+ 函数的封装是把一个/多个功能通过 **函数的方式封装起来**，对外只提供一个简单地函数接口
+ 封装类似于将电脑配件整合组装到机箱中（类似于快递打包）

<img src="/Users/aoki/Library/Application Support/typora-user-images/image-20210820145435536.png" alt="image-20210820145435536" style="zoom:40%;" />

### 2.4函数的使用

```js
        // 利用函数计算1~100之间的累加和
        // 1.声明函数
        function getSum() {
            var sum = 0;
            for (var i = 1; i <= 100; i++) {
                sum += i;
            }
            console.log(sum);
        }
        // 2.调用函数 
        getSum();
        getSum();
```

## 3.函数的参数

### 3.1形参和实参

**形参：**形式上的参数，**函数定义**的时候传递的参数，当前并不知道是什么

**实参：**实际上的参数，**函数调用**的时候传递的参数，实参是传递给形参的

**参数的作用：**在 **函数内部**某些值不能固定，通过参数在调用函数时传递不同的值进去

```js
        // 1.函数可以重复不同的代码
        // 2.利用函数的参数实现函数重复不同的代码
        function 函数名(形参1, 形参2...) { // 在声明函数的小括号里面是形参 (形式上的参数)

        }
        函数名(实参1, 实参2...); // 在函数调用的小括号里面是实参 (实际参数)
        // 3.形参和实参的执行过程
        function cook(aru) { // 形参是接受实参的 aru='cake' 形参类似于一个变量
            console.log(aru);
        }
        cook('cake');
        cook('bread');
        // 4.函数的参数可以有，也可以没有个数不限
```

<img src="/Users/aoki/Library/Application Support/typora-user-images/image-20210820151123527.png" alt="image-20210820151123527" style="zoom:50%;" />

```js
        // 1.利用函数求任意两个数的和
        function getSum(num1, num2) {
            console.log(num1 + num2);
        }
        getSum(1, 9);
        // 2.利用函数求任意两个数之间的和
        function getSums(start, end) {
            var num = 0;
            for (var i = start; i <= end; i++) {
                num += i;
            }
            console.log(num);
        }
        getSums(1, 100);
        // 3.注意⚠️
        // (1)多个参数之间用逗号隔开
        // (2)形参可以看做是不用声明的变量
```

### 3.3函数形参和实参个数不匹配问题

+ 实参个数=形参个数	输出正常结果

+ 实参个数 > 形参个数  只取到形参的个数

+ 实参个数 < 形参个数  多的形式定义为undefined，结果输出位NaN

  ⚠️JS中 形参的默认值是undefined

```js
        // 函数形参实参个数匹配
        function getSum(num1, num2) {
            console.log(num1 + num2);
        }
        // 1.如果实参的个数和形参的个数一致，则正常输出结果
        getSum(1, 2);
        // 2.如果实参的个数多于形参的个数，会取到形参的个数
        getSum(1, 2, 3);
        // 3.如果实参的个数小宇形参的个数，多余的形参定义为undefined，最终结果NaN
        // 形参可以看做是不用声明的变量，num2是一个变量但是没有接受值，结果是undefined，1+undefined= NaN
        getSum(1); // NaN
        // 建议尽量让实参的个数和形参相匹配
```

+ 函数可以带参数也可以不带参数
+ 声明函数的时候，函数名括号里面的是形参，形参的默认值为undefined
+ 调用函数的时候，函数名括号里面的是实参
+ 多个参数中间用逗号隔开
+ 形参的个数可以和实参个数不匹配，但是结果不可预计，要尽量匹配

## 4.函数的返回值

### 4.1 return语句

希望函数将值返回给调用者

```js
        // 1.函数时做某件事/实现某种功能
        // 2.函数的返回值格式
        function 函数名() {
            return 需要返回的结果;
        }
        // 函数名();
        // (1)函数只是实现某种功能，最终结果需要返回给函数的调用者-->函数名() 通过return实现的
        // (2)只要函数遇到return 就把后面的结果返回给函数的调用者，函数名() = return后面的结果
        // 3.代码验证
        function getResult() {
            return 999;
        }
        console.log(getResult());

        function getResults(cook) {
            return cook;
        }
        console.log(getResults('coffe'));
        // 4.求任意两个数的和
        function getSum(num1, num2) {
            return num1 + num2;
        }
        console.log(getSum(1, 99));
```

```js
        // 案例1：利用函数求任意两个数的最大值
        // 方法1：
        function getMax(num1, num2) {
            if (num1 > num2) {
                return num1;
            } else {
                return num2;
            }
        }
        console.log(getMax(1, 10));
        console.log(getMax(50, 1));
        // 方法2：三元表达式
        function getMax1(num1, num2) {
            return num1 > num2 ? num1 : num2; // : 否则
        }
        console.log(getMax(1, 10));
        console.log(getMax(50, 1));
```

<img src="/Users/aoki/Library/Application Support/typora-user-images/image-20210820162427052.png" alt="image-20210820162427052" style="zoom:50%;" />

```js
        // 案例2：利用函数求任意一个数组中的最大值
        // 利用函数求数组[5,2,99,101,67,77]中的最大值
        function getArrMax(arr) { // arr接受一个数组 arr=[5,2,99,101,67,77]
            var max = arr[0];
            for (var i = 1; i <= arr.length; i++) {
                if (arr[i] > max) {
                    max = arr[i];
                }
            }
            return max;
        }
        // console.log(getArrMax([5, 2, 99, 101, 67, 77])); //实参是一个数组送过去
        // 实际开发中，经常用一个变量来接受函数的返回结果，使用更简单
        var re = getArrMax([5, 2, 99, 101, 67, 77]);
        console.log(re);
```

<img src="/Users/aoki/Library/Application Support/typora-user-images/image-20210820165404673.png" alt="image-20210820165404673" style="zoom:50%;" />

### 4.2 return 终止函数

*return后面的代码不会被执行*

### 4.3 return的返回值 

return只能返回一个值。如果用逗号隔开多个值，以最后一个为准。

### 4.4函数没有return返回undefined

**函数都有返回值**

+ 如果有return则返回return后面的值
+ 如果没有return则返回undefined

### 4.5 break，continue，return的区别

+ break：结束当前的循环体（如for、while）
+ continue：跳出本次循环，继续执行下次循环（如for、while）
+ return：不仅可以退出循环，还能返回return语句中的值，同时还可以结束当前的函数体内的代码

```js
        // 1.return终止函数
        function getSum(num1, num2) {
            return num1 + num2; // return后面的代码不会被执行
            alert('不会被执行');
        }
        console.log(getSum(2, 3));
        // 2.return只能返回一个值
        function getSums(num1, num2) {
            return num1, num2; //返回的结果是最后一个值 num2不会被终止
        }
        console.log(getSums(2, 10));
        // 3.求任意两个数的加减乘除结果
        function fn(num1, num2) {
            return [num1 + num2, num1 - num2, num1 * num2, num1 / num2];
        }
        console.log(fn(100, 200)); // 返回的是一个数组
        // 4.函数如果有return则返回return后面的值。如果函数没有return则返回undefined
        function fun1(num1, num2) {
            return num1 + num2;
        }
        console.log(fun1(1, 2));
        function fun2(num1, num2) {

        }
        console.log(fun2());
```

<img src="/Users/aoki/Library/Application Support/typora-user-images/image-20210820171446295.png" alt="image-20210820171446295" style="zoom:50%;" /> 

<img src="/Users/aoki/Library/Application Support/typora-user-images/image-20210820171616666.png" alt="image-20210820171616666" style="zoom:40%;" />

```js
        // 0和1既不是质数也不是合数
        // 案例1：写一个函数，用户输入任意两个数字的任意算数运算（计算其功能），并能弹出最后结果
        var num1 = parseFloat(prompt('请输入数字1：'));
        var num2 = parseFloat(prompt('请输入数字2：'));
        function getNumber(num1, num2) {
            return num1 + num2;
        }
        var num = getNumber(num1, num2);
        alert(num);

        // 案例2：写一个函数，用户输入任意两个数字的最大值，并能弹出最后结果
        var num1 = parseFloat(prompt('请输入数字1：'));
        var num2 = parseFloat(prompt('请输入数字2：'));
        function getNumber(num1, num2) {
            if (num1 > num2) {
                return (num1);
            } else {
                return (num2);
            }
        }
        var num = getNumber(num1, num2);
        alert(num);

        // 案例3：写一个函数，用户输入任意三个数字的最大值，并能弹出最后结果
        var num1 = parseFloat(prompt('请输入数字：'));
        var num2 = parseFloat(prompt('请输入数字：'));
        var num3 = parseFloat(prompt('请输入数字：'));
        var arr = [num1, num2, num3];
        var max = 0;
        function getMax(num1, num2, num3) {
            for (var i = 0; i <= getMax.length; i++) {
                if (arr[i] > max) {
                    max = arr[i];
                }
            }
            return max;
        }
        var max1 = getMax(num1, num2, num3);
        alert(max1);

        // 案例3：写一个函数，用户输入任意三个数字的最大值，并能弹出最后结果
        // 方法1：函数
        var num1 = parseFloat(prompt('请输入数字：'));
        var num2 = parseFloat(prompt('请输入数字：'));
        var num3 = parseFloat(prompt('请输入数字：'));
        var arr = [num1, num2, num3];
        var max = 0;
        function getMax(num1, num2, num3) {
            for (var i = 0; i <= getMax.length; i++) {
                if (arr[i] > max) {
                    max = arr[i];
                }
            }
            return max;
        }
        var max1 = getMax(num1, num2, num3);
        alert(max1);

        // 方法2：if else
        var num1 = parseFloat(prompt('请输入数字：'));
        var num2 = parseFloat(prompt('请输入数字：'));
        var num3 = parseFloat(prompt('请输入数字：'));
        var max = 0;
        if (num1 > num2 && num1 > num3) {
            max = num1;
        } else if (num2 > num1 && num2 > num3) {
            max = num2;
        } else {
            max = num3;
        }
        alert(max);

        // 方法3:数组和for循环
        var num1 = parseFloat(prompt('请输入数字：'));
        var num2 = parseFloat(prompt('请输入数字：'));
        var num3 = parseFloat(prompt('请输入数字：'));
        var arr = [num1, num2, num3];
        var max = arr[0];
        for (var i = 0; i <= arr.length; i++) {
            if (arr[i] > max) {
                max = arr[i];
            }
        }
        alert(max);


```

### 5. arguments的使用

当不确定有多少个参数传递的时候，可以用arguments来获取。在JS中，arguments实际上是当前函数的一个内置对象。所有函数都内置了一个arguments对象，arguments对象中存储了传递的所有实参。

+ 具有length属性
+ 按索引方式存储数据
+ 不具有数组的push、pop等方法

```js
        // arguments的使用 只有函数才有arguments对象，而且每个函数都内置好了arguments（手机打电话 发短信等内置好的功能）
        function fn() {
            console.log(arguments); // 存储了所有传递过来的实参 arguments=[1,2,3]
            console.log(arguments.length);
            console.log(arguments[2]); // 3
            // 可以按照数组的方式 遍历arguments
            for (var i = 0; i < arguments.length; i++) {
                console.log(arguments[i]);
            }
        }
        fn(1, 2, 3)
        fn(1, 2, 3, 4, 5)
        // 伪数组并不是真正意义上的数组
        // 1.具有数组 length 属性
        // 2.按照索引的方式进行存储
        // 3.arguments伪数组没有真正数组的一些方法 pop() push()等
```

```js
        function fn() {
            for (var i = 0; i < arguments.length; i++) {
                console.log(arguments[i]);
            }
        }
        fn(1, 2, 3, 4, 'lee')
```

<img src="/Users/aoki/Library/Application Support/typora-user-images/image-20210821101649185.png" alt="image-20210821101649185" style="zoom:40%;" />

### 6.函数案例

```js
        // 案例：利用函数求任意个数的最大值
        function getMax() {
            var max = arguments[0];
            for (var i = 0; i < arguments.length; i++) {
                if (arguments[i] > max) {
                    max = arguments[i]
                }
            }
            return max;
        }
        console.log(getMax(1, 2, 3));
        console.log(getMax(1, 2, 3, 4, 5));
        console.log(getMax(1, 23, 35, 4, 500, 1000));
```

<img src="/Users/aoki/Library/Application Support/typora-user-images/image-20210821102301194.png" alt="image-20210821102301194" style="zoom:50%;" />

<img src="/Users/aoki/Library/Application Support/typora-user-images/image-20210821102316151.png" alt="image-20210821102316151" style="zoom:50%;" />

```js
        // 案例2：利用函数冒泡排序 sort=排序
        function sort(arr) {
            for (var i = 0; i <= arr.length - 1; i++) {
                for (var j = 0; j <= arr.length - i - 1; j++) {
                    if (arr[j] > arr[j + 1]) {
                        var max = arr[j];
                        arr[j] = arr[j + 1];
                        arr[j + 1] = max;
                    }
                }
            }
            return arr;
        }
        var arr1 = sort([5, 3, 2, 4, 1]);
        console.log(arr1);
        var arr2 = sort([1000, 999, 600, 500, 10]);
        console.log(arr2);
```

<img src="/Users/aoki/Library/Application Support/typora-user-images/image-20210821103313257.png" alt="image-20210821103313257" style="zoom:50%;" />

```js
        // 案例3：判断闰年
        function isRunYear(year) {
            var flag = false;
            if (year % 4 == 0 && year % 100 != 0 || year % 400 == 0) {
                flag = true;
            }
            return flag;
        }
        var year = isRunYear(2000);
        console.log(year);
        var year = isRunYear(1999);
        console.log(year);
```

<img src="/Users/aoki/Library/Application Support/typora-user-images/image-20210821104027120.png" alt="image-20210821104027120" style="zoom:50%;" />

#### 函数可以调用另一个函数

每个函数都是独立的代码块，用于完成特殊任务，经常会用到函数互相调用的情况

```js
        // 函数相互调用
        function fn1() {
            console.log(11);
            fn2(); // 在fn1函数里面调用了fn2函数
        }
        fn1();
        function fn2() {
            console.log(22);
        }
```

<img src="/Users/aoki/Library/Application Support/typora-user-images/image-20210821104626268.png" alt="image-20210821104626268" style="zoom:50%;" />

<img src="/Users/aoki/Library/Application Support/typora-user-images/image-20210821104616965.png" alt="image-20210821104616965" style="zoom:30%;" />

```js
        function fn1() {
            console.log(111);
            fn2();
            console.log('fn1');
        }
        function fn2() {
            console.log(222);
            console.log('fn2');
        }
        fn1();
```

<img src="/Users/aoki/Library/Application Support/typora-user-images/image-20210821104937622.png" alt="image-20210821104937622" style="zoom:50%;" />

```js
        // 案例4：
        // 用户输入年份，输出当前年份2月份的天数
        function backDay() {
            var year = prompt('请输入年份：');
            if (isRunYear(year)) { // 调用函数需要加小括号
                alert('当前是闰年2月有29天');
            } else {
                alert('当前是平年2月有28天');
            }
        }
        backDay();
        // 调用判断闰年函数
        function isRunYear(year) {
            // 如果是闰年返回 true， 否则返回 false
            var flag = false;
            if (year % 4 == 0 && year % 100 != 0 || year % 400 == 0) {
                flag = true;
            }
            return flag;
        }
```

### 函数的两种声明方式

```js
        // 函数的2种声明方式
        // 1.利用函数关键字自定义函数(命名函数)
        function fn(num1) {
            console.log(num1);
        }
        fn(1);
        // 2.函数表达式(匿名函数)
        // var 变量名 = function() {};
        var fun = function (aru) {
            console.log('函数表达式-匿名函数');
            console.log(aru);
        }
        fun('输出形参为实参 传递参数');
        // (1) fun是变量名 不是函数名
        // (2) 函数表达式声明方式跟声明变量差不多，只不过变量里面存的是值，而函数表达式里面存的是函数
        // (3) 函数表达式也可以进行传递参数
```

<img src="/Users/aoki/Library/Application Support/typora-user-images/image-20210821112041554.png" alt="image-20210821112041554" style="zoom:50%;" />

# JavaSript作用域

## 1.作用域

### 1.1 作用域概述

一段程序代码中所用到的名字并不总是有效和可用的，而限定这个名字的 **可用性的代码范围**就是这个名字的作用域。作用域的使用提高了程序逻辑的局部性，增强了程序的可靠性，减少名字冲突。

```js
        // 1.JS作用域：代码名字(变量)在某个范围内起作用和效果，目的是为了提高程序的可靠性更重要的是减少命名冲突
        // 2.JS的作用域(es6)之前：全局作用于    局部作用域
        // 3.全局作用于：整个scrip标签 / 一个单独的js文件
        var num = 10; // 被下面的num覆盖掉
        var num = 30;
        console.log(num);
        // 4.局部作用域(函数作用域)：在函数内部是局部作用域，这个代码的名字只在函数内部起效果和作用
        function fn() {
            // 局部作用域
            var num = 20; // 变量名相同 域不同不会起冲突
            console.log(num);
        }
        fn();
```

<img src="/Users/aoki/Library/Application Support/typora-user-images/image-20210821113301616.png" alt="image-20210821113301616" style="zoom:50%;" />

## 2.变量作用域

### 2.1 变量作用域的分类

根据作用域的不同，变量分为全局变量和局部变量

+ 全局变量
+ 局部变量

```js
        // 变量的作用域：
        // 1.全局变量：在全部作用域下的变量，在全局下都可以使用
        // ⚠️注意：如果在函数内部没有声明直接赋值的变量也属于全局变量 -->num2 = 20;
        var num = 10; // num是一个全局变量
        console.log(num);
        function fn() {
            console.log(num);
        }
        fn();
        console.log(aru); //局部变量 报错：aru is not defined at

        // 2.局部变量：在局部作用域下的变量，后者在函数内部的变量就是局部变量
        // ⚠️注意：函数的形参也可以看做是局部变量 -->aru
        function fun(aru) {
            var num1 = 10; // num1是局部变量，只能在函数内部使用
            num2 = 20; // 全局变量 
        }
        fun();
        // console.log(num1);
        console.log(num2);

        // 3.从执行效率看全局变量和局部变量 
        // (1) 全局变量只有浏览器关闭的时候才会销毁，比较占内存
        // (2) 局部变量当程序执行完毕就会销毁，比较省内存
```

### 2.2全局变量

全局作用域下声明的变量叫做 **全局变量**(在函数外部定义的变量)

+ 全局变量在代码的任何位置都可以使用
+ 在全局作用域下var声明的变量是全局变量
+ 特殊情况下，函数内不适用var声明的变量也是全局变量(不建议使用)

### 2.2局部变量

在局部作用域下声明的变量叫做 **局部变量**(在函数内部定义的变量)

+ 局部变量只能在该函数内部使用
+ 在函数内部var 声明的变量是局部变量
+ 函数的形参实际上就是局部变量

```js
        // 变量的作用域：
        // 1.全局变量：在全部作用域下的变量，在全局下都可以使用
        // ⚠️注意：如果在函数内部没有声明直接赋值的变量也属于全局变量 -->num2 = 20;
        var num = 10; // num是一个全局变量
        console.log(num);
        function fn() {
            console.log(num);
        }
        fn();
        console.log(aru); //局部变量 报错：aru is not defined at

        // 2.局部变量：在局部作用域下的变量，后者在函数内部的变量就是局部变量
        // ⚠️注意：函数的形参也可以看做是局部变量
        function fun(aru) {
            var num1 = 10; // num1是局部变量，只能在函数内部使用
            num2 = 20; // 全局变量 
        }
        fun();
        // console.log(num1);
        console.log(num2);

        // 3.从执行效率看全局变量和局部变量 区别：
        // (1) 全局变量只有浏览器关闭的时候才会销毁，比较占内存
        // (2) 局部变量当程序执行完毕就会销毁，比较省内存
```

<img src="/Users/aoki/Library/Application Support/typora-user-images/image-20210821115912708.png" alt="image-20210821115912708" style="zoom:33%;" />

### JS中没有块级作用域 –> es6的时候新增的块级作用域 	块级作用域{ }	if{}	for{}

## 3.作用域链

+ 只要是代码就至少有一个作用域
+ 写在函数内部的局部作用域
+ 如果函数中还有函数，那么在这个作用域中就可以诞生一个作用域
+ 根据在内部函数可以访问外部函数变量的这种机制，用链式查找决定哪些数据能被内部函数访问，就称为作用域链

```js
        // 作用域：内部函数访问外部函数的变量，采取的是链式查找的方式决定去哪个值，这种结构称为作用域链
        // 就近原则
        var num = 10;
        function fn() { // 外部函数
            var num = 20;
            function fun() { // 内部函数
                console.log(num); // 20
            }
            fun();
        }
        fn();
```

<img src="/Users/aoki/Library/Application Support/typora-user-images/image-20210821164455232.png" alt="image-20210821164455232" style="zoom:50%;" />

<img src="/Users/aoki/Library/Application Support/typora-user-images/image-20210821164734289.png" alt="image-20210821164734289" style="zoom:50%;" />

```js
        // 案例1：
        function f1() {
            var num = 123;
            function f2() {
                console.log(num); // 站在目标出发，一层一层往外找
            }
            f2();
        }
        var num = 456;
        f1();        
				
				// 案例2：
        var a = 1;
        function fn1() {
            var a = 2;
            var b = '22';
            fn2();
            function fn2() {
                var a = 3;
                fn3();
                function fn3() {
                    var a = 4;
                    console.log(a); // a的值
                    console.log(b); // b的值
                }
            }
        }
        fn1();
```

<img src="/Users/aoki/Library/Application Support/typora-user-images/image-20210821164856643.png" alt="image-20210821164856643" style="zoom:50%;" /><img src="/Users/aoki/Library/Application Support/typora-user-images/image-20210823150936589.png" alt="image-20210823150936589" style="zoom:50%;" />



## 1.预解析

JS代码是由浏览器中的JS解析器来执行的。JS解析器在运行JS代码的时候分为两步 ：预解析和代码执行。

```js
        // 1. JS引擎运行js分为两步：预解析 --> 代码执行
        // (1)预解析JS引擎会把JS里面所有的var 还有function提升到当前作用域的最前面
        // (2)代码执行按照代码书写顺序从上向下执行
        // 2.预解析分为变量预解析(变量提升)和函数预解析(函数提升)
        // (1)变量提升：把所有的变量声明提升到当前的作用域最前面，不提升赋值操作
        // (2)函数提升：把所有的函数声明提升到当前的作用域最前面，不调用函数

        // 1问
        // console.log(num);

        // 2问
        console.log(num);
        var num = 10; // undefined 坑2↓
        // 相当于执行以下代码
        // var num;
        // console.log(num);
        // num = 10;

        // 3问 函数提升 fn() 优先将函数声明提升到最前面
        fn();
        function fn() {
            console.log(11);
        }
        // 相当于执行以下代码
        // function fn() {
        //     console.log(11);
        // }
        // fn();

        // 4问
        fun(); // 报错 坑2↓
        var fun = function () {
            console.log(22);
        }
        // 相当于执行以下代码
        // var fun;
        // fun();
        // fun = function () {
        //     console.log(22);
        // }
        // ⚠️函数表达式调用必须写在函数表达式的下面
```

```js
        // 预解析 案例
        // 案例1：
        var num = 10;
        fun();
        function fun() {
            console.log(num);
            var num = 20;
        }
        // undefined
        // 相当于执行以下代码
        var num;

        function fun() {
            var num;
            console.log(num);
            num = 20;
        }
        num = 10;
        fun();

        // 案例2：
        var num = 10;
        function fn() {
            console.log(num);
            var num = 20;
            console.log(num);
        }
        fn();
        // undefined 20
        // 相当于执行以下代码
        var num;
        function fn() {
            var num;
            console.log(num);
            num = 20;
            console.log(num);
        }
        num = 10;
        fn();

        // 案例3：
        var a = 18;
        f1();
        function f1() {
            var b = 9;
            console.log(a);
            console.log(b);
            var a = '123';
        }
        // 相当于执行以下代码
        var a;
        function f1() {
            var b;
            var a;
            b = 9;
            console.log(a);
            console.log(b);
            a = '123';
        }
        a = 18;
        f1();

```

```js
        // 案例4：
        f1();
        console.log(c);
        console.log(b);
        console.log(a);
        function f1() {
            var a = b = c = 9;
            console.log(a);
            console.log(b);
            console.log(c);
        }
        // // 相当于执行以下代码
        function f1() {
            // 相当于 var a = 9; b = 9; c = 9; b和c直接赋值没有var声明当全局变量看
            // 集体声明 var a = 9, b = 9, c = 9;
            var a; // 局部变量
            a = b = c = 9;
            console.log(a);
            console.log(b);
            console.log(c);
        }
        f1();
        console.log(c); // 9
        console.log(b); // 9
        console.log(a); // 上方 var a属于局部变量 报错
```

案例1：<img src="/Users/aoki/Library/Application Support/typora-user-images/image-20210823160344622.png" alt="image-20210823160344622" style="zoom:50%;" />案例2：<img src="/Users/aoki/Library/Application Support/typora-user-images/image-20210823160422324.png" alt="image-20210823160422324" style="zoom:50%;" />案例3：<img src="/Users/aoki/Library/Application Support/typora-user-images/image-20210823160220526.png" alt="image-20210823160220526" style="zoom:50%;" />案例4：<img src="/Users/aoki/Library/Application Support/typora-user-images/image-20210823160110455.png" alt="image-20210823160110455" style="zoom:40%;" />

# JavaScript对象

+ 为什么需要对象

+ 使用字面量创建对象

+ 使用构造函数创建对象

+ 说出new的执行过程

+ 遍历对象

  

+ 对象

+ 创建对象的3种方式

+ new关键字

+ 遍历对象属性

## 1.对象

### 1.1什么是对象？

**对象是一个具体的事物**，数据库、网页…

在JS中，对象是一组**无序的相关属性和方法**的集合，所有事物都是对象，列入字符串、数值、数组、函数等

+ 属性：事物的特征，在对象中用属性来表示(常用名词)	大小、颜色、重量
+ 方法：事物的行为，在对象中用方法来表示(常用动词)    打电话、发短信

### 1.2为什么需要对象

保存一个值，可以使用**变量**，保存多个值(一组值)时，可以使用**数组**。如果要保存一个人的完整信息，使用 **对象**

<img src="/Users/aoki/Library/Application Support/typora-user-images/image-20210823161515755.png" alt="image-20210823161515755" style="zoom:50%;" />

## 2.创建对象的三种方式

现阶段可以采用是三种方式创建对象（object）

+ 利用**字面量**创建对象（最常用）
+ 利用**new Object**创建对象
+ 利用**构造函数**创建对象

### 2.1利用字面量创建对象

对象字面量：花括号{}里面包含表达这个具体事务(对象)的属性和方法。{}里面采取键值对的形式表示

+ 键：属性名
+ 值：属性值，可以是任意类型的值（数字类型、字符串类型、布尔类型、函数类型等）

###### 对象的调用：

+ 对象里面的属性调用 方法1：**对象.属性**，小点.理解为“的”
+ 对象里面的属性调用 方法2：**对象[‘属性名’]**，注意方括号里面的属性必须加引号
+ 对象里面的方法调用：**对象.方法名()**，注意这个方法名字后面一定加括号

```js
        // 1.利用字面量创建对象 {}
        // var obj = {} 创建了一个空的对象
        var obj = {
            name: 'lee',
            age: 18,
            sayHi: function () {
                console.log('Hello');
            }
        }
        // (1)里面的属性/方法采用键值对的形式   键 属性名： 值 属性值
        // (2)多个属性/方法中间用逗号隔开
        // (3)方法冒号后面跟的是一个匿名函数
        
        // 2.使用对象
        console.log(obj.name); // (1)调用对象属性 方法1：采取对象名.属性值
        console.log(obj['age']); // (2)调用对象属性 方法2：对象名['属性值']
        obj.sayHi(); // (3)调用对象的方法 sayHi 对象名.方法名() 一定要添加小括号

```

```js
      // 练习：  
			var obj = {
            name: 'coco',
            type: 'Alaskan',
            age: 5,
            color: 'brown',
            saySkill: function () {
                console.log('bark');
                console.log('showFilm');
            }
        }
        console.log(obj.name);
        console.log(obj.age);
        console.log(obj.type);
        console.log(obj['color']);
        obj.saySkill();
```

<img src="/Users/aoki/Library/Application Support/typora-user-images/image-20210823163733618.png" alt="image-20210823163733618" style="zoom:33%;" />

### 变量、属性、函数、方法的区别

+ 变量：单独声明赋值，单独存在
+ 属性：对象里面的变量称为属性，不需要声明，用来描述该对象的特征
+ 函数：单独存在的，通过“函数名()”的方式即可调用
+ 方法：对象里面的函数成为方法，方法不需要声明，使用“对象.方法名()”的方式就可以调用，方法用来描述该对象的行为和功能

### 2.2利用 new Object 创建对象

```js
        // 利用 new Object 创建对象
        var obj = new Object(); // 创建了一个空的对象
        obj.name = 'lee';
        obj.age = 18;
        obj.gender = 'man';
        obj.sayHi = function () {
            console.log('hello');
        }
        // (1) 利用等号 = 赋值的方法 添加对性的属性和方法
        // (2) 每个属性和方法之间用 分号结束；
        console.log(obj.name);
        console.log(obj['age']);
        obj.sayHi();
```

<img src="/Users/aoki/Library/Application Support/typora-user-images/image-20210823205742695.png" alt="image-20210823205742695" style="zoom:50%;" />

```js
        var obj = new Object();
        obj.name = 'naruto';
        obj.gender = 'man';
        obj.age = 19;
        obj.theSkill = function () {
            console.log('影分身术');
        }
        console.log(obj.name);
        console.log(obj['gender']);
        console.log(obj['age']);
        obj.theSkill();
```

### 2.3利用构造函数创建对象

构造函数**：是一种特殊的函数，主要用来初始化对象，即为对象成员变量赋初始值，它总是与new运算符一起使用。可以把对象中一些公共的属性和方法抽取出来，封装到这个函数里面。

```js
        // 构造函数的语法格式
        function 构造函数名() { //声明构造 函数
            this.属性 = 值; // this是当前的意思
            this.方法 = function () { }
        }
        new 构造函数(); // 调用构造函数

        // 构造函数和对象
        // 1.构造函数   Star 明星 泛指的某一大类，类似于Java语言里面的 类(class)
        function Star(name, age, gender) {
            this.name = name;
            this.age = age;
            this.gender = gender;
            this.sing = function (song) {
                console.log(song);
            }
        }
        // 2.对象：一个具体的事物   lee {name: "lee", age: "18", gender: "ms.", sing: ƒ}
        var lee = new Star('lee', '18', 'ms.');
        console.log(lee);
        lee.sing('icecream');
        // 3.利用构造函数创建对象的过程也称为对象的实例化
```

```js
        // 创建4大天王的对象 相同属性：名字 年龄 性别   相同的方法：唱歌
        function Star(name, age, gender) {
            this.name = name;
            this.age = age;
            this.gender = gender;
            this.sing = function (song) {
                console.log(song);
            }
        }
        var ldh = new Star('刘德华', 18, '男'); // 调用函数返回的是对象 Object
        console.log(typeof ldh);
        console.log(ldh.name);
        console.log(ldh.age);
        console.log(ldh.gender);
        ldh.sing('冰雨');
        console.log(ldh);
        var zxy = new Star('张学友', 19, '男');
        console.log(zxy.name);
        console.log(zxy.age);
        console.log(zxy.gender);
        zxy.sing('她来听我的演唱会')
        console.log(zxy);
        // 1.构造函数的名字首字母要大写
        // 2.构造函数不需要return就可以返回结果
        // 3.调用构造函数必须用 new
        // 4.只要new Star() 调用函数就创建一个对象 ldh {}
        // 5.属性和方法前面必须添加 this
```

```js
        // 练习：利用构造函数创建对象
        // 姓名属性(name) 类型属性(type) 血量属性(blood) 攻击方式(attack)
        function Wangzhe(name, type, blood) {
            this.name = name;
            this.type = type;
            this.blood = blood;
            this.attackType = function (attack) {
                console.log(attack);
            }
        }
        var lianpo = new Wangzhe('廉颇', '力量型', '500血量');
        console.log(lianpo.name);
        console.log(lianpo.type);
        console.log(lianpo.blood);
        lianpo.attackType('近战');
        var houyi = new Wangzhe('后裔', '射手型', '100血量');
        console.log(houyi.name);
        console.log(houyi.type);
        console.log(houyi.blood);
        houyi.attackType('远程');

//练习2：
        function friend(name, gender, type) {
            this.name = name;
            this.gender = gender;
            this.type = type;
            this.skill = function (deco) {
                console.log(deco);
            }
        }
        var vv = new friend('小王', 'ms.', '鼠巴拉西');
        console.log(vv);
        vv.skill('设计');
```

<img src="/Users/aoki/Library/Application Support/typora-user-images/image-20210824102243572.png" alt="image-20210824102243572" style="zoom:50%;" /><img src="/Users/aoki/Library/Application Support/typora-user-images/image-20210824102955660.png" alt="image-20210824102955660" style="zoom:40%;" />

### 2.4构造函数和对象

+ 构造函数：如 Star()，抽象了对象的公共部分，封装到函数里面，泛指某一大类(class)
+ 创建对象：如 new Stars()，特指某一个，通过 new 关键字创建对象的过程称为对象实例化

<img src="/Users/aoki/Library/Application Support/typora-user-images/image-20210824103229588.png" alt="image-20210824103229588" style="zoom:30%;" />



```js
        // new关键字执行过程
        // 1. new 构造函数可以在内存中创建一个新的空对象
        // 2. this 会指向刚才创建的空对象
        // 3. 执行构造函数中的代码，给新对象添加属性和方法
        // 4. 返回这个新对象 （所以构造函数中不需要写return）
        function Star(name, age, gender) {
            this.name = name;
            this.age = age;
            this.gender = gender;
            this.sing = function (song) {
                console.log(song);
            }
        }
        var lee = new Star('lee', '18', 'ms.');
```



## 4.遍历对象属性

```js
        // for...in 遍历对象
        for (变量 in 对象) {

        }
        // 遍历对象
        var obj = {
            name: 'lee',
            age: 18,
            gender: 'ms.',
            fn: function () { }
        }

        for (var k in obj) {
                console.log(k); // k 变量输出得到的是属性名
                console.log(obj[k]); // obj[k] 得到的是属性值
        }
        // 使用 for in 里面的变量，常用 k 或者 key
```

<img src="/Users/aoki/Library/Application Support/typora-user-images/image-20210824105626857.png" alt="image-20210824105626857" style="zoom:40%;" />

###### 1.对象可以让代码结构更清晰

###### 2.对象复杂数据类型Object

###### 3.本质：对象就是一组无序的相关属性和方法的集合

###### 4.构造函数泛指某一大类，比如苹果，不管红苹果还是青苹果，统称为苹果

###### 5.对象实例特指一个事物，比如这个苹果、这个人

###### 6.for in语句用于对对象的属性进行循环操作



```js
        // 作业1：
        // 创建一个电脑对象，该对象中有颜色、重量、品牌、型号，可以看电影、听音乐、打游戏、敲代码
        var obj = {
            name: 'mac',
            weight: '2.1kg',
            brand: 'Apple',
            type: 'Macbook Pro',
            sayHi: function () {
                console.log('movie');
                console.log('music');
                console.log('game');
                console.log('code');
            }
        }
        console.log(obj);
        obj.sayHi();
```

<img src="/Users/aoki/Library/Application Support/typora-user-images/image-20210824113123033.png" alt="image-20210824113123033" style="zoom:40%;" />

```js
        // 作业2：
        // 创建一个按钮对象，该对象中包含width、height、background-color和点击行为
        var button = new Object();
        button.width = 20;
        button.height = 20;
        button.bgc = 'skyblue';
        button.xingwei = function (click) {
            console.log('click');
        }
        console.log(button);
        button.xingwei();
```

<img src="/Users/aoki/Library/Application Support/typora-user-images/image-20210824113650987.png" alt="image-20210824113650987" style="zoom:50%;" />

```js
        // 作业3：
        // 创建一个车的对象，搞对象要有重量、颜色、牌子，可以载人、拉货和耕田
        function Car(weight, color, brand) {
            this.weight = weight;
            this.color = color;
            this.brand = brand;
            this.Skill = function (fun) {
                console.log('载人');
                console.log('拉货');
                console.log('耕田');
            }
        }
        var turbos = new Car('478kW/650 PS', 'white', 'Porsche');
        console.log(turbos);
        turbos.Skill();
```

<img src="/Users/aoki/Library/Application Support/typora-user-images/image-20210824114932825.png" alt="image-20210824114932825" style="zoom:40%;" />

```js
        // 作业4：
        // 写一个函数，实现反转任意数组
        function reverse(arr) {
            var newArr = [];
            for (var i = arr.length - 1; i >= 0; i--) {
                newArr[newArr.length] = arr[i];
            }
            return newArr;
        }
        var arr1 = reverse([1000, 999, 888, 777, 66, 5, 1]);
        console.log(arr1);
        var arr2 = reverse(['pig', 'dog', 'cat']);
        console.log(arr2);
```

<img src="/Users/aoki/Library/Application Support/typora-user-images/image-20210824120403754.png" alt="image-20210824120403754" style="zoom:50%;" />

```js
        // 写一个函数实现数字数组的排序
        function sort(arr) {
            for (var i = 0; i <= arr.length - 1; i++) {
                for (var j = 0; j <= arr.length - i - 1; j++) {
                    if (arr[j] > arr[j + 1]) {
                        var tump = arr[j];
                        arr[j] = arr[j + 1];
                        arr[j + 1] = tump;
                    }
                }
            }
            return arr;
        }
        var arr1 = sort([5, 4, 3, 2, 1]);
        console.log(arr1);
```

<img src="/Users/aoki/Library/Application Support/typora-user-images/image-20210824121013097.png" alt="image-20210824121013097" style="zoom:50%;" />

<img src="/Users/aoki/Library/Application Support/typora-user-images/image-20210824140630011.png" alt="image-20210824140630011" style="zoom:50%;" />

# 1.内置对象

+ JS中的对象分为3种：自定义对象、内置对象、浏览器对象
+ 前面两种对象是JS基础内容，属于ECMAScrip；第三个浏览器对象属于JS独有的，JS API讲解
+ 内置对象指JS语言自带的一些对象，这些对象供开发者使用，并提供了一些常用的或者最基本而且必要的功能（属性和方法）
+ 内置对象最大的优点是帮助我们快速开发
+ JS提供了多个内置对象：Math、Date、Array(数组)、String等

## 2.查文档

### 2.1 MDN

查文档学习，通过MDN/W3C

### 2.2如何学习对象中的方法

1. 查阅该方法的功能
2. 查看里面参数的意义和类型
3. 查看返回值的意义和类型
4. 通过demo进行测试

## 3.Math对象

```js
        // Math数学对象，不是一个构造函数，所以不需要 new 来调用，而是直接使用里面的属性和方法即可
        console.log(Math.PI); // 一个属性 圆周率
        console.log(Math.max(1, 888, 99)); // expected output:888
        console.log(Math.max(-1, -99)); // expected output:-1
        console.log(Math.max(1, 2, 3, 'lee')); // expected output：NaN
        console.log(Math.max()); // expected output: -Infinity
```

<img src="/Users/aoki/Library/Application Support/typora-user-images/image-20210824143032160.png" alt="image-20210824143032160" style="zoom:50%;" />

```js
        // 案例：封装自己的数学对象，里面有 PI 最大值和最小值
        var myMath = {
            PI: 3.14159265358,
            max: function () {
                var max = arguments[0];
                for (var i = 1; i < arguments.length; i++) {
                    if (arguments[i] > max) {
                        max = arguments[i];
                    }
                }
                return max;
            },
            min: function () {
                var min = arguments[0];
                for (var i = 1; i < arguments.length; i++) {
                    if (arguments[i] < min) {
                        min = arguments[i];
                    }
                }
                return min;
            }
        }
        console.log(myMath.PI);
        console.log(myMath.max(1, 2, 3, 4, 5));
        console.log(myMath.min(1, 2, 3, 4, 5));
```

<img src="/Users/aoki/Library/Application Support/typora-user-images/image-20210824144514727.png" alt="image-20210824144514727" style="zoom:33%;" />

### 3.1 Math概述

Math对象不是构造函数，具有数学常熟和函数的属性和方法。跟数学相关的运算（求绝对值、取整、最大值等）



```js
        // 1.绝对值方法 Math.abs()
        console.log(Math.abs(1)); // 1
        console.log(Math.abs(-1)); // 1
        console.log(Math.abs('-1')); // 1 隐式转换，把字符串型 -1转换为数字型
        console.log(Math.abs('lee')); //NaN
        // 2.三个取整方法
        // (1) Math.floor() 地板，取最小值
        console.log(Math.floor(1.1)); // 1
        console.log(Math.floor(1.9)); // 1
        // (2) Math.ceil()  天花板，取最大值
        console.log(Math.ceil(1.1)); // 2
        console.log(Math.ceil(1.9)); // 2
        // (3) Math.round() 四舍五入 但是.5比较特殊-->取大值
        console.log(Math.round(1.1)); // 1
        console.log(Math.round(1.5)); // 2
        console.log(Math.round(-1.1)); // -1
        console.log(Math.round(-2.5)); // 特殊情况 -2
				// 3.最大值和最小值	Math.max()/Math.min()
```

### 3.2 随机数方法 random()

```js
        // 1.Math对象随机数方法   random() 返回一个随机的小数     0 =< x < 1
        // 2.这个方法里面不跟参数
        // 3.代码验证
        console.log(Math.random()); // 随机小数
        // 4.两个数之间的随机整数 并且包含这个两个数
        // return Math.floor(Math.random() * (max - min + 1)) + min;
        function getRandom(min, max) {
            return Math.floor(Math.random() * (max - min + 1)) + min;
        }
        console.log(getRandom(1, 10)); // 随机整数
        // 5.随机点名
        var arr = ['lee', 'wang', 'zhang', 'elin', 'baby', 'ceil'];
        console.log(arr[getRandom(0, arr.length - 1)]);
```

<img src="/Users/aoki/Library/Application Support/typora-user-images/image-20210824155430761.png" alt="image-20210824155430761" style="zoom:50%;" />

```js
        // 案例：猜数字游戏
        // 程序随机生成一个1~10之间的数字，需要用到 Math.random()
        // while循环
        // 核心算法：if else if多分支语句来判断大于、小于、等于
        // 1.如果大于该数字，提示数字大了，继续猜；
        // 2.如果小于该数字，就提示数字小了，继续猜；
        // 3.如果等于该数字，就提示猜对了，结束程序
        function getRandom(min, max) {
            return Math.floor(Math.random() * (max - min + 1)) + min;
        }
        var random = getRandom(1, 10);
        while (true) { // 死循环
            var num = prompt('你来猜？输入1~10之间的数字');
            if (num > random) {
                alert('你猜大了');
            } else if (num < random) {
                alert('你猜小了');
            } else {
                alert('你猜对了！😎');
                break; // 退出整个循环结束程序
            }
        }
```

```js
        // 案例2：
        // 猜1~20之间的数字，只有10次机会
//方法1：
        function getRandom(min, max) {
            return Math.floor(Math.random() * (max - min + 1)) - min;
        }
        var random = getRandom(1, 50);
        for (var i = 1; i <= 10; i++) {
            var num = prompt('你来猜，输入1~50之间的数字');
            if (num > random) {
                alert('你猜大了');
            } else if (num < random) {
                alert('你猜小了');
            } else {
                alert('你猜对了');
                break;
            }
            if (i == 10) {
                alert('10次机会已用完');
                break;
            }
        }
//方法2：
        function getRandom(min, max) {
            return Math.floor(Math.random() * (max - min + 1)) - min;
        }
        var random = getRandom(1, 50)
        var count = 10;
        while (count >= 0) {
            count--;
            var num = prompt('参数字？请输入1~50之间的数字')
            if (num < 1 || num > 50) {
                alert('输入错误，还有剩余' + count + '次机会');
            } else if (num > random) {
                alert('猜大了，还有' + count + '次机会');
            } else if (num < random) {
                alert('猜小了，还有' + count + '次机会');
            } else {
                alert('猜对了！Bingo~~');
                break;
            }
            if (num == 10) {
                alert('次数已用完');
                break;
            }
        }
```

###### JavaScript 数组练习案例源码URL：https://www.codenong.com/cs109519679/



## 4.日期对象

### 4.1 Date概述

+ Date对象和Math对象不一样，是一个构造函数，需要实例化后才能使用(new)
+ Date实例用来处理日期和时间

### 4.2 Date()方法的使用

###### 1.获取当前时间必须实例化

```js
var date = Date();
console.log(date);
```

###### 2.Date()构造函数的参数

如果括号里有时间，就返回参数里面的时间。例如日期个事字符串：‘2021-8-24’，可以写为 new Date(‘2021-8-24’)或者new Date(‘2021/8/24’)

```js
        // Date()   日期对象，是一个构造函数，必须用 new 来调用创建的日期对象
        var arr = new Array(); // 创建一个数组对象
        var obj = new Object(); // 创建一个对象实例
        // 1.使用Date 如果没有参数，返回当前系统的当前时间
        var date = new Date();
        console.log(date);
        // 2.参数常用的写法：数字型--> 2021, 08, 24 或者是字符串型--> '2021-8-24 10:0:0'
        var date1 = new Date(2021, 01, 01);
        console.log(date1); //返回的是 2月不是 1月
        var date2 = new Date('2021-8-24 10:10:10');
        console.log(date2);
```

<img src="/Users/aoki/Library/Application Support/typora-user-images/image-20210824174538712.png" alt="image-20210824174538712" style="zoom:50%;" />

### 4.3日期格式化

<img src="/Users/aoki/Library/Application Support/typora-user-images/image-20210824175713904.png" alt="image-20210824175713904" style="zoom:50%;" />

```js
        var date = new Date();
        console.log(date.getFullYear()); // 返回当前的年份 2021
        console.log(date.getMonth() + 1); // 月份 返回的月份小1个月，⚠️月份+1
        console.log(date.getDate()); // 返回日期
        console.log(date.getDay()); // 返回星期 周一返回-->1  周六-->6  周日-->0
        // 格式 2021年 8月 24日 星期二
        var year = date.getFullYear();
        var month = date.getMonth();
        var dates = date.getDate();
        var day = date.getDay();
        var arr = ['星期日', '星期一', '星期二', '星期三', '星期四', '星期五', '星期六'];
        console.log('今天是：' + year + '年' + month + '月' + dates + '日 ' + arr[day]);
```

```js
        // 格式化日期 时分秒
        var date = new Date();
        console.log(date.getHours()); // 时
        console.log(date.getMinutes()); // 分
        console.log(date.getSeconds()); // 秒
        // 要求封装一个函数返回当前的时分秒 格式 08：08：08
        function getTimer() {
            var time = new Date();
            var h = time.getHours();
            h = h < 10 ? '0' + h : h;
            var m = time.getMinutes();
            m = m < 10 ? '0' + m : m;
            var s = time.getSeconds();
            s = s < 10 ? '0' + s : s;
            return h + ':' + m + ':' + s;
        }
        console.log(getTimer());
```

### 4.4获取日期的总的毫秒形式(时间戳)

Date对象基于1970年1月1日(世界标准时间)起的毫秒数

```js
        // 1.通过 valueOf() getTime()
        var date = new Date();
        console.log(date.valueOf()); // 现在时间距离1970.1.1总的毫秒数
        console.log(date.getTime());
        // 2.简单的写法（最常用）
        var date1 = +new Date();
        console.log(date1);
        // 3.H5新增写法获得总的毫秒数
        console.log(Date.now());
```

<img src="/Users/aoki/Library/Application Support/typora-user-images/image-20210824204825375.png" alt="image-20210824204825375" style="zoom:50%;" />

+ d = parseInt(总秒数 / 60 / 60 / 24);	// 计算天数
+ h = parseInt(总秒数 / 60 / 60 % 24);  // 计算小时
+ m = parseInt(总秒数/ 60 % 60);  // 计算分数
+ s = parseInt(总秒数 % 60);  // 计算当前秒数

```js
        // 案例：倒计时效果
        // 1. 核心算法：输入的时间减去现在的时间就是剩余的时间，即倒计时，但是不能拿着时分秒相减。比如05分减去25分，结果是负数
        // 2. 用时间戳来解决。用户输入时间总的毫秒数减去现在时间总的毫秒数，得到的就是剩余时间的毫秒数
        // 3.把剩余时间总的毫秒数转换为天、时、分、秒（时间戳转换为时分秒）
        function countDown(time) {
            var nowTime = +new Date(); // 当前时间总的毫秒数
            var inputTime = +new Date(time); // 返回用户输入的时间总的毫秒书
            var times = (inputTime - nowTime) / 1000; // times是剩余时间的毫秒数 /1000换算为总的秒数
            var d = parseInt(times / 60 / 60 / 24); // 天
            d = d < 10 ? '0' + d : d;
            var h = parseInt(times / 60 / 60 % 24); // 时
            h = h < 10 ? '0' + h : h;
            var m = parseInt(times / 60 % 60); // 分
            m = m < 10 ? '0' + m : m;
            var s = parseInt(times % 60); // 秒
            s = s < 10 ? '0' + s : s;
            return d + '天' + h + '时' + m + '分' + s + '秒';
        }
        console.log(countDown('2021-8-25 12:00:00'));
        var date = new Date();
        console.log(date);
```

<img src="/Users/aoki/Library/Application Support/typora-user-images/image-20210825102617666.png" alt="image-20210825102617666" style="zoom:50%;" />

## 5.数组对象

### 5.1 数组对象的创建

+ 字面量方式
+ new Array()

```js
        // 1.数组字面量
        var arr = [1, 2, 3];
        console.log(arr[0]);

        // 2. new Array()
        // var arr1 = new Array(); // 创建了一个空数组
        var arr1 = new Array(2); // 2表示数组的长度为2，里面有2个空的数组元素
        console.log(arr1);
        var arr2 = new Array(2, 3); // 等价于[2,3]，表示里面有2个数组元素是2和3
        console.log(arr2);
```

### 5.2 检测是否为数组

```js
        // 翻转数组 reverse翻转
        function reverse(arr) {
            //if (arr instanceof Array) { // (1)instanceof
          		if(Array.isArray(arr)){ // (2)Array.isArray(参数)
                var newArr = []; // 新的空数组
                for (var i = arr.length - 1; i >= 0; i--) {
                    newArr[newArr.length] = arr[i];
                }
                return newArr;
            } else {
                return ('error这个参数要求必须是数组格式[1,2,3]')
            }
        }
        console.log(reverse([1, 2, 3, 4, 5]));
        console.log(reverse(1, 2, 3)); // error

        // 检测是否为数组
        // (1) instanceof 运算符 
        var arr = []; // 数组
        var obj = {}; // 对象
        console.log(arr instanceof Array);
        console.log(obj instanceof Array);

        // (2) Array.isArray(参数);	H5新增方法，ie9以上版本支持
        console.log(Array.isArray(arr));
        console.log(Array.isArray(obj));
```

<img src="/Users/aoki/Library/Application Support/typora-user-images/image-20210825111315413.png" alt="image-20210825111315413" style="zoom:50%;" />

### 5.3添加或删除数组元素的方法

+ push(参数1…)  数组的末尾添加一个或多个元素，注意修改原数组	并返回新的长度
+ unshift(参数1…)  数组的开头添加一个或多个元素，注意修改原数组   并返回新的长度
+ pop()   删除数组最后一个元素，数组长度减1，无参数、修改原数组  返回它删除的元素的值
+ shift()   删除数组的第一个元素，数组长度减1，无参数、修改原数组  返回第一个元素的值

```js
        // 1. push() 在数组的末尾添加一个/多个数组元素 push 推
        var arr = [1, 2, 3];
        // arr.push(4, 'lee');
        console.log(arr.push(4, 'lee'));
        console.log(arr);
        // (1) push 是可以给数组追加新的元素
        // (2) push() 参数直接写数组元素就可以
        // (3) push完毕后，返回的结果是新数组的长度
        // (4) 原数组也会发生变化

        // 2. unshift 在数组的开头添加一个/多个数组元素
        // arr.unshift('star:');
        console.log(arr.unshift('star:'));
        console.log(arr);
        // (1) unshift 给数组前面追加新的元素
        // (2) unshift() 参数直接写数组元素就可以
        // (3) unshift完毕后，返回的结果是新数组的长度
        // (4) 原数组也会发生变化

        // 3.pop() 删除数组的最后一个元素
        // arr.pop();
        console.log(arr.pop()); //返回值
        console.log(arr);
        // (1) pop 删除数组的最后一个元素，一次只能删除一个元素
        // (2) pop() 没有参数
        // (3) pop完毕后，返回的结果是删除的元素值
        // (4) 原数组会发生变化

        // 4.shift() 删除数组的第一个元素
        // arr.pop();
        console.log(arr.shift()); //返回值
        console.log(arr);
        // (1) shift 删除数组的第一个元素，一次只能删除一个元素
        // (2) shift() 没有参数
        // (3) shift完毕后，返回的结果是删除的元素值
        // (4) 原数组会发生变化
```

<img src="/Users/aoki/Library/Application Support/typora-user-images/image-20210825113125267.png" alt="image-20210825113125267" style="zoom:50%;" />

```js
        // 工资数组[1500, 1200, 2000, 2100, 1800]。要求把数组中工资超过2000的删除，剩余的放到新数组中
        var arr = [1500, 1200, 2000, 2100, 1800];
        var newArr = [];
        for (var i = 0; i < arr.length; i++) {
            if (arr[i] < 2000) {
                // newArr[newArr.length] = arr[i];
                newArr.push(arr[i]); // 从arr[i]中小于2000的追加到newArr中
            }
        }
        console.log(newArr);
```

<img src="/Users/aoki/Library/Application Support/typora-user-images/image-20210825114055319.png" alt="image-20210825114055319" style="zoom:50%;" /> 

### 5.4 数组排序

+ reverse()	颠倒数组中元素的顺序，无参数   该方法会改变原来的数组，返回新数组
+ sort()    对数组的元素进行排序    该方法会改变原来的数组，返回新数组

```js
        // 数组排序
        // 1.翻转数组
        var arr = ['red', 'yellow', 'blue'];
        arr.reverse();
        console.log(arr);

        // 2.数组排序(冒泡排序)
        var arr1 = [5, 77, 16, 1, 7];
        arr1.sort(function (a, b) {
            return a - b; // 升序的顺序排列
            return b - a; // 降序的顺序排列
        });
        console.log(arr1);
```

<img src="/Users/aoki/Library/Application Support/typora-user-images/image-20210825115703736.png" alt="image-20210825115703736" style="zoom:50%;" />

### 5.5数组索引方法

+ indexOf()   数组中查找给定元素的第一个索引   如果存在返回索引号，如果不存在返回-1
+ IastIndexOf()   数组中的最后一个索引    如果存在返回索引号，如果不存在返回-1

```js
        // 1. indexOf(数组元素) 返回该数组元素的索引号，从前向后查找
        // ⚠️只返回第一个满足条件的索引号
        // 如果在数组中找不到元素，则返回-1
        var arr = ['red', 'yellow', 'blue', 'green', 'blue']; // 2
        var arr = ['red', 'yellow', 'green']; // -1
        console.log(arr.indexOf('blue'));

        // 2. lastIndexOf(数组元素) 返回该数组元素的索引号，从后向前查找
        console.log(arr.lastIndexOf('blue')); //-1
        var arr = ['red', 'yellow', 'blue', 'green', 'blue']; // 4
        console.log(arr.lastIndexOf('blue'));
```

<img src="/Users/aoki/Library/Application Support/typora-user-images/image-20210825120144139.png" alt="image-20210825120144139" style="zoom:50%;" />

```js
        // 案例：数组去重（重点案例）
        // 数组去重 ['c', 'a', 'z', 'a', 'x', 'a', 'x', 'c', 'b'] 要求去除数组中重复的元素。
        // 1.目标：把旧数组里面不重复的元素选取出来放到新数组中，重复的元素只保留一个，放到新数组中去重。
        // 2.核心算法：遍历旧数组，拿着旧数组元素去查询新数组，如果该元素在新数组里面没有出现过，就添加，否则不添加
        // 3.怎么知道该元素没有存在？ 利用 新数组.indexOf(数组元素) 如果返回值为-1，则说明新数组里面没有该元素
        // 封装去重函数 unique 独一无二的
        function unique(arr) {
            var newArr = [];
            for (var i = 0; i < arr.length; i++) {
                if (newArr.indexOf(arr[i]) === -1) { // 查询旧数组元素是否在新数组中
                    newArr.push(arr[i]); // 如果在新数组中查找，返回的是 ===-1 说明查询不到，则存放到新数组中
                }
            }
            return newArr;
        }
        var demo = unique(['c', 'a', 'z', 'a', 'x', 'a', 'x', 'c', 'b']);
        console.log(demo);
```

### 5.6 数组转换为字符串

+ toString()   把数组转换成字符串，逗号分隔每一项   返回一个字符串
+ join(‘分隔符’)   方法用于把数组中的所有元素转换为一个字符串   返回一个字符串

```js
        // 1. toString() 数组转换为字符串
        var arr = [1, 2, 3];
        console.log(arr.toString()); // 1,2,3

        // 2. join('分隔符')
        var arr1 = ['red', 'yellow', 'blue']
        console.log(arr1.join()); // red,yellow,blue
        console.log(arr1.join('-')); // red-yellow-blue
        console.log(arr1.join('&')); // red&yellow&blue
```

<img src="/Users/aoki/Library/Application Support/typora-user-images/image-20210825132133889.png" alt="image-20210825132133889" style="zoom:33%;" />

### 5.7 其他数组转换

+ concat()   连接两个/多个数组，不影响原数组	返回一个新的数组
+ slice()  数组截取slice(begin, end)   返回被截取项目的新数组
+ splice()  数组删除splice(第几个开始, 要删除个数)  返回被删除项目的新数组，⚠️这个会影响原数组(常用)

```js
        var myFish = ['a', 'b', 'c', 'd', 'e'];
        myFish.splice(3, 0, 'vv');
        console.log(myFish);
```

<img src="/Users/aoki/Library/Application Support/typora-user-images/image-20210825134232657.png" alt="image-20210825134232657" style="zoom:50%;" />

## 6.字符串变量

### 6.1 基本包装类型

方便操作基本数据类型，JS提供了三个特殊的引用类型：**String | Number | Boolean**

**基本包装类型**：把简单数据类型包装为复杂数据类型，这样基本数据类型有了属性和方法

```js
        var str = 'abcd';
        console.log(str.length);
        // 对象才有属性和方法，复杂数据类型才有属性和方法
        // 简单数据类型为什么会有length属性？
        // 基本包装类型：把简单数据类型包装成了复杂数据类型
        // (1) 生成临时变量，将简单数据类型包装为复杂数据类型
        var temp = new String('abcd');
        // (2) 把临时变量的值给 str;
        str = temp;
        // (3) 销毁这个临时变量
        temp = null;
```

### 6.2 字符串的不可变

里面的值不可变，虽然看上去可以改变内容，但其实是地址改变了，原来的值还存在，内存中新建了一个内存空间，

```js
        var str = 'andy';
        console.log(str);
        str = 'red';
        console.log(str);
        // 因为字符串的不可变，不要大量的拼接字符串
        var str = '';
        for (var i = 1; i <= 100; i++) {
            str += i;
        }
        console.log(str);
```

<img src="/Users/aoki/Library/Application Support/typora-user-images/image-20210825141337319.png" alt="image-20210825141337319" style="zoom:50%;" /><img src="/Users/aoki/Library/Application Support/typora-user-images/image-20210825141347356.png" alt="image-20210825141347356" style="zoom:30%;" />

```js
        // 案例：返回字符位置
        // 查找字符串"abcoefoxyozzopp"中所有o出现的位置以及次数        
        // 核心算法：先查找第一个o出现的位置
        // 然后 只要indexOf 返回的结果不是 -1 就继续往后查找
        // 因为indexOf 只能查找到第一个，所以后面的查找，一定是当前索引加1，从而继续查找
        var str = "abcoefoxyozzopp";
        var index = str.indexOf('o')
        var num = 0;
        while (index !== -1) {
            console.log(index);
            num++;
            index = str.indexOf('o', index + 1);
        }
        console.log('o出现的次数是：' + num);
```

<img src="/Users/aoki/Library/Application Support/typora-user-images/image-20210825142624323.png" alt="image-20210825142624323" style="zoom:50%;" />

```js
        // ['red','blue','red','green','pink','red'] 求red出现的位置和次数
        var str = ['red', 'blue', 'red', 'green', 'pink', 'red'];
        var index = str.indexOf('red');
        var num = 0;
        while (index !== -1) {
            console.log(index);
            num++;
            index = str.indexOf('red', index + 1);
        }
        console.log('red出现的次数是：' + num);
```

<img src="/Users/aoki/Library/Application Support/typora-user-images/image-20210825143754372.png" alt="image-20210825143754372" style="zoom:50%;" />

### 6.4根据位置返回字符（重点）

+ charAt(index)   返回指定位置字符（index字符串的索引号）   str.charAt(0)
+ charCodeAt(index)   获取指定位置字符ASCII码（index索引号）   str.charCodeAt(0)
+ str[index]   获取指定位置字符  HTML5、IE8+支持和chartAt()等效

```js
        // 1.chaAt(index) 根据位置返回字符
        var str = 'andy';
        console.log(str.charAt(3));
        // 遍历所有的字符
        for (var i = 0; i < str.length; i++) {
            console.log(str.charAt(i));
        }

        // 2.charCodeAt(index) 返回相应索引号的字符ASCII值，目的：判断用户按下哪个键
        console.log(str.charCodeAt(0)); // 97

        // 3. str[index]  H5新增
        console.log(str[0]);
```

<img src="/Users/aoki/Library/Application Support/typora-user-images/image-20210825145138340.png" alt="image-20210825145138340" style="zoom:30%;" />

```js
        // 案例：返回字符位置
        //  判断一个字符串 'abcoefoxyozzopp' 中出现次数最多的字符，并统计其次数。
        // o.a = 1
        // o.b = 1
        // o.c = 1
        // o.o = 4
        // 1.核心算法：利用charAt() 遍历这个字符串
        // 2.把每个字符都存储给对象，如果对象没有该属性为1，如果存在为+1
        // 3.遍历对象，得到最大值和该字符
        var str = 'abcoefoxyozzopp';
        var o = {}; // 花括号是创建对象的字面量 []创建数组使用中括号
        for (var i = 0; i < str.length; i++) {
            var chars = str.charAt(i); // chars 是字符串的每一个字符
            if (o[chars]) { // o[chars] 得到属性值
                o[chars]++;
            } else {
                o[chars] = 1;
            }
        }
        console.log(o);

        // 2.遍历对象
        var max = 0;
        var ch = '';
        for (var k in o) {
            // k得到的是属性名 o[k]得到的是属性值
            if (o[k] > max) {
                max = o[k];
                ch = k; // k出了for循环后不起作用 所以声明为ch
            }
        }
        console.log(max);
        console.log('最多的字符是：' + ch);
```

<img src="/Users/aoki/Library/Application Support/typora-user-images/image-20210825154949907.png" alt="image-20210825154949907" style="zoom:50%;" /><img src="/Users/aoki/Library/Application Support/typora-user-images/image-20210825155730777.png" alt="image-20210825155730777" style="zoom:50%;" />

### 6.5 字符串操作方法（重点）

+ concat(str1, str2, str3…)   concat()方法用于连接两个或多个字符串。拼接字符串，等效于+，+更常用
+ substr(start, length)   从start位置开始（索引号），length取的个数⚠️重点记
+ slice(start, end)   从start位置开始，截取到end位置，end取不到（都是索引号）
+ substring(star, end)   从start位置开始，截取到end位置，end取不到，基本和slice相同，但是不接受负值
+ toUpperCase()  转换为大写
+ toLowerCase()  转换为小写

```js
        // 1. concat('string1','string2'...)
        var str = 'lee';
        console.log(str.concat('❤️vv'));

        // 2. substr('截取的起始位置', '截取几个字符')
        var str1 = '慢慢喜欢你';
        console.log(str1.substr(2, 2)); // 第一个2是索引号2 从第几个开始，第二个2是取几个字符
```

<img src="/Users/aoki/Library/Application Support/typora-user-images/image-20210825161146832.png" alt="image-20210825161146832" style="zoom:40%;" />

```js
        // 1.替换字符 replace('被替换的字符', '替换为的字符')   只会替换第一个字符
        var str = 'andyandy';
        console.log(str.replace('a', 'b'));
        // 有一个字符串 'abcoefoxyozzopp' 要求把里面所有的o替换为*
        var str1 = 'abcdeabcdeabcde';
        while (str1.indexOf('e') !== -1) {
            str1 = str1.replace('e', '*');
        }
        console.log(str1);
        // 2.字符转换为数组 split('分隔符')    join 把数组转换为字符
        var str2 = 'red,blue,yellow';
        console.log(str2.split(','));
        var str3 = 'red&blue&yellow';
        console.log(str3.split('&'));
```

<img src="/Users/aoki/Library/Application Support/typora-user-images/image-20210825162407343.png" alt="image-20210825162407343" style="zoom:50%;" />

```js
       //作业
       // 给定一个字符串 'abdcfdjfajlafopaoswpq66331100'
        var str = 'abdcfdjfazjlafopaoswpq66331100'
        // 1.字符串长度
        console.log(str.length);
        // 2.取出位置的字符，如ao63等
        console.log(str.indexOf('a')); // a 第0个位置
        // 3.查找指定字符是否在以上字符串中存在：i、c、b等
        console.log(str.indexOf('z') !== -1);
        // 4.替换指定字符，如：f替换为15，p替换为e..
        console.log(str.replace('f', '15'));
        // 5.截取指定开始为指导结束位置的字符串，如取1~5的字符串
        console.log(str.slice(1, 6)); // 结果：bdcfd
        // 6.找出以上字符串中出现次数最多的字符和出现的次数
        var a = {};
        for (var i = 0; i < str.length; i++) {
            var chars = str.charAt(i);
            if (a[chars]) {
                a[chars]++;
            } else {
                a[chars] = 1;
            }
        }
        var max = 0;
        var ch = ''; // string 字面量
        for (var k in a) {
            if (a[k] > max) {
                max = a[k];
                ch = k;
            }
        }
        console.log(max);
        console.log('最多的字符是：' + ch);
```

<img src="/Users/aoki/Library/Application Support/typora-user-images/image-20210825165909806.png" alt="image-20210825165909806" style="zoom:50%;" />

# 简单数据类型 | 复杂数据类型

### 1.简单类型与复杂类型

简单类型(基本数据类型 / 值类型)	复杂类型(引用类型)

+ 值类型：简单数据类型或基本数据类型，在存储时变量中存储的是值本身，因此也叫做值类型
  string / number / boolean / undefined / null

+ 引用类型：复杂数据类型，在存储时变量中存储的仅仅是地址（引用），因此叫做引用数据类型

  通过new关键字创建的对象（系统对象、自定义对象）

  Object / Array / Date

```js
        // 简单数据类型 null    返回的是一个空的对象 object
        var timer = null;
        console.log(typeof timer);
        // 如果有个变量以后打算存储为对象，暂时没想好，这个时候给 null
```

### 2.堆和栈

###### 1.栈（操作系统）：由操作系统自动分配释放存放函数的参数值、局部变量的值等。其操作方式类似于数据结构中的栈；

**简单数据类型存放到栈里面**

###### 2.堆（操作系统）：存储复杂类型（对象），一般由程序员分配释放，若程序员不释放，由垃圾回收机制回收

**复杂数据类型存放到堆里面**

<img src="/Users/aoki/Library/Application Support/typora-user-images/image-20210825171721109.png" alt="image-20210825171721109" style="zoom:50%;" />

⚠️JS中没有堆栈的概念

<img src="/Users/aoki/Library/Application Support/typora-user-images/image-20210825172011089.png" alt="image-20210825172011089" style="zoom:50%;" />

```js
// 1.简单数据类型 直接存放在栈中，创建一个空间存放的是值
// 2.复杂数据类型 首先在栈里存放地址（十六进制表示）然后这个地址指向堆里面的数据
```

### 5.简单类型传参

函数的形参也可以看做是一个变量，把一个值类型变量作为参数传给函数的形参时，其实是把变量在栈空间里的值复制一份给形参，那么在方法内部对形参做任何修改，都不会影响到外部变量

<img src="/Users/aoki/Library/Application Support/typora-user-images/image-20210825173046605.png" alt="image-20210825173046605" style="zoom:50%;" />

```js
        // 简单数据类型传参
        function fn(a) {
            a++;
            console.log(a);
        }
        var x = 10;
        fn(x);
        console.log(x);
```

### 6.复杂类型传参

函数的形参也可以看做是一个变量，把引用类型变量传给形参时，其实是把变量在栈空间里保存的堆地址复制给了形参，形参和实参其实保存的是同一个堆地址，所以操作的是同一个对象

<img src="/Users/aoki/Library/Application Support/typora-user-images/image-20210826122854363.png" alt="image-20210826122854363" style="zoom:50%;" />

```js
       // 复杂数据类型传参
        function Person(name) {
            this.name = name;
        }

        function f1(x) {
            console.log(x.name); // 2.这个输出是什么    刘德华
            x.name = "张学友";
            console.log(x.name); // 3.这个输出是什么    张学友
        }
        var p = new Person("刘德华");
        console.log(p.name); // 1.这个输出是什么？  刘德华
        f1(p);
        console.log(p.name); // 4.这个输出是什么    张学友
```

<img src="/Users/aoki/Library/Application Support/typora-user-images/image-20210826122936389.png" alt="image-20210826122936389" style="zoom:50%;" />

# Web APIs简介

+ Web APIs阶段与JavaScript 语法阶段的关联性

+ 什么是API

+ 什么是Web API

  ·Web APIs和JS基础关联性

  ·API 和 Web API

  

## 1. Web APIs 和 JS基础关联性

### 1.1 JS的组成

<img src="/Users/aoki/Library/Application Support/typora-user-images/image-20210826123540604.png" alt="image-20210826123540604" style="zoom:50%;" />

### 1.2 JS基础阶段以及Web APIs阶段

<img src="/Users/aoki/Library/Application Support/typora-user-images/image-20210826130510937.png" alt="image-20210826130510937" style="zoom:50%;" />

## 2.API和Web API

### 2.1 API

（应用程序编程接口）一些预先定义的函数，目的是提供应用程序与开发人员基于某软件或硬件得以访问一组例程的能力，而又无需访问源码，或理解内部工作机制的细节

<img src="/Users/aoki/Library/Application Support/typora-user-images/image-20210826130806467.png" alt="image-20210826130806467" style="zoom:50%;" />

### 2.2 Web API

Web API是浏览器提供的一套操作浏览器功能和页面元素的API（BOM和DOM）

比如alert（‘弹出’）

MDN：https://developer.mozilla.org/zh-CN/docs/Web/API

### 2.3 API 和 Web API

1. API是给程序员提供的一个接口，帮助我们实现某种功能，会使用就可以
2. Web API 主要是针对于浏览器提供的接口，主要针对于浏览器做交互效果
3. Web API一般都有输入和输出（函数的传参和返回值），Web API很多都是方法（函数）
4. Web API 结合内置对象方法

# DOM

+ DOM
+ 获取页面元素
+ 给元素注册事件
+ 操作DOM元素的属性
+ 创建元素
+ 操作DOM节点

## 1.DOM简介

### 1.1DOM

文档对象模型(Document Object Model)，W3C组织推荐的处理可扩展标记语言（HTML或XML）的标准编程接口。

W3C已经定义了一系列的DOM接口，通过这些DOM接口可以改变网页的内容、结构和样式。

### 1.2 DOM 树

<img src="/Users/aoki/Library/Application Support/typora-user-images/image-20210826135815400.png" alt="image-20210826135815400" style="zoom:50%;" />

+ 文档：一个页面就是一个文档，DOM中使用document表示
+ 元素：页面中的所有标签都是元素，DOM中使用element表示
+ 节点：网页中的所有内容都是节点（标签、属性、文本、注释等），DOM中使用node表示

**DOM把以上内容都看做是对象**

## 2.获取元素

### 2.1如何获取页面元素

DOM在实际开发中主要用来操作元素

+ 根据ID获取
+ 根据标签名获取
+ 通过HTML5新增的方法获取
+ 特殊元素获取

### 2.2根据 ID 获取

使用getElementByld()

```html
    <div id="time">2021-8-25</div>
    <script>
        // 1.因为文档页面从上往下加载，所以闲先得有标签
        // 2.get获得 element元素 by通过 驼峰命名法
        // 3.参数 id是大小写敏感的字符串
        // 4.返回的是一个元素对象
        var timer = document.getElementById('time'); // 必须是字符串 加 '' 
        console.log(timer);
        console.log(typeof timer);
        // console.dir 打印返回的元素对象 更好的查看里面的属性和方法
        console.dir(timer);
    </script>
```

<img src="/Users/aoki/Library/Application Support/typora-user-images/image-20210826144231430.png" alt="image-20210826144231430" style="zoom:50%;" />

### 2.3 根据标签名获取

使用 getElementsByTagName() 方法可以返回带有指定标签名的对象集合。

```js
document.getElementsByTagName('标签名');
```

⚠️：

1. 得到的一个对象的集合，想要操作里面的元素就需要遍历

2. 得到元素对象是动态的

   ```html
   <ul>
       <li>2021年8月25日 1</li>
       <li>2021年8月25日 2</li>
       <li>2021年8月25日 3</li>
       <li>2021年8月25日 4</li>
       <li>2021年8月25日 5</li>
   </ul>
   <script>
       // 1.返回的是获取过来元素对象的集合，以为数组的形式存储的
       var lis = document.getElementsByTagName('li')
       console.log(lis);
       console.log(lis[0]);
       // 2.依次打印里面的元素对象可以采取遍历的方式
       for (var i = 0; i < lis.length; i++) {
           console.log(lis[i]);
       }
   </script>
   ```

   <img src="/Users/aoki/Library/Application Support/typora-user-images/image-20210826150422873.png" alt="image-20210826150422873" style="zoom:50%;" />

还可以获取某个元素（父元素）内部所有指定标签名的子元素。

```js
		element.getElementsByTagName('标签名'); // element 指父元素
    console.log(ol[0].getElementsByTagName('li'));

```

⚠️：父元素必须是单个对象（必须指明是哪一个元素对象），获取的时候不包括父元素自己

<img src="/Users/aoki/Library/Application Support/typora-user-images/image-20210826150926607.png" alt="image-20210826150926607" style="zoom:50%;" />ol中的li获取过来<img src="/Users/aoki/Library/Application Support/typora-user-images/image-20210826151300720.png" alt="image-20210826151300720" style="zoom:50%;" />

```js
    // 1.返回的是获取过来元素对象的集合，以为数组的形式存储的
    var lis = document.getElementsByTagName('li')
    console.log(lis);
    console.log(lis[0]);
    // 2.依次打印里面的元素对象可以采取遍历的方式
    for (var i = 0; i < lis.length; i++) {
        console.log(lis[i]);
    }

    // 3.如果页面中只有一个li，返回的还是为数组的形式
    // 4.如果页面中没有这个元素 返回的是空的伪数组  HTMLCollection [] length: 0
    // 5.element.getElementsByTagName('标签名');    父元素必须是指定的单个元素
    // var ol = document.getElementsByTagName('ol') //[ol]
    // console.log(ol[0].getElementsByTagName('li'));
    var ol = document.getElementById('ol'); // 起一个id名字，id是唯一的，找到单个元素ol
    console.log(ol.getElementsByTagName('li')); // 获取单个元素ol中所有指定标签名的子元素
```

<img src="/Users/aoki/Library/Application Support/typora-user-images/image-20210826151855664.png" alt="image-20210826151855664" style="zoom:50%;" />

### 2.4 通过 HTML5 新增的方法获取

```html
    <div class="box">1.盒子</div>
    <div class="box">2.盒子</div>
    <div id="nav">
        <ul>
            <li>首页</li>
            <li>产品</li>
        </ul>
    </div>
    <script>
        // 1. document.getElementsByClassName('类名'); 根据类名获取某些元素对象集合
        var boxs = document.getElementsByClassName('box');
        console.log(boxs);

        // 2. document.querySelector('选择器'); 根据指定选择器返回第一个元素对象  ⚠️切记里面的选择器名称需要加符号 .box #nav
        var firstBox = document.querySelector('.box'); // . 类选择器
        console.log(firstBox);
        var nav = document.querySelector('#nav'); // # id选择器
        console.log(nav);
        var li = document.querySelector('li');
        console.log(li);

        // 3. document.querySelectorAll('选择器'); 返回制定选择器的所有元素对象集合
        var allBox = document.querySelectorAll('.box');
        console.log(allBox);
        var lis = document.querySelectorAll('li')
        console.log(lis);
    </script>
```

<img src="/Users/aoki/Library/Application Support/typora-user-images/image-20210826163450278.png" alt="image-20210826163450278" style="zoom:50%;" />

### 2.5 获取特殊元素（body、html)

```js
        // 1.获取body元素   
        var bodyEle = document.body;
        console.log(bodyEle);
        console.dir(bodyEle);

        // 2.获取html元素
        var htmlEle = document.documentElement;
        console.log(htmlEle);
```

<img src="/Users/aoki/Library/Application Support/typora-user-images/image-20210826163947758.png" alt="image-20210826163947758" style="zoom:50%;" />

## 3.事件概述

### 3.1 事件概述

JS使我们有能力创建动态页面，而事件是可以被JS侦测到的行为。
网页中的每个元素都可以产生某些可以触发JS的事情，例如，用户点击某按钮时产生一个事件，然后去执行某些操作
触发—>响应机制

### 3.2 事件三要素

```js
        // 点击一个按钮，弹出对话框
        // 1.事件三部曲：事件源 事件类型 事件处理程序   也称为事件三要素
        // (1) 事件源 --> 事件被触发的对象   谁是按钮
        var btn = document.getElementById('btn');
        console.log(btn);
        // (2) 事件类型 如何触发什么事件 比如鼠标点击(onclick) 鼠标经过 键盘按下
        // (3) 事件处理程序 通过一个函数赋值的方式完成
        btn.onclick = function () {
            alert('❤️vv')
        }
```

###### 执行事件的步骤

1. 获取事件源
2. 注册事件（绑定事件）
3. 添加事件处理程序（采取函数赋值程序）

```html
    <div>123</div>
    <script>
        // 执行事件步骤
        // 点击div控制台输出 我被选中了
        // 1.获取事件源
        var div = document.querySelector('div');
        // 2.绑定事件 注册事件
        // div.onclick
        // 3.添加事件处理程序
        div.onclick = function () {
            console.log('我被选中了');
        }
    </script>
```

<img src="/Users/aoki/Library/Application Support/typora-user-images/image-20210826172316134.png" alt="image-20210826172316134" style="zoom:40%;" />

### 3.3常见鼠标事件

| 鼠标事件    | 触发条件         |
| ----------- | ---------------- |
| onclick     | 鼠标点击左键触发 |
| onmouseover | 鼠标经过触发     |
| onmouseout  | 鼠标离开触发     |
| onfocus     | 获得鼠标焦点触发 |
| onblur      | 失去鼠标焦点触发 |
| onmousemove | 鼠标移动触发     |
| onmouseup   | 鼠标弹起触发     |
| onmousedown | 鼠标按下触发     |

### 3.4 分析事件三要素

​	下拉菜单三要素
​	关闭广告三要素

## 4.操作元素

JS的DOM操作可以改变网页内容、结构和样式，可以利用DOM操作元素来改变元素里面的内容属性等。
注意以下都是属性

### 4.1 改变元素内容

```js
element.innerText
```

从起始位置到终止位置的内容，但它去除html标签，同时空格和换行也会去掉。

```js
element.innerHTML
```

从起始位置到终止位置的内容，包含html标签，同时保留空格和换行。

```html
    <button>显示当前系统时间</button>
    <div>某个时间</div>
    <p>abc</p>
    <script>
        // 点击按钮，div里面的的文字会发生变化
        // 1.获取元素
        var btn = document.querySelector('button');
        var div = document.querySelector('div');
        // 2.注册事件
        btn.onclick = function () {
            // div.innerText = '2021-8-26'
            div.innerText = getDate();
        }
        function getDate() {
            var date = new Date();
            console.log(date.getFullYear()); // 返回当前的年份 2021
            console.log(date.getMonth() + 1); // 月份 返回的月份小1个月，⚠️月份+1
            console.log(date.getDate()); // 返回日期
            console.log(date.getDay()); // 返回星期 周一返回-->1  周六-->6  周日-->0
            // 格式 2021年 8月 24日 星期二
            var year = date.getFullYear();
            var month = date.getMonth();
            var dates = date.getDate();
            var day = date.getDay();
            var arr = ['星期日', '星期一', '星期二', '星期三', '星期四', '星期五', '星期六'];
            return '今天是：' + year + '年' + month + '月' + dates + '日 ' + arr[day];
        }
        // 元素可以不用添加事件
        var p = document.querySelector('p');
        p.innerText = getDate();
    </script>
```

<img src="/Users/aoki/Library/Application Support/typora-user-images/image-20210826180103030.png" alt="image-20210826180103030" style="zoom:50%;" />

```html
    <div></div>
    <p>
        content
        <span>123</span>
    </p>
    <script>
        // 1. innerText 不识别HTML标签 非标准 去除空格和换行
        var div = document.querySelector('div');
        div.innerText = '<strong>今天是</strong>:2021年';
        // 2. innerHTML 识别html标签 W3C标准 保留空格和换行
        div.innerHTML = '<strong>今天是</strong>:2021年';
        // 这两个属性是可读写的 可以获取元素里面的内容
        var p = document.querySelector('p');
        console.log(p.innerText);
        console.log(p.innerHTML);
    </script>
```

<img src="/Users/aoki/Library/Application Support/typora-user-images/image-20210826195938401.png" alt="image-20210826195938401" style="zoom:30%;" />



### 4.2 常用元素的属性操作

1. innerText、innerHTML 改变元素内容
2. src、href
3. id、alt、title

```html
    <button id="ldh">刘德华</button>
    <button id="zxy">张学友</button> <br>
    <img src="images/ldh.jpg" alt="" title="刘德华">
    <script>
        // 修改元素属性 src
        // 1.获取元素
        var ldh = document.getElementById('ldh');
        var zxy = document.getElementById('zxy');
        var img = document.querySelector('img');
        // 2.注册事件
        zxy.onclick = function () {
            img.src = 'images/zxy.jpg';
            img.title = '张学友';
        }
        ldh.onclick = function () {
            img.src = 'images/ldh.jpg';
            img.title = '刘德华';
        }
    </script>
```

<img src="/Users/aoki/Library/Application Support/typora-user-images/image-20210826201229160.png" alt="image-20210826201229160" style="zoom:50%;" />

```js
        // 案例：分时显示不同图片，显示不同问候语
        // 1.根据系统不同时间来判断，需要用到日期内置对象
        // 2.利用多分支语句来设置不同的图片
        // 3.需要一个图片，并且根据事件修改图片，需要用到操作元素src属性
        // 4.需要一个div元素，显示不同问候语，修改元素内容即可

        // 1.获取元素
        var img = document.querySelector('img');
        var div = document.querySelector('div');
        // 2.得到当前小时数
        var date = new Date();
        var h = date.getHours();
        // 3.判断时间
        if (h < 12) {
            img.src = 'images/s.gif';
            div.innerHTML = '上午好呀~';
        } else if (h < 18) {
            img.src = 'images/x.gif';
            div.innerHTML = '下午好呀~';
        } else {
            img.src = 'images/w.gif';
            div.innerHTML = '晚上好呀~';
        }
```

<img src="/Users/aoki/Library/Application Support/typora-user-images/image-20210827094509355.png" alt="image-20210827094509355" style="zoom:50%;" />

### 4.3 表单元素的属性操作

​	利用 DOM 可以操作如下表单元素的属性：

```js
type、 value、checked、selected、disable
```

```html
    <button>Button</button>
    <input type="text" value="点击按钮">
    <script>
        // 1.获取元素
        var btn = document.querySelector('button');
        var input = document.querySelector('input');
        // 2.注册事件 处理程序
        btn.onclick = function () {
            // input.innerHTML = '点击了'; 这个对于普通盒子起作用，比如div标签里面的内容
            // 表单里面的值，文字内容是通过 value 来修改的
            input.value = '被点击了';
            // 如果想要某个表单被禁用了，不能再点击 disable，想要这个按钮 button禁用
            // btn.disabled = true;
            this.disabled = true;
            // this 指向的是事件函数的调用者btn
        }
    </script>
```

<img src="/Users/aoki/Library/Application Support/typora-user-images/image-20210827101035514.png" alt="image-20210827101035514" style="zoom:50%;" /><img src="/Users/aoki/Library/Application Support/typora-user-images/image-20210827101226394.png" alt="image-20210827101226394" style="zoom:30%;" />

#### 案例：显示密码

1. 核心思路：点击眼睛按钮，把密码框类型改为文本框就可以看见里面的密码
2. 一个按钮两个状态，点击一次，切换为文本框，继续点击一次切换为密码框
3. 算法：利用一个flag变量，来判断flag的值，如果是1就切换为文本框，flag设置为0，如果是0就切换为密码框，flag设置为1

```html
	<style>
        .box {
            position: relative;
            width: 300px;
            border-bottom: 1px solid #ccc;
            margin: 30px auto;
        }

        .box input {
            width: 270px;
            height: 30px;
            line-height: 30px;
            border: 0;
            outline: none;
        }

        .box img {
            position: absolute;
            top: 2px;
            right: 2px;
            width: 24px;
        }
    </style>
</head>

<body>
    <div class="box">
        <label for="">
            <img src="images/close.png" alt="" id="eye">
        </label>
        <input type="password" name="" id="pwd">
    </div>
    <script>
        // 1.获取元素
        var eye = document.getElementById('eye');
        var pwd = document.getElementById('pwd');
        // 2.注册事件 处理程序
        var flag = 0;
        eye.onclick = function () {
            // 点击一次之后，flag一定要发生变化
            if (flag == 0) {
                pwd.type = 'text';
                this.src = 'images/open.png';
                flag = 1; // 赋值操作
            } else {
                pwd.type = 'password';
                this.src = 'images/close.png';
                flag = 0;
            }
        }
    </script>
</body>
```

<img src="/Users/aoki/Library/Application Support/typora-user-images/image-20210827104621907.png" alt="image-20210827104621907" style="zoom:50%;" />

### 4.4样式属性操作

通过JS修改元素的大小、颜色、位置等样式

```js
1. element.style	行内样式操作
2. element.className   类名样式操作
```

⚠️：

1. JS里面的样式采取驼峰命名法，比如fontSize、backgroundColor
2. JS修改 style 样式操作，产生的是行内样式，JS修改的样式比CSS权重高

```html
    <style>
        div {
            width: 200px;
            height: 200px;
            background-color: #ccc;
        }
    </style>

    <div></div>
    <script>
        // 1. 获取元素
        var div = document.querySelector('div');
        // 2. 注册事件 处理程序
        div.onclick = function () {
          	// div.style 里面的属性 采取驼峰明法
            div.style.backgroundColor = '#999';
            div.style.width = '100px';
            div.style.height = '100px';
        }
    </script>
```

```html
    <style>
        .box {
            position: relative;
            width: 74px;
            height: 88px;
            border: 1px solid #ccc;
            margin: 100px auto;
            font-size: 12px;
            text-align: center;
            color: #f40;
        }

        .box img {
            width: 60px;
            margin-top: 5px;
        }

        .close-btn {
            position: absolute;
            top: -1px;
            left: -16px;
            width: 14px;
            height: 14px;
            line-height: 14px;
            border: 1px solid #ccc;
            font-family: Arial, Helvetica, sabns-serif;
            cursor: pointer;
        }
    </style>

    <div class="box">
        淘宝二维码
        <img src="images/tao.png" alt="">
        <i class="close-btn">x</i>
    </div>
    <script>
        // 案例关闭淘宝二维码
        // 1. 获取元素
        var btn = document.querySelector('.close-btn');
        var box = document.querySelector('.box');
        // 2. 注册事件 程序处理
        btn.onclick = function () {
            box.style.display = 'none';
        }
    </script>
```

<img src="/Users/aoki/Library/Application Support/typora-user-images/image-20210827124400365.png" alt="image-20210827124400365" style="zoom:30%;" />

###### 案例：循环精灵图背景

利用for循环，修改精灵图片的背景位置background-position

```html
    <style>
        * {
            margin: 0;
            padding: 0;
        }

        li {
            list-style-type: none;
        }

        .box {
            width: 250px;
            margin: 100px auto;
        }

        .box li {
            float: left;
            width: 24px;
            height: 24px;
            background-color: salmon;
            margin: 15px;
            background: url(images/sprite.png) no-repeat;
        }
    </style>

    <div class="box">
        <ul>
            <li></li>
            <li></li>
            <li></li>
            <li></li>
            <li></li>
            <li></li>
            <li></li>
            <li></li>
            <li></li>
            <li></li>
            <li></li>
            <li></li>
        </ul>
    </div>
    <script>
        // 案例关闭淘宝二维码
        // 1. 获取元素
        var lis = document.querySelectorAll('li');
        for (var i = 0; i < lis.length; i++) {
            // 让索引号 i * 44 就是每个li的背景y坐标 index是y坐标
            var index = i * 44;
            lis[i].style.backgroundPosition = '0 -' + index + 'px';
        }
    </script>
```

<img src="/Users/aoki/Library/Application Support/typora-user-images/image-20210827141736889.png" alt="image-20210827141736889" style="zoom:50%;" />

###### 案例：显示隐藏文本框内容

1. 首先表单需要两个新事件，获得焦点onfocus，失去焦点onblur
2. 如果获得焦点，判断表单里面内容是否为默认文字，如果是默认文字，就清空表单内容，改变文字颜色

```html
    <style>
        input {
            color: #999;
        }
    </style>

    <input type="text" value="手机">
    <script>
        // 1. 获取元素
        var text = document.querySelector('input');
        // 2.注册事件 获得焦点事件 onfocus
        text.onfocus = function () {
            // console.log('得到焦点');
            if (this.value === '手机') {
                this.value = '';
                // 获得焦点将文本框里的文字颜色变色
                this.style.color = 'salmon';
            }
        }
        // 3.注册事件 失去焦点事件 onblur
        text.onblur = function () {
            // console.log('失去焦点');
            if (this.value === '') {
                this.value = '手机';
                // 失去焦点将文本框里的文字颜色恢复
                this.style.color = '#999';
            }
        }
    </script>
```

<img src="/Users/aoki/Library/Application Support/typora-user-images/image-20210827144713605.png" alt="image-20210827144713605" style="zoom:50%;" /><img src="/Users/aoki/Library/Application Support/typora-user-images/image-20210827144727391.png" alt="image-20210827144727391" style="zoom:50%;" />

### 4.4 样式属性操作

```js
1. element.style	行内样式操作
2. element.className   类名样式操作
```

⚠️：

1. 如果样式修改较多，可以采取操作类名方式更改元素样式
2. class因为是保留字，因此使用className来操作元素类名属性
3. className会直接更改元素类名，会覆盖原先的类名

```html
    <style>
        .box {
            width: 200px;
            height: 200px;
            background-color: skyblue;
            color: thistle;
        }

        .change {
            width: 300px;
            height: 300px;
            margin-top: 100px;
            color: thistle;
            background-color: salmon;
        }
    </style>

    <div class="box">content</div>
    <script>
        // 1.使用 element.style 样式较少或者功能简单地情况下获得改变元素样式
        var text = document.querySelector('div');
        text.onclick = function () {
            // 2. 使用 element.className 更改元素样式，适用于样式较多或者功能复杂的情况
            // 3.如果想要保留原先的类名，可以用 多类名选择器
            // this.className = 'change';
            this.className = 'box change';
        }
    </script>
```

###### 案例：注册页面

```html
    <style>
        div {
            width: 600px;
            margin: 100px auto;
        }

        .message {
            display: inline-block;
            color: #ccc;
            font-size: 12px;
            padding-left: 20px;
            background: url(images/mess.png) no-repeat left center;
        }

        .wrong {
            color: red;
            background-image: url(images/wrong.png);
        }

        .right {
            color: green;
            background-image: url(images/right.png);
        }
    </style>

    <div class="register">
        <input type="password" class="ipt">
        <p class="message">请输入6~16位密码</p>
    </div>
    <script>
        // 1. 获取元素
        var ipt = document.querySelector('.ipt');
        var message = document.querySelector('.message');
        // 2.注册事件 失去焦点
        ipt.onblur = function () {
            // 根据表单里面值得长度 ipt.value.length
            if (this.value.length < 6 || this.value.length > 16) {
                message.className = 'message wrong';
                message.innerHTML = '您输入的密码格式不正确，请输入6~16位密码';
            } else {
                message.className = 'message right';
                message.innerHTML = '您输入的正确';
            }
        }
    </script>
```

<img src="/Users/aoki/Library/Application Support/typora-user-images/image-20210827161905862.png" alt="image-20210827161905862" style="zoom:50%;" />

```html
/* 开关灯案例 */
<body id="bg">
    <button class="btn">开关灯</button>
    <script>
        // 1.获取元素
        var btn = document.querySelector('.btn');
        // 2.注册事件
        var flag = 0;
        btn.onclick = function () {
            if (flag == 0) {
                bg.style.backgroundColor = 'salmon';
                flag = 1;
            } else {
                bg.style.backgroundColor = '#fff';
                flag = 0;
            }
        }
    </script>
</body>
```

<img src="/Users/aoki/Library/Application Support/typora-user-images/image-20210828112107198.png" alt="image-20210828112107198" style="zoom:50%;" />

###  4.5 排他思想

<img src="/Users/aoki/Library/Application Support/typora-user-images/image-20210830085530721.png" alt="image-20210830085530721" style="zoom:50%;" />

如果有同一组元素，想要某一个元素实现某种样式，需要用到循环的排他思想算法：

1. 所有元素全部清除样式(干掉其他人)
2. 给当前元素设置样式(留下我自己)
3. 注意顺序不能颠倒，首先干掉其他人，在设置自己

```html
    <button>1</button>
    <button>2</button>
    <button>3</button>
    <button>4</button>
    <button>5</button>
    <script>
        // 1. 获取所有按钮元素
        var btns = document.getElementsByTagName('button');
        // btns得到的是伪数组，里面的每一个元素 btns[i]
        // 2. 注册事件
        for (var i = 0; i < btns.length; i++) {
            btns[i].onclick = function () {
                // (1) 先把所有的按钮背景颜色去掉
                for (var i = 0; i < btns.length; i++) {
                    btns[i].style.backgroundColor = '';
                }
                // (2) 然后才放当前元素背景颜色为blue
                this.style.backgroundColor = 'blue';
            }
        }
    </script>
```

###### 案例：换肤

```html
    <style>
        * {
            margin: 0;
            padding: 0;
        }

        body {
            background: url(images/1.jpg) no-repeat center top;
        }

        li {
            list-style: none;
        }

        .baidu {
            overflow: hidden;
            margin: 100px auto;
            background-color: #fff;
            width: 410px;
            padding-top: 5px;
        }

        .baidu li {
            float: left;
            margin: 0 1px;
            cursor: pointer;
        }

        .baidu img {
            width: 100px;
        }
    </style>
</head>

<body>
    <ul class="baidu">
        <li><img src="images/1.jpg" alt=""></li>
        <li><img src="images/2.jpg" alt=""></li>
        <li><img src="images/3.jpg" alt=""></li>
        <li><img src="images/4.jpg" alt=""></li>
    </ul>
    <script>
        // 1. 获取元素
        var imgs = document.querySelector('.baidu').querySelectorAll('img');
        console.log(imgs);
        for (var i = 0; i < imgs.length; i++) {
            imgs[i].onclick = function () {
                // this.srcn 是点击图片的路径
                // console.log(this.src);
                // 把这个路径 this.src 给 body
                document.body.style.backgroundImage = 'url(' + this.src + ')';
            }
        }
    </script>
</body>
```

<img src="/Users/aoki/Library/Application Support/typora-user-images/image-20210830100324092.png" alt="image-20210830100324092" style="zoom:20%;" />

###### 案例：表格隔行案例

```html
    <style>
        table {
            width: 800px;
            margin: 100px auto;
            text-align: center;
            border-collapse: collapse;
            font-size: 14px;
        }

        thead tr {
            height: 30px;
            background-color: skyblue;
            color: seashell;
        }

        tbody tr {
            height: 30px;
        }

        tbody td {
            border-bottom: 1px solid #d7d7d7;
            font-size: 12px;
            color: sandybrown;
        }

        .bg {
            background-color: salmon;
        }
    </style>
</head>

<body>
    <table>
        <thead>
            <tr>
                <th>代码</th>
                <th>名称</th>
                <th>最新公布净值</th>
                <th>累计净值</th>
                <th>前单位净值</th>
                <th>净值增长率</th>
            </tr>
        </thead>
        <tbody>
            <tr>
                <td>003526</td>
                <td>农银金穗3个月定期开放债券</td>
                <td>1.075</td>
                <td>1.079</td>
                <td>1.074</td>
                <td>+0.047%</td>
            </tr>
            <tr>
                <td>003526</td>
                <td>农银金穗3个月定期开放债券</td>
                <td>1.075</td>
                <td>1.079</td>
                <td>1.074</td>
                <td>+0.047%</td>
            </tr>
            <tr>
                <td>003526</td>
                <td>农银金穗3个月定期开放债券</td>
                <td>1.075</td>
                <td>1.079</td>
                <td>1.074</td>
                <td>+0.047%</td>
            </tr>
            <tr>
                <td>003526</td>
                <td>农银金穗3个月定期开放债券</td>
                <td>1.075</td>
                <td>1.079</td>
                <td>1.074</td>
                <td>+0.047%</td>
            </tr>
            <tr>
                <td>003526</td>
                <td>农银金穗3个月定期开放债券</td>
                <td>1.075</td>
                <td>1.079</td>
                <td>1.074</td>
                <td>+0.047%</td>
            </tr>
            <tr>
                <td>003526</td>
                <td>农银金穗3个月定期开放债券</td>
                <td>1.075</td>
                <td>1.079</td>
                <td>1.074</td>
                <td>+0.047%</td>
            </tr>
        </tbody>
    </table>
    <script>
        // 1. 获取元素 获取的是 tbody 里面所有的行
        var trs = document.querySelector('tbody').querySelectorAll('tr');
        // 2. 利用循环绑定事件
        for (var i = 0; i < trs.length; i++) {
            // 3. 鼠标经过事件 onmouseover
            trs[i].onmouseover = function () {
                // console.log(11);  检测
                this.className = 'bg';
            }
            // 4. 鼠标离开事件 onmouseout 
            trs[i].onmouseout = function () {
                this.className = '';
            }
        }
    </script>
```

<img src="/Users/aoki/Library/Application Support/typora-user-images/image-20210830104626130.png" alt="image-20210830104626130" style="zoom:20%;" />

###### 案例：表单全选反选

```html
    <style>
        * {
            padding: 0;
            margin: 0;
        }

        .wrap {
            width: 300px;
            margin: 100px auto 0;
        }

        table {
            border-collapse: collapse;
            border-spacing: 0;
            border: 1px solid #c0c0c0;
            width: 300px;
        }

        th,
        td {
            border: 1px solid #d0d0d0;
            color: #404060;
            padding: 10px;
        }

        th {
            background-color: #09c;
            font: bold 16px "微软雅黑";
            color: #fff;
        }

        td {
            font: 14px "微软雅黑";
        }

        tbody tr {
            background-color: #f0f0f0;
        }

        tbody tr:hover {
            cursor: pointer;
            background-color: #fafafa;
        }
    </style>
</head>

<body>
    <div class="wrap">
        <table>
            <thead>
                <tr>
                    <th>
                        <input type="checkbox" id="j_cbAll" />
                    </th>
                    <th>商品</th>
                    <th>价钱</th>
                </tr>
            </thead>
            <tbody id="j_tb">
                <tr>
                    <td>
                        <input type="checkbox" />
                    </td>
                    <td>iPhone8</td>
                    <td>8000</td>
                </tr>
                <tr>
                    <td>
                        <input type="checkbox" />
                    </td>
                    <td>iPad Pro</td>
                    <td>5000</td>
                </tr>
                <tr>
                    <td>
                        <input type="checkbox" />
                    </td>
                    <td>iPad Air</td>
                    <td>2000</td>
                </tr>
                <tr>
                    <td>
                        <input type="checkbox" />
                    </td>
                    <td>Apple Watch</td>
                    <td>2000</td>
                </tr>

            </tbody>
        </table>
    </div>
    <script>
        // 1. 全选和取消全选的做法：让下面所有复选框的checked属性（选中状态）跟随全选按钮
        // 获取元素
        var j_cbAll = document.getElementById('j_cbAll');
        var j_tbs = document.getElementById('j_tb').getElementsByTagName('input');
        // 注册事件
        j_cbAll.onclick = function () {
            // console.log(this.checked); 可以的得到当前复选框的选中状态如果是true就是选中，如果是false就是未选中
            for (var i = 0; i < j_tbs.length; i++) {
                j_tbs[i].checked = j_cbAll.checked;
            }
        }
              
      // 2. 下面复选框需要全部选中， 上面全选才能选中做法： 给下面所有复选框绑定点击事件，每次点击，都要循环查看下面所有的复选框是否有没选中的，如果有一个没选中的， 上面全选就不选中。
        for (var i = 0; i < j_tb.length; i++) { // (1)第一个for循环 给4个元素添加点击绑定事件的for循环
            j_tb[i].onclick = function () {
                // flag 控制全选按钮是否选中
                var flag = true;
                // 每次点击下面的复选框都要循环检查4个按钮是否全部选中
                for (var i = 0; i < j_tb.length; i++) {
                    if (!j_tb[i].checked) { // 非checked-->没有被选中 
                        flag = false; // 取反
                        break; // 退出for循环，提高执行效率。因为只要有一个没被选中，剩下的就无须循环判断
                    }
                }
                j_cbAll.checked = flag;
            }
        }
    </script>
</body>
```

<img src="/Users/aoki/Library/Application Support/typora-user-images/image-20210830120505985.png" alt="image-20210830120505985" style="zoom:25%;" />

### 4.6 自定义属性的操作

#### 1.获取属性值

+  element.属性   获取属性值 –> 获取内置属性值（元素本身自带的属性）
+ element.getAttribute(‘属性’); –> 主要获得自定义属性（标准），程序员自定义的属性

```html
    <div id="demo" index="1"></div>
    <script>
        var div = document.querySelector('div');
        // 1. 获取元素的属性值
        // (1) element.属性
        console.log(div.id);
        // (2) element.getAttribute('属性') get-->得到属性 Attribute-->属性，程序员自己添加属性称为自定义属性-->index
        console.log(div.getAttribute('id'));
        console.log(div.getAttribute('index'));
    </script>
```

<img src="/Users/aoki/Library/Application Support/typora-user-images/image-20210830122307978.png" alt="image-20210830122307978" style="zoom:50%;" />

#### 2.设置属性值

+ element.属性 = ‘值’	设置内置属性值
+ element.setAttribute(‘属性’,‘值’);

```js
       // 2.设置属性值
        // (1) element.属性='值';
        div.id = 'test';
        div.className = 'navs';
        // (2) element.setAttribute('属性','值'); 主要针对于自定义属性
        div.setAttribute('index', 2);
        div, setAttribute('class', 'footer'); // class 特殊，写的是class，不是className
```

#### 3.移除属性

+ element.removeAttribute(‘属性’);

  ```js
          // 3.移除属性 removeAttribute('属性');
          div.removeAttribute('index');
  ```

###### 案例：tab栏切换（重点案例）

当鼠标点击上面对应的选项卡（tab），下面的内容跟随变化

<img src="/Users/aoki/Library/Application Support/typora-user-images/image-20210830134749733.png" alt="image-20210830134749733" style="zoom:50%;" /><img src="/Users/aoki/Library/Application Support/typora-user-images/image-20210830140807139.png" alt="image-20210830140807139" style="zoom:30%;" />

```html
    <style>
        * {
            margin: 0;
            padding: 0;
        }

        li {
            list-style-type: none;
        }

        .tab {
            width: 978px;
            margin: 100px auto;
        }

        .tab_list {
            height: 39px;
            border: 1px solid #ccc;
            background-color: #f1f1f1;
        }

        .tab_list li {
            float: left;
            height: 39px;
            line-height: 39px;
            padding: 0 20px;
            text-align: center;
            cursor: pointer;
        }

        .tab_list .current {
            background-color: #c81623;
            color: #fff;
        }

        .item_info {
            padding: 20px 0 0 20px;
        }

        .item {
            display: none;
        }
    </style>
</head>

<body>
    <div class="tab">
        <div class="tab_list">
            <ul>
                <li class="current">商品介绍</li>
                <li>规格与包装</li>
                <li>售后保障</li>
                <li>商品评价（50000）</li>
                <li>手机社区</li>
            </ul>
        </div>
        <div class="tab_con">
            <div class="item" style="display: block;">
                商品介绍模块内容
            </div>
            <div class="item">
                规格与包装模块内容
            </div>
            <div class="item">
                售后保障模块内容
            </div>
            <div class="item">
                商品评价（50000）模块内容
            </div>
            <div class="item">
                手机社区模块内容
            </div>
        </div>
    </div>
    <script>
        // 1.tab_list 点击当前模块变红，其他不变
        // 获取元素
        var tab_list = document.querySelector('.tab_list');
        var lis = tab_list.querySelectorAll('li');
        var items = document.querySelectorAll('.item');
        // for循环绑定点击事件
        for (var i = 0; i < lis.length; i++) {
            lis[i].setAttribute('index', i);
            lis[i].onclick = function () {
                for (var i = 0; i < lis.length; i++) {
                    // 干掉其他人 其余的li清楚class这个类
                    lis[i].className = '';
                }
                // 留下自己
                this.className = 'current';
                // 2.下面显示内容
                var index = this.getAttribute('index');
                console.log(index);
                // 让其与item 这些div隐藏
                for (var i = 0; i < items.length; i++) {
                    items[i].style.display = 'none';
                }
                // 留下自己 让对应的item 显示出来
                items[index].style.display = 'block';
            }
        }
    </script>
```

### 4.7 H5自定义属性

**自定义属性的目的：为了保存并使用数据。有些数据可以保存到页面中而不用保存到数据库中**

自定义属性获取是通过getAttribute（‘属性’）获取。
但是有些自定义属性很容易歧义，不容易判断是元素的内置属性还是自定义属性。

#### 1.设置H5自定义属性

H5规定自定义属性data-开头作为属性名并且赋值。

```html
    <div data-index="1"></div>
    JS：
		element.setAttribute('data-index', 2);
```

#### 2.获取H5自定义属性

1. 兼容性获取：element.getAttribute(‘data-index’);
2. H5新增 element.dataset.index 或者 element.dataset[‘index’] IE11才开始支持

```html
    <div data-index="99" getTime="10" data-list-name="Lee"></div>
    <script>
        var div = document.querySelector('div');
        console.log(div.getAttribute('getTime'));
        div.setAttribute('data-time', 20)
        console.log(div.getAttribute('data-index'));
        console.log(div.getAttribute('data-list-name'));
        // H5新增的获取自定义属性方法，只能获取data - 开头
        // dataset是一个集合里面存放了所有以data开头的自定义属性
        console.log(div.dataset);
        console.log(div.dataset.index);
        console.log(div.dataset['index']);
        // 如果自定义属性里面多个-链接单词，获取的时候采取 驼峰命名法
        console.log(div.dataset.listName);
        console.log(div.dataset['listName']);
    </script>
```

<img src="/Users/aoki/Library/Application Support/typora-user-images/image-20210830155521606.png" alt="image-20210830155521606" style="zoom:40%;" />

## 5.节点操作

### 5.1为什么学节点操作

获取元素通常使用两种方法：

##### 1.利用DOM提供的方法获取元素

+ document.getElementById()
+ document.getElementsByTagName()
+ document.querySelector等
+ 逻辑性不强、较为繁琐

##### 2.利用节点层级关系

+ 利用父子兄节点关系获取元素
+ 逻辑性强，兼容性差

### 5.2节点概述

网页中所有内容都是节点（标签、属性、文本、注释等）DOM中，节点使用node来表示。
HTML DOM树中的所有节点均可通过JS进行访问，所有HTML元素（节点）均可被修改，也可以创建或删除。

+ nodeType(节点类型)

+ nodeName(节点名称)

+ nodeValue(节点值)

  元素节点 nodeType –> 1

  属性节点 nodeType –> 2

  文本节点 nodeType –> 3 (文本节点包含文字、空格、换行等)

**实际开发中，节点操作主要操作的是元素节点**

### 5.3节点层级

利用DOM树可以把节点划分为不同层级关系，常见的是父子兄层级关系。

#### 1.父级节点

```js
node.parentNode
```

+ parentNode属性可返回某节点的父节点，注意事项最近的一个父节点
+ 如果指定的节点没有父节点则返回null

```html
    <div class="demo">
        <div class="box">
            <span class="erweima">x</span>
        </div>
    </div>
    <script>
        // 1. 父节点 parentNode
        var erweima = document.querySelector('.erweima');
        // var box = document.querySelector('.box')
        // 得到的是离元素最近的父级节点（亲爸爸）,如果找不到父节点就返回为null
        console.log(erweima.parentNode);
```

#### 2.子节点

```js
1. 子节点 parentNode.childNodes(标准)
```

parentNode.childNodes 返回包含指定节点的子节点的集合，该集合为及时更新的集合。

⚠️：返回值里面包含所有的子节点，含括元素节点，文本节点等。
如果只想要获得里面的元素节点，则需要专门处理。一般不适用childNodes

```html
    <ul>
        <li>我是li</li>
        <li>我是li</li>
        <li>我是li</li>
        <li>我是li</li>
    </ul>
    <script>
				var ul = document.querySelector('ul');
        for (var i = 0; i < ul.childNodes.length; i++) {
            if (ul.childNodes[i].nodeType == 1) {
                // ul.childNodes[i] 是元素节点
                console.log(ul.childNodes[i]);
            }
        }
		 </script>
```

<img src="/Users/aoki/Library/Application Support/typora-user-images/image-20210831085230146.png" alt="image-20210831085230146" style="zoom:50%;" />

```js
2.parentNode.children (非标准) // 推荐使用该方法
```

parentNode.children 是一个只读属性，返回所有的子元素节点。它只返回子元素节点，其余节点不返回（重点）。
得到各个浏览器的支持。

```html
    <ul>
        <li>我是li</li>
        <li>我是li</li>
        <li>我是li</li>
        <li>我是li</li>
    </ul>      
    <script>
// 2. parentNode.children (非标准) 获取所有的子元素节点
        var ul = document.querySelector('ul');
        console.log(ul.children);
		</script>
```

<img src="/Users/aoki/Library/Application Support/typora-user-images/image-20210831085620895.png" alt="image-20210831085620895" style="zoom:50%;" />

```js
3.parentNode.firstChild
4.parentNode.lastChild
```

firstChild 返回第一个子节点，找不到则返回null。同样，也是包含所有的节点。

```js
5.parentNode.firstElementChild
6.parentNode.lastElementChild
```

firstElementChild返回第一个子元素加点，找不到则返回null。⚠️：you兼容性问题，IE9以上支持。

```js
// 3.实际开发写法 既没有兼容性问题又返回第一个子元素(重点)
7.parentNode.children[0]
8.parentNode.children[parentNode.children.length - 1]
```

```html
    <ol>
        <li>我是li1</li>
        <li>我是li2</li>
        <li>我是li3</li>
        <li>我是li4</li>
        <li>我是li5</li>
    </ol>

    <script>
        var ol = document.querySelector('ol');
        // 1. firstChild 第一个子节点，不管是文本节点还是元素节点
        console.log(ol.firstChild); // #text
        console.log(ol.lastChild);
        // 2. firstElementChild 返回第一个子元素节点，IE9以上
        console.log(ol.firstElementChild);
        console.log(ol.lastElementChild);
        // 3.实际开发写法 既没有兼容性问题又返回第一个子元素
        console.log(ol.children[0]);
        console.log(ol.children[ol.children.length - 1]);
    </script>
```

<img src="/Users/aoki/Library/Application Support/typora-user-images/image-20210831091139528.png" alt="image-20210831091139528" style="zoom:40%;" />

###### 案例：下拉菜单

1. 导航栏里面的li都要有鼠标经过效果，所以需要循环注册鼠标事件
2. 核心原理：当鼠标经过li里面的第二个孩子ul显示，当鼠标离开，则ul隐藏

```html
    <style>
        * {
            margin: 0;
            padding: 0;
        }

        li {
            list-style-type: none;
        }

        a {
            text-decoration: none;
            font-size: 14px;
        }

        .nav {
            margin: 100px;
        }

        .nav>li {
            position: relative;
            float: left;
            width: 80px;
            height: 41px;
            text-align: center;
        }

        .nav li a {
            display: block;
            width: 100%;
            height: 100%;
            line-height: 41px;
            color: #333;
        }

        .nav>li>a:hover {
            background-color: #eee;
        }

        .nav ul {
            display: none;
            position: absolute;
            top: 41px;
            left: 0;
            width: 100%;
            border-left: 1px solid #FECC5B;
            border-right: 1px solid #FECC5B;
        }

        .nav ul li {
            border-bottom: 1px solid #FECC5B;
        }

        .nav ul li a:hover {
            background-color: #FFF5DA;
        }
    </style>
</head>

<body>
    <ul class="nav">
        <li>
            <a href="#">微博</a>
            <ul>
                <li>
                    <a href="">私信</a>
                </li>
                <li>
                    <a href="">评论</a>
                </li>
                <li>
                    <a href="">@我</a>
                </li>
            </ul>
        </li>
        <li>
            <a href="#">微博</a>
            <ul>
                <li>
                    <a href="">私信</a>
                </li>
                <li>
                    <a href="">评论</a>
                </li>
                <li>
                    <a href="">@我</a>
                </li>
            </ul>
        </li>
        <li>
            <a href="#">微博</a>
            <ul>
                <li>
                    <a href="">私信</a>
                </li>
                <li>
                    <a href="">评论</a>
                </li>
                <li>
                    <a href="">@我</a>
                </li>
            </ul>
        </li>
        <li>
            <a href="#">微博</a>
            <ul>
                <li>
                    <a href="">私信</a>
                </li>
                <li>
                    <a href="">评论</a>
                </li>
                <li>
                    <a href="">@我</a>
                </li>
            </ul>
        </li>
    </ul>
    <script>
        var nav = document.querySelector('.nav');
        var lis = nav.children;
        for (var i = 0; i < lis.length; i++) {
            lis[i].onmouseover = function () {
                this.children[1].style.display = 'block';
            }
            lis[i].onmouseout = function () {
                this.children[1].style.display = 'none';
            }
        }
    </script>
</body>
```

<img src="/Users/aoki/Library/Application Support/typora-user-images/image-20210831100757740.png" alt="image-20210831100757740" style="zoom:40%;" />

#### 3. 节点层级

```js
1.node.nextSibling
2.node.previousSibling
3.node.nextElementSibling
4.node.previousSibling
```

```html
    <div>我是div</div>
    <span>我是span</span>
    <script>
        var div = document.querySelector('div');
        // 1. nextSibling 下一个兄弟节点，包含元素节点或者文本节点等
        console.log(div.nextSibling);
        console.log(div.previousSibling);
        // 2. nextElementSibling 下一个兄弟元素节点，找不到则返回null， 兼容问题IE9以上支持
        console.log(div.nextElementSibling); // 返回当前元素下一个兄弟节点
        console.log(div.previousElementSibling); // 返回当前元素上一个兄弟节点
        // 解决兼容性问题，封装一个兼容性函数
        function getNextElementSibling(element) {
            var el = element;
            while (el = el.nextSibling) {
                if (el.nodeType === 1) {
                    return el;
                }
            }
            return null;
        }
    </script>
```

### 5.4 创建节点

```js
document.creatElement('tagName')
```

document.creatElement()方法创建由tagName指定的HTML元素。 因为这些元素原先不存在，是根据需求动态生成的，也称为动态创建元素节点。

### 5.4 添加节点

```js
1. node.appendChild(child) // 常用
```

node.appendChild() 方法将一个节点添加到指定父节点的子节点列表末尾。类似于CSS里面的after伪元素。

```js
2.node.insertBefore(child, 指定元素)
```

node.insertBefore() 方法将一个节点添加到父节点的指定子节点前面。类似于CSS里面的before伪元素。

```html
    <ul>
        <li>123</li>
    </ul>
    <script>
        // 1. 创建节点 元素节点
        var li = document.createElement('li');
        // 2. 添加节点 node.appendChild(child) node-->父级  child-->子级,后面追加元素，类似于push
        var ul = document.querySelector('ul');
        ul.appendChild(li);
        // 3. node.insertBefor(child, 指定元素);
        var lili = document.createElement('li');
        ul.insertBefore(lili, ul.children[0]);
        // 4. 页面添加一个新的元素： 1. 创建元素    2. 添加元素
    </script>
```

<img src="/Users/aoki/Library/Application Support/typora-user-images/image-20210831105251891.png" alt="image-20210831105251891" style="zoom:50%;" />

###### 案例：发布留言

1. 核心思路：点击按钮之后，动态创建一个li，添加到ul里面
2. 创建li的同时，把文本域里面的值通过li.innerHTML赋值给li
3. 如果想要新的留言后面显示就用appendChild，如果想要前面显示就用insertBefore

```html
    <style>
        * {
            margin: 0;
            padding: 0;
        }

        body {
            margin: 100px 100px;
        }

        textarea {
            width: 200px;
            height: 100px;
            border: 1px solid skyblue;
            outline: none;
        }

        ul {
            margin-top: 20px;
        }

        li {
            width: 300px;
            padding: 5px;
            background-color: #ccc;
            color: slateblue;
            font-size: 14px;
            list-style: none;
            margin: 10px 0;
        }
    </style>
</head>

<body>
    <textarea name="" id="" cols="30" rows="10"></textarea>
    <button>发布</button>
    <ul>

    </ul>
    <script>
        // 1. 获取元素
        var text = document.querySelector('textarea');
        var btn = document.querySelector('button');
        var ul = document.querySelector('ul');
        // 2. 注册事件
        btn.onclick = function () {
            if (text.value == '') {
                alert('没有输入内容')
                return false;
            } else {
                // (1) 创建元素
                var li = document.createElement('li');
                // 现有li才能赋值
                li.innerHTML = text.value;
                // (2) 添加元素
                ul.appendChild(li); // 正序 先来后到
                ul.insertBefore(li, ul.children[0]); // 倒叙 后来者居上
            }
        }
    </script>
</body>
```

<img src="/Users/aoki/Library/Application Support/typora-user-images/image-20210831112307050.png" alt="image-20210831112307050" style="zoom:40%;" />

### 5.5 删除节点

```js
node.removeChild(child)
```

node.removeChild() 方法从DOM中删除一个子节点，返回删除的节点。

```html
    <button>删除</button>
    <ul>
        <li>章鱼哥</li>
        <li>派大星</li>
        <li>海绵宝宝</li>
    </ul>
    <script>
        // 1. 获取元素
        var ul = document.querySelector('ul');
        var btn = document.querySelector('button');
        // 2. 删除元素 node.removeChild(child)
        // ul.removeChild(ul.children[0]);
        // 3. 点击按钮依次删除里面的孩子
        btn.onclick = function () {
            if (ul.children.length == 0) {
                this.disabled = true; // 不可用; 后台读值会不能读取。
            } else {
                ul.removeChild(ul.children[0]);
            }
        }
    </script>
```

<img src="/Users/aoki/Library/Application Support/typora-user-images/image-20210831113303565.png" alt="image-20210831113303565" style="zoom:50%;" />

###### 案例：删除留言

1. 文本域里面的值赋值给li的时候，多添加一个删除的链接
2. 需要把所有的链接获取过来，当我们点击当前的链接的时候，删除当前链接所在的li
3. 阻止链接跳转需要添加 javascript:void(0); 或者 javascript:;

<img src="/Users/aoki/Library/Application Support/typora-user-images/image-20210831121903534.png" alt="image-20210831121903534" style="zoom:40%;" />

```html
    <style>
        * {
            margin: 0;
            padding: 0;
        }

        body {
            margin: 100px 100px;
        }

        textarea {
            width: 200px;
            height: 100px;
            border: 1px solid skyblue;
            outline: none;
        }

        ul {
            margin-top: 20px;
        }

        li {
            width: 300px;
            padding: 5px;
            background-color: #ccc;
            color: slateblue;
            font-size: 14px;
            list-style: none;
            margin: 10px 0;
        }

        li a {
            float: right;
        }
    </style>
</head>

<body>
    <textarea name="" id="" cols="30" rows="10"></textarea>
    <button>发布</button>
    <ul>

    </ul>
    <script>
        // 1. 获取元素
        var text = document.querySelector('textarea');
        var btn = document.querySelector('button');
        var ul = document.querySelector('ul');
        // 2. 注册事件
        btn.onclick = function () {
            if (text.value == '') {
                alert('没有输入内容')
                return false;
            } else {
                // (1) 创建元素
                var li = document.createElement('li');
                // 现有li才能赋值
                li.innerHTML = text.value + "<a href='javascript:;'>删除</a>";
                // (2) 添加元素
                ul.appendChild(li); // 正序 先来后到
                ul.insertBefore(li, ul.children[0]); // 倒叙 后来者居上
                // (3) 删除元素 删除的是当前连接的li a的父级是li
                var as = document.querySelectorAll('a');
                for (var i = 0; i < as.length; i++) {
                    as[i].onclick = function () {
                        // node.removeChild(child); 删除的当前a所在的li（a的父级是li） this.parentNode;
                        ul.removeChild(this.parentNode);
                    }
                }
            }
        }
    </script>
```

### 5.6 复制节点（克隆节点）

```
node.cloneNode()
```

node.cloneNode()方法返回调用该方法的节点的一个副本。也称为克隆节点/拷贝节点

1. 如果括号参数为空或者为false，则为浅拷贝，即只克隆复制节点本身，不克隆里面的子节点
2. 如果括号参数为true，则是深拷贝，会复制节点本身以及里面所有的子节点

```html
    <ul>
        <li>章鱼哥111</li>
        <li>派大星</li>
        <li>海绵宝宝</li>
    </ul>
    <script>
        var ul = document.querySelector('ul');
        // 1. node.cloneNode(); 括号为空/false --> 浅拷贝，只复制标签不复制里面的内容
        // 2. node.cloneNode(); 括号为true --> 深拷贝，复制标签复制里面的内容
        var lili = ul.children[0].cloneNode();
        var lili = ul.children[0].cloneNode(true);
        ul.appendChild(lili);
    </script>
```

<img src="/Users/aoki/Library/Application Support/typora-user-images/image-20210831123513254.png" alt="image-20210831123513254" style="zoom:50%;" />

###### 案例：动态生成表格

1. 数据是动态的，需要js动态生成。模拟数据，自定义数据。数据采取对象形式存储。
2. 所有数据都放在tbody里的行里面
3. 行很多，需要循环创建多少个行（多少人）
4. 每个行里面又有很多单元格（对应里面的数据），还继续使用循环创建多个单元格，并且把数据存入里面（双重for循环）
5. 最后一列单元格是删除，需要单独创建单元格

```html
    <style>
        a {
            color: slateblue;
            text-decoration: none;
        }

        a:hover {
            text-decoration: slateblue wavy underline;
        }

        table {
            width: 500px;
            margin: 100px auto;
            border-collapse: collapse;
            text-align: center;
        }

        td,
        th {
            height: 30px;
            border: 1px solid slateblue;
        }

        thead tr {
            height: 40px;
            background-color: skyblue;
        }
    </style>
</head>

<body>
    <table cellspacing="0">
        <thead>
            <tr>
                <th>姓名</th>
                <th>科目</th>
                <th>成绩</th>
                <th>操作</th>
            </tr>
        </thead>
        <tbody>
        </tbody>
    </table>
    <script>
        // 1. 准备学生数据
        var datas = [{
            name: 'Lee',
            subject: 'JavaScript',
            score: 100,
        }, {
            name: 'vv',
            subject: 'JavaScript',
            score: 101,
        }, {
            name: '小李',
            subject: 'JavaScript',
            score: 99,
        }, {
            name: 'see',
            subject: 'JavaScript',
            score: 90,
        },];
        // 2. tbody里面创建行： 有几个人（通过数组的长度）就创建几行
        var tbody = document.querySelector('tbody');
        for (var i = 0; i < datas.length; i++) { // 外面的for循环管行 tr
            // 1. 创建tr行
            var tr = document.createElement('tr');
            tbody.appendChild(tr);
            // 2. 行里面创建单元格(和数据有关系的3个单元格) td 单元格的数量取决于每个对象里面的属性个数 for循环遍历对象-->datas[i]
            for (var k in datas[i]) { // 里面的for循环管列 td
                // 创建单元格
                var td = document.createElement('td');
                // 把对象里面的属性值 datas[i][k]给 td
                td.innerHTML = datas[i][k];
                tr.appendChild(td);
            }
            // 3. 创建-->删除 单元格
            var td = document.createElement('td');
            td.innerHTML = '<a href="javascript:;">删除</a>';
            tr.appendChild(td);
            // for (var k in obj){
            //     k 得到的是属性名
            //     obj[k] 得到的是属性值
            // }
        }
        // 4. 删除操作
        var as = document.querySelectorAll('a');
        for (var i = 0; i < as.length; i++) {
            as[i].onclick = function () {
                // 点击a删除，当前a所在的行（链接爸爸的爸爸） a-->td-->tr-->tbody(node) 所在行 node.removeChild(child)
                tbody.removeChild(this.parentNode.parentNode);
            }
        }
    </script>
</body>
```

<img src="/Users/aoki/Library/Application Support/typora-user-images/image-20210831153211484.png" alt="image-20210831153211484" style="zoom:30%;" />

### 5.8 **三种创建元素区别**
+   document.write()
+   element.innerHTML
+   document.createElement()
区别：
1. document.write 是直接将内容写入页面的内容流，但是文档流执行完毕，则会导致页面全部重绘

2. innerHTML 是将内容写入某个DOM节点，不会导致页面全部重绘

3. innerHTML 创建多个元素效率更高（不要拼接字符串，采取数组形式拼接），结构稍微复杂

4. createElement() 创建多个元素效率低，但结构清晰

   **不同浏览器下，innerHTML效率比 createElement高**

```html
    <button>click</button>
    <p>ABC</p>
    <div class="inner"></div>
    <div class="create"></div>
    <script>
        // 1. document.write() 创建元素 如果页面文档流加载完毕，再调用会导致页面重绘
        // var btn = document.querySelector('button');
        // btn.onclick = function () {
        //     document.write('<div>123</div>');
        // }

        // 2. innerHTML 创建元素
        var inner = document.querySelector('.inner')
        // inner.innerHTML = '<a href="javascript:;">Google</a>';
       	// for (var i = 0; i <= 100; i++) {
       	//   inner.innerHTML += '<a href="#">Google</a>';
       	// }
        var arr = []; // 数组追加
        for (var i = 0; i <= 100; i++) {
            arr.push('<a href="#">Google</a>');
        }
        inner.innerHTML = arr.join('');

        // 3.document.createElement() 创建元素
        var creat = document.querySelector('.create');
        // var a = document.createElement('a');
        // creat.appendChild(a);
        for (var i = 0; i <= 100; i++) {
            var a = document.createElement('a');
            creat.appendChild(a);
        }
    </script>
```



















































