<p align="center">
<img src="http://mars2d.cn/logo.png" width="300px" />
</p>
 
<p align="center">基于uni-app技术栈的 Mars2D🌎最简项目模板</p>

<p align="center">
<a target="_black" href="https://github.com/marsgis/mars2d">
<img alt="GitHub stars" src="https://img.shields.io/github/stars/marsgis/mars2d?style=flat&logo=github">
</a>
<a target="_black" href="https://www.npmjs.com/package/mars2d">
<img alt="Npm downloads" src="https://img.shields.io/npm/dt/mars2d?style=flat&logo=npm">
</a>
<a target="_black" href="https://www.npmjs.com/package/mars2d">
<img alt="Npm version" src="https://img.shields.io/npm/v/mars2d.svg?style=flat&logo=npm&label=version"/>
</a>
</p>
  

 
  
## 如何使用？
使用` HBuilder X`打开项目即可。【特别说明：暂不支持APP，只支持H5或webviewx】


 
## 常见问题

### 1. HbuilderX运行到手机上的就可以看到地图(自定义基座), 如果是打包后的apk安装到手机上的地图就是白屏

回复：
目前尚未找到具体原因, 目前如需将本项目运行到app平台，请先打包为静态资源后使用HbuilderX打包，或者使用webview。
如果您有解决方法，欢迎提交pull 或 发代码到我邮箱`wh@marsgis.cn`

可能的方式：
 需要改下lib.5plus.base-release.aar 基座代码，在WebviewActivity.java 中设置webView时加下允许跨域



## Mars2D 是什么 
  `Mars2D平台` 是[火星科技](http://marsgis.cn/)研发的一款免费的二维地图客户端开发平台，基于[Leaflet](http://leafletjs.com/)优化提升与B/S架构设计，支持多行业扩展的轻量级高效能GIS开发平台，提供了全新的大数据可视化、实时流数据可视化功能，通过本平台可快速实现浏览器和移动端上美观、流畅的地图呈现与空间分析，完成平台在不同行业的灵活应用。


### 相关网站 
- Mars2D官网：[http://mars2d.cn](http://mars2d.cn)  

- Mars2D开源项目列表：[https://github.com/marsgis/mars2d](https://github.com/marsgis/mars2d)


## 版权说明
1. Mars2D平台由[火星科技](http://marsgis.cn/)自主研发，拥有所有权利。
2. 任何个人或组织可以在遵守相关要求下可以免费无限制使用。
