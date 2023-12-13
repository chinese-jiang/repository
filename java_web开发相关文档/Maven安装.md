# 安装步骤

1. 解压apache-maven-3.6.1-bin

2. 配置本地仓库：在自己计算机上新一个目录（本地仓库，用来存储jar包）

   ![image-20230905095217565](C:/Users/xtk/AppData/Roaming/Typora/typora-user-images/image-20230905095217565.png)

3. 进入到conf目录下修改settings.xml配置文件，修改仓库下载地址为本地仓库

![image-20230905095254765](C:/Users/xtk/AppData/Roaming/Typora/typora-user-images/image-20230905095254765.png)

4. 配置阿里云私服：修改settings.xml配置文件的<mirrors>标签，添加一下内容：

   ```
       <mirror>  
         <id>alimaven</id>  
         <name>aliyun maven</name>  
         <url>http://maven.aliyun.com/nexus/content/groups/public/</url>
         <mirrorOf>central</mirrorOf>          
       </mirror>
   ```

5. 配置环境变量：MAVEN_HOME为maven的解压目录，并将其bin目录加入PATH环境变量。

   目的：在命令行能执行maven指令



# IDEA集成Maven