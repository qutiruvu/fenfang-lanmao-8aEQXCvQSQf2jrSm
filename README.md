大家好，我是汤师爷，专注 AI 智能体分享，致力于帮助 100W 人用智能体创富~

短视频内容创作小白经常会遇到这样的困扰。

每天花大量时间刷视频，想要找到你所在赛道的爆款内容，却总是难以系统地整理和分析？

想要批量获取某个关键词的爆款视频数据，但是市面上的采集工具要么特别贵，要么操作极其复杂？

或者，已经尝试过各种方法，但始终找不到一个高效、低成本的解决方案？

不用担心，今天我就教你搭建一个Coze智能体，轻松搞定这些烦恼。

篇幅不短，欢迎先收藏，再慢慢阅读。如果觉得有帮助，也请顺手点个赞、在看、转发支持一下~

## 1.为什么要做热点监控？

热点监控是内容创作者和营销人员的必备工具，它帮助我们在信息爆炸时代精准把握用户关注点，提升内容效果和影响力。以下是进行热点监控的四大核心理由：

**1. 把握用户兴趣，提高内容相关性**

用户的注意力是稀缺资源。通过实时监控热点话题，我们能了解目标受众当下最关心的问题和兴趣点。热点本质上是用户兴趣的集中体现，基于热点创作的内容自然具有更高的用户匹配度，更容易获得关注和互动。

**2. 节约选题时间，提高创作效率**

没有热点监控系统时，创作者需要在各平台间不断切换，手动搜索和筛选信息，这个过程既耗时又低效。自动化热点监控能持续追踪多平台热门内容，将重复性工作交给智能体，让创作者能专注于内容创作本身。

**3. 抓住时机，提高曝光机会**

热点具有明显的时效性，越早参与讨论，获得的曝光机会就越多。自动化热点监控系统能在热点刚出现时就发出提醒，帮助创作者抢占先机。比起等热点完全爆发后再跟进，提前布局能获得更多流量红利和平台算法青睐。

**4. 发现内容机会，避免同质化**

热点监控不只是追踪已经爆发的话题，更重要的是发现潜在新兴热点。通过分析热点数据，创作者可以识别尚未被充分挖掘的内容机会，避开同质化竞争，找到差异化表达角度，从而在激烈的内容竞争中脱颖而出。

既然这么重要，那我们当然需要一个好用的智能体来帮我们自动收集这些视频。

但是，批量获取抖音视频内容这件事，一直有技术门槛。很多朋友因为不懂技术，只能花钱买工具来完成这项任务。

今天我要分享一个Coze智能体的解决方案，小白也能搭建。

只需输入自己赛道的关键词就能自动批量获取爆款视频内容，轻松实现100条爆款视频的采集工作。效果如下：

![image.png]()

## 2.智能体的搭建流程

智能体的搭建流程主要分为两个步骤：梳理工作流、设置智能体。

**1、梳理工作流**

热点监控工作流是一套自动化信息采集和处理系统，能将人工需要几小时甚至几天完成的工作压缩至几分钟内自动完成。这一工作流主要包含三大环节：

**（1）根据关键词，批量获取热门视频**

系统根据预设的关键词（如行业热词、产品名称、竞品信息等），自动从抖音、小红书等平台搜索相关视频。这一步骤替代了手动搜索和浏览结果的过程，大幅提高效率。

**（2）批量获取视频详细信息**

获取视频列表后，系统进一步抓取每个视频的详细数据，包括：

* 基础信息：视频ID、标题、链接、发布时间、视频时长等
* 互动数据：点赞数、评论数、收藏数、分享数等关键指标
* 创作者信息：作者名称、用户ID、个人简介等

这些数据是分析视频热度和受欢迎程度的关键指标，也是判断内容价值的重要依据。系统将这些零散数据整合成结构化信息，便于后续分析。

**（3）将数据添加到多维表格**

最后，系统将处理好的数据自动导入到预设的飞书多维表格中。

通过这样的自动化处理，我们能建立一个实时更新的热点内容库，随时查看行业动态，发现爆款选题灵感。

这种工作流显著减轻了运营人员的工作负担，让我们能将更多精力投入到内容创作和策略制定上。

**2、设置智能体**

完成工作流搭建后，我们需要创建一个热点监控智能体来执行这个工作流。智能体设置过程分为三个关键步骤：

1. 设置人设与逻辑：配置智能体的特征、回复风格和决策逻辑
2. 绑定工作流：将工作流与智能体关联，赋予它执行具体任务的能力
3. 测试并发布：进行全面功能测试，确认一切正常后将智能体正式发布到生产环境

完成这三个步骤后，我们就成功搭建了一个热点监控智能体。

## 3.创建工作流

登录Coze官网，在“资源库-工作流”里新建一个空白工作流，取名“fetch\_douyin\_hot\_videos\_daily”。

### 3.1 开始节点

![image.png]()

### 3.2 根据关键词，批量获取热门视频

我们将使用【视频搜索】插件的**douyin\_search**功能。通过这个功能，我们可以批量获取热门视频。

![image.png]()

插件节点：根据关键词，批量获取热门视频

* 输入：
  + api\_token：点击“感叹号”，通过网站可以获取。
  + keyword：关键词，从开始节点获取
  + page：第一页
  + publish\_time：发布时间，可用值: \_0(不限), \_1(一天之内), \_7(一周之内), \_180(半年之内)，这里我们选择\_7
  + sort\_type：排序类型，可用值: \_0(综合), \_1(最多点赞), \_2(最新发布)，这里我们选择\_1

![image.png]()

### 3.3 批量获取视频详细信息

**1.选择器节点：校验视频列表不为空**

![image.png]()

**2.批处理节点：批量获取视频详细信息**

* 输入：
  + aweme\_list：从"根据关键词，批量获取热门视频"节点的输出变量中，选择business\_data
* 输出：
  + new\_aweme\_list：处理后的视频列表

![image.png]()

**3.选择器节点：校验视频信息不为空**

![image.png]()

**4.视频搜索插件：获取单个视频详细信息（douyin\_data）**

* 输入：
  + api\_token：点击“感叹号”，通过网站可以获取。
  + douyin\_url：从批量获取视频详细信息节点的输出中，选择share\_url

![image.png]()

**5.代码节点：将视频详情整合进视频列表中**

* 输入：
  + aweme\_detail：从获取单个视频详细信息节点的输出中，选择aweme\_detail
  + aweme：从批量获取视频详细信息节点的输出中，选择item
* 输出：
  + aweme：处理后的单条视频

![image.png]()

![image.png]()

下面是处理数据的Python代码：

```
async def main(args: Args) -> Output:
    params = args.params
    aweme_detail = params.get("aweme_detail", {})
    aweme = params.get("aweme", {})
    aweme["aweme_detail"] = aweme_detail

    ret: Output = {
        "aweme": aweme
    }
    return ret
```

### 3.4 将数据添加到多维表格

**1.代码节点：将信息整理为飞书表格可以使用的数据**

* 输入：
  + aweme\_list：从"批量获取视频详细信息"节点的输出中，选择new\_aweme\_list
  + keywords：从开始节点中，选择keyword
* 输出：
  + records：处理后的表格数据，选择Array类型

![image.png]()

下面是处理数据的Python代码：

```
async def main(args: Args) -> Output:
    params = args.params
    aweme_list = params.get("aweme_list", [])

    result = []

    # 遍历 aweme_list，依次处理
    for aweme in aweme_list:

        # 获取 aweme_detail 并判空
        aweme_detail = aweme.get("aweme_detail") or {}
        title = aweme_detail.get("desc") or ""
        link = aweme_detail.get("share_url") or ""

        # 安全获取 statistics
        statistics = aweme_detail.get("statistics") or {}

        # 提取各字段信息，并在取值时加默认值
        video_id = statistics.get("aweme_id") or ""
        digg_count = statistics.get("digg_count") or 0
        comment_count = statistics.get("comment_count") or 0
        collect_count = statistics.get("collect_count") or 0
        share_count = statistics.get("share_count") or 0

        # 获取作者信息
        author_info = aweme_detail.get("author") or {}
        author_name = author_info.get("nickname") or ""
        signature = author_info.get("signature") or ""
        sec_uid = author_info.get("sec_uid") or ""
        raw_create_time = aweme_detail.get("create_time", 0)
        # 如果不是 int，就尝试转换，失败则为 0
        try:
            create_time = int(raw_create_time)
        except (TypeError, ValueError):
            create_time = 0

        # 创建时间以毫秒计，避免 None 或非法值导致报错
        create_time_ms = create_time * 1000

        raw_duration = aweme_detail.get("duration", 0)
        # 如果不是数字，尝试转换为 float，失败则为 0
        try:
            duration = float(raw_duration)
        except (TypeError, ValueError):
            duration = 0.0
        duration_sec = duration / 1000

        # 组装返回数据
        item_dict = {
            "fields": {
                "视频ID": video_id,
                "标题": title.strip(),
                "关键词": params.get("keywords", ""),
                "链接": {
                    "text": "查看视频",
                    "link": link.strip(),
                },
                "点赞数": digg_count,
                "评论数": comment_count,
                "收藏数": collect_count,
                "分享数": share_count,
                "作者": author_name,
                "用户简介": signature,
                "用户ID": sec_uid,
                "发布日期": create_time_ms,  # 毫秒级时间戳
                "时长": duration_sec        # 秒
            }
        }
        result.append(item_dict)

    return result
```

**2.我们需要创建一个多维表格，设置好表头字段，如下图所示。**

![image.png]()

表格模板链接：[https://xtninrlicw.feishu.cn/base/BRwvbkFzfaER27smZ7kcKN9wnSe?table=tbl2XVrl6Z0bWpNh&view=vewSzOF5Ix](https://github.com)

**3.飞书表格插件：将数据添加到多维表格（add\_records）**

![image.png]()

* 输入：
  + app\_token：提前创建一个多维表格，将多维表格的链接复制进去**。**
  + records：从"将信息整理为飞书表格可以使用的数据"的输出变量中，选择records。
  + table\_id：多维表格数据表的唯一标识符

![image.png]()

多维表格数据表的唯一标识符：

![image.png]()

### 3.5 结束节点

![image.png]()

## 4.创建智能体

### 4.1 新建智能体

在Coze平台创建一个新的智能体，命名“热点监控智能体”。

![image.png]()

### 4.2 设置人设与逻辑

设置人设与逻辑是创建智能体的关键步骤。在这一环节，我们需要明确智能体的行为模式和响应方式。

对于抖音热点监控智能体，我们希望它能直接执行任务，无需过多交互。因此，我们设置简单明了的指令，让智能体在接收到关键词后立即执行视频采集工作。

```
直接执行`fetch_douyin_hot_videos`
```

### 4.3 绑定工作流

把“fetch\_douyin\_hot\_videos\_daily”工作流加进来，让智能体在合适的时机自动调用它。

![image.png]()

### 4.4 测试并发布

全面的功能测试，确认正常后将智能体正式发布到生产环境。

![image.png]()

## 5.总结

本文详细讲解了如何利用Coze打造热点监控智能体，实现抖音平台热门视频数据的自动采集与分析。

通过设计工作流，这个智能体可以定时获取特定关键词的热门视频，并将所有数据自动整理到飞书多维表格中，方便后续深入分析。

有了这个工具，创作者不再需要手动搜索各个关键词，就能高效跟踪行业热点，从而腾出更多时间专注于内容创作本身。

> 本文已收录于，我的技术博客：[tangshiye.cn](https://github.com):[悠兔机场官网](https://youtu2.com) 里面有，AI 学习资料，Coze 智能体教程，算法 Leetcode 详解，BAT 面试真题，架构设计，等干货分享。
