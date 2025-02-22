<div align=center><img src="https://urlshare.img.ink/2022/63b4c05602c63.png"/>
<h1>DailyInfo</h1>
<h6>基于 Python 的每日图文推送</h6>
<a href="https://github.com/thund1r/daily-info">
<img src="https://shields.io/badge/Daily--Info-blue?logo=github&style=for-the-badge&logoColor=white&link=https://github.com/thund1r/daily-info"></img></a>
<a href="https://gitee.com/thund1r/daily-info"><img src="https://shields.io/badge/Daily--Info-red?logo=gitee&style=for-the-badge&logoColor=white&link=https://gitee.com/thund1r/daily-info"></img></a>
</div>



## Notice

✅**企业微信通道恢复，可信域名已有解决方法，有需要的的朋友可以进群联系群主。**

🆙**2022年10月10日、18日更新，修复疫情中高风险区数据对应文字错误、多图文模式下文章图片不显示的Bug**

🆙**第一个公开的付费定制DailyTip日常提醒发布，支持获取自己准备的图片，支持21种天行数据。详情请看 [更新日志](https://mp.weixin.qq.com/s/ZTDU6_vVSaNQJyu712hYDw) 。**

⚠️**受企业微信官方9月19日策略调整影响，新建企业用户在新建应用时需要配置可信域名，且备案信息与企业一致。有服务器和备案域名的朋友可以按照官方要求自行配置。没有上述条件的朋友请进群联系群主，或使用微信接口测试号/电子邮件通道。9月19日前已建企业及应用的用户暂时不受此影响。**

💻**企业微信通道、带图文详情页面的接口测试号通道——只支持云服务器或腾讯云函数平台部署。**

💻**电子邮件通道、不带图文详情页面的接口测试号通道——支持任意平台部署。**

❗︎︎**本项目采用 [GPLv3](https://www.gnu.org/licenses/gpl-3.0.txt) 协议，仅供个人学习和使用，不得用于其他用途，未授权任何商业化、付费行为。使用本项目源码/教程即视为同意本条款，本人保留对一切违反本条款行为诉诸法律的权利。**

🔔**当前支持的内容过多，容易突破图文链接长度上限，请合理安排有关多城市、多日期等内容。**

📖**扫描文末二维码，关注微信公众号 勃然大陆 ，回复 教程 即可获取最新部署教程地址。**

🤔**有问题可扫描文末二维码进群询问，有功能需求可联系群主定制。**

## Introduction

- Bing必应 每日壁纸
- 金山词霸 每日一句
- ONE·一个 每日图文
- 夸克 多城市疫情数据
- 和风天气 多城市天气预报
- 可点击卡片 自带图文展示页
- 可选单图文 / 多图文推送模式
- 多日期提醒 纪念日 / 单日 农历 / 公历
- 可选企业微信 / 微信接口测试号 / 电子邮件通道
- 可自定义机器人名称 头像 卡片头图 标题 内容 称呼
- 详细的拓展模板

## Preview

- 单图文

<div align=center><img src="https://urlshare.img.ink/2022/f9a9f06cb0b14.png" width="600"/></div>

- 多图文

<div align=center><img src="https://urlshare.img.ink/2022/41d989a8bfa51.png" width="600"/></div>

<div align=center><img src="https://urlshare.img.ink/2022/75dbbc1e4585f.png" width="600"/></div>

## Preparation

|  环境变量  |                             含义                             |
| :--------: | :----------------------------------------------------------: |
|   corpid   |        企业微信企业ID<br />需要发送企业微信消息时必填        |
| corpsecret |      企业微信应用Secret<br />需要发送企业微信消息时必填      |
|  agentid   |       企业微信AgentId<br />需要发送企业微信消息时必填        |
|   appid    |          测试号appID<br />需要发送测试号消息时必填           |
| appsecret  |        测试号appsecret<br />需要发送测试号消息时必填         |
|   userid   | 测试号后台用户微信号<br />需要发送测试号消息时必填<br />多用户以&&分割<br />例如：abc123&&def456 |
| templateid |          测试号模板ID<br />需要发送测试号消息时必填          |
| emailfrom  |          发送邮件的邮箱地址<br />需要发送邮件时必填          |
| emailtoken |        发送邮件的邮箱的授权码<br />需要发送邮件时必填        |
|  emailto   | 接收邮件的邮箱地址<br />需要发送邮件时必填<br />多地址以&&分割<br />例如：abc123@qq.com&&def123@126.com |
|  qweather  |           和风天气应用Key<br />需要天气预报时必填            |
|    city    | 天气预报地址<br />需要天气预报时必填<br />格式：省/市-市/区/县，多城市以&&间隔<br />例如：成都-双流&&江苏-江宁 |
| beginname  | 单日事件名称<br />只有某一年有的日子，多日期以&&分隔<br />例如：跟XX在一起&&某某某出生 |
|  beginday  | 单日日期<br />公历格式20XX-XX-XX，农历年份前加n<br />多日期以&&分隔，注意与名称对应<br />例如：n2020-08-11&&2060-08-26 |
| targetname | 纪念日事件名称<br />每年都有的日子，多日期以&&分隔<br />例如：某某某的生日&&结婚纪念日 |
| targetday  | 纪念日日期<br />公历格式20XX-XX-XX，农历年份前加n<br />多日期以&&分隔，注意与名称对应<br />例如：n2020-08-11&&2021-08-26 |
|  msgtype   |        图文类型，默认单图文<br />1为单图文，2为多图文        |
|    pic     |   自定义固定头图链接<br />务必以 http:// 或 https:// 开头    |
|    call    |                 自定义称呼<br />例如：宝贝~                  |
|   title    |            自定义标题<br />例如：今天的推送来啦！            |
|  content   |          自定义第一段内容<br />例如：记得喝水水哦~           |
|    tian    |             天行数据APIKEY<br />需要彩虹屁时必填             |
|  pictype   | 随机头图类型，默认风景<br />可选项（接口要求）meizi、dongman、fengjing、suiji、none<br />分别是妹子、动漫、风景、随机、单图文不显示图片<br />多类型以&&分隔，例如：dongman&&fengjing |
|   yqcity   | 需要疫情数据的城市名称<br>需要疫情数据时必填，只能是市级<br />多城市以&&分隔，例如：成都&&南京 |
|    link    | 图文详情页网址<br />需要点击卡片进入页面时必填<br />务必以 http:// 或 https:// 开头 |

