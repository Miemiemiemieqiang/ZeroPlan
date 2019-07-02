### 创建一个 SSH key
```bash
ssh-keygen -t rsa -C "your_email@example.com"
```
-t 指定密钥类型，默认是 rsa ，可以省略。  
-C 设置注释文字，比如邮箱。  
-f 指定密钥文件存储文件名。  

### 查看配置 git config --list
### 客户端的公钥内容追加到服务器器的授权⽂文件(~/.ssh/authorized_keys)尾部
```bash
ssh-copy-id [-i [identity_file]] root@服务器器主机地址
```
同:
```bash
cat ~/.ssh/id_rsa.pub | ssh user@machine “mkdir ~/.ssh; cat >> ~/.ssh/authorized_keys”
```