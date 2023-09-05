# git下载

下载地址：https://registry.npmmirror.com/binary.html?path=git-for-windows/v2.38.1.windows.1/



# git安装

全部点击下一步



# git用户名和邮箱配置

在 git bash里面

    git config --global user.name "随便取一个用户名" (回车)
    
    git config --global user.email "输入你自己的邮箱" (回车)

表示你这台机器上所有的Git仓库都会使用这个配置。



# 第一次git使用

第一步：新建一个本地仓库（一个目录文件）用于存放要上传的文件

<img src="C:/Users/xtk/AppData/Roaming/Typora/typora-user-images/image-20230903085522349.png" alt="image-20230903085522349"  />

该文件夹中会出现一个.git的文件夹，如果我们想要删除该仓库，只要rm -rf .git 删除该文件夹即可。

第二步：鼠标右键该文件点击git bash

![image-20230903085717443](C:/Users/xtk/AppData/Roaming/Typora/typora-user-images/image-20230903085717443.png)

第三步：初始化本地仓库

```
git init
```

第四步：将文件添加至缓冲区

```
git add . //.添加全部文件
git add 文件名 //添加指定文件
```

第五步：提交文件

```
git commit -m "描述此次操作" // 比如"add a new file"
```

第六步：用SSH来将本地仓库和githu仓库进行连接

1. 新建一个github仓库

2. 配置本机SSH与github连接

   ```
   ssh-keygen -t rsa -C "xxxx@qq.com" #输入GitHub的用户名（邮箱的那个，不是自己取得名字）
   ```

   ![image-20230903090649291](C:/Users/xtk/AppData/Roaming/Typora/typora-user-images/image-20230903090649291.png)

3. 在c盘里面找到id_rsa_pub文件；这个是公钥文件，另一个是私钥

   C:\Users\xtk\.ssh

   ![image-20230903090738587](C:/Users/xtk/AppData/Roaming/Typora/typora-user-images/image-20230903090738587.png)

4. 打开gituh设置SSH，将id_rsa_pub文件的内容复制到github上面绑定

第七步：建立本地仓库和远程仓库连接

```
git remote add origin "SSH路径"
```

![image-20230903091052678](C:/Users/xtk/AppData/Roaming/Typora/typora-user-images/image-20230903091052678.png)

第八步：将文件上传

```
git push -u origin master
```

![image-20230903091214243](C:/Users/xtk/AppData/Roaming/Typora/typora-user-images/image-20230903091214243.png)



# 以后的每一次使用

1. ```
   git add .
   ```

2. ```
   git commit -m "描述"
   ```

3. ```
   git push -u origin master
   ```

# git学习网站

https://blog.csdn.net/bjbz_cxy/article/details/116703787?ops_request_misc=%257B%2522request%255Fid%2522%253A%2522169370271116800215012168%2522%252C%2522scm%2522%253A%252220140713.130102334..%2522%257D&request_id=169370271116800215012168&biz_id=0&utm_medium=distribute.pc_search_result.none-task-blog-2~all~top_positive~default-1-116703787-null-null.142^v93^chatgptT3_2&utm_term=git&spm=1018.2226.3001.4187