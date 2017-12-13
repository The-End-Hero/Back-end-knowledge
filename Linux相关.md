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