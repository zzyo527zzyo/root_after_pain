# 一、有关刷机和ADB无法连接的疑难杂症

Tips：<br>
&emsp;&emsp;本人是25年9月份接触到刷机的,当时什么也不会,所以跑了很多次线下拜托别人刷机,其中就包括重庆和南京.<br>
&emsp;&emsp;在一个城市的手机城能刷操作系统的人不少,但是会刷root的就两三个<br>
&emsp;&emsp;有的甚至拒绝给你刷,毕竟这是风险大且吃力不讨好的活.<br>
&emsp;&emsp;本人在多次碰壁后,总结了各种问题，所以有了这篇文章.<br>

## 本人机型:一加ACE3

## 驱动问题
&emsp;&emsp;本人进了个刷机群,经常听见群友讨论.ADB连接不上就装驱动试试<br>
&emsp;&emsp;然而发过来的图片又如下所示,各种文件千奇百怪,<br>
&emsp;&emsp;而且每次发过来的驱动还不一样,有时候又让你用软件装,所以要连接ADB装的驱动究竟是指什么？<br>
![img.png](img.png)

### 驱动分为两种,一种是USB驱动,一种是ADB驱动
&emsp;&emsp;ADB驱动是使用ADB命令必装的驱动,主流的ADB驱动就三种:<br>
### 1.Android Studio自带的ADB驱动：<br>
![img_1.png](img_1.png)<br>
&emsp;&emsp;这个一般是开发者使用的官方驱动.<br>
### 2.模拟器自带的驱动,这里以雷电模拟器为例子:<br>
![img_2.png](img_2.png)<br>
### 3.就是大佬魔改的驱动:<br>
&emsp;&emsp;例如说残芯ADB<br>

&emsp;&emsp;USB驱动是为了让你设备被电脑识别装的驱动<br>
&emsp;&emsp;USB驱动分两种:<br>
### 1.Android Studio自带的USB驱动:<br>
![img_3.png](img_3.png)<br>
&emsp;&emsp;下载好了的USB驱动在这个目录下:<br>
![img_5.png](img_5.png)<br>
&emsp;&emsp;这个是谷歌官方的USB驱动主要用来适配谷歌的机型<br>
### 2.各大手机厂家自己的USB驱动：<br>
&emsp;&emsp;如果你发现谷歌官方的USB驱动适配不了你的机型,那说明厂家魔改了自己的操作系统<br>
&emsp;&emsp;这个时候你就要下载对应机型的USB驱动,比如说下面👇这个就是OPPO的USB驱动<br>
![img_4.png](img_4.png)<br>

## 系统设置问题
&emsp;&emsp;解BL锁🔒之前一定要开启OEM,还有关闭系统自动更新!!!<br>
&emsp;&emsp;本人就是没关自动更新,root效果直接失效了<br>
&emsp;&emsp;悠悠苍天！何薄于我？😭😭😭<br>

## USB选项配置问题
&emsp;&emsp;在系统成功识别设备后,会让你选择USB选项配置：<br>
![img_6.png](img_6.png)<br>
&emsp;&emsp;这里也是坑了我好久,平常的设备选择文件传输才可以连接上ADB<br>
&emsp;&emsp;而一加和华为的机型要选择仅充电才可以连接上ADB<br>
&emsp;&emsp;踩坑了好久.我直接破防了.<br>
&emsp;&emsp;华为这个机型选择仅充电我没有尝试过,是线下给我刷机的大佬给我说的.<br>

## 系统识别不到设备
&emsp;&emsp;win+x打开设备管理器,如果发现下图所示,说明你的设备没有被系统识别.<br>
![img_7.png](img_7.png)<br>
&emsp;&emsp;首先检查你的USB线,如果你的线是两芯的,没有数据传输功能,你插上线之后就不会弹出USB选项配置窗口<br>
&emsp;&emsp;如果不是线的问题,就可以尝试更新驱动了<br>
![img_8.png](img_8.png)<br>

## fastboot问题
&emsp;&emsp;这是fastboot刷镜像的命令：fastboot flash boot Masik修补过的.img<br>
&emsp;&emsp;可怎么刷都没有成功得到ROOT权限<br>
&emsp;&emsp;在线下大佬通过遍历扫描手机的全文件才知道,一加把这boot分区重命名了<br>
&emsp;&emsp;你需要刷fastboot flash init_boot Masik修补过的.img才能ROOT<br>
&emsp;&emsp;我直接破大防了,你现在看的都是我一步一步踩进去的坑.<br>

## 熔断机制
&emsp;&emsp;看到文章最后,我相信你是真心想要刷机了,最后提醒一下<br>
&emsp;&emsp;在刷机之前一定要备份好重要数据,看看最新的公告<br>
&emsp;&emsp;注意一下手机厂商有没有发布出有关刷机或退版本熔断的消息<br>
&emsp;&emsp;刷机顺利 GOOD LUCK<br>

## Star History

<a href="https://star-history.com/#zzyo527zzyo/-&Date">
  <picture>
    <source media="(prefers-color-scheme: dark)" srcset="https://api.star-history.com/svg?repos=zzyo527zzyo/-&type=Date&theme=dark" />
    <source media="(prefers-color-scheme: light)" srcset="https://api.star-history.com/svg?repos=zzyo527zzyo/-&type=Date" />
    <img alt="Star History Chart" src="https://api.star-history.com/svg?repos=zzyo527zzyo/-&type=Date" />
  </picture>
</a>
