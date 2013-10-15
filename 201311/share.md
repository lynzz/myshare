title: 11月分享
speaker: zhizhonglin
url: https://github.com/lynzz/myshare/201311
transition: cards
files: /js/demo.js,/css/nodeppt.css

[slide]

# 目录

- webstorm7介绍
- requirejs模块化运用
- grunt自定义模板

[slide]

#WebStorm — The smartest JavaScript IDE

这个做前端的童鞋们应该都比较熟悉了吧，jetBrain出品的IDE神器，做Web开发、Node.js开发都可以，集成很多前端开发常用的功能

[slide] 
##webstorm7新增了如下几个功能（较会用到的功能）

* Karma,一个很强大的测试框架(Test Runner),可能有些童鞋不认识，不过相信有不少人用过JSTestDriver（webstorm5有集成），是的，Karma也是Google出品，其前身叫做TestAcular,是Google在开发AngularJS的时候，感觉到jsTestDriver有一些不足，从而重新开发了一套测试框架，官网：[http://karma-runner.github.io/0.10/index.html](http://karma-runner.github.io/0.10/index.html "http://karma-runner.github.io/0.10/index.html")
* 对Mustache和Handlebars模板文件的支持
* 支持less/sass/scss
* 新增AMD文件模板
* 支持package.json文件

更多新增见：[http://blog.jetbrains.com/webstorm/2013/05/webstorm-7-eap/](http://blog.jetbrains.com/webstorm/2013/05/webstorm-7-eap/)

[slide]

不对webstorm的使用做具体介绍，下面给出一些相关的资料地址：


- 官网：[http://www.jetbrains.com/webstorm](http://www.jetbrains.com/webstorm)
- 淘宝明河同学的webstorm最佳实践(在线电子书)：[http://www.book.36ria.com/webstorm/index.html](http://www.book.36ria.com/webstorm/index.html)

[slide style="background-image:url('/img/bg1.png')"]

# 背景图片 {:&.flexbox.vleft}
## 使用方法：&#91;slide style="background-image:url('/img/bg1.png')"&#93;

[slide]
## 使用.class/#id/自定义属性样式
----

```html
使用：.class{:.class}
使用：#id{:#id}
组合使用：{:.class.class2 width="200px"}
父元素样式：{:&.class}
```

[slide]

## 主页面样式
### ----是上下分界线
----

nodeppt是基于nodejs写的支持 **Markdown!** 语法的网页PPT

nodeppt：https://github.com/ksky521/nodePPT

[slide]

## 这是一个列表
---

* 列表支持淡入淡出 {:&.build}
    * 上下左右方向键翻页 {:&.build}
    * 支持多级列表
    * 使用方法，markdown列表第一条加上：{:&.build}
* 完全基于markdown语法哦

[slide]
## 表格示例
### 市面上主要的css预处理器：less\sass\stylus
---
 |less| sass | stylus
:-------|:------:|-------:|--------
环境 |js/nodejs | Ruby | nodejs
扩展名 | .less | .sass/.scss | .styl
特点 | 老牌，用户多，支持js解析 | 功能全，有成型框架，发展快 | 语法多样，小众
案例/框架 | [Bootstrap](http://getbootstrap.com/) | [compass](http://compass-style.org) [bourbon](http://bourbon.io) |

[slide]

## 代码格式化
### 使用 **highlightjs**
----

```javascript
(function(window, document){
    var a = 1;
    var test = function(){
        var b = 1;
        alert(b);
    };
    //泛数组转换为数组
    function toArray(arrayLike) {
        return [].slice.call(arrayLike);
    }
}(window, document));
```
[slide]
## 支持 HTML 语法插入
----
[code]
<div class="file-setting">
    <p>这是html</p>
</div>
<p id="css-demo">这是css样式</p>
<p>使用&#91;code]&#91;/code]包裹的代码，会直接插入到页面</p>
<p>具体看下项目中 ppts/demo.md 代码</p>
<script>
    function testScriptTag(){

    }
    console.log(typeof testScriptTag);
</script>
<style>
#css-demo{
    color: red;
}
</style>
[/code]

[slide]
## iframe
----
<iframe data-src="http://www.google.com/doodle4google/resources/history.html" src="about:blank;"></iframe>

[slide]

## 居中图片
----
{:.flexbox.vcenter}

![FEinit帮助界面](https://github.com/ksky521/FEinit/raw/master/pic/feinit.png "FEinit帮助界面")

npm install -g feinit

[slide]
[note]
##这里是note

使用n键，才能显示
[/note]
## 使用note笔记
### note笔记是多窗口，或者自己做一些笔记用的
---
按下键盘【n】键测试下note，

markdown语法如下：
```markdown
[note]
这里是note，{ 要换成中括号啊！！
{/note]
```
[slide]

## 使用画笔
### 使用画笔做标记哦~你也可以随便作画啊！
---
按下键盘【p】键。按下鼠标左键，在此处乱花下看看效果。

按下键盘【c】键。清空画板

[slide]

## 使用宽屏模式
---
按下键盘【w】键。看下效果。

再按下键盘【w】键。

[slide]
## 使用overview模式
---
按下键盘【o】键。看下效果。

在overview模式下，方向键下一页，【enter】键进入选中页

或者按下键盘【o】键，退出overview模式

[slide]

## 多窗口演示
## 双屏演示不out！
---
本页面网址改成 url?_muliscreen=1，支持多屏演示哦！

跟powderpoint一样的双屏功能，带有备注信息。

[slide]
## 多种转场动画随心换
----
支持的动画包括：

 * horizontal3d
 * horizontal
 * vertical3d
 * zoomin
 * zoomout
 * cards

当然你可以自己写更炫的动画啊，记得[fork](https://github.com/ksky521/nodePPT)代码然后push给我哦~

[slide data-transition="zoomin"]

## 这是一个zoomin的动画
----
使用方法：

&#91;slide data-transition="zoomin"&#93;

[slide data-transition="vertical3d"]

## 这是一个vertical3d的动画
----
使用方法：

&#91;slide data-transition="vertical3d"&#93;

[slide data-outcallback="outcallback" data-incallback="incallback" ]
## 使用回调
----
使用方法：

&#91;slide data-outcallback="outcallback" data-incallback="incallback"&#93;

即：

 * 进入执行回调incallback函数
 * 退出执行outcallback函数

[slide]
## 设置slide？
### 修改 markdown 文件头部内容
----

``` javascript
title: nodeppt markdown 演示 //演讲主题名字
speaker: Theo Wang //演讲者名称
url: https://github.com/ksky521/nodePPT //网址
transition: zoomin //通用动画名称，可在
files: /js/demo.js,/css/demo.css //引入的文件，在页面底部
```
[slide]

## 更多玩法
---
https://github.com/ksky521/nodePPT

什么？这些功能还不够用？

极客模式：查看源码的nodeppt.js，相信你会找到牛逼的手机互动（摇一摇换页）功能

查看项目目录ppts获取更多帮助信息
