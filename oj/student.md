## 常见问题

Q:这个在线裁判系统使用什么样的编译器和编译选项?  
A:系统运行于Debian/Ubuntu Linux. 使用GNU GCC/G++ 作为C/C++编译器, Free Pascal 作为pascal 编译器 ，用 openjdk-7 编译 Java. 对应的编译选项如下:

|C: | :   gcc Main.c -o Main -fno-asm -O2 -Wall -lm --static -std=c99 -DONLINE\_JUDGE |
| :--- | :--- |
| C++: | g++ -fno-asm -Wall -lm --static -std=c++11 -DONLINE\_JUDGE -o Main Main.cc |
| Pascal: | fpc Main.pas -oMain -O1 -Co -Cr -Ct -Ci |
| Java: | javac -J-Xms32m -J-Xmx256m Main.java \*Java has 2 more seconds and 512M more memory when running and judging. |



