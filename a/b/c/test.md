#### 宽屏适配指南

refusing to merge unrelated histories

refusing to merge unrelated histories

refusing to merge unrelated histories

refusing to merge unrelated histories

#### 1. 页面窗体级适配方案：leftWindow、rightWindow、topWindow
以目前手机屏幕为主window，在左右上，可新扩展 leftWindow、rightWindow、topWindow，这些区域可设定在一定屏幕宽度范围自动出现或消失。这些区域各自独立，切换页面支持在各自的window内刷新，而不是整屏刷新。

refusing to merge unrelated histories

这里有2个例子：
- hello uni-app：[https://hellouniapp.dcloud.net.cn/](https://hellouniapp.dcloud.net.cn/)
- 分栏式的新闻模板：[https://static-7d133019-9a7e-474a-b7c2-c01751f00ca5.bspapp.com/#/](https://static-7d133019-9a7e-474a-b7c2-c01751f00ca5.bspapp.com/#/)，这个示例对应的源码在：[https://github.com/dcloudio/uni-template-news](https://github.com/dcloudio/uni-template-news)


refusing to merge unrelated histories

这些例子特点如下：
- hello uni-app使用了topWindow和leftWindow，分为上左右3栏。新闻模板使用了rightWindow区域，分为左右2栏。宽屏下点击左边的列表在右边显示详情内容。而窄屏下仍然是点击列表后新开一个页面显示详情内容。
- leftWindow或rightWindow 里的页面是复用的，不需要重写新闻详情页面，支持把已有详情页面当组件放到 leftWindow或rightWindow 页面中。

这套方案是已知的、最便捷的分栏式宽屏应用适配方案。

__H5 宽屏下 tabBar(选项卡) 与窗体的关系__

> 目前做如下调整：leftWindow、rightWindow、topWindow 中有其一存在，则 tabBar 隐藏；不存在，则不隐藏。

leftWindow等配置，在pages.json里进行。文档见：[https://uniapp.dcloud.net.cn/collocation/pages?id=topwindow](https://uniapp.dcloud.net.cn/collocation/pages?id=topwindow)

pages.json 配置样例

### 新增文档

这里是新增的需要翻译的文档 123132465