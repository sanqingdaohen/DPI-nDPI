# 时空规则用户画像 + few-shot —— 专利与论文调研

> **需求**（创新点）：
> 1. **基于时空规则的用户画像**：路由器在不同**时间**（时段/星期/季节）以及不同**小区**（区域/空间）下，都存在一个**预训练机制**（非常小的模型）——即"按时空维度预先训练好一批小模型，部署时按当前时空自动选用"。
> 2. **few-shot（少量样本）**：新场景/新应用只需极少样本即可快速适配识别与画像。
> **检索来源**：Patent9 专利在线（中国专利）+ arXiv API（论文）
> **检索规模**：`时空 用户画像` → 764 件发明；`小样本 流量 识别` → 1052 件发明；arXiv 两轮共 20+ 篇，以下均为**精选**。
> **链接说明**：专利给出 Patent9 详情页链接（已实测可打开）+ Google Patents 链接（需代理）；论文给出 arXiv 官方页面链接。

---

## 一、专利清单（按两个创新点分组）

### 创新点①：时空 / 时空规则 用户画像（764 件中精选）

| 专利 | 申请人 | 干什么的 | 链接 |
|---|---|---|---|
| **CN117131287A** 基于时空协同的用户画像个性化推荐 | 长城汽车 | 用户属性向量+行为序列向量→画像向量→聚类分群；**将时空因素作为触发条件**，满足条件即实时推送功能应用 | [Patent9](https://www.patent9.com/PatentDetails.aspx?PatentNo=202311125392.X) ｜ [Google Patents](https://patents.google.com/patent/CN117131287A/zh) |
| **CN118278970A** 基于大数据算法建设用户时空画像阵列 | 快付（厦门） | 采集全天操作行为，**标签衰减算法定义固定周期内不同时间维度的偏好**，抽取同一时间窗口内不同用户的相同业务，构建**用户时空画像阵列** | [Patent9](https://www.patent9.com/PatentDetails.aspx?PatentNo=202410381675.9) ｜ [Google Patents](https://patents.google.com/patent/CN118278970A/zh) |
| **CN111695046A** 基于时空移动数据表征学习的用户画像推断 | 清华大学 | 用户-地点带权图（时空模式相似度）+ 表征学习，无需大量特征工程即推断画像 | [Patent9](https://www.patent9.com/PatentDetails.aspx?PatentNo=202010328213.2) ｜ [Google Patents](https://patents.google.com/patent/CN111695046A/zh) |
| **CN121958839A** 基于GMM的电动汽车用户时空行为画像 | 南方电网贵州 | 时空行为特征系数 + 高斯混合模型，输出**时空行为画像聚类标签**（概率化软划分） | [Patent9](https://www.patent9.com/PatentDetails.aspx?PatentNo=202512054923.6) ｜ [Google Patents](https://patents.google.com/patent/CN121958839A/zh) |
| **CN107066458A** 基于车联网数据的时空维度用户画像分析 | 北京车网互联 | 从时间+空间两维度描述出行习惯，含"规律度描述、性质识别" | [Patent9](https://www.patent9.com/PatentDetails.aspx?PatentNo=201610742722.3) ｜ [Google Patents](https://patents.google.com/patent/CN107066458A/zh) |
| **CN121211153A** 用户实时画像更新方法及系统 | 深圳云中鹤 | 时序自注意力模型分析行为演化路径，冲突状态动态调整置信度，**反馈闭环局部更新画像** | [Patent9](https://www.patent9.com/PatentDetails.aspx?PatentNo=202511104502.3) ｜ [Google Patents](https://patents.google.com/patent/CN121211153A/zh) |

### 创新点②：few-shot / 小样本 流量识别（1052 件中精选，均为 DPI/流量方向）

| 专利 | 申请人 | 干什么的 | 链接 |
|---|---|---|---|
| **CN120602237A** 基于小样本增量学习的未知加密流量识别 | 哈工大（深圳） | 每类已知流量建 VAE 生成潜在表示→细粒度分类；评分函数判漂移/未知样本→分层聚类分配标签；**图注意力网络增量更新分类器**，支持新类低样本建模 | [Patent9](https://www.patent9.com/PatentDetails.aspx?PatentNo=202511100443.2) ｜ [Google Patents](https://patents.google.com/patent/CN120602237A/zh) |
| **CN119397466A** 基于小样本数据增强的异常网络流量识别 | 东北大学 | 流量转灰度图+孪生注意力网络；类间差异矩阵选训练域；对比学习生成增强集；**各边缘服务器用本地样本训练个性化模型** | [Patent9](https://www.patent9.com/PatentDetails.aspx?PatentNo=202510012248.8) ｜ [Google Patents](https://patents.google.com/patent/CN119397466A/zh) |
| **CN122179242A** 样本关联引导注意力的小样本恶意流量检测 | 空军工程大学 | 格拉姆角差场成像+样本关联注意力+**元学习框架预训练**+最近邻原型分类器，检测含未知攻击的流量 | [Patent9](https://www.patent9.com/PatentDetails.aspx?PatentNo=202610644559.0) ｜ [Google Patents](https://patents.google.com/patent/CN122179242A/zh) |
| **CN121365292A** 对比学习跨Tor版本域小样本网站指纹识别 | 东南大学 | 监督对比学习预训练+双分支置信对齐微调+原型驱动分类，**跨域小样本**网站识别 | [Patent9](https://www.patent9.com/PatentDetails.aspx?PatentNo=202511406752.2) ｜ [Google Patents](https://patents.google.com/patent/CN121365292A/zh) |
| **CN117640476A** 基于关系网络的小样本应用层协议识别 | 解放军61660部队 | 流量清洗→流重组→二维矩阵→**关系网络（relation network）小样本协议识别** | [Patent9](https://www.patent9.com/PatentDetails.aspx?PatentNo=202410090432.X) ｜ [Google Patents](https://patents.google.com/patent/CN117640476A/zh) |
| **CN119945789A** 基于LSTM的涉诈网络流量识别 | 北京赋乐科技 | 通信/行为特征加权可疑度评分（此前已收录，补充 few-shot 场景参考） | [Patent9](https://www.patent9.com/PatentDetails.aspx?PatentNo=202510133836.7) ｜ [Google Patents](https://patents.google.com/patent/CN119945789A/zh) |

---

## 二、论文清单（arXiv，按主题分组，均附官方页面链接）

### A. few-shot + 流量识别（创新点②直接支撑）

| 论文 | 年份 | 核心内容 | 链接 |
|---|---|---|---|
| **NetMamba+**：预训练模型的流量分类框架 | 2026 | Mamba+Flash Attention 高效架构；**预训练后 few-shot 能力强**（更少标注数据即达好效果）；在线系统吞吐 261.87 Mb/s | https://arxiv.org/abs/2601.21792 |
| **FlowletFormer**：网络行为语义感知预训练模型 | 2025 | BERT 式预训练，把流量切成"行为语义单元"；**同时提升分类精度与 few-shot 能力** | https://arxiv.org/abs/2508.19924 |
| **HLoG**：层级局部-全局特征的 few-shot 恶意流量检测 | 2025 | 滑窗分段+层级双向 GRU 捕获局部交互+全局上下文，会话相似度评估，few-shot 下低误报 | https://arxiv.org/abs/2504.03742 |
| **M3S-UPD**：多阶段自监督加密流量分类+未知发现 | 2025 | 自监督四阶段（嵌入生成→聚类→离群识别→模型更新），few-shot 加密分类+零样本未知发现 | https://arxiv.org/abs/2505.21462 |
| **Replication: Contrastive Learning + flowpic**（IMC 2023） | 2023 | 对比学习+数据增强，**100 个样本即可高精度**流量分类（flowpic 输入表示） | https://arxiv.org/abs/2309.09733 |
| **GETA**：通用加密流量分析（元学习） | 2026 | 元学习+自注意力+嵌入细化，**少样本跨域适配**（9 个数据集） | https://arxiv.org/abs/2605.31277 |
| **CBR**：检索式自适应分类（免重训练） | 2024 | 基于检索的方法**无需重训练即可识别新类别**（few-shot），可与 RF 等互补 | https://arxiv.org/abs/2403.11206 |
| **Packet Inspection Transformer**：自监督 few-shot 恶意流量 | 2024 | SSL 预训练 Transformer 学包内容嵌入，few-shot 适配未见恶意软件 | https://arxiv.org/abs/2409.18219 |

### B. 时空 + 流量（创新点①"不同时间×不同小区"直接支撑）

| 论文 | 年份 | 核心内容 | 链接 |
|---|---|---|---|
| **An Adaptive Framework for Generalizing Network Traffic Prediction** | 2023 | 无监督聚类时间序列识别"趋势与季节性模式"→每个簇训练专用模型→**为从未见过的新小区动态挑选最合适的模型，随时空波动自适应切换** | https://arxiv.org/abs/2311.18824 |
| **Graph-based Foundation Model for Network Traffic**（时空图） | 2024 | 把网络流量建模为**动态时空图**，自监督链路预测预训练，**few-shot 微调**即可适配入侵检测/流量分类/僵尸网络（平均 +6.87%） | https://arxiv.org/abs/2409.08111 |
| **TEST**：基于时空特征提取的端到端流量识别 | 2019 | CNN（空间特征）+LSTM（时间特征）自动提取，加密流量分类准确率 **99.98%** | https://arxiv.org/abs/1908.10271 |
| **DP-LET**：高效时空网络流量预测框架（GLOBECOM 2025） | 2025 | TCN 局部特征 + Transformer 长程依赖，蜂窝流量预测 MSE −31.8% | https://arxiv.org/abs/2504.03792 |
| **STHGCN**：时空混合图卷积网络流量预测 | 2020 | GRU 时序 + 混合 GCN 空间（邻近/功能相似/趋势相似三视角），蜂窝网络流量预测 | https://arxiv.org/abs/2009.09849 |
| **Time-Distributed Feature Learning for IoT NTC** | 2024 | 时间分布式特征学习提取包内/包间/流间伪时序+时空特征，IoT 流量分类 +13.5% | https://arxiv.org/abs/2409.05096 |

---

## 三、对你们创新点的启示（重点）

### 启示 1："时空规则 = 预训练小模型池 + 时空自选"有直接论文支撑
论文 **2311.18824**（[链接](https://arxiv.org/abs/2311.18824)）的做法：**先按时间序列聚类出若干"行为模式簇"，每个簇训练一个小模型，新小区来临时按实时测量自动选择最匹配的簇模型**——这正是你说的"不同时间/不同小区都有预训练机制（非常小模型）"。你们可把它从"流量预测"迁移到"用户画像"：
> 路由器侧预训练一组**按时段（早/晚/周末）和区域类型（家庭/办公/公共场所）划分的小画像模型**，部署时按当前时空上下文自动加载对应小模型 → 对应权利要求可写"**时空上下文感知的小模型动态加载方法**"。

### 启示 2：few-shot 与"时空画像"天然互补，论文已给出"时空×few-shot"先例
论文 **2409.08111**（[链接](https://arxiv.org/abs/2409.08111)，时空图基础模型）已经证明：**时空结构预训练 + few-shot 微调**可以在新环境快速适配。你们可写：
> 新路由器/新用户接入时，用**少量流量样本（如 100 条流，参考 IMC'23 flowpic [2309.09733](https://arxiv.org/abs/2309.09733)）**在预训练的时空小模型上微调，几小时内完成个性化画像——对应"**基于少量样本的时空画像快速初始化方法**"。

### 启示 3：专利占坑现状（写作时必须避开的雷区）
- ❌ "基于 LSTM/Transformer 的小样本流量识别"——已满（431+309 条在先）
- ❌ "小样本流量识别"泛泛写——1052 条在先
- ✅ 可写的差异点：**时空规则驱动的画像模型选择**（专利检索"时空 用户画像"764 条里，几乎没有"路由器/网关时空画像 + 小模型自动加载"的组合）；**画像+few-shot 的闭环**（先验画像指导少样本采样，少样本反馈更新画像）

---

## 四、给"明天"的汇报速览

1. **时空规则用户画像**：专利 764 件（车联网/电网场景为主，**路由器场景几乎空白**）；论文 2311.18824（小区级自适应模型分配）是最贴切的直接先例。
2. **few-shot 流量识别**：专利 1052 件（哈工大深圳增量、东北大学边缘增强、东南大学跨域指纹等 5 件精选）；论文 NetMamba+/FlowletFormer/flowpic（100 样本）/GETA 等 8 篇精选。
3. **两者结合（你们的差异化）**：目前"**时空预训练小模型池 + few-shot 快速适配**"的组合在专利库未检索到强占坑，是可写的创新空间。

---

## 附：检索记录与核验方式
- Patent9：`时空 用户画像`（764 件发明）、`小样本 流量 识别`（1052 件发明）——检索入口 https://www.patent9.com/ ，可用公开号/申请号反查核验
- arXiv：`"few-shot" AND "traffic classification"`（11 篇）、`"spatio-temporal" AND "network traffic"`（22 篇）——检索入口 http://export.arxiv.org/api/query
- 每个专利链接 = 申请号直达 Patent9 详情页；每篇论文链接 = arXiv 官方摘要页，均来自本次实际检索返回的原始数据
