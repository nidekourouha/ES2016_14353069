## 一、DOL框架描述
分布式操作层（DOL）是一个软件开发框架编程并行应用程序，是由劳工部允许指定的基础上计算的卡恩过程网络模型应用程序和功能的基础上的SystemC模拟引擎。此外，劳工部提供了一个基于XML的规范格式来描述一个包括绑定和映射并行应用程序的执行的多处理器系统。分布式操作系统负责管理分布式处理系统资源和控制分布式程序运行。它和集中式操作系统的区别在于资源管理、进程通信和系统结构等方面。
![分布式操作层结构图](http://upload-images.jianshu.io/upload_images/3250499-79dc82d0700baf5a.jpg?imageMogr2/auto-orient/strip%7CimageView2/2/w/1240)
##二、DOL安装笔记
1. 安装一些必要的环境：
   `$sudo apt-get update`
   `$sudo apt-get install ant`
   `$    sudo apt-get install openjdk-7-jdk`
   `$sudo apt-get install unzip`

2. 下载dolethz.zip和systemc文件；
3. 解压后进入systemc-2.3.1的目录下
   `$  cdsystemc-2.3.1`
   新建一个临时文件夹objdir
   `$  mkdirobjdir`
   进入该文件夹objdir
   `$  cdobjdir`
   运行configure(能根据系统的环境设置一下参数，用于编译)
   `$  ../configureCXX=g++ --disable-async-updates`

    ![运行configure后的截图](http://upload-images.jianshu.io/upload_images/3250499-4d16846cd239ef89.png?imageMogr2/auto-orient/strip%7CimageView2/2/w/1240)

   编译
   `$  sudomake install`
   记录当前的工作路径(会输出当前所在路径，记下来，待会有用)
   `$  pwd`

4. 编译dol
   进入刚刚dol的文件夹
   `$  cd../dol`
   修改build_zip.xml文件
   找到下面这段话，就是说上面编译的systemc位置在哪里，
   `<property name="systemc.inc"value="YYY/include"/>`
   `<property name="systemc.lib"value="YYY/lib-linux/libsystemc.a"/>`
   把YYY改成上页pwd的结果
5. 然后是编译
   `$ant -f build_zip.xml all`
   若成功会显示build successful
   接着可以试试运行第一个例子进入build/bin/mian路径下
   `$cd build/bin/main`
   然后运行第一个例子
   `$ant -f runexample.xml -Dnumber=1`
   成功结果如下图：

   ![成功结果如图](http://upload-images.jianshu.io/upload_images/3250499-ed64fa29756de90d.png?imageMogr2/auto-orient/strip%7CimageView2/2/w/1240)

##三、实验感想和实验心得
本次实验是一次较为基础的配置实验，为以后的实验奠定了基础，也让我们熟悉了分布式操作层的概念和结构。在实验的过程中遇到了一点小麻烦，就是在最后面运行ant的时候报错，初步认为是ant库没有装好，后来重装几次还是不行。最后发现问题所在，原来是虚拟机本身网络没有配置好，导致多次安装都没有成功，重新配置好虚拟机网络之后按照步骤进行的很顺利。本次实验让我明白了实验过程不可能一帆风顺，但是只要坚持下去，一定会克服各种难题，最后成功实现！


