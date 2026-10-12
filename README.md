# Lokesh Cheng

### 产品设计 · AI 应用 · 可运行作品

我喜欢从生活中具体的问题出发，把想法做成能使用的产品：收入不稳定时如何看清自己的现金状况，面对复杂选择时如何梳理人物与影响，如何减少重复搜索，以及如何让 AI 对话更有连续性。

下面是我的四个个人项目。它们展示了我从需求整理、功能规划、界面设计到应用实现与验证的产品实践。

## 作品概览

| 作品 | 用来做什么 | 产品形态 |
| --- | --- | --- |
| [**Buffer · 缓冲区**](https://github.com/cheng-Lokesh/buffer) | 看清手里的钱还能支撑多久，比较收入或支出变化后的结果 | 网站、微信小程序开发 |
| [**Astraloom**](https://github.com/cheng-Lokesh/Astraloom) | 梳理复杂处境中的人物关系，用 AI 模拟不同变化，并查看结果的依据 | AI 情景模拟应用 |
| [**TradeSniper**](https://github.com/cheng-Lokesh/tradesniper) | 自动搜索二手商品，过滤干扰信息，整理值得进一步查看的候选 | 桌面工具原型 |
| [**星夜伴侣**](https://github.com/cheng-Lokesh/StarNight_Companion) | 与不同设定的 AI 角色聊天，切换场景，保留对话并播放语音 | AI 聊天网站原型 |

---

## Buffer · 缓冲区

### 现在有多少钱，按现有收支还能撑多久？

Buffer 是为收入不稳定时期设计的现金观察与试算工具。用户输入当前余额、日常支出、固定收支和已知的未来事项，网站就会画出未来 30、60、90 天的余额变化，帮助用户看清钱会怎样变化、什么时候会触及自己设定的保留金额。

![Buffer 当前网站：现金概览与未来曲线](assets/buffer-now-20261012.jpg)

<p align="center"><sub>当前网站实机截图 · 图中金额为演示数据</sub></p>

**用户可以做什么**

- **看现状：** 查看当前余额、预计可支撑时间和保留金额。
- **看未来：** 查询某一天预计还剩多少钱，或余额什么时候会降到指定金额。
- **比较变化：** 试算“下个月多一笔收入”“房租发生变化”等情况，并把多项变化放在一起比较。
- **更新现实：** 确认余额、核对已发生事项，或用一句话描述变化；系统整理后由用户核对保存。
- **查看记录：** 回看已确认的变化和当时的预测，保留备份并恢复数据。

**这个项目体现了我的产品思考**

将复杂的现金计算整理为“现在、未来、依据、记录”四个清晰入口；用曲线、金额和日期解释结果；让用户试算时始终保留真实数据。AI 用于减少输入负担，写入前必须经过用户确认。

网站采用夜空视觉与响应式布局，兼顾电脑和手机阅读；微信小程序围绕同样的现金规则持续开发。

<details>
<summary>查看当前网站的未来页面</summary>

![Buffer 当前网站：未来余额与日期查询](assets/buffer-future-20261012.jpg)

<p align="center"><sub>当前网站实机截图 · 演示数据</sub></p>

</details>

**技术应用：** JavaScript、Node.js、微信小程序、语言模型解析、CloudBase / PostgreSQL、EdgeOne。

[查看 Buffer 项目 →](https://github.com/cheng-Lokesh/buffer)

---

## Astraloom

### 把复杂的人物关系和现实选择，整理成可以查看过程的 AI 模拟。

面对职业、关系或家庭中的复杂选择，用户往往需要同时考虑多个人的立场与影响。Astraloom 根据用户提供的背景，整理关键人物、各自特点和人物关系，再用 AI 模拟可能发生的事件，让用户查看不同变化路径及其依据。

![Astraloom 人物关系与情景模拟界面](https://raw.githubusercontent.com/cheng-Lokesh/Astraloom/main/docs/assets/astraloom-overview.jpg)

**用户可以做什么**

- 输入背景、目标与限制，检查系统整理出的信息。
- 查看并确认关键人物和关系图谱。
- 运行多角色情景模拟，查看事件过程和结果。
- 从结论回到对应事件，检查依据，并补充反馈。

**这个项目体现了我的产品思考**

把一次复杂的 AI 分析拆成可检查的步骤，让用户能修改输入、确认人物关系、理解结果来源。设计中区分现实信息、AI 推断和未知内容，避免用一句看似确定的回答代替完整过程。

**技术应用：** Next.js、React、TypeScript、Supabase、React Flow、Three.js。

[查看 Astraloom 项目 →](https://github.com/cheng-Lokesh/Astraloom)

---

## TradeSniper

### 自动找二手商品，减少反复搜索和筛选。

用户设置商品关键词和价格范围后，TradeSniper 自动巡检商品列表，先按规则过滤疑似商家和无关信息，再用 AI 分析商品描述，给出候选列表与筛选理由。

桌面面板展示搜索日志、过滤过程和候选商品。用户可以集中查看值得进一步了解的结果，再自行联系卖家与判断商品。

**这个项目体现了我的产品思考：** 把重复浏览变成可观察的自动流程；用简单规则先处理明确问题，再让 AI 处理描述理解，保留人工判断环节。

**技术应用：** Python、Playwright、Tkinter、DeepSeek API。

[查看 TradeSniper 项目 →](https://github.com/cheng-Lokesh/tradesniper)

---

## 星夜伴侣 · StarNight Companion

### 有角色、有场景，也能接着上次对话聊下去的 AI 聊天网站。

用户可以选择五个不同设定的 AI 角色，在日常、校园、冒险等场景中聊天。每个角色保留独立对话记录，支持语音播放、多会话管理和聊天内容导出。

![星夜伴侣多角色聊天界面](https://raw.githubusercontent.com/cheng-Lokesh/StarNight_Companion/main/docs/assets/starnight-overview.jpg)

**这个项目体现了我的产品思考：** 将角色设定、场景和历史对话一起用于生成回复，让角色切换和连续对话保持清晰；同时处理文字、语音、等待与错误状态，兼顾电脑和手机使用。

**技术应用：** Next.js、React、TypeScript、Zustand、Tailwind CSS、MiniMax 对话与语音接口。

[查看星夜伴侣项目 →](https://github.com/cheng-Lokesh/StarNight_Companion)

---

## 这些作品背后的实践

- **把问题说清楚：** 从具体使用场景出发，确定产品解决什么、用户如何完成任务。
- **把流程设计清楚：** 整理信息和功能，让复杂逻辑能通过界面被理解和操作。
- **把 AI 放在合适的位置：** 用于理解、分析或对话，并保留必要的核对与人工决定。
- **把想法推进成作品：** 从需求与界面推进到应用实现，再通过实际操作和测试持续改进。
