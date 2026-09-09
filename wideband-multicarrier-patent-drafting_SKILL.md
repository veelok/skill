---
name: wideband-multicarrier-patent-drafting
description: 大带宽载波与多载波领域无线通信专利申请撰写技能。用于将大带宽载波（wide channel bandwidth/wideband carrier）与多载波（multi-carrier/carrier aggregation）相关的技术交底、3GPP提案或初步方案转化为中国、美国、欧洲及PCT专利申请的完整撰写框架、权利要求体系和说明书内容。覆盖单载波宽带化（200/400 MHz）、单宽带CC与多窄CC/CA关系、跨载波BWP与carrier-specific resource grid、多载波单小区/逻辑单小区、RF链边界与载波组合冲突、非对称UL/DL带宽、guard band/RB配置、跨载波参考、同步组与参考载波、6G RAN1/RAN4标准化等。当用户需要撰写大带宽载波或多载波领域的新申请、从交底书生成完整专利文稿（权利要求书+说明书+摘要）、进行3GPP标准对应分析或专利挖掘时使用。触发词：大带宽载波、wideband carrier、多载波、载波聚合、carrier aggregation、跨载波BWP、多载波单小区、RF链、RF-chain boundary、400MHz、写大带宽载波专利、撰写多载波专利。
---

# 大带宽载波与多载波领域专利申请文件撰写 Skill

## 1. Skill定位

本Skill用于无线通信领域“大带宽载波（wide channel bandwidth / wideband carrier）与多载波（multi-carrier / carrier aggregation）”相关中国、美国、欧洲及PCT专利新申请的技术方案梳理、标准对应分析、权利要求布局及说明书完整撰写。

适用主题包括但不限于：

- 单载波最大信道带宽扩展，例如200 MHz、400 MHz及其间其他带宽值；
- 单个宽带CC与多个较窄CC/CA之间的关系、选择、切换、等效处理或能力协同；
- 基站与UE、上行与下行之间的非对称channel bandwidth；
- irregular channel bandwidth、非整齐/非典型信道带宽及频谱适配；
- 最大传输带宽配置、RB数量、SCS、保护带、频谱利用率及其相互约束；
- 大带宽载波中的BWP、CORESET、PDCCH、PDSCH、PUSCH、PUCCH、PRACH、SSB、CSI-RS、SRS、DMRS等资源配置与映射；
- 400 MHz等宽带实现中的单RF链/多RF链、RF-chain boundary、基带与射频分段及逻辑单载波接口；
- 跨载波调度、cross-carrier scheduling、单/多DCI、单/多TB、HARQ、CSI及测量；
- 多载波之间的参考关系，包括参考载波、目标载波、调度载波、被调度载波、UL/DL paired/unpaired carrier、TA/定时参考；
- 宽带场景的功率、PAPR、峰值抑制、相位连续性、功率一致性、联合信道估计；
- 宽带UE能力、网络能力、带宽组合、RF链能力、CA能力的上报与配置。

本Skill的核心目标不是简单把技术交底扩写成长文，而是把技术方案转化为：

1. 可对接3GPP演进的标准化特征；
2. 可在中美欧获得稳定说明书支持的多层次技术特征；
3. 可形成宽、中、窄多个保护层次的权利要求体系；
4. 可覆盖终端侧、网络侧、装置、芯片、介质、程序产品等不同实施主体；
5. 可在后续标准落地时方便做claim chart和标准必要性分析。

---

## 2. 资料来源与证据边界

### 2.1 新申请模板

以用户提供的《新申请撰写输出模板》作为文档结构、措辞风格、实施例展开方式和权利要求架构的主要模板来源。

必须继承的模板特征包括：

- “技术领域—背景技术—发明内容—附图说明—具体实施方式—权利要求书—摘要”的完整结构；
- 发明内容优先采用“第一方面/第二方面/第三方面……”的多方面结构；
- 终端方法与网络方法镜像撰写；
- 方法之后配置模块/单元型装置、处理器型装置、芯片/芯片系统、通信系统、计算机可读存储介质、计算机程序产品等保护客体；
- 每个关键可选设计后说明其技术作用/有益效果；
- 对“第一/第二”“至少一个”“多个”“和/或”“指示”“配置”“预定义/预配置”等通用术语建立解释；
- 明确“指示”覆盖直接/间接、显式/隐式，且待指示内容可以整体发送或拆分发送；
- 配置方式覆盖RRC、DCI、SIB、预配置以及必要时的其他信令；
- 对相同技术目标至少展开多个实现层次，例如资源粒度不同、跨边界/不跨边界、相同/不同预编码、绝对值/偏移值等；
- 对装置、芯片、接口电路、处理器及软件实现提供完整落脚点。

### 2.2 公开专利样本

本Skill的专利样本经验库包括：

- CN 112020145 A；
- CN 115314984 A；
- CN 117835425 A；
- CN 117857274 A；
- CN 116746242 A；
- WO 2026/132931 A1；
- WO 2026/132934 A1；
- WO 2026/123262 A1。

其中，2026-08-13新增的五件样本（92099476CN01、92111937CN01、92115288CN01、92115289CN01、92118256CN01）为已提交/已批准的中国专利申请，重点用于补强以下撰写方向：载波切换与时序控制的参数化写法、参数多层递进与双轨列表模式、频域资源四层抽象体系、M=N/M=N-1/M=N+1多分支bitmap指示、数学公式在权利要求中的嵌入规范、连续载波的多层次定义和终端侧负向行为写法。

此前2026-08-13新增的四件样本重点用于补强以下撰写方向：RF前端共享资源造成的多载波组合冲突；multi-carrier single-cell下跨多个carrier-specific resource grid的逻辑BWP；per-carrier与joint CORESET/FDRA指示；多载波同步组、参考CC与动态资源激活。

证据边界：

- CN116746242A、WO2026132931A1、WO2026123262A1已取得可核验的公开说明书/权利要求或较完整公开文本；
- WO2026132934A1已核验公开日、申请人、发明人、PCT申请号、优先权及摘要。当前检索环境未稳定取得其完整权利要求正文，因此本Skill仅使用其已核验摘要所明确支持的UL BWP/FDRA特征，不将未核验细节写成该案事实；
- WO2026132931A1与WO2026132934A1具有相同标题、申请人及发明人，但分别具有不同PCT申请号和不同美国临时申请优先权。二者作为并行申请的组合可用于启发“将DL控制资源、DL/UL数据资源分配等标准化轴拆分为不同申请”的组合布局策略；该布局结论属于基于公开书目信息和摘要的专利策略推断，而非对其内部申请策略的事实认定。

### 2.3 3GPP来源

重点跟踪：

- 3GPP TR 38.760-1《Study on 6G Radio RAN1 aspects》；
- R4-2602139，6G system parameter (part I)相关Topic Summary；
- RP-260798，RAN#111涉及7 GHz最大channel bandwidth的plenary文档。

注意：TR 38.760-1当前仍属于Release 20研究阶段草案。任何“proposal / view / discussion / working assumption / agreement / plenary way forward”必须区分状态，不能将公司观点或工作组讨论写成已经冻结的规范要求。

---

## 3. 角色设定

运行本Skill时，你是一名无线通信领域资深专利代理人/专利工程师，同时具备：

- 3GPP LTE、5G NR、5G-Advanced与6G RAN1/RAN4技术背景；
- 大带宽载波、载波聚合、多RF链、BWP、频域资源分配、RF requirement方面的专业知识；
- 中国、美国、欧洲专利申请文件撰写和审查实践经验；
- 从标准化提案/agreement中抽象专利技术特征并进行claim layering的能力；
- 避免新增事项、说明书支持不足、术语不一致、纯结果性限定和标准术语过度绑定的能力。

---

## 4. 核心技术抽象框架

收到技术交底后，不得直接开始写权利要求。先把方案映射到以下技术维度。

### 4.1 带宽维度

至少识别：

- carrier/channel bandwidth；
- maximum channel bandwidth；
- transmission bandwidth / maximum transmission bandwidth configuration；
- occupied bandwidth；
- active bandwidth/BWP bandwidth；
- aggregated channel bandwidth；
- UL bandwidth与DL bandwidth；
- BS bandwidth与UE bandwidth；
- 100/200/400 MHz等离散值以及“第一带宽大于第二带宽”的相对关系；
- 位于两个标准带宽值之间的intermediate bandwidth；
- regular/irregular channel bandwidth。

不要在独立权利要求中无必要地固定“200 MHz”或“400 MHz”。优先写相对关系或能力关系，再在从属权利要求中落到具体数值。

### 4.2 频域资源维度

至少区分：

- carrier/CC；
- BWP；
- RB/PRB；
- RBG；
- PRG；
- REG/REG bundle；
- RE；
- subcarrier；
- contiguous resource与discrete/non-contiguous resource；
- guard band；
- RF-chain boundary两侧资源；
- 载波边缘与BWP边缘。

每个方案至少考虑“粗粒度”和“细粒度”两个实施例。例如：carrier/BWP级 + RB/RBG级，或PRG级 + RB级。

### 4.3 载波关系维度

对多个载波，不仅写“第一载波、第二载波”，还应检查是否存在：

- serving carrier / non-serving carrier；
- scheduling carrier / scheduled carrier；
- source carrier / target carrier；
- reference carrier / referenced carrier；
- paired DL/UL carrier；
- unpaired UL或unpaired DL carrier；
- primary/secondary carrier或PCell/SCell；
- activated/deactivated carrier；
- measured carrier / reporting carrier；
- transmitting carrier / receiving carrier；
- carrier group / TAG / band / frequency range。

优先把“载波身份”和“载波功能”分开定义，避免权利要求只能覆盖固定PCell/SCell或固定UL/DL场景。

### 4.4 RF实现维度

大带宽载波必须检查：

- 一个RF chain处理整个channel bandwidth；
- 两个或更多RF chains共同处理一个逻辑载波；
- 每个RF chain对应第一/第二频域部分；
- RF chain boundary是否限制PRG、REG bundle、CORESET、SSB、CSI-RS、DMRS或数据资源映射；
- 两个RF链是否共享/独立LO、PA、LNA、ADC/DAC、FFT/IFFT、滤波器或基带处理；
- 两侧频域资源是否具有相同/不同增益、相位、功率、时延或校准参数；
- UE视角是否仍表现为一个CC、一个BWP、一个DCI、一个PDSCH/PUSCH或一个TB。

说明书应同时覆盖“物理上分段、逻辑上统一”和“物理与逻辑均分段”两类架构。

### 4.5 信令维度

每个核心参数都至少检查以下指示方式：

- RRC半静态配置；
- DCI动态指示；
- MAC CE（如适用）；
- SIB/系统信息（如适用）；
- capability reporting；
- pre-defined / pre-configured；
- explicit indication；
- implicit determination；
- absolute value；
- offset/delta；
- index/table；
- bitmap；
- ratio；
- number/count；
- range；
- one-bit selection；
- jointly indicated与separately indicated。

独立权利要求优先使用“根据第一信息确定……”或“第一信息用于指示……”等功能化上位表达；从属权利要求再限定具体信令载体。

### 4.6 多载波单小区/逻辑资源层级维度

当交底涉及多个物理载波但希望向UE呈现统一调度或单小区行为时，必须建立至少四层资源抽象：

1. **物理载波层**：第一CC、第二CC……，每个CC保留其carrier-specific frequency-domain resource grid；
2. **载波内资源层**：每个CC上的sub-BWP、RB/RBG/PRG/REG bundle、CORESET、参考信号资源；
3. **逻辑BWP层**：由多个CC上的资源集合按配置顺序组合/拼接形成的DL/UL BWP；
4. **逻辑小区层**：多个CC作为一个serving cell或single logical cell为UE提供统一控制、调度、测量或同步。

撰写时至少检查：

- 多个CC是否相邻/非相邻、同频段/跨频段；
- 各CC资源集合大小是否相同；
- 逻辑顺序是否等于物理频率顺序，还是由serving-cell index、RRC配置顺序或其他规则确定；
- resource set是否允许跨CC边界，还是RBG/PRG/REG bundle被限制在单个CC内；
- 是否需要保留每个CC自身的Point A、CRB0或其他reference point；
- 同一组物理CC是否需要同时兼容“multi-carrier single-cell UE”和“single-carrier single-cell UE”。

### 4.7 联合配置/独立配置双轨维度

凡是多个CC共享一个逻辑BWP或逻辑小区的方案，至少成对展开：

- **per-carrier/separate**：每个CC分别配置/指示资源；
- **joint/common**：多个CC通过一个联合字段、联合bitmap、联合RIV或共同配置进行指示。

联合与独立两条路径至少检查：

- RRC配置：多个独立IE vs 单一联合IE；
- CORESET：per-carrier bitmap vs joint bitmap；
- RB offset：每CC独立offset、offset list、共同reference+offset；
- DCI FDRA：多个carrier-specific FDRA字段 vs 单一joint FDRA字段；
- Type-0/Type-1 FDRA是否分别支持；
- bitmap/字段中每个CC占用的bit block如何确定；
- 不同CC资源大小/粒度不同情况下字段长度如何计算；
- 参考信号序列是否per-carrier确定或基于联合FDRA统一确定。

独立权利要求可以先上位写成“一个或多个资源分配指示”，从属权利要求再分别落到separate indication与joint indication。

### 4.8 同步组/参考载波与动态激活维度

当多个CC共享同步、参考信号或激活机制时，必须检查：

- 是否配置一个component-carrier group / synchronization group / cell subgroup；
- 组内是否配置多个候选synchronization reference resources；
- 是否指定reference CC；
- 一个参考资源是否适用于多个CC，UE是否上报这种适用能力；
- 参考CC是否可动态改变；
- 资源配置是否分为component-carrier agnostic与component-carrier specific两类；
- PDSCH/PUSCH等通信资源是否joint mapping到多个CC或仅映射到一个CC；
- UL mapping与DL mapping是否可以不同；
- 激活信息是否同时指示CC、BWP、SSB、CSI-RS、PUCCH、PRACH或其他resource category/resource ID；
- 是否支持“在第二CC使用DL参考资源，为第一CC的UL BWP/UL-only activation提供同步”；
- carrier on/off、reference-signal on/off、load balancing、energy saving是否成为动态激活触发场景。

### 4.9 RF前端共享资源/载波组合冲突维度

多载波能力不应只按band combination从协议层描述，还应下钻到UE RF实现：

- 哪些band/CC共享同一个RF front-end resource set、RX path、duplexer、LNA、filter、switch或SDR port；
- 哪些载波组合可完全并发，哪些组合会导致retuning、Rx diversity丢失、完全调离或性能退化；
- 发生资源冲突时，是抑制/去激活某CC、降低优先级、改变测量报告、还是修改capability advertisement；
- 冲突判断是否依赖CC是否configured/activated、grant数量、业务优先级或订阅状态；
- 能力报告是否应排除不支持的band/carrier combination，而不是仅报告最大CC数量。

对大带宽载波而言，该维度同样适用于“一个逻辑宽带CC由多个RF前端资源共同实现”时的内部冲突、共享和优先级管理。

---

## 5. 从新申请模板提炼的固定撰写规则

### 5.1 背景技术

背景技术采用三段式：

1. 标准/系统演进背景；
2. 现有机制；
3. 在大带宽/多载波场景下暴露的具体问题。

避免在背景技术中提前给出本发明解决方案。

可优先使用以下问题类型：

- 单载波带宽扩大后，传统资源映射/控制信令不适配；
- UE与BS带宽能力不一致；
- UL/DL带宽不一致；
- 单RF链能力不足，需要多个RF链但希望维持单载波空口行为；
- 大带宽使保护带、RB数量、频谱利用率出现新的权衡；
- BWP/SSB/CORESET/PRG/REG跨RF链边界造成处理复杂度或性能损失；
- 单一参考载波无法为另一载波提供定时/功率/测量参考；
- 多CC实现增加DCI/HARQ/CSI/射频切换开销；
- 宽带信号PAPR、功率一致性、相位连续性或校准难度增加。

### 5.2 发明内容

推荐至少形成：

- 第一方面：终端侧方法；
- 第二方面：网络侧方法；
- 第三方面：终端侧装置；
- 第四方面：网络侧装置；
- 第五方面：处理器/接口电路型通信装置；
- 第六方面：通信系统；
- 第七方面：计算机可读存储介质；
- 第八方面：计算机程序产品；
- 第九方面：计算机程序（如模板/法域需要）。

如果发明具有两个真正独立的技术核心，例如“宽带资源确定”与“跨RF链边界调度”，可以形成两个方法独立发明组，但必须先检查单一性和商业价值。

### 5.3 “在一种可能的设计中”展开方法

每个独立方案至少从以下层次展开4—8组可选设计：

- 参数定义；
- 资源位置/范围；
- 资源粒度；
- 信令方式；
- 计算/确定规则；
- 边界情况；
- UE能力差异；
- 网络能力差异；
- 单RF/多RF实现；
- UL/DL镜像或非对称；
- 单载波/多载波替代实现；
- 技术效果。

### 5.4 技术效果写法

不得只写“提高性能”。至少建立“特征—机制—效果”链：

> 技术特征A改变/限制了机制B，因此减少/避免问题C，从而获得性能D。

大带宽领域常用效果包括：

- 提升频谱利用率；
- 降低保护带或控制开销；
- 在保持保护带要求的同时增加可用RB；
- 避免资源跨RF链边界导致的处理复杂度；
- 允许低能力UE接入高带宽载波；
- 降低UE射频复杂度和功耗；
- 保持单CC调度语义，减少CA控制复杂度；
- 提升频率分集；
- 提高信道估计/CSI测量精度；
- 保证相位连续性或功率一致性；
- 降低PAPR；
- 提高宽带调度灵活性。

### 5.5 说明书撰写通用规则（华为全球撰写指南）

以下规则来自华为全球专利申请撰写指南，适用于所有法域的首次申请。

#### 5.5.1 开放式术语

说明书应使用开放式术语，不可直接说"the invention"（本发明）。正确做法：

- 发明内容中使用"方面"（aspects）和"实施方式"（implementation forms）；
- 具体实施方式中使用"实施例"（embodiments）或"示例"（examples）；
- 使用"在某些实施例中""本发明的示例提供""在一个说明性实施例中"等表述。

**禁止**：将具体实施例称为"本发明"本身，也不应将任何实施例称为"优选实施例"。

#### 5.5.2 强制性语言与非强制性语言

- 强制性语言（"是"、"配置为"、"用于"）仅用于描述aspects、implementation forms和embodiments；
- 非强制性语言（"可以"、"可选地"）仅用于描述真正可选的非必要特征；
- **禁止**使用"仅"、"必须"、"关键"、"必要"、"重要"、或"绝不可"等绝对化用语。

#### 5.5.3 申请人定义术语

- 权利要求术语通常按其在本领域技术人员中的普通含义解释；
- 若使用申请人自定义术语，必须在说明书中**清晰、无歧义**地定义；
- 若术语在相关技术领域的普通含义已为技术人员普遍理解，则无需额外定义。

#### 5.5.4 中文申请中的英文术语

- 中文申请中首次出现英文术语时，应同时提供完整英文和中文：
  - 格式："特征xx，英文称为feature xyz"
  - 格式："通用串行总线（Universal Serial Bus，USB）存储器"
- 大带宽/多载波领域的高频术语（如guard band、BWP、CORESET、FDRA、RF chain、carrier aggregation等）应在首次出现时按此格式处理。

#### 5.5.5 发明名称

- 发明名称应清晰、简洁，使用所属技术领域通用技术术语，优先使用国际专利分类中的术语；
- **不需要**在发明名称中包含发明核心或目的；
- 在中国，发明名称不超过25个汉字；在美国和欧洲无强制字数和内容要求。

### 5.6 背景技术安全规则（华为全球撰写指南）

背景技术部分具有极高的法律风险——任何内容都可能被认定为"申请人自认现有技术"（AAPA），且无法更改。

#### 5.6.1 绝对禁止

- **禁止**在背景技术中描述本发明或本发明的任何特征；
- **禁止**使用"现有技术"、"常规"、"已知"等术语——应使用"参考文献"（reference）；
- **禁止**解释或概括现有技术，即使是引用专利文献的描述也应使用该文献自身的术语；
- **禁止**描述具体的"发明目的"（objects），这会导致权利要求限缩解释；
- **禁止**引用未公开的申请或内部文件；
- **禁止**引用未公开的标准或标准草案。

#### 5.6.2 推荐做法

- 背景技术仅描述到足以区分本发明的程度；
- 只包含有物理证据（已公开专利、期刊论文等）的内容；
- 不确定是否应提及的内容一律删除；
- 如果技术问题是发明人首次识别的，不应写入背景技术，而应写入发明内容；
- 对华为自身在先专利/申请，避免负面评价（可以说"改进"但不能说"不能正常工作"或"有缺陷"）；
- 在背景技术中描述的缺点必须是本发明确实能解决的问题。

### 5.7 发明内容撰写规范（华为全球撰写指南）

#### 5.7.1 aspects/implementation forms 结构

发明内容应以"方面"（aspects）和"实施方式"（implementation forms）的形式组织权利要求树，覆盖所有可设想的特征组合：

- 每个独立权利要求称为"第一方面"（first aspect）、"第二方面"（second aspect）等；
- 每个从属权利要求称为"第一方面的一种实施方式"（implementation form）；
- 每个aspect和implementation form应**按数字顺序编号**；
- 每个implementation form的引入应引用其依赖的aspect和先前implementation forms。

#### 5.7.2 多重引用的权利要求树

为满足某些法域（如EP）要求在首次申请时公开所有可能的特征组合：

1. 先起草多重引用权利要求（multi-reference claims）；
2. 将权利要求作为"aspects"和"implementation forms"插入发明内容（保留多重引用）；
3. 将权利要求部分的多重引用简化为单一引用（发明内容中保留多重引用）；

这样即使首次申请只提交单一引用权利要求，说明书也保留了所有组合的公开基础。

#### 5.7.3 技术效果/优势写法

- 每个aspect和每个implementation form必须说明其技术效果/优势；
- 技术效果必须与技术特征直接关联，形成"特征→机制→效果"链；
- 技术问题必须确实由独立权利要求所定义的技术方案解决；
- 若某技术效果仅在特定约束条件下实现，必须说明该约束条件；
- **禁止**使用"本发明的实施例具有以下优点或有益效果"的风格——直接描述效果即可。

#### 5.7.4 发明内容结语

发明内容应以类似以下语句结束：
> "本发明的这些和其他方面将从下文描述的实施例中显而易见并将参照这些实施例予以阐明。"

---

## 6. 公开专利样本提炼的撰写经验

### 6.1 CN112020145A：离散频域资源/部分子载波映射

核心可复用经验：

1. 不停留在“扩大频域跨度”的效果层面，而是用N、M、L、K等参数建立可验证的资源关系；
2. 将资源分布进一步参数化为位置、编号、步长、资源数量、比例等；
3. 同时覆盖网络显式指示与终端依据预设规则确定；
4. 同时覆盖连续频域范围内选择部分RB、以及跨多个RB的离散映射；
5. 对“物理占用较少资源但经历更宽频域范围”的技术效果建立明确因果关系；
6. 终端侧与网络侧完全镜像；
7. 对新概念（如离散资源块）说明“名称不构成限定”，避免术语锁死。

迁移到大带宽/多载波领域时，可转化为：

- 宽带carrier内稀疏/离散资源映射；
- 多个frequency segment之间的分布式分配；
- 跨RF chain segment选择部分RB；
- 通过步长、比例、偏移、bitmap或索引确定资源；
- 用少量激活资源获得更大频域采样跨度。

### 6.2 CN115314984A：跨载波定时参考与载波解耦

核心可复用经验：

1. 将“目标载波”与“参考载波”解耦；
2. 参考关系既可直接指示具体载波，也可通过TAG/载波组等间接确定；
3. 采用“reference + adjustment/offset”的结构撰写；
4. 覆盖没有paired downlink carrier的UL carrier等异常/边界场景；
5. 对timer、TAG、DL timing、UL timing等已有机制建立多种组合关系；
6. 网络侧和终端侧镜像。

迁移到本领域时，任何多载波方案都应检查：

- 定时参考是否跨载波；
- 功率控制参考是否跨载波；
- pathloss reference是否跨载波；
- CSI/测量参考是否跨载波；
- beam/TCI/QCL reference是否跨载波；
- 宽带载波的一个frequency segment是否参考另一segment的参数。

### 6.3 CN117835425A：宽带波形中的PAPR/峰值抑制资源

核心可复用经验：

1. 用“数据资源两侧的第一部分和第二部分”描述频域几何关系；
2. 覆盖两侧资源数量不相等的非对称分配；
3. 把数量关系进一步表达为ratio、number、granularity multiple、rounding rule；
4. 同时覆盖信令指示和预定义参数；
5. 用少量比特选择不同映射方案，形成信令压缩从属层；
6. 将物理波形、资源位置、生成处理链和多用户资源复用分别展开；
7. 对UL和DL或不同发送主体进行镜像/变形保护。

迁移到大带宽场景，应特别写：

- 载波两端或RF链边界两侧资源是否对称；
- guard band/PRT/unused tones能否复用；
- 参数是否必须是RB或其他粒度的整数倍；
- 如何用比例/索引减少大带宽配置开销。

### 6.4 CN117857274A

本版本不对其技术内容作实质推断。后续如获取全文，执行：

1. 提取独立权利要求；
2. 提取说明书中所有资源层级、载波关系和信令方式；
3. 建立“技术特征—写法—可迁移经验”三列表；
4. 与上述三件样本去重后更新本Skill。

### 6.5 CN116746242A：RF前端资源冲突驱动的载波抑制与能力修剪

该案虽然主要针对多订阅/多SIM场景，但对多载波与大带宽RF实现具有高度可迁移价值。核心撰写经验：

1. **先建立“载波组合—硬件资源”关系，再定义协议动作。** 权利要求不是抽象地说“避免冲突”，而是先确定第一/第二频带共享RF前端资源集，再基于该硬件关系处理第三频带/SCC；
2. **把冲突处理展开为多级动作。** 包括丢弃/抑制SCC、降低载波优先级、通过经补偿测量促使网络去配置、抑制测量报告、根据grant数量决定是否保留载波；
3. **覆盖configured但未activated与已经activated两类状态。** 这类状态分支适合迁移到SCell、sub-BWP、RF segment、reference resource等对象；
4. **把RF限制前移到capability阶段。** UE可在能力报告中排除会导致不可并发/完全调离的band combination；
5. **硬件约束与协议行为之间建立因果链。** “共享RF前端资源→不能完全并发→选择/抑制特定SCC→维持其他载波通信”是完整技术闭环。

迁移到大带宽/多载波申请时，应固定增加：

- RF frontend sharing/conflict matrix实施例；
- “配置但未激活/已激活/正在调度”三态处理；
- per-carrier priority与保留/抑制规则；
- capability report中支持/排除的carrier combination；
- 逻辑单宽带CC内部多个RF segment之间的共享硬件冲突管理。

### 6.6 WO2026132931A1：multi-carrier single-cell下的跨载波BWP、CORESET和FDRA

该案是本Skill新增的核心样本。其公开文本将多个物理载波的资源统一到一个逻辑BWP，并保留carrier-specific resource grid。核心经验：

1. **把“多个载波”抽象为“一个逻辑BWP中的多个carrier-specific resource grids”。** 每个carrier保留自己的reference point，并可对应不同大小的resource set；
2. **用资源集合拼接定义逻辑BWP。** 多个carrier上的RB/REG bundle/RBG/PRG可按配置顺序concatenate，逻辑顺序不必等于物理频率顺序；
3. **明确支持相邻/非相邻、同band/跨band载波。** 这样保护范围不锁定于连续频谱；
4. **CORESET同时布局separate RRC与single/joint RRC。** per-carrier bitmap与joint bitmap并列，并利用per-carrier RB offset对齐carrier-specific grid；
5. **FDRA同时布局per-carrier与joint DCI。** 多个carrier-specific FDRA字段可以分别指示，也可以在一个joint field中按carrier block拼接；
6. **Type-0与Type-1分别展开。** 字段长度与carrier数量、各sub-BWP大小、RBG数量、start/size和granularity建立关系；
7. **将sub-BWP作为连接物理CC与逻辑BWP的中间层。** 多个configured/active sub-BWPs形成覆盖多个carrier的dedicated BWP；
8. **把carrier boundary写成资源映射约束。** 可配置carrier-specific BWP portion，使RBG/PRG被限制在单一carrier内；
9. **参考信号序列也要跟随跨载波FDRA展开。** DMRS/PTRS等序列可基于resource-set mapping与实际FDRA分别确定；
10. **强调与legacy/single-carrier operation共存。** 通过carrier-specific reference grid、offset等设计，使同一组物理载波可以同时服务multi-carrier single-cell UE和legacy/single-carrier UE。

本案对申请文件的直接启示是：凡主方案涉及“多个窄载波获得类似宽带单载波的统一调度”，说明书必须至少写出“逻辑资源坐标系、物理载波坐标系、拼接顺序、边界规则、separate/joint control、legacy compatibility”六层。

### 6.7 WO2026132934A1：UL跨载波BWP与一个或多个FDRA指示

已核验的公开摘要明确给出：接收包含两个或更多carrier-specific frequency-domain resource grids信息的dedicated UL BWP configuration；在接收到调度UL数据传输的DCI时，基于DCI中的一个或多个FDRA indications确定跨多个carrier的UL FDRA，并据此发送UL数据。

可复用经验：

1. **UL方向应形成可独立商业化/标准化的权利要求主线。** 不要默认DL多载波BWP的文字支持当然覆盖UL；
2. **“one or more FDRA indications”是很好的上位写法。** 独立权利要求保留joint/separate两种空间，从属权利要求再拆分；
3. **UL BWP本身应显式包含carrier-specific grid信息。** 避免只写“跨多个载波发送PUSCH”而缺少统一资源坐标关系；
4. **并行申请布局启示。** WO2026132931A1与WO2026132934A1具有相同标题、相同申请人/发明人、同日PCT提交但不同临时优先权；从公开摘要看，前者的摘要重心在DL BWP/CORESET/DCI，后者重心在UL BWP/FDRA。对于标准必要性强且技术轴相对独立的方案，可评估是否将DL控制、DL数据、UL数据、同步/激活等拆成平行申请或后续分案，以减少单一权利要求组过度拥挤并提高对标清晰度。该结论是专利布局策略推断，具体案件需结合优先权支持、单一性和法域实践判断。

### 6.8 WO2026123262A1：多载波同步组、共享参考资源与动态激活

该案把多个CC进一步抽象为“组”，并围绕同步参考和资源激活建立完整配置—激活两阶段架构。核心经验：

1. **configuration与activation分层。** RRC等高层先配置group、候选reference resources、mapping和共享参数，随后MAC CE等动态信令选择实际激活资源；
2. **配置多个候选同步参考资源，再动态选择一个。** 这比固定reference carrier更利于load balancing、energy saving和carrier on/off；
3. **reference CC可动态改变。** 说明书应覆盖reference carrier的静态指定、隐式确定和动态切换；
4. **能力上报与组配置联动。** UE可上报同一同步参考资源适用于哪些CC，网络据此形成carrier group/subgroup；
5. **共同配置与carrier-specific配置并存。** group内既可存在component-carrier agnostic参数，也可保留per-carrier参数；
6. **joint mapping与single-carrier mapping并存。** PDSCH/PUSCH等channel resource可映射到多个CC，也可只映射到其中一个CC，且UL/DL mapping pattern可以不同；
7. **动态激活信令面向“资源类别+资源ID”。** 可扩展到BWP、SSB、CSI-RS、PUCCH、PRACH等多个资源对象；
8. **跨carrier、跨link-direction参考。** 可在第二CC使用DL同步参考资源，并把同步结果用于激活第一CC的UL BWP；
9. **宽DL/窄UL、UL-only activation应作为固定边界实施例。** 这与6G asymmetric UL/DL bandwidth专利挖掘高度相关。

### 6.9 四件新增样本的综合撰写规则

新增样本共同表明，多载波申请应从“列举多个CC”升级为以下六层结构：

1. **硬件层**：RF front-end sharing / concurrency / conflict；
2. **物理载波层**：carrier-specific resource grid与reference point；
3. **逻辑资源层**：sub-BWP/resource set拼接成跨载波BWP；
4. **控制层**：separate vs joint RRC/DCI/FDRA/CORESET；
5. **参考与激活层**：carrier group、reference CC、synchronization reference resource、dynamic activation；
6. **能力与兼容层**：UE capability、band/carrier combination、legacy single-carrier coexistence。

以后运行本Skill，只要交底出现“多个载波联合使用”“多个载波像一个大带宽载波一样工作”“单小区多载波”“载波组”“共享RF链/参考信号”等表述，就必须逐层检查上述六层，不得只围绕PDSCH/PUSCH调度写一组权利要求。

### 6.10 92099476CN01：载波切换与时序控制

该案涉及同小区内下行载波间切换（BWP切换或休眠/去休眠），以及Intra-gNB-DU LTM场景下的处理时延优化和上行功率控制。核心撰写经验：

1. **"第一信息"功能化上位**：独立权利要求仅用"第一信息用于指示从第一载波切换到第二载波"，不限定是DCI、MAC CE还是RRC，具体信令类型全部留在从属权利要求中展开；
2. **时间偏移参数化**：T1=接收时间+第一时间偏移，T2=HARQ反馈时间+第二时间偏移，T5=max(T3, T4)，用参数化公式替代具体数值，保护范围不受固定定时关系限制；
3. **终端能力分层**：明确区分"不具有第一能力（不支持并行接收）"和"具有第一能力（支持并行接收）"两条路径，每种能力对应不同的行为规则，说明书应同时覆盖两种能力等级；
4. **切换方式并列**：BWP切换和休眠/去休眠作为两种平行实现方式，在从属权利要求中分别限定，利用"或"逻辑拓展保护维度；
5. **跨载波HARQ进程共享**：将载波切换与时序控制延伸至HARQ重传维度，第一载波和第二载波可关联相同的HARQ进程，实现跨载波数据传输和重传的灵活性。

### 6.11 92111937CN01：参数化序列设计与多层递进

该案将PSS（主同步信号）序列从m序列替换为ZC序列。虽然主题是同步信号，但其参数化撰写的多层递进和双轨列表设计对任何涉及参数配置的专利具有通用参考价值。核心撰写经验：

1. **三层参数递进模式**：第一层—功能化等价限定（"ZC序列长度≤M，M与最低能力UE带宽能力相关"）；第二层—具体数值范围（"M=180"）；第三层—优选值列表（11个质数取值），从宽到窄逐层收束，每一层独立成权利要求；
2. **双轨原则+列表模式**：权利要求7用功能性原则描述根索引选取（"大频偏下时域偏移值≤第二阈值"），不依赖具体值；权利要求8、9分别给出两组完整候选值列表（时延优先/频偏优先），两组列表互相独立，覆盖不同优化方向；
3. **开放式枚举**："包括如下的一项或者多项：value1、value2、……"确保每个值可单独作为保护范围，同时支持任意组合；
4. **12个方面全覆盖**：终端侧/网络侧方法、四种装置形态（模块型/处理器型/逻辑电路型/芯片）、系统、存储介质、程序产品，全面覆盖所有实施主体；
5. **"对比分析"式背景引入**：先用m序列缺陷（需多次频偏假设）对比ZC序列优势（时频二元性，一次计算），用具体数值示例增强说服力。

迁移到大带宽/多载波领域时，可转化为：
- 大带宽下RB数量/保护带/频谱利用率的参数多层递进（功能化关系→公式→具体数值表）；
- 多个候选资源配置方案的双轨列表（覆盖不同优化目标，如频谱利用率优先vs保护带最小化）；
- 序列长度/根索引的开放式枚举写法适用于任何需要候选值列表的参数（如BWP大小、CORESET频域资源、SSB频域位置等）。

### 6.12 92115288CN01：大带宽频域资源层级划分

该案直接针对大带宽载波场景，通过指示频域边界位置将频域资源集合划分为两个子集合，与现有技能的RF-chain boundary和频域资源维度高度互补。核心撰写经验：

1. **四层资源抽象体系**：第一频域资源集合（大带宽载波）→第一/第二频域资源子集合（由频域边界划分）→第三/第四频域资源子集合（网络设备实际调度的资源）→具体功能（TBS/CB/CBG/信道估计/预编码/CSI/PDCCH），独立权利要求仅用前两层，从属权利要求逐层下位；
2. **偏移量间接指示**：第一频域位置通过第一偏移量（相对于第二频域位置）间接指示，第二频域位置可枚举为Point A、公共RB频率位置、载波位置、SSB关联位置、第二频域资源集合位置等5种可能，减少信令开销同时适配多种参考系；
3. **8个从属梯度设计**：偏移量指示→参考位置枚举→参考资源集合具化→独立通信功能（调度资源级）→独立通信功能（测量/控制级）→指示粒度→信令承载方式→大带宽触发条件，从手段到约束到场景，层层递进；
4. **多种信令承载方式全覆盖**：PBCH、SIB、RRC信令，覆盖不同RRC状态；
5. **大带宽触发条件**：带宽条件（"第一频域资源集合带宽>终端单TB最大带宽"）放在最末从属权利要求，避免在独立权利要求中引入不必要的场景限制。

### 6.13 92115289CN01：频域单元切分与bitmap指示

该案在92115288CN01基础上进一步下位到频域单元（RB/RBG）级切分，核心撰写经验在于多分支bitmap指示设计：

1. **M=N/M=N-1/M=N+1三值分支**：处理bitmap中M个比特指示N个频域单元（含切分单元）的关系——M=N时剩余1比特用于指示切分单元/子单元（三种子方式），M=N-1时两子单元分别与相邻频域单元共同指示（节省开销），M=N+1时两子单元分别独立指示（提高准确性），每个分支对应不同的技术效果权衡；
2. **频域单元粒度覆盖**：独立权利要求使用"频域单元"上位概念，从属权利要求仅覆盖RB和RBG两个粒度，说明书中进一步扩展PRG、CSI子带、CORESET等更多粒度，为后续分案留有余地；
3. **子单元独立功能列表**：第一频域子单元和第二频域子单元可分别独立用于TBS确定、TB/CB/CBG资源映射、信道估计、预编码、CSI测量/上报、PDCCH资源确定，共列举8种功能，形成"切分→独立功能"的完整技术闭环；
4. **忽略子单元场景**：当网络设备仅调度某个子集合中的子单元时，终端可忽略该子单元以降低数据处理开销，覆盖节省功耗的边界场景；
5. **16个方面极致覆盖**：终端侧/网络侧方法×2（第一信息+第二信息），加上装置、系统、芯片、存储介质、程序产品共16个方面。

### 6.14 92118256CN01：连续载波配置与公式约束

该案将两个物理载波配置为频域连续（取消保护间隔），并通过gap比例约束调度降低PAPR，核心撰写经验在于数学公式在权利要求中的嵌入和约束条件的定义：

1. **公式在权利要求中的嵌入**：连续载波的定义用频率起始位置等式表达（f_{0,0}+N_{RB,0}×N_{sc}^{RB}×f_{scs}=f_{0,1}），gap约束用不等式表达（L_GAP_all/(L1+L2+L_GAP_all)≤const），每个变量均在公式后用"其中"段落逐一定义，变量含义映射到物理量；
2. **"连续"的多层次定义**：权利要求中只使用"在频域上连续"上位表述，说明书中展开为三层等价定义——保护间隔=0、子载波级差值=子载波间隔、频率起始位置等式，确保不同解读层面均有说明书支持；
3. **终端侧忽略逻辑**：当gap比例>const时终端忽略调度信息，这种"条件不满足→不执行"的负向行为分支是保护终端侧独立可实施性的重要撰写手段；
4. **复合参数定义**：L_GAP_all = L_GAP1（载波内gap）+ L_GAP2（载波间gap）+ GB（保护间隔转化的RB等效值），将频率间隔通过子载波带宽换算为RB数量，统一到同一量纲；
5. **BWP级连续**：在载波连续的基础上进一步配置跨载波边界的连续BWP，形成"载波连续→BWP连续→资源调度"三层递进保护。

### 6.15 五件新增样本的综合撰写规则

新增五件样本共同表明，大带宽/多载波领域申请应从以下维度强化撰写质量：

1. **参数表达维度**：优先使用功能化关系（"与……相关""满足……条件"）而非具体数值，形成"功能化→数值范围→优选值列表"三层递进梯度；数值列表使用开放式枚举（"包括如下的一项或者多项"）；
2. **多分支展开维度**：对M=N/M=N-1/M=N+1等多值关系、多种切换方式、不同能力等级等场景，在从属权利要求中形成独立分支，每个分支对应不同的技术效果；
3. **资源层级维度**：建立"资源集合→资源子集合→调度资源→具体功能"至少四层抽象，独立权利要求仅用前两层；
4. **时间与时序维度**：时间参数优先用公式表达（T1=接收时间+偏移、T5=max(T3,T4)），不写死具体时长；
5. **公式嵌入维度**：数学公式可在权利要求中直接使用，但每个变量必须逐一用"其中"段落定义，并将频率/时间/数量等物理量统一到同一量纲；
6. **负向行为维度**：为终端侧增加"条件不满足→忽略/不执行"的负向行为分支，增强终端侧独立可实施性。

---

## 7. 3GPP 6G大带宽/多载波标准化启示

### 7.1 TR 38.760-1

TR 38.760-1是Release 20的6G RAN1 study TR。运行本Skill时必须优先检查最新版本，而不能固化当前草案内容。

当前可用于专利挖掘的高价值问题包括：

- wider channel bandwidth（至少200 MHz级别）对PHY设计的影响；
- 大带宽下的DL/UL control和shared channel设计；
- 单个宽带传输与多个较窄传输的关系；
- 资源映射、HARQ、测量、参考信号、波形和RF实现的耦合；
- BWP是否继续承担低能力UE接入宽载波的复杂度隔离角色。

### 7.2 R4-2602139

R4-2602139的6G system parameter讨论对专利布局最重要的不是单一数值，而是以下参数维度：

- maximum single-carrier channel bandwidth；
- 200 MHz与400 MHz级别方案的比较；
- 400 MHz支持是否作为某类UE/实现的可选能力；
- asymmetric UL/DL channel bandwidth；
- irregular channel bandwidth；
- guard-band consistency及不同channel bandwidth/SCS下保护带设计；
- RF和性能要求随channel bandwidth扩大而变化。

必须注意：Topic Summary中可能同时存在多家公司view/proposal。只有明确的agreement/working assumption/plenary decision才能写成“3GPP已同意”；其他内容应写为“讨论方向/候选方案”。

### 7.3 RP-260798

RP-260798是RAN#111与约7 GHz场景最大channel bandwidth相关的关键plenary文档。本次环境已确认该文档存在于官方3GPP RAN#111文档目录，但未稳定解析到ZIP内完整正文。

因此，本Skill的硬规则是：

- 在具体案件中引用RP-260798的数值、单RF/双RF实现、UL/DL最大带宽或单DCI/PDSCH等结论前，必须重新获得并核对原文；
- 未取得原文时，可以把这些方向作为“专利挖掘问题”，不得作为已冻结标准事实写入申请背景或法律意见；
- 对任何plenary way forward，应进一步跟踪其如何进入TR 38.760-1及后续RAN1/RAN4 agreement。

---

## 8. 大带宽/多载波专利挖掘矩阵

对每份技术交底，必须逐项询问/推导下列问题。即使交底未写，也应作为“待补充问题”列出，不得无依据直接写入申请。

### A. 单载波 vs 多载波

- 一个400 MHz逻辑载波是否可由两个200 MHz RF处理段实现？
- 与2CC CA相比，空口可观察行为有什么不同？
- UE是否看到一个CC还是两个CC？
- 是否只有一个cell ID、一个BWP集合、一个DCI、一个HARQ process、一个TB？
- 是否允许在单CC模式和CA模式之间切换？触发条件是什么？

### B. RF-chain boundary

- PDSCH/PUSCH可否跨boundary？
- PDCCH/CORESET可否跨boundary？
- PRG、REG bundle、RBG能否跨boundary？
- SSB、CSI-RS、SRS、DMRS是否跨boundary？
- 跨boundary时预编码、功率、相位、定时是否相同？
- 是否需要校准信息/补偿信息？

### C. UL/DL非对称

- DL bandwidth > UL bandwidth时，UE如何选择UL frequency portion？
- UL BWP和DL BWP如何关联？
- RA/PUCCH/SRS/PUSCH位于何处？
- DL全带宽测量如何由较窄UL能力支持反馈？
- UL载波是否必须与某一DL segment配对？

### D. Guard band / RB数量 / 频谱利用率

- 新带宽下最小保护带如何确定？
- RB数量由公式、表格、比例、向上/向下取整还是候选集合确定？
- 是否满足“更宽载波频谱利用率不低于较窄载波”的约束？
- 是否同时要求绝对保护带增大？
- 不同SCS下规则是否一致？
- 是否存在边缘RB、partial RB或不可调度RB？

### E. Capability与配置

- UE上报max DL/UL CBW分别是多少？
- 是否上报single-RF / multi-RF capability？
- 是否上报可同时处理的frequency segments数量？
- 是否上报single-CC 400 MHz能力和2CC CA能力分别？
- 网络如何根据能力选择配置？
- 能力是per band、per band combination还是per UE？

### F. 调度与控制

- 一个DCI调度一个宽带PDSCH还是多个segment？
- 频域资源分配字段如何扩展？
- RIV/bitmap/VRB-to-PRB mapping是否变化？
- MCS、TB size、HARQ、RV如何跨segment处理？
- 跨carrier/segment是否共享search space、CORESET或TCI？

### G. 测量和参考信号

- CSI-RS是否覆盖整个宽带或分segment？
- CSI report按wideband/subband/segment上报？
- 不同segment是否具有独立CQI/PMI/RI？
- SRS是否扫过多个frequency portion？
- 测量gap/retuning是否需要？

### H. 功率、PAPR、相位与校准

- 总功率在多个segment/RF链之间如何分配？
- 是否存在per-segment power scaling？
- DMRS/数据功率关系是否跨boundary一致？
- RF链之间是否要求phase continuity / power consistency？
- PAPR reduction tones如何放置？

### I. Multi-carrier single-cell / 跨载波逻辑BWP

- 多个CC是否对UE表现为一个logical cell？
- 是否形成跨多个CC的dedicated DL/UL BWP？
- 每个CC是否保留独立Point A/CRB0/resource grid？
- 多个resource sets如何排序/拼接？
- carrier的逻辑顺序与物理频率顺序是否可以不同？
- 不同CC上的resource set大小是否不同？
- RBG/PRG/REG bundle是否允许跨CC boundary？
- 相邻/非相邻、同band/跨band是否均覆盖？
- legacy single-carrier UE如何与multi-carrier single-cell UE共存？

### J. Joint vs separate resource indication

- CORESET是per-carrier RRC配置还是single/joint配置？
- per-carrier bitmap与joint bitmap如何构造？
- 是否存在per-carrier rb-offset / offset list？
- FDRA是多个carrier-specific indication还是一个joint indication？
- Type-0/Type-1是否分别覆盖？
- joint field内各carrier block的长度/顺序如何确定？
- 不同carrier的RBG/PRG granularity不同时如何编码？
- DMRS/PTRS/CSI-RS序列或映射如何随joint FDRA确定？

### K. Synchronization group / reference carrier / activation

- 是否配置CC group/subgroup/synchronization group？
- 是否存在多个候选同步参考资源？
- reference CC是否静态、隐式或动态确定？
- 同一reference resource可否服务多个CC？
- UE是否上报reference applicability capability？
- group参数哪些是common/agnostic，哪些是carrier-specific？
- PDSCH/PUSCH mapping是joint还是per-carrier？
- UL与DL mapping pattern是否不同？
- 激活信令是否以resource category + resource ID方式编码？
- 是否支持carrier on/off、BWP/SSB/CSI-RS/PUCCH/PRACH动态激活？
- 是否支持跨CC/跨link-direction同步参考？

### L. RF front-end conflict / capability pruning

- 哪些CC/band共享RF front-end resource set？
- 哪些组合可完全并发，哪些会引起retuning/脱谐/RxD或MIMO能力损失？
- 冲突时优先抑制PCC/SCC中的哪一类？依据是什么？
- configured但未activated与active CC处理是否不同？
- 是否根据grant数量/业务量/优先级决定去激活？
- 是否通过修改测量结果或抑制测量报告促使网络调整配置？
- capability report是否排除不支持的band/carrier combination？

---

## 9. 权利要求布局规则

### 9.1 独立权利要求原则

独立权利要求应抓住“最少但足够形成技术闭环”的特征。

推荐结构：

> 一种通信方法，包括：
> 获取/接收/确定第一信息；
> 根据所述第一信息确定第一载波/第一频域资源的第一参数或第一资源配置；
> 基于所述第一参数或第一资源配置执行发送、接收、调度、测量或处理；
> 其中，第一对象与第二对象满足能够体现发明点的结构/关系/约束。

避免把背景参数、所有信令字段、具体标准名称一次性塞入权1。

### 9.2 推荐独立权利要求族

根据交底内容可选择以下一项或多项：

1. **宽带资源确定型**：根据载波带宽确定RB数量/可用频域资源/保护带；
2. **RF链边界型**：根据RF链对应的frequency portion确定资源映射或调度；
3. **UL/DL非对称型**：根据第一方向带宽确定第二方向资源/参考关系；
4. **single-CC vs CA型**：在逻辑单载波和多个处理单元之间建立映射；
5. **跨载波参考型**：目标载波基于另一载波的定时/功率/测量参数工作；
6. **能力协商型**：UE上报宽带/RF链能力，网络据此配置；
7. **宽带测量型**：分segment测量、合并或报告；
8. **宽带功率/PAPR型**：根据资源分布确定功率或峰值抑制资源；
9. **multi-carrier single-cell资源网格型**：基于多个carrier-specific resource grids构造跨载波DL/UL BWP并执行控制/数据资源分配；
10. **joint/separate资源指示型**：通过一个或多个RRC/DCI资源分配指示确定多个载波上的CORESET或FDRA；
11. **同步组/参考资源激活型**：配置多个CC的候选同步参考资源并动态激活其中一个，用于组内多个CC同步/激活；
12. **RF前端冲突管理型**：基于载波间共享RF前端资源关系选择、抑制、去激活或降低特定载波优先级；
13. **能力组合修剪型**：基于RF并发能力或共享参考能力上报支持/不支持的carrier combinations或carrier group能力。

### 9.3 从属权利要求梯度

从属权利要求优先按以下顺序形成保护梯度：

- 对象定义；
- 相对关系；
- 具体数值；
- 资源粒度；
- 资源位置；
- RF实现；
- 信令实现；
- 计算公式；
- 边界处理；
- UE能力；
- 网络能力；
- 具体信道/信号；
- 具体技术效果对应的限制。

### 9.4 数值与公式

涉及RB数量、保护带、频谱利用率、带宽、比例、offset时：

- 独立权利要求优先使用关系式或约束；
- 说明书必须给出变量定义、单位、边界值、取整规则；
- 同时给出公式表达和非公式文字表达；
- 对floor/ceil/round、整数倍、候选集合分别提供实施例；
- 若存在200 MHz对应547/548/549 RB等候选，说明书应同时支持“候选集合”“网络配置”“协议预定义”“按约束计算”四种确定路径（仅在交底或标准材料支持时使用）。

---



### 9.5 标准对标权利要求策略（华为全球撰写指南）

对于标准相关申请，权利要求撰写应遵循以下原则：

#### 9.5.1 使用标准语言

- 申请应使用与标准相同的语言，减少后续claim construction争议；
- 不要使用华为内部术语或非标准术语，除非其含义等同于标准术语；
- 在中文申请中，重要术语同时提供英文（标准语言）对照。

#### 9.5.2 宽窄结合策略

- 独立权利要求使用比标准更宽泛的术语以获得广泛保护，保护的范围应覆盖标准的所有当前和未来版本；
- **至少一套权利要求**应精确对标标准的确切措辞，以加速授权和便于许可/专利池使用；
- 其他权利要求组可以在从属权利要求中复制标准的确切措辞；
- 独立权利要求应覆盖实现标准相关部分的多种不同方案。

#### 9.5.3 概念权利要求对照表

- 建议准备"概念权利要求对照表"（concept claim chart），将发明的高层概念与标准文本对应；
- 这有助于专利审查委员会聚焦发明的关键特征，也有助于撰写人员使用标准语言，提高权利要求对标标准的可能性。

#### 9.5.4 标准提交文本的注意事项

- **谨慎**从标准贡献或提案中直接复制文本——标准提案和专利申请的目标不同；
- 标准提案中的限制性表述（如"该问题不打算由本方案覆盖"、"xxx是必需的"）必须删除；
- 标准提案中适合的窄定义（如具体数值范围）在专利申请中通常**不适当**。

#### 9.5.5 加速授权策略

- 对于需要加速授权的标准相关案件，可将独立权利要求有意窄化，加入更多限制但仍保持对标准和计划的对标；
- 目标是在明显区别于已知现有技术的前提下获得授权，后续可通过继续申请（continuation）争取更宽权利要求；
- 注意可能需要对原始申请和继续申请之间的期限作出终端免责声明（terminal disclaimer）。

### 9.6 权利要求撰写禁止项与最佳实践（华为全球撰写指南）

#### 9.6.1 语言清晰性

- 使用清晰、明确的语言；
- 避免使用"基本上"、"约"、"大约"、"几乎"、"高"、"大"、"小"等模糊术语——若必须使用，应在说明书中精确定义；
- 缩写词至少在首次使用时在说明书中完整说明，最好在每个部分（背景、发明内容、具体实施方式、摘要）首次使用时都说明。

#### 9.6.2 消除不必要限制

- 独立权利要求只包含区分已知现有技术所必需的限制，避免不必要限制；
- 避免在权利要求前序部分（preamble）加入不必要的描述或限制；
- 避免使用改进型格式（Jepson型权利要求）。

#### 9.6.3 方法权利要求步骤

- **不要对方法步骤排序**，除非必要——美国法律下，除非权利要求中明确声明步骤按所述顺序执行，否则不解释为按顺序执行；
- 不要用字母或数字标记每个步骤（(a),(b),(c)或(1),(2),(3)），因为这暗示步骤顺序。

#### 9.6.4 数量与组合

- 不要使用复数形式（如"移动站们"），除非确实需要多于一个该要素才能克服现有技术；
- 使用"comprising"和"including"（开放组），**避免**"consisting of"或"consisting essentially of"（封闭组）；
- 最佳实践：使用"comprising"和"further comprising"来区分主要权利要求特征与前序，使用"including"来进一步定义已述及的权利要求特征。

#### 9.6.5 单一实体侵权

- 权利要求应尽可能覆盖单一实体（如基站供应商、处理器供应商）制造或实施的项目；
- 至少有一套装置权利要求应由单一供应商直接侵权（如"a processor **configured to** perform..."），而非仅由最终用户侵权（如"a processor performing..."）；
- 确保权利要求容易利用——每项权利要求应由价值链中的单一当事方侵权。

#### 9.6.6 权利要求形式

- 首次申请的权利要求应使用**一体式**（one-part form），而非两段式；
- 每个从属权利要求最好只包含一个权利要求要素或一组相关要素；
- 替代方案应写入不同的从属权利要求（如颜色、材料、形状分别依赖不同的从属权利要求），除非各替代方案之间存在互斥关系；
- 权利要求应使用**正面描述**（positive recitations），避免负面限定。

#### 9.6.7 多重引用

- 初稿应包含多重引用权利要求（可满足EP等法域的要求，在首次申请时公开所有可能的特征组合）；
- 如果首次申请在美国提交，多重引用权利要求应改为单一引用；
- 注意：USPTO将多重引用每项计为单独权利要求以计算费用；且美国不允许多重引用权利要求引用其他多重引用权利要求。

#### 9.6.8 附图标记与品牌名称

- 首次申请时**不要在权利要求中加入附图标记**；
- 权利要求中不要使用品牌名称来标识权利要求要素；
- 避免在权利要求中使用缩写词——如果使用，必须在说明书中定义；
- 确认术语是本领域公知术语而非公司内部术语。

### 9.7 装置权利要求US特化原则（华为全球撰写指南）

#### 9.7.1 避免means-plus-function

- 在美国，means-plus-function权利要求被解释为仅限于说明书中描述的对应结构及其等同物，保护范围较窄；
- 申请的权利要求不应全部由means-plus-function权利要求组成；
- 应包含描述结构的非功能性权利要求。

#### 9.7.2 避免"module"和"unit for doing something"

- 在美国，"module"和"unit for doing something"可能被解释为纯软件实现（不符合35 USC 101），或被作为means-plus-function处理；
- 建议使用："a processor configured to..."、"a transmitter configured to..."、"a receiver configured to..."；
- 推荐硬件术语：transceiver, transmitter, receiver, memory, processor, modulator, demodulator, antenna, display, detector, controller, encoder, decoder, circuit, circuitry, integrated circuit。

#### 9.7.3 三种硬件装置权利要求风格

根据实际产品选择以下三种风格之一：

1. **处理器型**：An apparatus comprising a processor configured to xx（如US 2010/0284377）；
2. **存储器型**：An apparatus comprising a memory storing instructions or routines, the instructions or routines is configured to xx（如US 5,946,647）；
3. **处理器+存储器型**：An apparatus comprising a processor and a memory that are configured to perform certain functions with other components（如US 5,657,317）。

#### 9.7.4 硬件产品与虚拟装置双轨

- 说明书应至少包含两类装置实施例：一类对应实际硬件产品（放在前面），另一类对应虚拟装置（使用模块/单元描述）；
- 实际硬件产品实施例应尽可能反映实际产品的硬件结构；
- 通用计算机的必要组件（如输出单元、输入单元、接口）即使不是发明的改进部分，也应在申请中描述——这有助于克服US 101/112驳回，但不应在说明书中将其标识为"本领域公知"。

#### 9.7.5 软件/介质权利要求

- 虽然计算机可读存储介质在中国不能获得保护，但在EP和US可以——因此首次申请应在说明书中包含相应实施例；
- 考虑写入"计算机程序使处理器执行前述方法权利要求"的权利要求，覆盖初始安装和软件升级两种场景；
- 对于纯软件发明，可在说明书中描述相关算法或流程图作为"结构"来支持装置权利要求。

---
## 10. 说明书实施例固定展开顺序

### 实施例0：系统与术语

- 网络架构；
- UE/网络设备；
- carrier、CC、BWP、RB、channel bandwidth等定义；
- “第一/第二”“指示”“配置”“预定义”等通用解释。

### 实施例1：核心流程

画终端—网络时序图，给出最小核心流程。

### 实施例2：参数与资源关系

用频域示意图说明：

- 整个channel bandwidth；
- transmission bandwidth；
- guard bands；
- BWP；
- first/second frequency portion；
- RF-chain boundary；
- 具体RB/RBG/PRG/REG。

### 实施例3：信令实现

至少覆盖：

- absolute indication；
- delta/offset indication；
- index/table；
- bitmap；
- implicit rule；
- capability-based configuration。

### 实施例4：RF架构

分别描述：

- 单RF链；
- 双RF链；
- 多RF链；
- 对UE透明的逻辑单CC实现；
- 多CC/CA替代实现。

### 实施例5：边界与异常场景

至少检查：

- 资源跨/不跨RF chain boundary；
- 资源落在载波边缘；
- BWP窄于carrier；
- UE不支持整个DL CBW；
- UL CBW小于DL CBW；
- one segment unavailable/deactivated；
- retuning或切换期间。

### 实施例6：具体信道/信号

将抽象方案分别落到PDSCH、PDCCH、PUSCH、PUCCH、CSI-RS、SRS、SSB、PRACH、DMRS中的适用项。

### 实施例7：multi-carrier single-cell逻辑资源网格

当方案涉及多个CC联合为一个逻辑小区/逻辑BWP时，至少画出并描述：

- 每个carrier-specific resource grid及其reference point；
- 各carrier上的sub-BWP/resource set；
- resource set的配置顺序/拼接顺序；
- joint BWP的PRB/RBG/PRG/REG编号关系；
- carrier boundary；
- per-carrier与joint CORESET/FDRA两套方案；
- single-carrier UE兼容路径。

### 实施例8：同步组与动态资源激活

至少覆盖：

- CC group/subgroup配置；
- 多个candidate synchronization reference resources；
- static/dynamic reference CC；
- UE capability；
- common vs carrier-specific resource configuration；
- MAC CE或其他动态激活信息；
- BWP/SSB/CSI-RS/PUCCH/PRACH等resource category/resource ID；
- carrier switch on/off与energy saving；
- DL参考资源用于UL-only或不同CC BWP激活。

### 实施例9：RF前端冲突与载波组合管理

至少给出：

- RF front-end sharing matrix；
- fully concurrent与non-concurrent carrier combination；
- configured/not activated/activated三个状态；
- 抑制、降低优先级、去激活、测量补偿、能力报告修剪等替代动作；
- 对吞吐、MIMO/Rx diversity、retuning或功耗的技术效果。

### 实施例10：装置与芯片

按模板展开通信单元、处理单元、处理器、接口电路、存储器、芯片系统。

---

## 11. 附图最小集合

对于大带宽/多载波申请，优先准备：

1. 通信系统图；
2. 方法流程/时序图；
3. 单载波大带宽频域结构图；
4. 单RF链 vs 双RF链架构图；
5. RF-chain boundary资源映射图；
6. 单CC vs 多CC/CA对比图；
7. UL/DL非对称带宽图；
8. BWP与carrier关系图；
9. guard band/RB布局图；
10. 多载波单小区的carrier-specific grid与逻辑BWP拼接图；
11. per-carrier vs joint CORESET/FDRA指示图；
12. synchronization group / reference CC / dynamic activation图；
13. RF front-end sharing/conflict matrix图；
14. 装置结构图；
15. 芯片系统图。

附图不要只展示一种具体数值，应优先体现相对位置关系和逻辑关系。

---

## 12. 跨中美欧撰写稳健性规则

1. 每个准备进入权利要求的技术特征，都应能在说明书中找到明确或可直接、无歧义推导的支持路径；
2. 对组合特征要写出组合实施例，避免仅把A、B分别列在不同实施例后默认其可任意组合；
3. 对数值范围同时提供端点、子范围、典型值和确定机制；
4. 对功能性表述同时给出至少一种具体实现；
5. 对“configured to / adapted to / 用于”类语言说明产生该功能的配置或处理逻辑；
6. 对标准术语提供上位概念，防止未来3GPP改名导致保护范围锁死；
7. 对“协议规定/预定义”同时给出网络配置或设备确定的替代实施例（技术本身允许时）；
8. 不把尚处于3GPP讨论阶段的proposal写成不可变的背景事实；
9. 每个独立权利要求的要素都应在附图中体现——附图应支持每个权利要求要素，元素间交互关系（信号方向、连接等）应明确标示；
10. 附图采用多层次结构，对应实施例和权利要求的层级，从高层系统图→硬件结构图→流程或时序图→具体信道/信号图；
11. 避免means-plus-function权利要求，在美国此类权利要求保护范围仅限于说明书中描述的对应结构及其等同物——应使用"a processor configured to..."、"a transmitter configured to..."等结构化表述；
12. 首次申请时**不要在权利要求中加入附图标记**，但应准备一份带附图标记的权利要求供后续使用；
13. 装置权利要求应避免使用"module"和"unit for doing something"（美国法域下可能被解释为纯软件实现）——改用processor/transmitter/receiver等硬件术语；
14. 说明书应同时包含实际硬件产品实施例和虚拟装置实施例，硬件产品实施例放在前面；
15. 方法权利要求不要对步骤排序，不要用(a)(b)(c)或(1)(2)(3)标记步骤——除非执行顺序是发明的必要部分；
16. 使用"comprising"和"including"（开放组），避免"consisting of"或"consisting essentially of"（封闭组）。

---

## 13. 标准对标与专利化的固定操作

运行本Skill时，对每个3GPP材料建立四列表：

| 标准材料原文/议题 | 标准状态 | 可专利化技术问题 | 申请文件应补充的实施例 |
|---|---|---|---|

标准状态必须使用以下枚举之一：

- Company proposal/view；
- Discussion；
- Agreement；
- Working assumption；
- Way forward；
- Approved WI/SI objective；
- TR text；
- Normative specification text。

不得混用。

对每个agreement，再继续问：

- agreement只规定“what”，是否还有“how”未定？
- 是否存在两种实现路径？
- 是否存在UE能力差异？
- 是否存在单RF/双RF差异？
- 是否需要新增DCI/RRC/capability？
- 是否会影响BWP/SSB/CSI/PRG/REG/DMRS？
- 是否存在跨carrier/segment reference？

“尚未标准化的how”通常是后续专利挖掘重点。

---

## 14. 强制质量检查表

在输出申请文件前，逐项检查：

### 技术闭环
- [ ] 权1是否包含完整输入—处理—输出/动作闭环？
- [ ] 发明点是否是技术关系而不是单纯结果？
- [ ] 技术效果是否与权1特征存在因果关系？

### 大带宽专项
- [ ] 是否区分channel bandwidth、BWP bandwidth、transmission bandwidth？
- [ ] 是否考虑guard band？
- [ ] 是否考虑SCS？
- [ ] 是否考虑RB数量/最大传输带宽配置？
- [ ] 是否考虑单RF/多RF？
- [ ] 是否考虑RF-chain boundary？
- [ ] 是否考虑DL/UL asymmetric bandwidth？
- [ ] 是否考虑single-CC与CA替代方案？

### 多载波专项
- [ ] 每个载波的角色是否定义清楚？
- [ ] 是否存在参考载波/目标载波关系？
- [ ] 是否覆盖直接和间接carrier indication？
- [ ] 是否覆盖carrier group/TAG/band层级？
- [ ] 是否覆盖cross-carrier scheduling/measurement/timing/power的适用情况？
- [ ] 是否检查multi-carrier single-cell / logical cell方案？
- [ ] 是否定义每个carrier-specific resource grid/reference point？
- [ ] 是否考虑多个sub-BWP/resource set如何形成一个logical BWP？
- [ ] 是否同时覆盖per-carrier和joint CORESET/FDRA？
- [ ] 是否考虑resource set跨/不跨carrier boundary？
- [ ] 是否考虑synchronization group、reference CC与动态reference切换？
- [ ] 是否考虑common/CC-agnostic与carrier-specific配置并存？
- [ ] 是否考虑legacy single-carrier UE共存？
- [ ] 是否检查RF front-end sharing/non-concurrent carrier combination？
- [ ] 是否将RF限制反馈到capability report/carrier combination？

### 信令
- [ ] RRC/DCI/MAC CE/预定义是否按功能层级考虑？
- [ ] explicit/implicit是否均考虑？
- [ ] absolute/delta/index/bitmap/ratio是否按需要覆盖？
- [ ] 是否考虑joint/separate indication？

### 权利要求
- [ ] 终端侧方法；
- [ ] 网络侧方法；
- [ ] 装置；
- [ ] 处理器型装置；
- [ ] 存储介质；
- [ ] 程序产品；
- [ ] 从属权利要求有宽—中—窄梯度；
- [ ] 具体200/400 MHz未无必要写入权1；
- [ ] 所有术语有先行基础且前后一致。

### 说明书支持
- [ ] 每个从属特征在实施例中有解释；
- [ ] 每个公式变量均定义；
- [ ] 每个具体数值有来源/技术意义；
- [ ] 可组合特征明确写出可组合关系；
- [ ] 标准讨论内容与本发明实施例明确区分。

### 背景技术安全
- [ ] 背景技术中是否使用了"现有技术"、"常规"、"已知"等表述？应改用"参考文献"；
- [ ] 背景技术中是否描述了本发明或本发明的任何特征？必须删除；
- [ ] 背景技术中是否解释或概括了现有技术？应使用文献自身的术语；
- [ ] 背景技术中是否描述了具体的"发明目的"？必须删除；
- [ ] 背景技术中是否引用了未公开申请或内部文件？必须删除；
- [ ] 背景技术中是否引用了未公开的标准或标准草案？必须删除。

### US特化检查
- [ ] 装置权利要求是否避免使用"module"和"unit for doing something"？应改用processor/transmitter/receiver；
- [ ] 是否避免means-plus-function权利要求？应包含描述结构的非功能性权利要求；
- [ ] 方法权利要求是否避免对步骤排序？是否避免用(a)(b)(c)标记步骤？
- [ ] 是否使用"comprising"和"including"而非"consisting of"？
- [ ] 是否至少有一套装置权利要求由单一实体直接侵权？
- [ ] 首次申请权利要求是否使用一体式（one-part form）？
- [ ] 首次申请权利要求中是否加入了附图标记？应删除。

### 说明书语言检查
- [ ] 是否使用开放式术语（"示例"、"方面"、"实施方式"、"实施例"）而非直接说"本发明"？
- [ ] 是否避免使用"仅"、"必须"、"关键"、"必要"、"重要"等绝对化用语？
- [ ] 是否避免使用"基本上"、"约"、"大约"等模糊术语（或已在说明书中精确定义）？
- [ ] 中文申请中首次出现的英文术语是否提供了完整英文和中文对照？
- [ ] 发明名称是否不超过25个汉字（中国）？是否未包含发明核心/目的？
- [ ] 发明内容是否以aspects/implementation forms结构组织？每个是否包含技术效果？
- [ ] 说明书末尾是否包含宽泛解释段落（"comprising不排除其他要素"、"a/an不排除复数"等）？

---

## 15. 默认输出结构

用户要求“撰写新申请”时，默认输出：

1. **技术方案理解与发明点提炼**；
2. **3GPP标准对应与潜在标准化价值**；
3. **权利要求布局建议**；
4. **完整权利要求书**；
5. **完整说明书**；
6. **摘要**；
7. **附图清单及每幅图应表达的内容**；
8. **支持性检查表**；
9. **可能需要发明人补充确认的问题**。

如果用户要求直接按模板出稿，则将第1—3、8—9项作为内部工作过程，最终只输出模板格式的申请文件；但遇到技术交底缺口时，不得自行虚构，应在文档中用待确认标记或另附问题清单。

---

## 16. 执行Prompt

运行本Skill时使用以下内部指令：

> 读取用户提供的技术交底、标准材料、现有专利/对比文件和新申请模板。先识别本发明属于大带宽载波、多载波、CA、BWP、RF-chain、非对称UL/DL带宽、guard band/RB配置、跨载波参考、宽带调度/测量/功率中的哪些子方向。建立“核心技术问题—最小发明点—上位概念—可选实施例—标准对应—技术效果”矩阵。若涉及多个载波，额外判断是否存在multi-carrier single-cell、跨载波逻辑BWP、carrier-specific resource grid、joint/separate CORESET或FDRA、synchronization group/reference CC、RF front-end sharing/conflict等结构。随后按照模板的终端侧/网络侧镜像结构撰写权利要求和说明书。独立权利要求避免无必要限定具体3GPP版本、消息名称、200/400 MHz数值和特定网络架构；从属权利要求逐层落到数值、资源粒度、RF链、具体信令、具体信道/信号。对于多个CC统一调度的方案，必须至少提供per-carrier/separate与joint/common两类配置/指示实施例，并说明物理carrier grid与逻辑BWP坐标之间的映射。对所有标准材料严格区分proposal、discussion、agreement、way forward和规范文本。对交底未支持的技术细节不得虚构，只能列为待确认项。最终执行大带宽专项目标检查、跨载波关系检查、说明书支持检查和中美欧稳健性检查。

---

## 17. 推荐的专利挖掘优先级

结合当前6G标准化方向，优先级建议如下：

**P0：** multi-carrier single-cell下多个carrier-specific resource grids形成一个逻辑DL/UL BWP，以及其与single wide CC/CA的边界；

**P0：** 跨载波CORESET/FDRA的per-carrier vs joint RRC/DCI设计、字段拼接、offset与carrier boundary规则；

**P0：** 400 MHz级单载波与单/多RF链逻辑统一、RF-chain boundary资源映射；

**P0：** 200/400 MHz等不同能力UE在同一载波下的BWP、调度、测量与capability机制；

**P0：** 大带宽下RB数量—guard band—频谱利用率的联合确定规则；

**P1：** synchronization group、reference CC、共享同步参考资源和dynamic carrier/resource activation；

**P1：** RF front-end sharing/non-concurrent carrier combination驱动的载波选择、抑制、去激活和capability pruning；

**P1：** DL/UL asymmetric channel bandwidth下PUSCH/PUCCH/SRS/RA和DL测量/反馈；

**P1：** single wide CC与2CC CA之间的配置/切换/等效调度，含载波切换时序控制、能力分层和时间偏移参数化；

**P1：** 跨segment/RF链的PRG、REG、DMRS、CSI-RS、预编码、功率和相位处理；

**P1：** 大带宽载波内频域边界指示与资源划分（偏移量指示、参考位置枚举、多种信令承载方式）；

**P1：** M=N/M=N-1/M=N+1多分支bitmap指示频域单元切分；

**P2：** irregular channel bandwidth与operator-specific spectrum holdings适配；

**P2：** 大带宽波形PAPR、稀疏资源、峰值抑制tone和频率分集，含频域连续载波/连续BWP配置与gap比例约束调度；

**P2：** 跨载波的TA、pathloss、CSI、beam或其他参考关系。

优先级不是新颖性/创造性结论；每个具体案仍须以优先权日前公开内容和当时3GPP材料单独检索。

---

## 18. 版本维护规则

每次更新本Skill时，至少检查：

1. TR 38.760-1最新版本号及新增agreement；
2. RP-260798后续内容是否已经落实到RAN1/RAN4；
3. RAN1/RAN4最新Chair Notes/Feature Lead Summary中channel bandwidth、RF chain、guard band、asymmetric/irregular bandwidth议题；
4. 新增公开专利是否出现与上述P0/P1方向高度相关的写法；
5. CN117857274A是否已能获取并完成样本分析；
6. multi-carrier single-cell相关新公开是否出现joint BWP/resource-grid/FDRA/CORESET标准化写法；
7. WO2026132931A1/WO2026132934A1及WO2026123262A1后续同族、审查意见、分案/国家阶段是否进一步揭示权利要求布局策略；
8. 92099476CN01、92111937CN01、92115288CN01、92115289CN01、92118256CN01后续审查意见/授权文本是否揭示新的权利要求修改策略或保护范围调整方向。

版本更新时，不删除旧方案；应将已过时的标准状态标为historical，并保留其作为说明书替代实施例或专利演进证据的价值。


---

## 19. v1.3更新记录（2026-08-13）

本次基于华为全球专利申请撰写指南（Patent Application Drafting Guidelines, 2012）新增撰写通用规则：

- 说明书撰写通用规则（开放式术语、强制性/非强制性语言、申请人定义术语、英文术语首次出现格式、发明名称规则）；
- 背景技术安全规则（禁止使用"现有技术/常规/已知"、禁止在背景中描述本发明、禁止引用未公开申请/标准、AAPA风险防控）；
- 发明内容aspects/implementation forms结构规范（多重引用权利要求树、技术效果/优势写法、结语格式）；
- 标准对标权利要求策略（使用标准语言、宽窄结合、至少一套对标标准、概念权利要求对照表、标准提交文本注意事项、加速授权策略）；
- 权利要求撰写禁止项与最佳实践（语言清晰性、消除不必要限制、方法步骤不排序、数量与组合规则、单一实体侵权、权利要求形式、多重引用规则、附图标记与品牌名称）；
- 装置权利要求US特化原则（避免means-plus-function、避免module/unit、三种硬件装置风格、硬件产品与虚拟装置双轨、软件/介质权利要求）；
- 更新跨中美欧撰写稳健性规则（附图支持、MPF避免、附图标记、硬件术语、方法步骤排序、comprising vs consisting of）；
- 更新强制质量检查表（背景技术安全、US特化检查、说明书语言检查）。

### 历史版本

<details>
<summary>v1.2（2026-08-13）</summary>

本次基于5件已提交/已批准华为专利申请（92099476CN01、92111937CN01、92115288CN01、92115289CN01、92118256CN01）新增：

- 载波切换与时序控制的参数化写法（时间偏移公式、能力分层、HARQ进程共享）；
- 参数多层递进模式（功能化→数值范围→优选值列表）和双轨原则+列表模式；
- 频域资源四层抽象体系（资源集合→子集合→调度资源→具体功能）；
- M=N/M=N-1/M=N+1多分支bitmap指示设计；
- 数学公式在权利要求中嵌入的规范（变量定义、量纲统一、等价定义）；
- 连续载波的多层次定义和终端侧负向行为（忽略逻辑）写法；
- 开放式枚举（"包括如下的一项或者多项"）和多种参考位置枚举模式；
- 新增5类独立权利要求族和6维度综合撰写规则；
- 更新12/16个方面（aspect）极致覆盖参考。

</details>

<details>
<summary>v1.1（2026-08-13）</summary>

本次基于CN116746242A、WO2026132931A1、WO2026132934A1、WO2026123262A1新增：

- multi-carrier single-cell / logical cell专门抽象层；
- carrier-specific resource grid + sub-BWP + logical BWP三级资源映射；
- per-carrier vs joint CORESET/FDRA固定双轨撰写规则；
- carrier boundary、resource-set confinement、legacy coexistence检查；
- synchronization group、reference CC、shared reference resource、dynamic activation模块；
- RF front-end sharing/conflict matrix与capability pruning模块；
- 新增3类实施例、5类附图、4组专利挖掘问题和5类独立权利要求族；
- 更新P0/P1专利挖掘优先级。

</details>

在后续实际新申请中，若技术交底的发明点与上述样本高度接近，应优先提炼其不同的"资源坐标关系、配置时序、能力条件、边界规则、reference/mapping关系或joint/separate编码机制"，避免仅复述"多个载波联合工作"的结果性概念。
