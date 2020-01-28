# 图床设置记录

![tuchuang.png](http://img.isundae.cn/tuchuang.png)
[![tuchuang.png](http://img.isundae.cn/tuchuang.png)](http://img.isundae.cn/tuchuang.png)

## 概念

1. 图床就是专门用来存放图片，同时允许你把图片对外连接的网上空间。

2. CDN的全称是Content Delivery Network，即内容分发网络。CDN是构建在网络之上的内容分发网络，依靠部署在各地的边缘服务器，通过中心平台的负载均衡、内容分发、调度等功能模块，使用户就近获取所需内容，降低网络拥塞，提高用户访问响应速度和命中率。CDN的关键技术主要有内容存储和分发技术。

## 工具
- [github](https://github.com/) -- https://github.com/
- [qiniu](https://portal.qiniu.com) -- https://portal.qiniu.com
- [picgo](https://picgo.github.io/PicGo-Doc/zh/) -- https://picgo.github.io/PicGo-Doc/zh/
- [jsDelivr](https://www.jsdelivr.com/) -- https://www.jsdelivr.com/



## 图床对比

1. 七牛云   
官网地址：https://portal.qiniu.com     
简介：注册认证后有10G永久免费空间，每月10G国内和10G国外流量，速度相当快，七牛云时国内专业CDN服务商，插件支持比较多。

2. postimg   
官网地址：https://postimages.org   
简介：国外的图床，但是速度也很快。永久存储免注册，图片链接支持https，可以删除上传的图片，提供多种图片链接格式。   
限制：匿名上传和免费帐户上传的图片仅限于12Mb和10k x 10k像素。高级帐户仅限于24Mb和10k x 10k像素。每批最多限制为1000张图像，如果不够可以创建一个帐户并将多批图像上传到同一个图库中。

3. SM.MS   
官网地址：https://sm.ms/   
特点：永久存储免注册，图片链接支持https，可以删除上传的图片，提供多种图片链接格式。   
限制：每个图片最大5M，每次最多上传10张。最近越来越慢了.

4. 极简图床   
官网地址：http://jiantuku.com   
主要提供图片上传和管理界面，需要用户自己设置微博、七牛云或者阿里云OSS信息。

5. 路过图床   
官网地址：https://imgchr.com/   
简介：支持免注册上传图片，永久存储，支持HTTPS加密访问和调用图片，提供多种图片链接格式。   
限制：最大10M，速度还可以，但是不支持api上传，使用起来略微麻烦。

现在安利一种基于github和jsdeliver加速的免费图床。PicGo工具一键上传，操作简单高效，GitHub和jsDelivr都是大厂，不用担心跑路问题，不用担心速度和容量问题，而且完全免费，可以说是目前免费图床的最佳解决方案！

### GitHub图床
```json
{
  "repo": "", // 仓库名，格式是username/reponame
  "token": "", // github token
  "path": "", // 自定义存储路径，比如img/
  "customUrl": "", // 自定义域名，注意要加http://或者https://
  "branch": "" // 分支名，默认是master
}
```
1. 首先你得有一个GitHub账号。

2. 新建一个仓库
   ![new1.png](http://img.isundae.cn/new1.png)
   记下你取的仓库名。
   ![new2.png](http://img.isundae.cn/new2.png)
   

3. 生成一个token用于PicGo操作你的仓库：

   访问：https://github.com/settings/tokens

   ![new3.png](http://img.isundae.cn/new3.png)

   然后点击`Generate new token`。

   ![new4.png](http://img.isundae.cn/new4.png)

   ![new5.png](http://img.isundae.cn/new5.png)

   把repo的勾打上即可。然后翻到页面最底部，点击Generate token的绿色按钮生成token。



   ![new6.png](http://img.isundae.cn/new6.png)

    **注意：** 这个token生成后只会显示一次！你要把这个token复制一下存到其他地方以备以后要用。

   ![new7.png](http://img.isundae.cn/new7.png)


4. 配置PicGo   
   下载Picgo，picgo可以快捷键上传图片Ctrl+Shipt+P，并且上传完了自动把图片网址复制到剪切板。

   **注意：** 仓库名的格式是用户名/仓库，比如我创建了一个叫做test的仓库，在PicGo里我要设定的仓库名就是Molunerfinn/test。一般我们选择master分支即可。然后记得点击确定以生效，然后可以点击设为默认图床来确保上传的图床是GitHub。


   至此配置完毕，已经可以使用了。当你上传的时候，你会发现你的仓库里也会增加新的图片了


## VS Code 版的PicGo：vs-picgo   
[vs-picgo地址](https://github.com/PicGo/vs-picgo)

1. 打开VScode。
2. 安装本插件
   ![vs-picgo.png](http://img.isundae.cn/vs-picgo.png)
3. 设置插件   
   
### github图床设置   

   ![github-vs.png](http://img.isundae.cn/github-vs.png)
   
   设置jsDelivr加速

   **格式：https://cdn.jsdelivr.net/gh/用户名/图床仓库名**

   ![jsdelivr.png](http://img.isundae.cn/jsdelivr.png)

   ![github2.png](http://img.isundae.cn/github2.png)

### 七牛图床   
   
   ![qiniu1.png](http://img.isundae.cn/qiniu1.png)
   ![qiniu2.png](http://img.isundae.cn/qiniu2.png)
   
   VSCode 设置插件

   ![qiniu3.png](http://img.isundae.cn/qiniu3.png)
