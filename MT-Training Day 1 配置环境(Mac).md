# MT-Training Day 1 配置环境(Mac)

## 安装JDK
1. 检查是否已经安装JDK

   打开Terminal，输入java -version，回车

   ![image-20210809144038315](/Users/chanyeefan/Library/Application Support/typora-user-images/image-20210809144038315.png)

2. 若未安装，从官网下载所需要的JDK版本

   https://www.oracle.com/java/technologies/javase-downloads.html

   ![image-20210809144419893](/Users/chanyeefan/Library/Application Support/typora-user-images/image-20210809144419893.png)

3. 安装JDK

4. 配置JDK环境

   (1) 输入 [/usr/libexec/java_home -V] 查看默认的 jdk 下载地址

   ![image-20210809144938369](/Users/chanyeefan/Library/Application Support/typora-user-images/image-20210809144938369.png)

    将红色框框内的地址复制下来，一会需要用到！

   (2) 如果是第一次配置环境变量，需要先输入 [touch .bash_profile] 创建一个 .bash_profile 的隐藏配置文件

   ![image-20210809145259339](/Users/chanyeefan/Library/Application Support/typora-user-images/image-20210809145259339.png)

   (3)如果已经配置过环境变量，可以直接输入 [open -e .bash_profile]
   ![image-20210809145329400](/Users/chanyeefan/Library/Application Support/typora-user-images/image-20210809145329400.png)

   (4)回车，将会弹出一个新窗口

   ![image-20210809145527497](/Users/chanyeefan/Library/Application Support/typora-user-images/image-20210809145527497.png)

   (5) 再输入以下命令

   JAVA_HOME=/Library/Java/JavaVirtualMachines/jdk1.8.0_181.jdk/Contents/Home

   PATH=$JAVA_HOME/bin:$PATH:.

   CLASSPATH=$JAVA_HOME/lib/tools.jar:$JAVA_HOME/lib/dt.jar:.

   export JAVA_HOME

   export PATH

   export CLASSPATH

   其中，JAVA_HOME需要更改成step(1)中复制的个人路径：

   ![image-20210809145806006](/Users/chanyeefan/Library/Application Support/typora-user-images/image-20210809145806006.png)

   (6) 关闭窗口，Terminal会自动保存

   (7) 再次打开Terminal，输入 [source .bash_profile] 使配置生效

   ![image-20210809145941610](/Users/chanyeefan/Library/Application Support/typora-user-images/image-20210809145941610.png)

   (8) 输入 [echo $JAVA_HOME] 显示刚才配置的路径

   ![image-20210809150143083](/Users/chanyeefan/Library/Application Support/typora-user-images/image-20210809150143083.png)