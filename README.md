# Human-motion

面向 Human Motion 生成研究的文献调研与可视化研究图谱。从人体表示和数据来源出发，逐步理解动作估计、生成方法、多模态条件与自然交互。

**[打开调研网页 →](https://ZhikaiXu24.github.io/Human-motion/)**

## 当前内容

网页目前展示 10 篇已整理工作，沿着三层结构连续展开：

- **Representation Foundation**：SMPL、SMPL-X。
- **Dataset Evolution**：AMASS、KIT Motion、BABEL、HumanML3D、Motion-X、Motion-X++。
- **Motion Estimation & Reconstruction**：VIBE、HuMoR。

通过人体与动作示意图、数据依赖连线和方法流程，区分人体表示、数据集与估计方法。实线表示数据依赖或直接扩展，虚线表示研究能力的演进；AMASS 对 VIBE、HuMoR 的训练作用与测试时的观测输入分别呈现。点击论文卡片可查看贡献、技术流程及原文链接，也可切换训练与推理路径。

## 调研思路

先厘清 **数据与表示**，再理解 **评测协议**，最后比较 **方法与能力边界**。以下为完整的 50 篇阅读路线规划，并不表示网页已覆盖全部论文或已经完成全部精读。

| 阶段 | 范围 | 核心问题与代表工作 |
| --- | --- | --- |
| 人体表示与通用数据集 | 01–08 | 从 SMPL、SMPL-X、AMASS 到 KIT、BABEL、HumanML3D、Motion-X 系列：动作如何表示，数据来自哪里，文本如何标注，哪些数据复用了相同来源。 |
| Motion Estimation 背景 | 09–11 | VIBE、HuMoR、WHAM：视频如何变成动作，运动先验、相机运动、根轨迹与接触误差如何影响后续生成。 |
| 单人动作生成 | 12–20 | ACTOR、TEMOS、MDM、MLD、T2M-GPT、MotionGPT、MoMask、STMC、DART：比较潜空间、离散码本、自回归、扩散与组合控制。 |
| 音乐、舞蹈与群体编舞 | 21–26 | AIST++、Bailando、EDGE、FineDance、AIOZ-GDANCE、FreeDance：先看音乐—舞蹈数据与划分，再研究节拍、身体范围和群体协调。 |
| 自然对话手势 | 27–34 | 从 Trimodal Context、BEAT 到 DiffGesture、EMAGE／BEAT2、GestureDiffuCLIP、Audio2Photoreal 与 GENEA：区分动作自然性、语音适切性及对交谈者行为的响应。 |
| 双人、人—物与人—场景交互 | 35–39 | InterGen／InterHuman、Inter-X、InterAct、SAMP、BEHAVE：关注相对位置、接触、角色、空间约束与互动条件。InterAct 指 Ho 等人的双人日常互动工作。 |
| 头部生成与视频条件动画 | 40–46 | VOCA、FaceFormer、CodeTalker、SadTalker、First Order Motion Model、Animate Anyone、EMO：区分 3D 面部动作、显式运动系数和人物视频生成。 |
| 近期数据、规模化与在线模型 | 47–50 | Inter-X++、HY-Motion 1.0、Kimodo、ARDY：计划检查数据增量、统一表示、评测协议、空间控制与连续在线生成。 |

阶段性整理重点：

1. 建立“数据来源—人体表示—身体范围—模态—标注粒度”对照表；不将 AMASS 与其衍生数据集规模直接相加。
2. 将 HumanML3D 的数据、动作表示、划分与评测编码器一起阅读，明确后续实验的可比条件。
3. 对比 MDM、MLD、T2M-GPT、MoMask 的表示、训练目标、采样、控制方式与误差来源。
4. 区分身体、手指、面部的覆盖范围，以及单人动作、对话响应、多人互动和视频动画的任务边界。

## 使用方式

- **在线**：访问上方调研网页链接。
- **离线**：下载仓库，保留 `index.html` 与 `assets/` 的相对位置，双击 `index.html` 即可打开。
- 自然滚动浏览；点击论文卡片展开详情，按 `Esc` 或点击弹窗外关闭。

网页使用原生 HTML、CSS、JavaScript 与本地 SVG，无需构建、服务器、CDN 或远程字体。主要内容与交互可离线使用，跳转论文原文需要联网。

本项目用于学术调研与汇报；图形为技术示意，具体方法、实验设置与结论请以原论文为准。
