###一、死锁停在第几次的截图：
####1.Linux环境下的死锁产生：

![linux.jpg](http://upload-images.jianshu.io/upload_images/3250499-971c1812967e9a45.jpg?imageMogr2/auto-orient/strip%7CimageView2/2/w/1240)
####2.windows环境下的死锁产生：

![window.jpg](http://upload-images.jianshu.io/upload_images/3250499-36d5199b30306a37.jpg?imageMogr2/auto-orient/strip%7CimageView2/2/w/1240)
###二、死锁产生的4个必要条件：
1.互斥条件：一个资源每次只能被一个进程使用；
2.请求与保持条件：一个进程因请求资源而阻塞时，对已获得的资源保持不放；
3.不剥夺条件:进程已获得的资源，在末使用完之前，不能强行剥夺；
4.循环等待条件:若干进程之间形成一种头尾相接的循环等待资源关系。
###三、对上述程序产生死锁的解释：
上述的程序种包含两个进程，A进程和B进程，而在程序运行的时候设置count的值使得AB进程轮流占用资源，这时候就会出现资源调度，调度到的进程就会占用资源且运行，当调度到下一进程时资源仍被上个进程所占用，死锁产生的4个条件已经具备，这时候调度就会出现阻塞，进而产生死锁。
