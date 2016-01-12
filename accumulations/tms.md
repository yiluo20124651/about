# tms模版迁移

## 需求描述

由于tms新版升级，不支持php，现用的php模版需要进行变更为前端模版，从而平滑迁移到新版tms。

##  头文件

### 主要功能概况
* 分享功能
* 环境识别功能
* 浏览器识别功能
	
### 所做改动
* 将内联的静态资源作为外链资源引入
* 分享功能独立为单独组件
* 环境识别功能和浏览器识别功能，将php实现的代码改为js实现
* 改用vue的类库来替代php对某些逻辑（如：判断alishare的存在，运营所配置的pageTitle以及分享的文案等信息）
	
### 改动后的调用方式
* 	发布环境的判断： envJudge(  );
* 	浏览器的识别： 

```
`<script type="text/javascript" src="js/browser.js"></script>

```

* 微博分享初始化：


```
`<script type="text/javascript" src="js/weiboinit.js"></script>

```	

### 总结

