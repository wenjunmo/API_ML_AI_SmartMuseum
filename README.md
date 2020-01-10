<div align="center">
  <h1>:whale2: 博物馆语音导览小助手 :whale2:</h1>
  <p>基于微信平台开发的 智能线上博物馆语音导览 小程序</p>
  <p>Seeking True from Fact 网新人，有态度，不认输，不头秃</p>
</div>


## PRD 价值主张设计

### 目标：多层次多长度版本

1. 一句话版本

> 此款小程序是基于微信平台开发的 **博物馆语音导览** ，针对传统语音导览对场景的识别不够精确，博物馆文物众多、分类细致的特点，该应用通过调取 **阿里云** 的 **语音识别/合成/处理** 3种API，结合馆内地图 ，只需用户输入指定的相关类型文物检索，自助导览会同步获取相关文物内容介绍并反馈。

2. 一分钟60s版本 (图文线上可阅读含可查连结)

> 此款小程序是基于微信平台开发的 **博物馆语音导览**，使用 **云开发模式** ，针对传统语音导览对 **场景的识别不够精确** ，**博物馆文物众多、分类细致** 的特点，该应用只需输入指定的相关类型文物检索来进行自助导览，并获取相关文物内容介绍。通过调取 **阿里云** 的 **智能语音识别ASR** 、**语音合成服务TTS** 、**自然语音处理NLU** 3种API，并结合馆内地图进行融合 ，提前将需要进行语音处理的文本上传小程序来合成语音，发布在小程序 “ **博物馆语音导览** ” 模块 ，用户输入关键词搜索文本，导览反馈语音，实现同步交译效果。


3. 400 秒版本 Pecha Kucha 20x20 版本 (线上投影片含可查连结)-此版本不需要


## 智能博物馆产品 PRD —— 以阿里巴巴 API 为基础语音导览器移动端 落地案例使用说明

## :sparkles: 价值主张设计

### :star: 加值宣言

|使用到的API&数据库技术分析|应用原理|
|-----------|--------|
|语音识别服务ASR|将语音转换成文字的能力快速集成，打造出“能听”的应用|
|语音合成服务TTS|将文字转换为声音的能力快速集成，打造出“会说”的应用|
|自然语音处理NLU|集语义解析、智能问答、意图识别等功能于一体，让应用具备理解能力|

### :star: 核心价值宣言

1.产品目标：用户通过语音导览，享受在线语音交互
2.目标用户群体需求分析（面向参观者、管理者）
- 参观者（游客）用户需求分析：
   - 智能语音导览的识别准确度：通过线上调查和用户访谈，用户对智能语音导览反馈其对场景识别不够精确，必须在一定范围内才能很好地识别场景。
   - 智能语音导览的语音合成清晰度：博物馆的文物众多、分类细致，用户期望可通过语音输入指定相关类型的文物来检索进行自助导览，并获取对应内容介绍，在前期通过获取博物馆文物的数据统计与资料收集，使用阿里巴巴语音识别 API 接口来实现用户输入语音，合成文字再转化传输到导览器，在导览器进行识别后会反馈信息。
   - 智能语音导览器人机交互需求：语音助手逐渐流行，用户更注重人机交互功能的实现，用户对语音交互在导览器上实现比较期待。各年龄层的用户在使用导览器时存在的常见问题可以通过智能语音识别ASR、语音合成服务TTS、自然语音处理NLU三种技术的结合来实现导览器“能听”"会说"“智能问答和意图识别”等功能于一体，具备理解用户和反馈信息的能力。定位地理信息（区域地理信息）并且将文本内容转化为语音内容。

- 管理者（工作人员）用户需求分析：
   - 设备（导览器）的管理和调试功能的操作是否简便：结合用户需求，工作人员在派发导览器时，需向用户简单介绍设备，并交付设备前确认设备是否可以正常使用。
   - 工作人员对导览器的更新是否会操作：文物收录和转移都需要人工对设备进行实时更新，工作人员能否简易地使用导览器的后台来进行数据的修改是个需求。

![输入图片说明](https://images.gitee.com/uploads/images/2019/1113/075313_e57bd2b6_1831543.png "微信图片_20191112211607.png")

### :star: 用户痛点宣言

游客模式

|用户痛点|解决方案|
|---------|-------|
|到达博物馆不清楚想找的展品位置在哪|通过使用导览小助手产品对展品进行搜索，产品在屏幕上显示出相对应的位置以及通过配套耳机进行语音导览
|当到达展品处，对展品的简介无法理解|可使用导览小助手产品进行自定义语音导览以及展品介绍解说|

管理员模式

|用户痛点|解决方案|
|---------|-------|
|博物馆发生突发事件|语音导览器可实时查看安保人员所处的位置，第一时间就近调动相关的安保人员进行维护处理|
|博物馆想要知道哪些展品比较受欢迎？展品摆放区域是否合理？|通过语音导览器在后台系统对用户进行实时监测所得出来的数据，如每日游客数量、游览行为数据，来对展品分布和游客接待工作进行调整。|

### :star: 人工智能概率性与用户痛点

|概率性|用户痛点|
|---------|-------|
|阳性 Positive|没有很好用户体验的语音导览|
|假阳 False Positive|展品的介绍信息一般针对阅读困难人士|
|假阴 False Negative|用户地图路线的规划不一定符合用户预期|
|阴性 Negative|语音导览范围视博物馆面积大小而定|

### :star: 需求列表与人工智能 API 加值

|经典使用场景|需求列表|核心功能|优先级|可用人工智能API|
|-------|-------|-------|-------|-------|
|定位地理信息（区域地理信息）|用户获得在展馆内精准定位信息，提供导航功能，用户输入具体馆内展品名字或者类别指引用户到达该展品展区，避免了用户在小区域内使用常用的导航app效果甚微|导览模块|首要|高德地图 API|
|文本内容转化为语音内容|用户参观展品时可选择把展品历史介绍的文字内容转化为语音输出(OCR)，解决人流量大下展品解说人员人手不足|语音模块|首要|阿里巴巴语音识别 API|


## :sparkles: 原型

### :star: 交互及界面设计
(在 PRD 文件中是否有说明且原型是否有做到：交互及界面设计的某个核心交互环节使用了人工智能的加值 1*5%=5%)

[智能博物馆原型交互文档](http://nfunm065.gitee.io/api_ml_ai_smartmuseum/#g=1&p=%E6%99%BA%E8%83%BD%E5%8D%9A%E7%89%A9%E9%A6%86%E8%AF%AD%E9%9F%B3%E5%AF%BC%E8%A7%88%E5%B0%8F%E5%8A%A9%E6%89%8B)

>1. 在推荐(推荐参观+推荐路线)使用了协同过滤的推荐算法，根据用户反馈的内容来实时生成可操作的游览路线
>2. 在定制(定制语音)使用了文本识别转换为语音输出，并且使用不同的API开放接口来对导览小助手来进行语音优化

#### 博物馆：

>![产品架构](https://images.gitee.com/uploads/images/2020/0110/041602_b6d38aa2_1831543.png "屏幕截图.png")
>![核心功能交互说明](https://images.gitee.com/uploads/images/2020/0110/041641_b5aba9d4_1831543.png "屏幕截图.png")

#### 首页+推荐+定制+我的(其中推荐和定制使用了人工智能API)

##### 首页(简介+地图)

>![首页(简介+地图)](https://images.gitee.com/uploads/images/2020/0110/041842_fde31293_1831543.png "屏幕截图.png")

##### 推荐(推荐参观+推荐路线)

>![推荐(推荐参观+推荐路线](https://images.gitee.com/uploads/images/2020/0110/092253_eef17eed_1831543.png "屏幕截图.png")
>![推荐参观](https://images.gitee.com/uploads/images/2020/0110/092343_2ce9a202_1831543.png "屏幕截图.png")
>![推荐路线](https://images.gitee.com/uploads/images/2020/0110/092429_88045417_1831543.png "屏幕截图.png")

##### 定制(定制语音)选择页

>![定制(定制语音)选择页](https://images.gitee.com/uploads/images/2020/0110/092505_4f07c234_1831543.png "屏幕截图.png")
>![定制(定制语音)自定义语音](https://images.gitee.com/uploads/images/2020/0110/092739_8ea6faf9_1831543.png "屏幕截图.png")
>![定制(定制语音)自定义上传语音](https://images.gitee.com/uploads/images/2020/0110/092834_a6ae50f1_1831543.png "屏幕截图.png")

##### 我的(基本信息+足迹+浏览

>![我的(基本信息+足迹+浏览](https://images.gitee.com/uploads/images/2020/0110/092916_e6bb845c_1831543.png "屏幕截图.png")

### :star: 信息设计
(在 PRD 文件中是否有说明且原型是否有做到：信息设计的某个核心信息或设计使用了人工智能的加值 1%*5=5%)

>1. 自动化 - 减少时间人力等成本，减少错误，增加人工智能成功的概率性（错误的判断可以作为系统训练的集合） 
>2. 认知科技 - 人机交互（智能交互中，使用合成语音作为交流，智能化让机器懂用户。认知即人类知觉，认知科技即靠机器学习具有人的认知并可以自动化辨别人脸与语音。

>作为分类本身，诸多应用价值主张抽出来就是在这一类清楚简单靠谱且具有专业性，做好这个分类就是同样科技在不同价值主张中就是与不同的价值主张宣言匹配，根据价值主张，自动识别文本，使用产品价值逻辑来对交互进行定义，不能陷入工程师逻辑。

>所以我们可以来类比，可以文本自动化批量处理转换为语音就是自动化的价值主张，而认知技术就是将语音导览小助手当人看待来提高使用效率而不是单纯的自动化要求。语音导览小助手反馈给人是客体（认知科技设计重点是辅助性的）和文本识别自动化。

具体原型见文档以及上图交互及界面设计的推荐(推荐参观+推荐路线)与定制(定制语音)选择页

### :star: 原型文档
(多少程度上有提供 MVP 可交互的原型文档，供它人在 Github 上下载使用 1%*5=5%)

全部使用 GitHub 开源，详细地址见 [智能博物馆语音导览小助手 rp 原型文件下载](https://github.com/wenjunmo/API_ML_AI_SmartMuseum/tree/master/Smart_Museum_rp)

### :star: 口头操作说明
(多少程度上在 2-3 分钟时间限制内，对听众留下了「的确这是个可行丶可用的人工智能加值产品」的印象 1%*5=5%)

>本语音导览已语音库和路线推荐位主要功能，并且在使用API人工智能加值的基础上对博物馆的展览路线进行合理的规划安排，解决用户在庞大的博物馆中迷路以及找不到想看的重点馆藏的痛点。首先对语音库进行提取关键词，并且结合路线推荐调用所使用的API来形成个性化行走路线，添加协同过滤推荐算法，提供用户多种游览路线的选择，确定使用即生成游览路线并且语音导航，拒绝使用会提示备用选项来再次选择，最终确定游览路线。


### :star: 使用风险报告

案例：广东省博物馆总大小6.7万平方米

    - 技术说明：高德地图室内定位 SDK 是由高德室内地图部和阿里智能生活事业部联合出品的一套室内定位开发调用接口，供开发者在应用中加入室内定位相关的功能。通过基于WIFI、蓝牙以及PDR的室内定位技术，可实现平滑的1-8米的定位效果和精度。

![输入图片说明](https://images.gitee.com/uploads/images/2019/1113/075516_4d1e7967_1831543.png "1.png")
 
    - 方案出台：博物馆空间较大，选择wifi方案更为正确。

![输入图片说明](https://images.gitee.com/uploads/images/2019/1113/075642_3e43a058_1831543.png "2.png")
 
    - 数据采集：每半年都需进行一次（假设一次采集费用为x，则每年要花费2x的费用）。产品需要结合地理信息来回馈语言提示以替代以前博物馆的语音导览设备，需要对部分存在和其它独特信息相关联的地理信息进行该特殊信息的记录。要求需要建立相关数据库，并随着不同展品展出、活动举办、时间的过去做出相应的改变，聘请专业人员维护。

### :star: 案例产品方案

1. 场地无线网络布置

根据广东省博物馆无线网络建设需求，构建安全可靠高速稳定易于管理的无线网络，本设计方案采用 AC+Fit AP 的网络构架对博物馆薄盖目标区域进行无线覆盖。广东省博物馆的大小为6.7万平方米，采用设备为新支点ICG-S2600（后续简称为S2600），S2600的覆盖人群为1000人，单位覆盖500平方米，预计使用140个S2600对场馆进行无线网络全覆盖。每个S2600价格在900元，共计126,000元。其他方面采用了CMAX-3030-CPUSEV53天线、L4A-HPNMDM-3M射频跳线以及合路和射频传输线等产品，具体使用情况根据场馆内的人群数量决定，根据广东省博物馆以往日均人流量初步将覆盖人群的数量定在同时20000人，费用保持在100,000元上下浮动10,000元。无线网络的覆盖总成本控制在300,000元。

2. 使用 API 接口成本

本产品采用由阿里云提供的API服务，预付费计算（每3000万次/54000元），根据阿里云的定价标准以及结合广东省博物馆的人流量，将成本控制在60,000元。

3. 数据库运维人员成本

以广州市2019从业人员人数和从业人员工资的统计数据计算，人均7450元，聘请三人，每年的运维人员成本为250,000元。

综合以上成本，最后共计610,000元。


-----
OVER



