---
title: "国内怎么用上 Codex？CC Switch + DeepSeek 三步配置实测"
date: 2026
source: https://newbeebnb.cn/posts/codex-china-ccswitch-deepseek-guide
---

# 国内怎么用上 Codex？CC Switch + DeepSeek 三步配置实测

> 提醒：本文是工具配置教程，只讲怎么下载、怎么配置，不构成任何投资建议。文中软件请认准官方渠道下载。

## 一、Codex 好用在哪，又卡在哪

Codex 是 OpenAI 推出的桌面智能体工具。说人话：一个桌面 App，能帮你把日常的活干完——整理文档、写稿、跑脚本、处理那些重复点来点去的操作。

但它有个门槛：OpenAI 家的东西，正常得配 ChatGPT 账号 + 订阅。很多人就卡在这一步。

其实它只是个桌面客户端，底层接哪个模型是能换的。换成国内的 API 服务，一样跑得起来，还便宜不少。下面这套流程我自己走过一遍，全程不到 10 分钟。

Codex 的定位不是"聊天机器人"，而是能动手干活的智能体。它的强项在任务编排：知道什么时候该调工具、什么时候该反过来问你、什么时候该自己琢磨。

**它卡在哪**

- 需要 OpenAI 账号体系，正常路径要配 ChatGPT 订阅；
- 订阅要海外支付方式，这一步劝退了大半人；
- 官方订阅 20 美元/月，只是体验一下的话成本偏高。

**为什么有解**

Codex 是客户端，模型是后端。把后端从 OpenAI 换成国内可直连的 API 服务（比如 DeepSeek），功能照用，成本从"每月 20 美元"降到"几十块人民币用很久"。

## 二、两条路线怎么选

| | 官方订阅路线 | 国内平替路线（本文） |
|---|---|---|
| 需要准备 | ChatGPT 账号 + 海外支付方式 | 国内手机号 + 实名 + 几十块钱 |
| 月成本 | 约 20 美元 | 30 元能用很久 |
| 数据位置 | 请求走海外服务器 | 文件都在你本机 |
| 可用模型 | GPT 系 | DeepSeek / 通义千问 / GLM 等可切换 |
| 上手时间 | 卡在账号和支付门槛 | 约 10 分钟 |

一句话选路：想要官方模型的原味体验，走第一条；想省钱、想快、想把文件留在本地，走第二条。本文把第二条讲到底。

## 三、三步配置，不到 10 分钟

<img src="/images/posts/codex-china/w03.png" alt="Codex 官网下载页面" style="max-width:100%;height:auto;border-radius:10px;border:1px solid #e5e7eb;margin:14px 0">

**① 下载 Codex**

打开 Codex 官网下载安装包，Mac 和 Windows 都支持，安装流程和普通软件一样，下一步下一步。

<img src="/images/posts/codex-china/w04.png" alt="CC Switch 官网下载页面" style="max-width:100%;height:auto;border-radius:10px;border:1px solid #e5e7eb;margin:14px 0">

**② 安装 CC Switch**

CC Switch 是个开源的 AI 智能体网关代理工具，你可以把它理解成一个"转接头"——一头接国产 AI 服务，一头接 Codex。去官网下载即可，开源免费。

⚠️ 注意版本：**必须是 3.16.1 或以上**。低于这个版本，不支持在 Codex 里挂 DeepSeek、GLM。

<img src="/images/posts/codex-china/w05.png" alt="DeepSeek 官网进入 API 开放平台" style="max-width:100%;height:auto;border-radius:10px;border:1px solid #e5e7eb;margin:14px 0">

**③ 注册 DeepSeek 并拿 API Key**

打开 DeepSeek 官网，进的是**开放平台**（不是聊天页面）。注册需要实名认证，这是正常流程。然后充值——30 块钱日常使用绰绰有余。

进控制台 →「API Key 管理」→ 新建 Key，复制出来。

<img src="/images/posts/codex-china/w06.png" alt="DeepSeek 开放平台充值页面" style="max-width:100%;height:auto;border-radius:10px;border:1px solid #e5e7eb;margin:14px 0">

<img src="/images/posts/codex-china/w07.png" alt="DeepSeek API Key 管理页面" style="max-width:100%;height:auto;border-radius:10px;border:1px solid #e5e7eb;margin:14px 0">

**④ 把 Key 填进 CC Switch**

打开 CC Switch：左侧先选中 **GPT**，点右边的加号，供应商选 **DeepSeek**，把刚才的 API Key 填进去，应用。

<img src="/images/posts/codex-china/w08.png" alt="CC Switch 主界面选择 GPT 供应商" style="max-width:100%;height:auto;border-radius:10px;border:1px solid #e5e7eb;margin:14px 0">

<img src="/images/posts/codex-china/w09.png" alt="CC Switch 添加 DeepSeek 并填入 API Key" style="max-width:100%;height:auto;border-radius:10px;border:1px solid #e5e7eb;margin:14px 0">

**⑤ 重启 Codex**

重启之后就能正常用了。整个过程不到 10 分钟，不需要海外账号，也不需要信用卡。

## 四、装好之后怎么用（两个真实场景）

**场景一：把它当"文档工作台"**

这是最耐用的用法。先在电脑上建一个文件夹，然后告诉 Codex：这是我的写作/工作区，我关注什么领域、我的表达习惯是什么。

它不会上来就动手写，而是先给你一套组织方案——素材放哪、草稿怎么命名、截图丢哪个子目录。你确认，它就按这个节奏走。

之后每次开工开一个新会话，把想法、素材、语音转写的稿子、截图都丢进去。长文不是一次写成的，是今天冒个想法、明天补点素材、后天再打磨。**这套上下文它会一直记着**，这才是它和普通问答工具的区别。

组织起来之后，这个文件夹就不只是写作区了——学习笔记、工作文档、产品文档都能套同一个模式。它还有技能扩展，能调用上传图片、处理图片、发布到博客之类的工具，基本就是你的内容控制台。

<img src="/images/posts/codex-china/w10.png" alt="Codex 整理的写作工作区目录结构" style="max-width:100%;height:auto;border-radius:10px;border:1px solid #e5e7eb;margin:14px 0">

<img src="/images/posts/codex-china/w11.png" alt="Codex 对话界面与文件拖入工作流" style="max-width:100%;height:auto;border-radius:10px;border:1px solid #e5e7eb;margin:14px 0">

**场景二：让它自己研究接口**

这个场景最能看出它和同类工具的差别。

比如有件事：每天要打开某个网页、填信息、点确定。想让 AI 代劳，试过几个工具都没成——要么页面太复杂，要么它直接说做不到。

Codex 的思路不一样。它没有硬上浏览器去点，而是说：**"你自己操作一遍，把开发者模式里的接口请求信息发给我。"**

照做之后，它拿到请求参数和网址，很快写了个脚本，把 cookie 和 token 提取出来。原先没解决的问题，就这么解决了。

另一个例子：有七八个 App 安装包要传到内测平台，一个个填太麻烦。它同样先去研究那个平台，发现支持 API，于是让你去申请 Key，然后自己分析项目结构、找到编译产物、配好上传参数，自动打包、自动上传、自动更新信息。

**它的方法论是：先研究，再动手。** 不是蛮干，是找更省事的那条路。

注册入口（站内跳转，落地为官方注册页）：

- 👉 [币安注册入口（含 20% 手续费减免）](https://newbeebnb.cn/go?t=join)
- 👉 [欧易 OKX 注册入口](https://newbeebnb.cn/go?t=okxo)

## 五、常见问题（10 问）

**Q1. Codex 是什么？**

OpenAI 推出的桌面智能体（Agent）工具。与聊天机器人的区别在于它能实际读取文件、执行脚本、调用工具，按目标把任务做完，而不是只给建议。

**Q2. 国内用 Codex 一定要有 ChatGPT 账号吗？**

不一定。Codex 是桌面客户端，模型后端可替换。借助 CC Switch 这类网关代理工具把后端换成国内可直连的 API 服务，即可绕开账号与海外支付门槛。

**Q3. CC Switch 是什么？要收费吗？**

开源的 AI 智能体网关代理工具，用于把第三方 AI 服务的 API 接入 Codex。开源免费。注意版本需 3.16.1 以上，低于该版本不支持挂载 DeepSeek 和 GLM。

**Q4. 整套方案大概要花多少钱？**

成本很低。以 DeepSeek 为例，充值 30 元人民币日常使用可用很久，对比 ChatGPT 官方订阅约 20 美元/月。

**Q5. DeepSeek 注册需要实名认证吗？**

需要。DeepSeek 开放平台注册需完成实名认证，这是国内 API 服务的常规合规要求。

**Q6. 配置后可以切换成别的模型吗？**

可以。CC Switch 本身就是做转接的，更换 API Key 即可切换到通义千问、GLM 等国内模型，无需重装 Codex。

**Q7. 我的项目文件会被上传到云端吗？**

国内平替路线下项目文件保存在本机，由本地客户端读取处理，不强制上传。这也是不少人选择该方案的原因之一。

**Q8. 配好之后 Codex 主要能干哪些活？**

文档工作台（写作、笔记、项目文档整理与协作）、网页操作自动化、批量脚本执行、应用包自动打包上传发布等；也可通过技能扩展增加能力。

**Q9. 和 Claude Code 相比有什么差别？**

底层大模型可以完全相同，主要差异在智能体本身的设计。Codex 为可视化界面，会话管理更直观，支持侧边聊天——能够在不丢失当前上下文的前提下另开一条对话线。命令行形态的同类工具对普通用户门槛更高。

**Q10. 配置完成后 Codex 打不开或报错，先查什么？**

优先检查三点：CC Switch 版本是否不低于 3.16.1；API Key 是否填在 GPT 供应商项下；填写后是否重启过 Codex。这三点覆盖了绝大多数配置失败的情况。

## 六、如果你要的是官方 ChatGPT Plus

上面的方案走的是"够用、便宜、快"。如果你要的是官方原味体验（GPT 系模型、原生额度、官方功能更新第一时间可用），那就得走官方订阅路线——而这条路真正卡人的不是账号，是**支付**：需要一张能过海外支付的卡。

解决思路有两条：办一张实体海外卡，或者用加密支付卡。后者这几年在圈内用得比较多：把 USDT 充进卡里就能付，开卡门槛低，具体流程我们整理过一份完整教程：

👉 [Bitget Wallet Card 开卡全攻略：Fiat24 虚拟卡申请与绑定教程](https://newbeebnb.cn/posts/bitget-wallet-fiat24-card-guide-2026)

想先比较各家交易所的手续费和入金门槛，可以看[交易所对比](https://newbeebnb.cn/exchange-compare.html)。

---

<script type="application/ld+json">{"@context": "https://schema.org", "@type": "FAQPage", "mainEntity": [{"@type": "Question", "name": "Codex 是什么？", "acceptedAnswer": {"@type": "Answer", "text": "OpenAI 推出的桌面智能体（Agent）工具。与聊天机器人的区别在于它能实际读取文件、执行脚本、调用工具，按目标把任务做完，而不是只给建议。"}}, {"@type": "Question", "name": "国内用 Codex 一定要有 ChatGPT 账号吗？", "acceptedAnswer": {"@type": "Answer", "text": "不一定。Codex 是桌面客户端，模型后端可替换。借助 CC Switch 这类网关代理工具把后端换成国内可直连的 API 服务，即可绕开账号与海外支付门槛。"}}, {"@type": "Question", "name": "CC Switch 是什么？要收费吗？", "acceptedAnswer": {"@type": "Answer", "text": "开源的 AI 智能体网关代理工具，用于把第三方 AI 服务的 API 接入 Codex。开源免费。注意版本需 3.16.1 以上，低于该版本不支持挂载 DeepSeek 和 GLM。"}}, {"@type": "Question", "name": "整套方案大概要花多少钱？", "acceptedAnswer": {"@type": "Answer", "text": "成本很低。以 DeepSeek 为例，充值 30 元人民币日常使用可用很久，对比 ChatGPT 官方订阅约 20 美元/月。"}}, {"@type": "Question", "name": "DeepSeek 注册需要实名认证吗？", "acceptedAnswer": {"@type": "Answer", "text": "需要。DeepSeek 开放平台注册需完成实名认证，这是国内 API 服务的常规合规要求。"}}, {"@type": "Question", "name": "配置后可以切换成别的模型吗？", "acceptedAnswer": {"@type": "Answer", "text": "可以。CC Switch 本身就是做转接的，更换 API Key 即可切换到通义千问、GLM 等国内模型，无需重装 Codex。"}}, {"@type": "Question", "name": "我的项目文件会被上传到云端吗？", "acceptedAnswer": {"@type": "Answer", "text": "国内平替路线下项目文件保存在本机，由本地客户端读取处理，不强制上传。这也是不少人选择该方案的原因之一。"}}, {"@type": "Question", "name": "配好之后 Codex 主要能干哪些活？", "acceptedAnswer": {"@type": "Answer", "text": "文档工作台（写作、笔记、项目文档整理与协作）、网页操作自动化、批量脚本执行、应用包自动打包上传发布等；也可通过技能扩展增加能力。"}}, {"@type": "Question", "name": "和 Claude Code 相比有什么差别？", "acceptedAnswer": {"@type": "Answer", "text": "底层大模型可以完全相同，主要差异在智能体本身的设计。Codex 为可视化界面，会话管理更直观，支持侧边聊天——能够在不丢失当前上下文的前提下另开一条对话线。命令行形态的同类工具对普通用户门槛更高。"}}, {"@type": "Question", "name": "配置完成后 Codex 打不开或报错，先查什么？", "acceptedAnswer": {"@type": "Answer", "text": "优先检查三点：CC Switch 版本是否不低于 3.16.1；API Key 是否填在 GPT 供应商项下；填写后是否重启过 Codex。这三点覆盖了绝大多数配置失败的情况。"}}]}</script>

---

> 原文: [https://newbeebnb.cn/posts/codex-china-ccswitch-deepseek-guide](https://newbeebnb.cn/posts/codex-china-ccswitch-deepseek-guide)
