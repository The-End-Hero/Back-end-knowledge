命令

Linux命令格式

```
 命令      选项          参数
command  [-options]  [parameter1]

ls -alh -hal -a -l -h  是一样的（可简写，无顺序要求）
```



- ls    当前目录下的文件
  - ls / 显示根目录下的所有文件(夹)
  - ls -a 显示隐藏文件
  - ls -l 列表风格显示
  - ls -l -h 显示大小
  - ls > xxx.txt 将当前文件路径写入xxx.txt(删除之前，若没有则创建)中(重定向)
  - ls >> xxx.txt 将当前文件路径追加在xxx.txt
  - ls -lha /bin | more  管道查看
- pwd   相对根目录的路径
- cd  xx   进入xx目录
- touch xxx.txt   在当前目录下创建xxx.txt文件
  - touch .xxx.txt 创建xxx.txt隐藏文件
- clear 清屏
- mkdir  xxx  新建xxx文件夹
- history  获取历史命令
  - !xxxx 执行xxxx次命令
- rm 删除
- cat xxx.txt 查看xxx.txt
- more xxx.txt 查看xxx.txt（分屏）





vi命令
命令模式:

	yy:复制 光标所在的这一行
	4yy:复制 光标所在行开始向下的4行
	
	p: 粘贴
	
	dd:剪切 光标所在的这一行
	2dd:剪切 光标所在行 向下 2行
	D:从当前的光标开始剪切，一直到行末
	d0:从当前的光标开始剪切，一直到行首
	x:删除当前的光标，每次只会删除一个
	X:删除当前光标前面的那个，每次只会删除一个
	
	h左 j下 k上 l右
	
	H:当前屏幕的上方
	M:当前屏幕的中间
	L:当前屏幕的下方
	
	ctrl+f--->向下翻一页代码
	ctrl+b--->向上翻一页代码
	
	ctrl+d--->向下翻半页代码
	ctrl+u--->向上翻半页代码


	20G:快速的定位到第2行代码
	G:快速的回到 整个代码的最后一行
	gg:快速回到 整个代码的第1行
	
	w:向后跳一个单词的长度，即调到下一个单词的开始出
	b:向前跳一个单词的长度，即调到上一个单词的开始出
	
	u:撤销刚刚的操作
	ctrl+r:反撤销
	
	选中一片代码
	v:
	V:
	
	>>:向右移动代码
	<<:向左移动代码
	
	.:重复执行上一次的命令
	
	r:替换一个字符
	R:替换光标以及后面的字符
	
	shift+zz:相当于wq

末行模式:
	w:保存
	q:退出
	wq:保存并且推出




