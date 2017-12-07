1.dubbo中xmlxsi:schemaLocation会所xml错误，没关系不会影响运行
2.zookeeper运行bin下zkServer.cmd启动
3.zookeeper集群配置 
复制3个zookeeper(配置如下，clientPort不相同) 
tickTime = 2000
dataDir = /path/to/zookeeper/data
clientPort = 2181
initLimit = 5
syncLimit = 2
#Clusters  
server.1=127.0.0.1:2888:3888  
server.2=127.0.0.1:2889:3889  
server.3=127.0.0.1:2890:3890
# the directory where the snapshot is stored.  
dataDir=E:/zookeeper/zookeeper-1/data  
# the directory where the log  
dataLogDir=E:/zookeeper/zookeeper-1/log  

在每个dataDir下面的data下面添加myid(根据server.x添加数字)

注意：分别启动zookeeper的时候可能会报错，等全部都启动起来就正常了

