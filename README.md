# 你好，我是 Lokesh Cheng

### 把现实问题，做成可以操作、解释与验证的产品。

这里记录我在个人现金状态、复杂情景模拟、信息筛选和 AI 角色交互上的产品实践。我关注从问题定义、交互设计到数据边界与运行验证的完整过程。

**近期重点：Buffer（缓冲区）** · 个人现实状态与未来模拟工具

[Buffer](https://github.com/cheng-Lokesh/buffer) · [Astraloom](https://github.com/cheng-Lokesh/Astraloom) · [TradeSniper](https://github.com/cheng-Lokesh/tradesniper) · [星夜伴侣](https://github.com/cheng-Lokesh/StarNight_Companion)

---

## Buffer · 缓冲区

> 看清现在的现金现实，理解未来的变化，比较自己建立的假设。
>
> **缓冲区负责反映，不负责指导。**

面向收入不稳定时期，Buffer 将现金状态、持续收支与已知事项放进同一条可解释的未来轨迹。产品围绕三个问题展开：**现在是什么状态？当前条件持续时会怎样？改变条件后会有什么不同？**

### 四个空间，一条连续的观察路径

| 现在 | 未来 | 条件 | 记录 |
| --- | --- | --- | --- |
| 当前余额、可支撑时间、预计触及保留边界 | 30 / 60 / 90 天现金轨迹与假设对照 | 现金基础、固定收支、未来一次事项 | 已确认变化、事项核对与预测快照 |

### 最近的产品更新

- **查找具体日期或余额**：从图表旁直接定位日期，或查找余额首次不高于指定金额的时间，让曲线上的信息更容易找到。
- **组合试算**：叠加一次或周期收支、调整条件金额、按日期暂停条件，并保存或重新打开假设草稿。
- **更轻的现实更新**：通过余额确认、到期事项核对和一句话输入整理变化；自然语言解析只生成候选，经过程序校验与本人确认后才写入现实。
- **当前网站体验**：夜空全景、四空间布局与手机适配，让状态、轨迹和变化记录有清晰的阅读层次。
- **双端共用规则**：网页版与微信小程序持续统一现金计算、日期/金额查询、现实确认与组合试算的核心逻辑。

### 关键工程判断

**事实与假设分开。** 已确认现实是唯一事实来源；预测由现实推导；模拟草稿不能修改真实数据。预计事项到期后仍须核对，未知金额也不会被当作零。

**AI 的权力有边界。** 模型理解语言，代码校验，用户确认，代码写入。模型不能直接修改现金、条件或事项；复杂解析涉及外部服务时须明确披露。

**跨端能力按证据交付。** 账号配对、持久化同步、离线队列和冲突保护已有开发进展，真实设备与线上全流程验收仍在推进。

> **当前状态 · 2026-10：** 网站为受密码保护的试用阶段；公开服务、完整双端一致和自动同步的真实使用验收尚未完成。当前不提供公开访问入口，计划中的能力不等同于已上线能力。

`JavaScript` `Node.js` `确定性现金引擎` `LLM 结构化解析` `微信小程序` `CloudBase / PostgreSQL` `EdgeOne`

[查看项目 →](https://github.com/cheng-Lokesh/buffer) · [产品定义](https://github.com/cheng-Lokesh/buffer/blob/main/PRODUCT.md) · [最新实施状态](https://github.com/cheng-Lokesh/buffer/blob/main/docs/PUBLIC_SERVICE_IMPLEMENTATION_STATUS.md)

---

## Astraloom · 证据链驱动的多角色情景模拟

> 把复杂现实处境整理成可以检查、回溯和继续修正的模拟过程。

<a href="https://github.com/cheng-Lokesh/Astraloom">
  <img src="https://raw.githubusercontent.com/cheng-Lokesh/Astraloom/main/docs/assets/astraloom-overview.png" alt="Astraloom 人物关系与情景模拟界面" width="100%">
</a>

从现实材料、关键人物与 Agent Profile，到关系图谱快照、事件序列和证据化结论，探索复杂处境中的不同变化路径。

- **可追溯结论**：重要结论关联具体模拟事件。
- **稳定输入**：确认并锁定关系图谱快照，减少运行时输入漂移。
- **数据边界**：通过账户隔离与安全规则，区分现实事实、模型推断和未知信息。

`Next.js` `TypeScript` `Supabase` `Multi-Agent` `Knowledge Graph`

[查看项目 →](https://github.com/cheng-Lokesh/Astraloom)

---

## TradeSniper · 二手商品智能筛选

> 减少重复搜索，把大量商品缩小为值得人工判断的候选列表。

浏览器自动巡检先按关键词、价格与卖家规则过滤，再用 AI 分析描述并给出排序理由。桌面面板呈现日志、异常和候选结果，最终判断留给用户。

**工程重点：** 规则与模型协同、浏览器会话管理、采集与分析模块分离、运行过程可观察。

`Python` `Playwright` `Tkinter` `DeepSeek API`

[查看项目 →](https://github.com/cheng-Lokesh/tradesniper)

---

## 星夜伴侣 · 多角色 AI 聊天

> 探索稳定人设、场景上下文与连续记忆如何形成沉浸式交互。

<a href="https://github.com/cheng-Lokesh/StarNight_Companion">
  <img src="https://raw.githubusercontent.com/cheng-Lokesh/StarNight_Companion/main/docs/assets/starnight-overview.png" alt="星夜伴侣多角色聊天界面" width="100%">
</a>

支持预设角色、场景切换、独立本地会话、语音合成和会话导出。角色设定、场景与历史共同进入每轮请求，各角色的会话状态分别维护。

`Next.js` `React` `TypeScript` `Zustand` `MiniMax TTS`

[查看项目 →](https://github.com/cheng-Lokesh/StarNight_Companion)

---

## 我的构建方式

- **先明确问题与边界**，再决定 AI 介入的环节。
- **让中间过程可检查**，把模型输出放进结构化、可追溯的流程。
- **同时考虑桌面与手机**，处理异常、数据恢复与后续维护。
- **用实际运行验证结果**，清楚区分源码实现、自动化验证与真实上线。

持续探索：AI 原生产品、可解释模拟、个人现实观察工具与可信的人机协作。
