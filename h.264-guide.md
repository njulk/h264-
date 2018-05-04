## 关于H264, 通用的5个进阶文档为

* [H.264_MPEG-4 Part 10 White Paper]
* [Video coding using the H.264 MPEG-4 AVC compression standard]
* [H.264 and MPEG-4 video compression]
* [Overview of the H.264_AVC Video Coding Standard]
* [Overview and Introduction to the Fidelity Range Extensions]

## 分三个阶段学习

### 第一阶段

学习H.264, 首先要把最基本最必要的资料拿在手里, 内容包括: 标准文档(即ITU协议), 测试模型(即ITU 提供的编解码器源代码), 经典文章(即后面提到的文章, H.264相关论文经典文章).

怎么使用这些资料呢? 首先看里面的<H.264_MPEG-4 Part 10 White Paper>, 看完之后再看<Video coding using the H.264 MPEG-4 AVC compression standard> 和<Halsted.Press.H.264.And.MPEG-4.Video.Compression.Video.Coding.For.Next.Generation.Multimedia.eBook-LiB>, 然后可以抽空看<Overview of the H.264_AVC Video Coding Standard.pdf>. 

前三篇文章看完后, 你应该对H.264的整体框架有个比较深入的了解了. 这个时间可能只需要花费你三周左右的时间, 最后一篇文章是<Overview and Introduction to the Fidelity Range Extensions>, 该文的价值主要在于对H.264的第四个档次high profile做了介绍, 前面的文章都没有涉及该档次.

### 第二阶段

然后你就可以看代码了. 这个时候你最常用的工具就是标准文档和测试模型. 看代码也有讲究. 并不是像我开始那样看得那么仔细, 结果后来才知道远没有这个必要. 正如peter李说的: 看代码也要先从整体框架入手. 先搞懂H.264的整体框架在代码里是怎么分布的, 一个功能模块的前伸模块和后继模块是什么. 也就是搞清楚整个代码流程. 这个阶段对标准文档的使用可能很少. 如果你使用的测试模型是JM, 那么有一个好处: JVT提供了该测试源代码的说明书 - <H.264_MPEG-4 AVC Reference Software Manual>, 对编解码的所有参数做了详细介绍.

### 第三阶段

然后你找到一个自己感兴趣的切入点, 开始以此为中心研究这个问题. 你研究问题的时候应该是联系测试模型来研究, 这个时候你就需要仔细看代码中对这个问题的实现了. 这个阶段我绝对支持你一行行代码跟踪, 一个参数一个参数地跟踪. 而代码中不懂的地方可能需要查标准. 这时你再来看标准文档就有了针对性. 也因为能将标准文档和代码对应起来, 从而看标准文档也不觉得有太大困难, 也能明白标准文档说的是什么问题, 在测试模型中是如何通过代码实现的. 在这个阶段中, 会牵连到很多H.264的相关知识, 这样通过以点带线, 以线带面. 你会对H.264的内容认识越来越多. 而你也就找到了自己的方向, 最终走上了缔造中国人的H.264的光辉大道.

## 注意事项

1. 切忌将代码和标准文档独立开看, 否则, 你的困难会很大.
2. 对于刚开始接触H.264的人, 切忌直接看代码和标准, 哪怕是将标准和代码结合起来看, 你也会不太顺利. 换句话说: 在没有了解H.264整体框架之前, 你最好什么都不要做.
3. 你千万不要觉得自己参加讨论, 以及帮助别人找答案(当然是在你觉得别人问的问题你似曾相识的时候)是一个浪费时间的过程. 因为你参加讨论, 特别是你帮别人找答案的时候, 很多你似是而非的问题却能够得到一个更深刻的认识.
4. 学问, 学问, 即要问也要学. 不要养成自己的依赖思想. 其实你在自己查资料的过程中, 也会学到很多东西. 比如会知道某个问题在哪篇文章里能找到答案, 或者收集到更多相关问题的有价值的文章....而且自己查到的到底比别人告诉的印象深刻.
5. 读代码要讲究方法. 代码中有很多变量, 不要一开始就去看头文件, 想把里面所有变量都弄清楚是什么. 直接从main函数开始读c文件就可以了. 遇到不懂的变量再去查头文件, 如果头文件里没有说明, 自己又理解不了的问其他人——不要养成依赖性.

## 讲H264的中文书籍
* <H.264和MPEG-4视频压缩>: 欧阳合(我看的英文原版, 翻译过来的应该也不错)
* <新一代视频压缩编码标准—H.264/AVC>: 毕厚杰(书中有较多错误, 但仍然值得买, 建议只做参考)
* <小波编码与网络视频传输>: 沈兰荪, 卓力(个人觉得不错, 有关于 high profile 的介绍).

## H.264学习资源
* JVT所有的会议文件都在这里: <ftp://standards.polycom.com>
* ITU的站点: <http://ftp3.itu.ch/av-arch/>
* 流媒体论坛的FTP: <ftp://ftp.wonew.org>, usr: `liumeiti.upload` pass: `liumeiti.upload`
* 清华的FTP: <ftp://166.111.66.184>, usr: `video` pass: `smth`
* 所有JM的测试模型: <http://iphome.hhi.de/suehring/tml/>
* 中国人的H.264--AVS: <http://www.avs.org.cn>

## 视频序列下载网址
* <http://trace.eas.asu.edu/>
* <http://ise.stanford.edu/video.html>
* <http://www-mobile.ecs.soton.ac.uk/peter/links/work.html>
* <http://eeweb.poly.edu/~yao/VideobookSampleData/doc/sample/sample.htm>
* <http://www.tkn.tu-berlin.de/research/evalvid/>
* <http://www.cipr.rpi.edu/resource/sequences/>
* <http://kbs.cs.tu-berlin.de/~stewe/vceg/sequences.htm>
* <http://standard.pictel.com/ftp/video-site/sequences>
* <http://www.i3s.unice.fr/~garciav/goodies.php>

## H.264论坛
* <http://bbs.lmtw.com/index.asp?boardid=108>
* <http://bbs.edw.com.cn/index.asp?boardid=47>
* <http://www.newsmth.net/>

## H.264个人站点
* <http://lspbeyond.go1.icpcn.com/>
* <http://spaces.msn.com/members/naiqa/>
* <http://blog.chinaunix.net/index.php?blogId=2553>
* <http://h263.blogchina.com/>
* <http://blog.csdn.net/sunshine1314/category/123075.aspx>
* <http://zmshy2128.blog.163.com/>
* <http://www.fastvdo.com/spie04/> H.264/AVC综述文章，包含了新的高精度拓展(Sullivan, Topiwala, and Luthra)
* <http://iphome.hhi.de/wiegand/pubs.htm> 一些有关H.264/AVC的文章(Wiegand)
* <http://iphome.hhi.de/marpe/pub.htm> 更多的关于H.264/AVC的文章(Marpe)
* <http://iphome.hhi.de/suehring/tml/> H.264/AVC参考软件
* <http://www.vcodex.com/h264.html> H.264/MPEG-4 Part 10教程 (Richardson)
* <http://www.vcodex.com/h264mpeg4/> 书: H.264 and MPEG-4 Video Compression (Richardson)
* <http://internet.impress.co.jp/books/1983/> H.264/AVC 教科书 (日文: Okubo, Kadono, Kikuchi, and Suzuki)
* <http://ftp3.itu.ch/av-arch/jvt-site>  JVT Experts Group 文档
* <http://www.mpegla.com/news/n_03-11-17_avc.html> MPEG LA 关于H.264/MPEG-4 AVC专利授权的条款
* <http://www.videolan.org/x264.html> 一个基于GPL的H.264编码库, 支持大部分H.264的功能
* <http://www.m4if.org/> MPEG工业论坛
* <http://www.itu.int/rec/recommendation.asp?type=folders&lang=e&parent=T-REC-H.264> ITU-T 官方网页
* <http://www.iso.ch/iso/en/CatalogueDetailPage.CatalogueDetail?CSNUMBER=40890&ICS1=35&ICS2=40&ICS3= H.264> ISO 官方网页
* <http://www.wwcoms.com/technology/standard.htm> W&W Communications H.264 概述和IEEE文章
* <http://www.apple.com/quicktime/hdgallery/> 苹果公司H.264素材实例
