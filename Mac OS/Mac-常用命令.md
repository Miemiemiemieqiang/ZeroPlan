### 复制-粘贴 pbcopy 和 pbpaste
可以将主目录的文件列表复制到剪贴板:
```bash
$ ls ~ | pbcopy
```
把任意文件的内容读入剪贴板:
```bash
$ pbcopy < blogpost.txt
```
pbcopy和pbpaste也可以用于自动化或加速执行一些事情。例如把一些邮件的主题存为任务列表，就可以先从Mail.app中复制主题，再运行:
```bash
$ pbpaste >> tasklist.txt
```
### 截屏 screencapture
抓取包含鼠标光标的全屏幕，并以image.png插入到新邮件的附件中:
```bash
$ screencapture -C -M image.png 
```
更多用法请参阅screencapture --help。
### 文本转语音 say
### 比较文件 diff