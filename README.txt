
xFsRedir是集成多种功能于一身的复合型程序。
  它可以是一个分布式网络文件系统程序，
    提供的目录或者文件重定向功能，能把各种异构的文件服务器集中于windows本地文件系统中，
    如同访问本地文件系统一样，提供了目前最普遍使用的10多种网络文件传输协议。
  它可以是分区或磁盘的模拟器，
    可以把服务器端的磁盘镜像文件通过各种通讯协议模拟成本地分区或磁盘，
    可以直接把服务端的分区或者物理磁盘模拟成本地分区或磁盘。
  它可以构建起庞大的虚拟局域网，
    可以让处于任何地方的电脑之间互相通信，如同在同一个内网中一样，
    可以让不同城市，不同国家地区的同一网段的内网组建在一起，
    可以让不同城市，不同国家地区的不同网段的内网组建起一个庞大局域网。
  它可以承担起NAT路由角色，也可以代理内网或做为本机代理，
    可以作为NAT路由器使用，可以监控各种网络通讯数据并做限速，
    可以作为网关代理，让内网的其他设备全部通过代理上网，
    可以作为本机代理，根据代理的各种过滤规则，让不支持代理的程序也能通过代理上网。

xFsRedir包括四大部分功能：
   一，核心的功能是通过各种通讯协议把远程目录或文件映射成本地目录或文件。
   二，通过各种通讯协议把远程镜像文件或磁盘映射成本地磁盘。
   三，虚拟局域网：包括虚拟局域网节点，桥接到真实局域网，跨地区的不同网段局域网组网。
   四，NAT路由和网络重定向 (代理)：包括NAT网关代理和本机代理。

简单使用说明：
  本软件不隐含连接到某个固定服务器，也不会提供任何数据服务器。
  本软件完全可以在隔绝的网络环境中使用。
  xFsRedir建议您使用私有存储，防止特别隐私的数据泄露，
  同时提供非常多的通讯协议以满足不同需求。
  本软件提供的虚拟局域网功能帮助您在复杂的网络环境中直接访问文件服务。
  对于虚拟局域网功能，需要数据包转发服务器xfs_rdsvr，
  对于网络代理功能，也需要搭建xfs_rdsvr的代理服务端。
  这些都需要自行去搭建配置，xfs_rdsvr服务端的配置是十分简单的。

法律申明：
  请遵守您所在的国家及地区的相关法律法规使用本软件，
  若违法使用或违法搭建服务器，一切后果自行承担。

本软件不提供版本自动更新功能，若需要获新版本，或者发现BUG，
可以给本人发送邮件, mailto:fanxiushu@163.com，或者到CSDN以及GitHUB获取。
CSDN :  https://blog.csdn.net/fanxiushu 
GitHUB: https://github.com/fanxiushu 
本软件不属于任何组织和公司，版权归fanxiushu个人所有。

                                                                                                        范秀树 2015-2021


程序安装使用：
进入到xfsredir目录下，选择你感兴趣版本号对应的 xFsRedir-X.X.X.X.zip 打包文件。
下载到本地电脑，然后解压到某个目录下，运行 xFsRedir.exe ，加载服务。
看到状态显示 驱动和服务都处于 Running 状态，说明已经成功运行了。

***因为不同版本之间并不兼容，因此在替换版本的时候， 必须要一起替换(包括服务端xfs_rdsvr程序)。
如果先前运行了老版本xFsRedir.exe，
请先运行老版本程序，然后卸载服务，卸载驱动，
再重启电脑，再次运行老版本程序，查看状态栏的服务和驱动都已经卸载了，这时才可放心删除老版本所有程序。
再运行新版本程序。
如果要使用扩展虚拟磁盘驱动，可以进入virtual_disk_driver目录进行安装。

可能使用xFsRedir程序的地方， xFsRedir程序运行在各类windows平台
（WINXP, WIN7，WIN8，WIN10,其中虚拟局域网驱动只能运行在WIN7，WIN8，WIN10）：
1，想把各类文件集中到本地电脑，扩展磁盘容量，比如大量的视频文件放到专门的服务器上，
     利用此软件可以把这些视频目录集成到本地目录。
2，远程执行程序，尤其是大量的游戏程序，
     游戏程序的体积现在是越来越大，动不动就是几十GB，因此放到一个统一文件服务器上，利用xFsRedir直接远程运行游戏。
3, 各个不同的局域网需要互相直接通讯，比如远程桌面，局域网游戏，共享打印机等等。
4，把windows平台作为NAT路由网关，或者需要主机代理，或者本地代理等需求。
5，其他各类应用。

程序使用说明以及开放源代码说明：
    本软件目录重定向和虚拟磁盘驱动部分不限制使用范围，
    虚拟局域网和代理部分限制商用，（这点和xdisp_virt项目的限制一致）。
    整个软件并不开放源代码,也并不出售工程源码，
    同时也不会开放和出售相关API接口，也不会提供专门的技术支持。
    (尤其是目录重定向部分，因为过于复杂且可能出现的问题也较多，
    虚拟局域网驱动和代理部分可以帮忙定制开发或出售)。
    4以上的版本增加了桌面水印，同时每个监控目录下增加“范秀树.xFsRedir.说明.txt”版权说明文件，
    如果讨厌水印等版权申明，请使用之前的版本，但是同时也享受不到xFsRedir提供的最新技术功能和某些BUG的修改。
    如有兴趣，可参阅发布到CSDN或GITHUB上的其他开源代码。

请合法使用本软件：
     请遵守您所在的国家及地区的相关法律法规使用本软件，
     若违法使用或违法搭建服务器，一切后果自行承担。
     尤其是本软件最新提供的虚拟局域网和集成多种功能的代理功能。
     有些国家或地区针对这些方面限制比较严格，请务必遵循当地法律法规。

软件通讯协议以及限制：
    本软件提供的私有文件传输通讯协议目前并未公布协议细节，
    通讯格式非常类似HTTP格式，使用一般的网络抓包工具，并不难获取通讯协议细节。
    但请勿破解和公布协议格式。
    您如果有其他通讯扩展需求，可以使用NFS, SFTP, SMB，FTP，WebDav等通用的通讯协议，效果都是一样的。
    同时请保持本软件的独立使用。
    *** 严禁通过非正常手段窃获软件内部各种接口，冒充并且集成到自己产品中。否则一旦发现会追责。

2021年6-9月更新日志：
1，进一步优化网络代理功能，NAT路由功能，增加了HTTP Connect代理等功能。
2，虚拟局域网部分增加了组网功能，也就是多个不同网段的跨不同地区的局域网可以组合在一起进行通讯。
3，虚拟局域网部分增加了UDP转发功能，P2P功能，这样在打洞成功之后，尽量使用点对点的传输，减少中转服务器的传输压力。
4，程序界面做了部分修改，把英文和中文完全分开，不再英文和中文混杂。不过英文界面大部分使用google和百度翻译的，
      会出现词不达意等现象，因此如果熟悉中文，请尽量使用中文界面。

2021年2-6月更新日志：
1, 修正目录重定向功能中移动文件或目录的严重BUG，
    如果遇到巨大文件的移动，中途如果取消，会造成原先文件被删除，
    同时后台实际并没取消，还在传输。这次修改解决了这个BUG。
    同时增加了删除到回收站功能选择何种删除办法。
2, 添加网络代理功能，包括NAT网关代理和本机代理两个部分。
    相关日志可查阅：
       https://blog.csdn.net/fanxiushu/article/details/117451203

2021-02月更新：
1，增加虚拟局域网功能，能让不同局域网的电脑互相访问。
更新日志，以及如何使用这个虚拟局域网，请查阅如下连接：
https://blog.csdn.net/fanxiushu/article/details/113934822

2020-12月更新：
1,  目录重定向部分增加单个文件重定向，增加可以指定特殊程序才能使用重定向的功能
2,  SMB通讯协议同时提供了第三方开源代码和windows系统调用两种方式，可根据情况自行选择某种SMB通信。
3，虚拟磁盘部分增加iSCSI通讯协议, 必须使用扩展虚拟磁盘驱动才能支持iSCSI协议映射整块磁盘
4，版本4.0以上的xFsRedir在每个重定向目录增加了‘范秀树.xFsRedir.说明.txt’版权说明文件，
     增加了桌面水印，同时必须以System系统账户和服务方式运行xFsRedir，
5，修改了扩展虚拟磁盘驱动和主驱动的某些BUG
更新日志：
      https://blog.csdn.net/fanxiushu/article/details/110956277
      
2020更新：
1，使用基于Storport底层框架的虚拟磁盘驱动代替直接IO的虚拟磁盘驱动，
     windows系统把这种虚拟磁盘当成真正的物理磁盘，
     并且能在磁盘管理器和设备管理器中查询到虚拟磁盘。
2，添加了两个命令行：xfsredir.exe -register, xfsredir.exe -unregister,
     用于注册成后台服务并且允许，停止运行并且注销后台服务，功能与配置界面中的“加载服务”和“卸载服务”相同。
     至于其他参数配置，任然需要界面配置，或者打开xFsRedir.ini手动配置（如果手动配置不嫌麻烦的话）。
     更新xFsRedir.ini配置文件后，无需重启服务，因为xFsRedir.exe程序会定时检测xFsRedir.ini 配置更新。
     添加此命令行，是因为较多人想要命令行（不明白有现成的界面配置不用，为何要不嫌麻烦的使用命令行）。

2019-09月更新：
1，文件系统缓冲功能可手动配置。
     文件系统缓冲是指在操作系统内核为每个文件数据开辟内存块，文件数据读写都是先在内存中读写，
     内存没有的才由操作系统引发类似“缺页中断“发起真正的读写磁盘请求，从磁盘读写的数据再次缓冲到内存中。
     xFsRedir以前的版本都是在驱动里默认开启了文件系统缓存功能，并且固定预读和延迟写的缓冲大小为1MB。
     测试发现改变这些参数会影响读写速度，因此本次更新中提供了手动配置这些参数的功能。
     针对千兆网甚至万兆网，适当增大预读和延迟写的缓冲大小，能提升速度，
     有些特殊场所，比如大文件的复制，禁用系统缓冲可能会快些 , 不过实际读写速度根据环境可能更复杂些。
     但是执行程序以及反复使用文件以及每次读一个字节的程序等许多情况下，启用缓冲肯定快的多。
2，优化windows端的xfs_rdsvr.exe程序，使得IO性能更好.

2019年更新日志：
1，扩展了虚拟磁盘功能，可以创建虚拟光驱，虚拟硬盘分区，创建虚拟内存磁盘。
     并且提供10多种磁盘镜像文件通讯协议。
     从而保证各种各样的镜像存储方式都能被访问。
2,  优化了目录重定向的某些IO性能。
3,  路径文件名的处理改成UTF8编码为默认编码。
4，xfs_rdsvr服务端增加了映射物理分区的功能，同时优化了IO性能。
更新日志：
       https://blog.csdn.net/fanxiushu/article/details/99402380

2018年更新日志：
1，重写了虚拟磁盘镜像文件存储方式，以前的版本只是简单的利用稀疏文件来存储虚拟磁盘镜像。
2，在第一条的基础上，扩展实现了内存虚拟磁盘，从而给xFsRedir实现内存目录提供基础。
     同时也实现了重定向到本地任意一个目录。
3，删除了百度网盘的接口，替代成微软的OneDrive云盘接口。
4，软件配置界面做了些修改，配置界面对高分屏的电脑屏幕提供了支持。
5，修改了其他一些BUG。
更新日志：
      https://blog.csdn.net/fanxiushu/article/details/80289261

可能出现的BUG以及注意事项：
   1，被xFsRedir设置为重定向的目录，不能设置成windows共享目录。这个问题是从开发xFsRedir以来一直存在的BUG，至今未解决。
      造成这种现象的原因是：
      经过xFsRedir主驱动重定向的所有文件对象 FILE_OBJECT 都是被拦截的，也就是不再继续发给底层的 NTFS文件驱动。
      而FILE_OBJECT内部的两个重要参数 FsContext和FsContext2，在NTFS文件驱动是被指向一个NTFS文件系统未公开的结构对象SCB的，
      为了防止某些特殊驱动或程序直接使用FsContext或FsContext2指针而造成系统蓝屏，
      xfs_redir.sys驱动采用打开当前分区卷的根目录的FILE_OBJECT，然后把这个FILE_OBJECT的FsContext和FsContext2赋值给所有被拦截的FILE_OBJECT。
      这样虽然能防止某些特殊驱动或程序直接访问FsContext而造成系统蓝屏，不过很显然，会造成这类特殊驱动或程序的访问行为混乱(但是至少防止系统崩溃蓝屏。)
      很不幸的，设置windows共享，就属于这类特殊的驱动或程序。 2020-10-20 特此注明原因。

   2，如果使用xFsRedir开启了新盘符，可能会造成windows的“磁盘管理器”无法正常打开，这是由于xFsRedir内部集成的虚拟磁盘驱动造成的。
      遇到这种情况，暂时把xFsRedir停止或者删除虚拟的新盘符就又能正常打开“磁盘管理器”了。
   3，可能许多人的习惯都是把远程文件夹映射成一个单独的虚拟磁盘的盘符来使用。
      但是本软件的核心是远程目录映射成本地目录，尤其是本地目录如果是个真实的磁盘下的某个子目录，才能更好的与本地文件系统融合在一起。
      正如CSDN上文章阐述的，xFsRedir集成的虚拟磁盘驱动是基于非常简单的直接IO模型，有时不能与真正的磁盘融合在一起。
      这可能会造成某些软件使用出现一些问题。但我相信大部分普通软件都应该不会有问题。
      因此映射时候尽量映射到真实磁盘目录下，如果一定要映射为新的虚拟盘符，则尽量映射到新虚拟盘符中的某个子目录中。
      不要映射成整个虚拟磁盘的盘符。
   4，同样是基于简单的虚拟磁盘模型的原因，需要xFsRedir以windows服务的方式运行，才能保证虚拟盘符中的文件获得全部的访问权限。
   5，解决以上问题，可以使用storport驱动框架生成windows真正识别的虚拟磁盘驱动能解决，
        你可以安装virtual_disk_driver目录下的虚拟磁盘驱动，从而让windows系统当成真正的磁盘。
        
   6，把远程目录映射成本地目录，会遇到有时候远程目录发生变化而本地无法及时得知，需要刷新本地资源管理器。
      这不是一个BUG，因为xFsRedir支持的大部分通讯协议都没有远程目录发生变化而通知的机制
     （包括PRIVATE私有通讯协议当初设计的时候也没实现这种通知机制），因此刷新一下就行了。
      这个部分是把数据实时传输到服务端的，一般不容易造成数据丢失，除非传输过程网络中断，即使中断，程序也开启了多次重试尝试。
   7，把远程镜像文件映射成本地磁盘，这个部分对写操作要慎重处理，否则可能会丢失数据。
      因为windows对磁盘读写的规律，一般都是缓存到系统缓冲中，不会实时刷新到磁盘扇区中。
      目前还没找到办法如何把数据实时刷新到磁盘扇区中。  

   8，速度损失。经过xFsRedir软件重定向的速度肯定会有一定的损失，但是所有通讯协议，速度基本都能达到原始速度的80%以及以上。
      其中xFsRedir提供的私有协议，经过优化，尤其是windows中的xfs_rdsvr.exe，在千兆网环境下，速度能达到100MB/s以上的速度。
   9, 软件不提供命令行参数，必须在界面中配置，如果需要命令行参数，请自行想法解决。
   10, 软件不会链接到某个固定服务器，因此不会提供自动更新功能，当然更不会搜集您的使用情况等信息。
      如果由于使用不当或者其他原因造成您的数据损坏丢失，后果需您自行负责。不得违法使用本软件，否则一切后果也得您自行负责。
   11，如果使用中遇到奇怪的问题，可以在CSDN或GITHUB上提出。
   
--------------------------------------------------------------------------------------------------------------
软件原理及开发说明：

基本功能是把对windows平台某个目录的所有访问重新定向到
网络上的另外一个机器的某个目录，实现基本的网络文件系统。
比如A机器的某个 'D:\\dir' 目录，经过本程序，
被定向到 B 机器的 'E:\\' 目录，A机器上的任何程序访问'D:\\dir'的
内容，实际上是在访问B机器的 'E:\\' 目录。

本程序的工作原理是在内核驱动层，拦截某个目录如'd:\\dir'的所有请求，
然后转发所有请求到程序的应用层，再通过网络转发到B机器服务端程序。

驱动程序 xfs_redir.sys 是本人自主开发，驱动中无任何开源代码参合，
驱动实现了windows Cache功能，同时是细化到某个目录来拦截请求，
这是市面上大部分类似驱动所没有的，大部分驱动都只能重定向到一个新的虚拟盘符，
比如NetDrive，WebDrive等许多类似软件，他们都只能虚拟到新盘符。
因此，你可以像linux挂载文件系统那样，随意在某个目录下挂载新的目录，
也可以多级的复杂挂载，
比如 'd:\\Path1' 挂载到S1服务器，'d:\\Path1\\Path2' 挂载到S2服务器等，
从而实现一个复杂的小型分布式文件系统。

断断续续的开发，以及断断续续的调试本驱动的BUG，延续的时间比较长，即便如此，
也不敢保证本驱动代码不存在BUG，以及在某些特殊应用程序调用特殊WIN32API
时候，不会造成本驱动蓝屏崩溃。

本程序目前支持的网络通信协议有10种。
一，PRIVATE协议，这个是最初开发这个驱动的时候，没想到还能支持很多公开
的网络文件系统协议而自己定义的TCP层上的简单和方便的私有网络文件系统协议。
二，NFS协议，这个是广泛使用在UNIX操作系统之间的网络文件系统协议，
windows服务器版本支持NFS服务端，同时也有免费的windows平台的NFS服务程序。
三，SMB协议，这个就是大家非常熟悉的windows的文件夹共享，能在各个windows
系统或者linux，macOS系统直接进行文件共享，
四，SFTP协议，如果非常熟悉linux的ssh登录，会非常熟悉这个协议，凡是linux
系统，都会默认安装ssh。
五，FTP协议，古老而方便的文件协议。
六，WebDAV协议，目前有些网络云存储支持这个协议，比如坚果云或者box等。
七，内存目录，可以把任何一个本地目录重定向到内存，使得操作这个目录的文件，全是存储在内存中。
八，本地目录，可以把本地目录重定向到另一个本地目录。
九，微软OneDrive云盘
十，GitHUB，这个是国外比较出名的代码托管网站，之所以开发这个，因为偶尔会在
上边托管些程序，但是它的接口并不完全符合文件系统的API，比如就没有rename等功能。

使用到的开源库：
1, NFS, SMB，iSCSI三个通讯协议客户端借用的是 Ronnie Sahlberg 作者的代码
   GITHUB地址：https://github.com/sahlberg 
2, 系统集成的SMB是直接打开 \\ server\ ShareFolder 方式的文件处理。
3, SFTP是借用 libssh2 + openssl 库 
4, FTP是以socket为基础开发 
5, WebDaV， OneDrive，GitHUB都是借用 curl + openssl 库。

命令行：
1, xFsRedir -register 功能等同界面上的-加载服务
2, xFsRedir -unregister 功能等同界面上的-卸载服务

=================================================================
xFsredir is a composite program integrating multiple functions.
It can be a distributed network file system program,
The directory or file redirection function can concentrate all kinds of 
heterogeneous file servers in the windows local file system,
Just like accessing local file system, it provides more than 10 kinds of 
network file transfer protocols which are most commonly used at present.
Can be a disk simulator, the network server disk through a variety of communication protocols mapped to the local disk.
Virtual LAN can be built to realize the mutual communication between devices in different LANs.
Can achieve network proxy function, so that does not support proxy programs 
or devices can also access the Internet through the proxy.

xFsredir includes four major functions
1, The core function is to map remote directory or file to local directory or file through various communication protocols.
2, The remote image file or disk is mapped to local disk through various communication protocols.
3, Virtual LAN, including virtual LAN nodes and bridging to real LAN.
4, Network agent, including NAT gateway agent and native agent.

This software does not implicitly connect to a fixed server, nor does it provide any data server.
For the function of VLAN, XFS is needed_ rdsvr，
For the network proxy function, we also need to build XFS_ Rdsvr proxy server.
All of these need to be configured, XFS_ The configuration of rdsvr server is very simple.

Please use the software in accordance with the relevant laws of your country,
If you use or build the server illegally, you should bear all the consequences.

This software does not provide automatic version update function. If you need to get a new version or find a bug,
You can send me an email, mailto:fanxiushu@163.com , or get it from CSDN and GitHub.
CSDN : https://blog.csdn.net/fanxiushu 
GitHUB: https://github.com/fanxiushu 
This software does not belong to any organization or company. The copyright belongs to fanxiushu.

                                                          fanxiushu 2015-2021
