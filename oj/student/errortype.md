### 答案正确 （Acepted， AC）

恭喜你！所提交的代码通过了数据！这个评测结果应该是大家最喜欢见到的，也非常好理解。如果是单点测试，那么通过一组数据，就会返回一个`Accepted`；如果是多点测试，那么只有当通过了所有数据时，才会返回`Accepted`。  
分以下三种情况

* ![](/images/oj/student/ac.png) 你的答案可能是第一个提交，或你提交的代码与别人的没有相似之处
* ![](/images/oj/student/ac1.png) 你提交的代码与提交ID为`102081` 完全一样
* ![](/images/oj/student/ac2.png) 你提交的代码与提交ID为`97347` 有`95%` 相似

### 格式错误 （Presentation Error，PE）

**原因：**输出结果行末没有_换行_或_有多余换行_以及_行末有空格_均算格式错误！

* ![](/images/oj/student/format.png)

  #### 一行上输出58示例：

  对于PASCAL来说，要写成`writeln(58)`;而不能是`write(58);`  
  对于C/C++来说，要写成 `printf("58\n");` 或者 `cout<<58<<endl;`

  #### 一行输出1-10 十个数 之间空一格示例：

  PASCAL：不能这样写
```pascal
  for i:=1 to 10 do write(i,' ');
```
  正确的写法是 
```pascal
  for i:=1 to 9 do write(i,' ');
  writeln(10);
```
  C++：不能写成 
```C++ 
  for (int i = 1; i<= 10; i ++) 
     printf("%d ",i); 
```
应写成   
```C++ 
 for( int i = 1; i <= 9; i ++ ) printf( "%d ", i ); 
 printf( "%d\n", 10 ); 
```
对于数组`a(10)`;

PASCAL：不能这样写 
```pascal
for i:=1 to 10 do write(a[i],' '); 
```
正确的写法是
```pascal
for i:=1 to 9 do write(a[i],' ');
writeln(a[10]);
```

C++正确写法
```C++
for (int i=1; i<=9; i++) cout<<a[i]<<" ";
cout<<a[10]<<endl;
```

### 编译错误（Compile Error，CE）

很显然，如果代码没有办法通过编译，那么就会返回`Compile Error`。
![](/images/oj/student/ce1.png)

错误原因可能有:
* 选错了语言，你用`C++`的代码，提交了`C`的编译器
* 本地尚未测试\(调试\)，存在语法错误

### 答案错误（Wrong Answer， WA）

“答案错误”时比较令人懊恼的结果，因为这说明代码有漏洞或者算法根本就是错误的，只是恰好能过样例而已。不过有时可能时应为输出了一些调试信息导致的，那就删除多余的输入内容再输出。当然，大部分情况下都需要认真检测代码逻辑有没有问题。
* ![](/images/oj/student/wa1.png) 所有组的数据都没有通过
* ![](/images/oj/student/wa2.png) 通过了`90%`的数据，即错误 `10%`,可以理解为100分的题目，得了90分。

### 运行超时（Time Limit Exceeded， TLE）

由于每道题都会规定程序运行时间的上限，因此当超过这个限制时就会返回`TLE`。一般来说，这一结果可能是由算法的时间复杂度过大而导致的，当然也可能时某组数据使得代码中某处地方死循环掉了。因此，要仔细思考最坏时间复杂度是多少，或者检查代码中是否可能数显特殊数据死循环的情况。

### 运行错误（Runtime Error， RE）![](/images/oj/student/runtime.png)![](/images/oj/student/re1.png)![](/images/oj/student/re2.png)

### 

Runtime Error:Segmentation fault

![](/images/oj/student/re1.png)这一结果的可能性非常多，常见的有段错误（直接的原因时非法访问了内存，例如数组越界，指针乱指），浮点错误（例如除数为0，模数为0），递归爆栈（一般由递归时层数过深导致的）等。一般来说，需要先检查数组大小是否比题目的数据范围大，然后再去检查可不可能有特殊数据可以使除数或者模数为0，有递归的情况则检查是否在大数据时递归层数太深。

### 内存超限（Memory Limit Exceed，MLE）![](/images/oj/student/mle1.png)![](/images/oj/student/mle2.png)

每道题目都有规定程序使用的空间上限，因此如果程序中使用太多的空间，则会返回MLE，例如数组太大一般最容易导致这个结果。  
格式错误（Presentation Error， PE）  
  这应该是最接近Accepted 的错误了，基本上由多输出了空格或者换行导致的，稍作修改即可。

### 输出超限（Output Limit Exceeded， OLE）![](/images/oj/student/ole1.png)![](/images/oj/student/ole2.png)

如果程序输出了过量的内容（一般是指过量非常多），那么就会返回OLE。一般是由输出了大量的调试信息或者特殊数据导致的死循环输出导致的。

