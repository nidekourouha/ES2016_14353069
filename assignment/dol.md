### 一、改完的*.dot截图
####1.修改example2，让3个square模块变成2个：

![example2的dot图](http://upload-images.jianshu.io/upload_images/3250499-c727703d19c7b368.png?imageMogr2/auto-orient/strip%7CimageView2/2/w/1240)

####2.修改example1，使其输出3次方数：

![example1的dot图](http://upload-images.jianshu.io/upload_images/3250499-857ec3bac2c15fda.png?imageMogr2/auto-orient/strip%7CimageView2/2/w/1240)

###二、具体如何修改的解释
####1.example2的修改：
首先考虑到example原本的功能是得到0到20每个数经过3次平方得到的结果，示意图如下：

![example2的dot图](http://upload-images.jianshu.io/upload_images/3250499-22894da772af3ae0.png?imageMogr2/auto-orient/strip%7CimageView2/2/w/1240)

因此只需要去掉一个square的步骤即可得到实验要求的经过两次平方得到的结果，结合实验文档给出的提示，做以下修改，将xml中的自由变量由原本的3变为2，成功得到结果：

![example2修改](http://upload-images.jianshu.io/upload_images/3250499-e5fdcde8fb9c6782.jpg?imageMogr2/auto-orient/strip%7CimageView2/2/w/1240)

![修改完的example2运行结果](http://upload-images.jianshu.io/upload_images/3250499-66e4fe1654d3f908.jpg?imageMogr2/auto-orient/strip%7CimageView2/2/w/1240)

####2.example1的修改：
考虑到原本的example1得到的是0到20每个数的平方数，示意图如下：

![example1的dot图](http://upload-images.jianshu.io/upload_images/3250499-ad6e85f2e8bef6ad.png?imageMogr2/auto-orient/strip%7CimageView2/2/w/1240)

结合实验文档的提示，需要修改的是example里面的square函数，将原本的i=i*i改成得到立方数的i=i*i*i即可得到实验结果：

![example1修改.jpg](http://upload-images.jianshu.io/upload_images/3250499-ab431a516fb247eb.jpg?imageMogr2/auto-orient/strip%7CimageView2/2/w/1240)

![修改完的example1运行结果](http://upload-images.jianshu.io/upload_images/3250499-61286c9c3c111961.jpg?imageMogr2/auto-orient/strip%7CimageView2/2/w/1240)

###三、实验感想
本次实验中，我对于dot开发的理解更进一步，对其应用的把握也更为深刻。虽说本次实验难度不大，而且关于算法的应用也不是太难，但是却让我理解了dot中模块与模块之间的联系，懂得通过修改模块的算法来解决实际遇到的问题。总而言之收获还是蛮大的，希望再接再厉，做的更好恩！