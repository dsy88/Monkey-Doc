1. json的状态消息放在哪里？

公用的消息放在monkey/monkey/contants.py里，私有的消息放在每个模块中，org以1xxx开始，ad以2xxx开始，每次提交pull以后，把公用的消息合并monkey/monkey/contants.py。

2.发现bug的政策如何界定？

每次发现bug，都打开一个issue，把issue的链接附在有bug的代码行后面，在issue中详细说明bug的内容，解决办法，发现者，指派者。编写者阅读以后确认bug的正确性，提交commit，关闭这个issue。每个issue扣除代码编写者5块钱，bug发现者获得。

3.消息格式以及跳转

按会议记录中的字段名吧，这样{"status": 300, "message": "xx", "next":"org/account/profile"}
跳转前端做

4.临时跳转路径

/org/account/login-->/org/account/register--> /org/account/profile --> /org/activity/list --> /org/activity/create --> /org/ads/add-->/org/activity/get --> /org/activity/update --> /org/activity/get --> /org/activity/delete --> /org/activity/get --> /org/activity/list --> /org/account/profile --> /org/ads/list --> /org/ads/get --> /org/ads/accept --> /org/ads/list

/ads/account/login --> /ads/account/register --> /ads/account/profile --> /ads/activity/list --> /ads/activity/get --> /ads/bid/create --> /ads/activity/get --> /ads/activity/list-->/ads/bid/list-->/ads/bid/get-->/ads/bid/list
 
5.活动管理页面功能

活动管理页面的主页面是在Profile页面中，用户点击活动管理，右边应该看到它已有的活动列表，如
http://dev.mrdaguanjia.com/monkey_admin/activity/activity/
可以点击添加，进入一个活动提交的表格，与目前的django后台管理的页面类似，只是增加了一些字段。
http://dev.mrdaguanjia.com/monkey_admin/activity/activity/add/。
同时还有更新删除修改等功能。

目前新增页面，更新页面是弹出显示还是内嵌在profile页面待定。

5.美工设计注意事项

现在需要在上次Profile的基础上增加功能页面的设计
目前我们正在实现活动管理及竞标管理的功能
点击Profile页面左侧的活动管理
应该看到目前该用户所有的活动或者投标
点击可以进入看详情，可以新增，删除
新增删除是跳转到新页面还是在右侧重新直接展示由你们来决定，你需要给出这些页面的设计图，切图，跳转顺序，以及交互过程
郑婷也是我们设计组的一员，一直以来帮助我们设计海报等
设计过程中，千遇可以带着郑婷做一些部分设计，郑婷也可以从女性的视角增加一些设计的元素
在设计和实现过程中，和李丽师姐密切配合，经常沟通，最终你们的设计成果的验收不仅仅是看你们给出的图片和切图，更重要的是李丽师姐设计出来以后部署的网页
所以在李丽师姐实现的过程中，密切沟通，保证设计和实现的一直，经常查看一下部署出来的网页，看看是否和你们的想法一直
部署网页的url将经常更新发给你们
有些不懂的问题，经常查看FAQ文档
https://github.com/dsy88/Monkey-Doc/edit/master/FAQ.md

6.活动列表的内容，竞拍列表的内容是什么

活动列表目前内容与django 后台的列表基本保持一致，可能会增加一些内容，和李丽的讨论结果，有两种可能的呈现方式，一种还是列表，类似于app第二栏，左边是图右边是介绍，一种是类似小酱油的图堆积呈现。 第二个问题是点击如何打开，是弹出新窗口还是就在这个页面出现，目前暂时选择弹出新窗口。

竞标的列表应该和活动列表差不多， 也是这么一个表，里面是活动名字，广告位名字，广告位内容，竞拍价格，是否成交，应该是类似于淘宝已经买到的东西那样

点击相应活动进去看到的应该是，活动的信息（链接到活动页面），社团的部分信息，已经购买到的广告位的信息等等，包括布这个活动的社团信息，联系人的信息，已经购买到的广告位（比如是横幅，多大，挂在哪）这种信息




