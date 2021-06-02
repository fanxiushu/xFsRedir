这是专门为xFsRedir提供的文件块传输协议的服务端程序。
     程序提供了目录映射服务端，能把服务端的某个或者多个目录映射到xFsRedir客户端
     程序提供了虚拟磁盘映射服务端，能把服务端的分区和物理磁盘映射到xFsRedir客户端
     程序提供了虚拟局域网IP数据包转发服务端，能让xFsRedir客户端组成虚拟局域网
     程序提供了代理中转服务器端，能让xFsRedir客户端通过代理上网

                                               CopyRight 2015-2021 Fanxiushu.

xfs_rdsvr服务端程序提供了 windows，linux，macOS三个平台，
其中windows编译了32和64位版本，其他的只编译了64位版本。
linux是在CentOS7平台编译的，macOS是在macOS15.3平台编译的。

windows目录下的xfs_rdsvr.ini有每个配置字段的详细说明，同样适用于其他平台的说明。
windows平台的xfs_rdsvr可以提供映射本地硬盘的功能，
如果用于代理服务端，因为可能会产生非常多的连接，尽量使用windows server版本的系统，或者linux系统。

