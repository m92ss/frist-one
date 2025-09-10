

---
config:
  layout: elk
---
flowchart TB
    A["外部触发信号<br>（美食/财富）"] --> B["多巴胺释放<br>【预期】"]
    B --> C["提供动力与渴望<br>驱动追逐行为"]
    C --> D["获得奖励结果"]
    D --> E{"奖励 vs 预期？"}
    E -- 奖励 &gt; 预期<br>（惊喜） --> F["多巴胺剧烈释放<br>“这个行为超赞”"]
    E -- "奖励 = 预期<br>（预料之中）" --> G["多巴胺释放平平<br>“一切尽在掌握”"]
    E -- 奖励 &lt; 预期<br>（失望） --> H["多巴胺水平骤降<br>“下次别再这么干了”"]
    F --> I["更新对未来奖励的预期"]
    G --> I
    H --> I
    I --> B
    style A fill:#FFF9C4
    style B fill:#FFD600
    style C fill:#FFF9C4
    style D fill:#FFF9C4
    style E fill:#BBDEFB
    style F fill:#FF6D00,color:#FFFFFF
    style G fill:#FFE0B2
    style H fill:#E1BEE7
    style I fill:#00C853,color:#FFFFFF

---
---
config:
  layout: elk
  theme: redux
---
flowchart TD
 subgraph K["血清素释放"]
        K2["平静与满足"]
        K3["抑制多巴胺"]
  end
    A["外部触发信号<br>（财富/美食）"] --> B["多巴胺释放<br>【预期】"]
    B --> C["提供动力与渴望<br>驱动追求行为"]
    C --> D["获得奖励结果"]
    D --> E{"奖励 vs 预期？"} & K
    E -- 奖励 &gt; 预期<br>（惊喜） --> F["多巴胺剧烈释放<br>“这个行为超赞”"]
    E -- "奖励 = 预期<br>（预料之中）" --> G["多巴胺释放平平<br>“一切尽在掌握”"]
    E -- 奖励 &lt; 预期<br>（失望） --> H["多巴胺水平骤降<br>“下次别再这么干了”"]
    F --> I["更新对未来奖励的预期"]
    G --> I
    H --> I
    K -- 反馈 --> I
    I --> B
    style K2 fill:#BBDEFB
    style K3 fill:#BBDEFB
    style A fill:#FFF9C4
    style B fill:#FFD600
    style C fill:#FFF9C4
    style D fill:#FFF9C4
    style E fill:#BBDEFB
    style F fill:#FF6D00,color:#FFFFFF
    style G fill:#FFE0B2
    style H fill:#E1BEE7
    style I fill:#00C853,color:#FFFFFF



---
# 紧张时发生了什么
---

config:
  layout: elk
  theme: redux
---
flowchart LR
 subgraph G["身体变化"]
        G1["心跳加快<br>心肌收缩力增强"]
        G2["支气管扩张<br>呼吸加快"]
        G3["肌肉紧张待命<br>能量涌入"]
        G4["瞳孔放大"]
        G5["消化系统血液供应减少"]
  end
    A["感知到压力或威胁"] --> B("杏仁核激活")
    B --> C["下丘脑-垂体-肾上腺轴<br>HPA轴启动"] & D["自主神经系统<br>交感神经兴奋"]
    C --> E["释放压力激素<br>皮质醇和肾上腺素"]
    D --> F["指令直达器官"]
    E --> G
    F --> G
    G1 --> H1["心慌<br>上不来气"]
    G2 --> H2["过度换气"]
    G3 --> H3["手抖、全身哆嗦"]
    G4 --> H4["进光量增加、视线模糊<br>捕捉广阔范围内危险"]
    G5 --> H5["恶心、胃部不适"]
     H1:::Peach
     H1:::Sky
     H2:::Peach
     H2:::Sky
     H3:::Peach
     H3:::Sky
     H4:::Peach
     H4:::Sky
     H5:::Peach
     H5:::Sky
    classDef Peach stroke-width:1px, stroke-dasharray:none, stroke:#FBB35A, fill:#FFEFDB, color:#8F632D
    classDef Sky stroke-width:1px, stroke-dasharray:none, stroke:#374D7C, fill:#E2EBFF, color:#374D7C
    style G1 fill:#E1BEE7
    style G2 fill:#E1BEE7
    style G3 fill:#E1BEE7
    style G4 fill:#E1BEE7
    style G5 fill:#E1BEE7
    style A fill:#D50000,color:#FFFFFF
    style B fill:#FF6D00,color:#FFFFFF
    style C fill:#FFE0B2
    style D fill:#FFE0B2
    style E fill:#FFE0B2
    style F fill:#FFE0B2


---
# 正确的发泄
---
config:
  layout: elk
---
flowchart LR
 subgraph D[" "]
    direction TB
        D1["高强度运动<br>快跑/拳击/跳舞"]
        D2["感官降温<br>冷水洗头/冰贴后颈"]
        D3["深呼吸<br>4-7-8呼吸法"]
        D_Effect["消耗应激激素<br>激活副交感神经"]
  end
 subgraph E[" "]
    direction TB
        E1["描述创伤<br>写日记/写信撕掉"]
        E2["具象化表达<br>绘画/作曲/陶艺"]
        E3["倾诉与共情<br>人或AI"]
        E_Effect["为情绪提供安全出口<br>理清思绪，获得验证"]
  end
 subgraph F[" "]
    direction TB
        F1["正念冥想<br>观察而不评判"]
        F2["认知重评<br>换角度解读事件"]
        F_Effect["创造思维空间<br>从根源改变情绪反应"]
  end
    Start("感到强烈情绪") --> A["发现与分析情绪"]
    A --> B["暂停与接纳<br>我要用健康的排解方式"]
    B --> C{"健康的排解方式"}
    C --> D & E & F
    D1 --> D_Effect
    D2 --> D_Effect
    D3 --> D_Effect
    E1 --> E_Effect
    E2 --> E_Effect
    E3 --> E_Effect
    F1 --> F_Effect
    F2 --> F_Effect
    D_Effect --> G["身心状态平稳"]
    E_Effect --> G
    F_Effect --> G
    G --> H["理性思考解决方案"]
    H --> End("问题解决/情绪平复")
    Start -. 不健康方式：<br>攻击他人/自我/压抑 .-> I["导致更糟的结果：<br>关系破坏、羞愧、问题恶化"]
    style D1 fill:#FFF9C4
    style D2 fill:#FFF9C4
    style D3 fill:#FFF9C4
    style D_Effect fill:#FFD600
    style E1 fill:#FFF9C4
    style E2 fill:#FFF9C4
    style E3 fill:#FFF9C4
    style E_Effect fill:#FFD600
    style F1 fill:#FFF9C4
    style F2 fill:#FFF9C4
    style F_Effect fill:#FFD600
    style Start fill:#D50000,color:#FFFFFF
    style A fill:#BBDEFB
    style B fill:#BBDEFB
    style C fill:#E1BEE7
    style G fill:#C8E6C9
    style H fill:#C8E6C9
    style End fill:#00C853,color:#FFFFFF
    style I fill:#FF6D00,color:#FFFFFF

---
# 红薯抑郁观察

---
---
---
config:
  layout: dagre
  look: neo
---
flowchart TB
    A["红薯抑郁群体观察"] --> B["第一类: 清醒的求助者"] & C["第二类: 原生家庭困境者"] & D["第三类: 抗拒改变者"]
    B --> B1["具备自察能力<br>内省、强烈自救意识、行动力"]
    B1 --> B2["听劝<br>容易接受专业引导"]
    B2 --> B3["预后<br>大概率康复"]
    C --> C1["糟心困境<br>与“抑郁源头”系统性捆绑"]
    C1 --> C2["暂时的系统性无解<br>无法脱离有毒环境<br>创伤性绑定与未分化自我"]
    C2 --> C3["建立心理边界<br>完成哀悼<br>实现心理独立"]
    C3 --> C4["预后<br>困难、漫长、易反复"]
    D --> D1["仪式性身份<br>“抑郁症”作为挡箭牌"]
    D1 --> D2["继发性获益<br>痛苦成为舒适区<br>低能量与无解信念闭环"]
    D2 --> D3["打破身份认同与防御<br>处理继发性获益"]
    D3 --> D4["预后<br>最困难、无力"]
     B:::Ash
     C:::Ash
     D:::Ash
     B3:::good
     C4:::hard
     D4:::hardest
    classDef good fill:#dfd,stroke:#0a0
    classDef hard fill:#fdd,stroke:#f00
    classDef hardest fill:#fcc,stroke:#c00
    classDef Ash stroke-width:1px, stroke-dasharray:none, stroke:#999999, fill:#EEEEEE, color:#000000
    style A fill:#FF6D00,color:#FFFFFF
    style B1 fill:#BBDEFB
    style B2 fill:#C8E6C9
    style C1 fill:#FFE0B2
    style C2 fill:#FFD600
    style C3 fill:#FFF9C4
    style C4 fill:#FFE0B2,color:#000000
    style D1 fill:#FFE0B2
    style D2 fill:#FFD600
    style D3 fill:#FFF9C4
    style D4 fill:#FFE0B2,color:#000000

---
# 遗忘
---
config:
  layout: elk
---
flowchart TB
 subgraph C["记忆失效风险1：编码失败"]
    direction LR
        B["编码<br>感觉信号被初步转化为神经模式"]
        C1["缺乏注意"]
        C2["没记住"]
  end
 subgraph I["记忆失效风险2：存储弱化"]
    direction LR
        I1["记忆痕迹理论<br>突触连接因不使用而弱化"]
  end
 subgraph L["记忆失效风险3：提取失败"]
    direction LR
        L1["线索依赖<br>缺少合适的回忆线索"]
        L2["干扰<br>相似记忆相互竞争"]
        L3["动机性遗忘<br>潜意识压抑痛苦记忆"]
  end
    A["外部事件或信息"] --> B
    C1 --> B
    B --> C2
    B -- 成功编码 --> D["短期记忆<br>脆弱且容量有限"]
    D -- 大量信息自然丢失 --> E["遗忘"]
    D -- 通过重复/深度处理 --> F["巩固<br>神经模式被强化、稳定与转移"]
    F -- 巩固过程中断<br>（如缺氧、脑震荡） --> G["巩固失败<br>记忆无法长期保存"]
    F -- 成功巩固 --> H["长期记忆<br>存储在皮层网络中的稳定模式"]
    H --> J["提取(回想)"]
    J -- 成功 --> K["记忆被成功回忆"]
    L -- 导致 --> M["“话在嘴边”现象<br>记忆存在但无法访问"]
    I1 --> E
    M --> E
    style B fill:#FFF9C4
    style C1 fill:#FFF9C4
    style C2 fill:#E1BEE7
    style I1 fill:#FFF9C4
    style L1 fill:#FFF9C4
    style L2 fill:#FFF9C4
    style L3 fill:#FFF9C4
    style A fill:#BBDEFB
    style D fill:#FFF9C4
    style E fill:#E1BEE7
    style F fill:#FFD600
    style G fill:#E1BEE7
    style H fill:#FFD600
    style J fill:#C8E6C9
    style K color:#FFFFFF,fill:#00C853
    style M fill:#FFF9C4
---

# 焦虑时发生了什么——抑郁如何发生
---
---
config:
  layout: elk
  look: neo
  theme: redux
---
flowchart TB
 subgraph B1["压力激素释放"]
    direction LR
        C["皮质醇<br>身体能量重新分配"]
        D["去甲肾上腺素<br>警惕与专注"]
  end
 subgraph E_Details["能量重新分配"]
        E1["大幅提升血糖<br>肌肉绷紧全身颤抖"]
        E2["抑制前额叶<br>难以集中注意力"]
        E2_1["消化系统活动减弱<br>肚子疼/恶心"]
        E2_2["抑制免疫系统<br>免疫力下降"]
        E2_3["持续供能<br>失眠"]
  end
 subgraph F_Details["即时警报"]
        F1["心血管系统剧烈反应<br>心慌/心悸"]
        F2["肌肉紧张准备行动<br>手抖/出汗"]
        F3["感官极度敏锐<br>瞳孔放大/视线模糊"]
        F4["启动战/逃反应<br>坐立不安"]
        F5["能量耗尽<br>疲惫不堪"]
  end
 subgraph H_Details["思维模式改变"]
        H1["反复预测威胁<br>思维反刍"]
        H2["预期最坏结果<br>灾难化思维"]
        H3["放大负面情绪<br>怀疑人生价值"]
  end
 subgraph O["运动的正向作用"]
        O1["代谢皮质醇<br>平衡去甲肾上腺素"]
        O2["模拟战逃反应<br>欺骗大脑威胁已解除"]
        O3["产生血清素<br>稳定情绪"]
  end
    A["预测模型与现实不符合<br>感知到压力"] --> B["下丘脑被激活<br>启动HPA轴与SAM轴"]
    C --> E_Details
    D --> F_Details
    J["心理生理不适加剧"] --> I["大脑判定威胁持续存在<br>持续信号反馈给下丘脑"]
    I --> M["恶性循环<br>焦虑/惶恐/易怒/失眠<br>躯体化症状"] & B
    H_Details --> J
    B --> B1
    F_Details --> n1["处理方法"]
    E_Details --> n1
    N["运动干预<br>（跑步/骑行/游泳/力量训练）"] --> O
    O --> P["压力激素水平回落<br>身体解除警报"]
    n1 --> N & n2["毫无行动"]
    n2 --> H_Details
    P --> R["身心状态改善<br>应对压力能力增强"]
    O2@{ shape: rect}
    n1@{ shape: diam}
    style C fill:#E1BEE7
    style D fill:#BBDEFB
    style H1 fill:#FFFFFF
    style H2 fill:#FFFFFF
    style H3 fill:#FFFFFF
    style O1 fill:#FFFFFF
    style O2 fill:#FFFFFF
    style O3 fill:#FFFFFF
    style A fill:#FFE0B2,color:#000000
    style B fill:#FFD600
    style E_Details fill:#E1BEE7
    style F_Details fill:#BBDEFB
    style J fill:#FFE0B2
    style I fill:#FF6D00,color:#FFFFFF
    style M fill:#D50000,color:#FFFFFF
    style H_Details fill:#FFE0B2
    style n1 fill:#FFD600
    style N fill:#C8E6C9,color:#000000
    style O fill:#C8E6C9
    style P fill:#C8E6C9
    style n2 fill:#FFE0B2
    style R fill:#4CAF50,color:#FFFFFF
    linkStyle 0 stroke:#FF6D00,fill:none
    linkStyle 1 stroke:#AA00FF,fill:none
    linkStyle 2 stroke:#2962FF,fill:none
    linkStyle 3 stroke:#FF6D00,fill:none
    linkStyle 4 stroke:#D50000,fill:none
    linkStyle 5 stroke:#FF6D00,fill:none
    linkStyle 6 stroke:#FF6D00,fill:none
    linkStyle 7 stroke:#FF6D00,fill:none
    linkStyle 8 stroke:#2962FF,fill:none
    linkStyle 9 stroke:#AA00FF,fill:none
    linkStyle 10 stroke:#00C853,fill:none
    linkStyle 11 stroke:#00C853,fill:none
    linkStyle 13 stroke:#000000
    linkStyle 14 stroke:#FF6D00,fill:none
    linkStyle 15 stroke:#00C853,fill:none
---

# 深度学习
---
config:
  layout: elk
  look: handDrawn
---
flowchart TD
 subgraph B["深度理解"]
        B1["高度专注<br>激活前额叶皮层"]
        B2["主动加工<br>而非被动接收"]
  end
 subgraph C["首次强化"]
        C1["合上材料"]
        C2["尝试复述、总结、自测"]
  end
 subgraph D["离线巩固"]
        D1["完全脱离学习内容"]
        D2["散步、喝水、冥想"]
        D3["默认模式网络激活<br>后台整合信息"]
  end
    A["开始学习新内容"] --> B
    B1 --> B2
    B --> C
    C1 --> C2
    C --> D
    D1 --> D2
    D2 --> D3
    D --> E["下一个学习周期"] & F["后续步骤 (每日/每周)"]
    E --> B
    F --> G["间隔重复"]
    G --> H["再次主动回忆与测试"]
    H --> I["触发记忆重新巩固<br>极大强化突触连接"]
    style B fill:#BBDEFB
    style C fill:#FFF9C4
    style D fill:#FFD600
    style E fill:#BBDEFB
    style F fill:#C8E6C9
    style G fill:#f3e5f5
    style H fill:#E1BEE7
    style I fill:#E1BEE7,color:#000000


# 叙事疗法
---
config:
  layout: elk
  look: handDrawn
---
flowchart TD
 subgraph F["语言组织的过程"]
    direction TB
        F1["赋予时间顺序<br>(首先...然后...)"]
        F2["赋予逻辑与因果<br>(为什么发生?)"]
        F3["为感觉贴标签<br>(命名情绪)"]
  end
    A["经历强烈刺激/创伤"] --> B["记忆初始状态<br>内隐的、碎片化的"]
    B --> C["存储特点<br>感官碎片(图像、气味、感觉)<br>与恐惧强烈关联<br>像是正在发生的威胁"]
    C --> D["行为: 尝试用语言描述经历"]
    D --> E["激活高级认知中心<br>(前额叶皮层)"]
    E --> F
    F --> G["在安全环境下提取记忆"]
    G --> H["关键机制: 记忆重新巩固<br>记忆变得不稳定，进入修改窗口"]
    H --> I["将新的安全信息<br>(‘我现在是安全的’)<br>整合进原始记忆"]
    I --> J["记忆最终状态 <br>外显的、叙事性的"]
    J --> K@{ label: "存储特点<br>成为一个有连贯性的'故事'<br>整合进自传体记忆<br>被前额叶皮层调控" }
    K --> L["最终效果"]
    L --> M["情感强度降低"] & N["威胁性解除"] & O["掌控感提升"]
    K@{ shape: rect}
    style A fill:#FF6D00,color:#FFFFFF
    style B fill:#BBDEFB
    style C fill:#BBDEFB
    style D fill:#FFF9C4
    style E fill:#FFF9C4
    style F fill:#FFD600
    style G fill:#FFF9C4
    style H fill:#FFE0B2
    style I fill:#FFF9C4
    style J fill:#FFF9C4
    style K fill:#FFF9C4
    style L fill:#FFF9C4
    style M fill:#C8E6C9
    style N fill:#C8E6C9
    style O fill:#C8E6C9


---
# 群体极化
---
config:
  layout: elk
  look: neo
  theme: redux
---
flowchart TD
 subgraph C["KOL运作机制：强化认同"]
    direction LR
        C1["树立共同敌人<br>“对家”/“黑粉”"]
        C2["神圣化偶像<br>“哥哥只有我们了”"]
        C3["制定仪式性行为<br>打榜/控评/反黑/集资"]
  end
 subgraph D["形成闭环系统与心理现实"]
    direction LR
        D1["信息茧房与回音室<br>内部叙事自我印证"]
        D2["神经奖赏机制<br>为群体行动获多巴胺"]
        D3["非人化外部批评<br>“皆为黑子，无需共情”"]
  end
 subgraph G["低配宗教特征体现"]
        G1["**教皇/神**<br> KOL与偶像"]
        G2["**教义**<br> 内部叙事与规则"]
        G3["**圣战**<br> 网络暴力与“出征”"]
        G4["**赎罪券**<br> 购买代言/集资"]
        G5["**天堂/救赎**<br> 偶像的成功与认可"]
  end
    C --> D
    D --> E["强烈的群体极化"]
    E --> F["观点极端化<br>内部同质化<br>对外攻击性增强"]
    F --> G
    G -- 反馈强化 --> C
    G1 --> G5 & G2
    G5 --> G4
    A["个体身份焦虑与归属感需求<br>寻找并加入粉丝圈层"] --> C
    C2 --> C3
    C3 --> C1
    G2 --> G3
    D2 --> D3
    D1 --> D2
    style C fill:#E1BEE7
    style D fill:#E1BEE7
    style E fill:#E1BEE7
    style F fill:#FF6D00,color:#FFFFFF
    style G fill:#FFE0B2
    style A fill:#BBDEFB


---
# 我们为什么善良
---
---
config:
  layout: elk
---
flowchart TD
 subgraph A["生物基础"]
        A1["社会性动物的利他本能<br>进化遗迹：亲缘选择、互惠利他"]
  end
 subgraph B["心理机制"]
        B1["共情<br>情感共情与认知共情"]
  end
 subgraph C["社会文化强化"]
        C1["群体极化与道德规范<br>“善良是对的”"]
  end
    A1 -- 提供行为模板 --> B1
    B1 -- 转化为情感动力 --> D["具体的善良行为<br>帮助、合作、分享"]
    D -- 产生 --> E["积极反馈与强化<br>快乐、认同、归属感"]
    E -- 被群体总结颂扬为 --> C1
    C1 -- 内化为个人价值观 & 强化 --> B1
    C1 -- 提供道德支持以对抗 --> F["现实规训的挑战<br>自私、冷漠、算计"]
    B1 -- 提供情感动力以对抗 --> F
    A1 -- 提供深层冲动以对抗 --> F
    style A1 fill:#FFD600
    style B1 fill:#FFCDD2
    style C1 fill:#FFD600
    style D fill:#00C853,color:#FFFFFF
    style E fill:#FFF9C4
    style F fill:#FF6D00,color:#FFFFFF
    style A fill:transparent,stroke:#333,stroke-width:2px
    style B fill:transparent,stroke:#333,stroke-width:2px
    style C fill:transparent,stroke:#333,stroke-width:2px

---
# 群体极化的两条路径

flowchart TD
 subgraph C["导致极化的力量"]
    direction LR
        C1["信息瀑布<br>共享支持性信息<br>隐藏异议"]
        C2["社会比较<br>调整观点以获认可<br>竞赛忠诚度"]
        C3["回音室效应<br>大数据与同质化社交圈<br>强化固有观点"]
        C4["神经与心理机制<br>杏仁核劫持/多巴胺奖赏/去个体化"]
  end
 subgraph D["抑制极化的机制"]
    direction LR
        D1["审慎的制度设计<br>司法抗辩、科学证伪、民主制衡"]
        D2["积极的文化规范<br>批判性思维、智力谦逊<br>建设性对话"]
        D3["多元化的联系<br>跨越圈子的社交与信息交换"]
  end
    A["群体形成"] --> B{"选择路径"}
    B -- 遵循自然趋势 --> C
    B -- 采用抑制机制 --> D
    C -- 结果 --> E["🔄 群体极化<br>观点趋于极端、内部同质、对抗外部"]
    D -- 结果 --> F["✅ 理性共识或健康分歧<br>观点经批判、更稳健、包容异见"]

    style C1 fill:#E1BEE7
    style C2 fill:#E1BEE7
    style C3 fill:#E1BEE7
    style C4 fill:#E1BEE7
    style D1 fill:#FFD600
    style D2 fill:#FFD600
    style D3 fill:#FFD600
    style A fill:#BBDEFB
    style B fill:#BBDEFB
    style E fill:#FF6D00,color:#FFFFFF
    style F fill:#00C853,color:#FFFFFF


---
# 改变认知为什么那么难

---
config:
  layout: dagre
---
flowchart TB
 subgraph B["认知防御反应"]
    direction LR
        B1["杏仁核被激活<br>触发抵制情绪"]
        B2["前额叶皮层活动降低<br>屁股决定脑袋"]
  end
 subgraph D["为何改变如此之难?"]
    direction LR
        D1["认知失调<br>否定或曲解新信息"]
        D2["确认偏误<br>只寻找支持原有观点的证据"]
        D3["身份威胁<br>改变观点=部分否定自我"]
  end
 subgraph F["为何新信徒更激进?"]
    direction LR
        F1["高能耗<br>构建新神经通路<br>消耗大量能量"]
        F2["认知失调<br>“我过去错了”<br>带来巨大心理不适"]
        F3["过度补偿<br>急需通过极端言行<br>证明新身份的正确性与忠诚度"]
  end
 subgraph G["自我强化的激进循环"]
        G1["激进言行"]
        G3["内心失调感暂时缓解"]
        G2["获得群体认可<br>多巴胺奖赏"]
  end
    A["新信息/事实与现有认知冲突"] --> B
    B --> C{"心理与行为选择"}
    C -- 路径一: 拒绝改变 --> D
    D --> E["维持原有认知<br>能量消耗低, 感觉安全"]
    C -- 路径二: 接受改变 --> F
    F ==> G
    G1 --> G2
    G2 --> G3
    G3 --> G1
    G --> H["形成新的更极端的<br>固化认知身份"]
    style A fill:#BBDEFB
    style B fill:#FFE0B2
    style C fill:#FFD600
    style D fill:#FFE0B2
    style E fill:#FFF9C4
    style F fill:#FFE0B2
    style G fill:#E1BEE7
    style H fill:#E1BEE7

---
# 运动与血清素合成
---
config:
  layout: elk
  look: neo
---
flowchart TB
 subgraph Precondition["获取原料"]
        B["色氨酸进入血液"]
        A["饮食摄入色氨酸<br>禽蛋奶坚果"]
  end
 subgraph s1["健康生活习惯"]
        L["规律生活/晒太阳"]
        G["促进维生素D生成<br>改善合成环境"]
  end
 subgraph s2["运动的强大促进作用"]
        S["🏃‍♂️ 规律运动"]
        D["分解脂肪释放游离脂肪酸<br>置换出与白蛋白结合的色氨酸"]
        n2["提升脑源性神经营养因子水平<br>提升抗抑郁韧性"]
  end
    A --> B
    S --> D & n2
    L --> G
    E["大幅提高血液中<br>色氨酸比例"] --> H["更多色氨酸突破脑血屏障"]
    Precondition --> C["色氨酸与其它大中性氨基酸<br>竞争进入大脑"]
    C --> H
    H --> n1["血清素合成<br>大脑血清素水平提高"]
    n1 --> M["白天稳定情绪<br>晚上有足够原料制造褪黑素<br>并且不会emo"]
    D --> E
    n2 --> n1
    G --> n1
    B@{ shape: rounded}
    L@{ shape: rect}
    G@{ shape: rounded}
    S@{ shape: rect}
    D@{ shape: rounded}
    n2@{ shape: rounded}
    n1@{ shape: rect}
     L:::action
     S:::action
    classDef action fill:#6ef,stroke:#333,stroke-width:2px
    classDef sun fill:#ff0,stroke:#333,stroke-width:2px
    classDef result fill:#9f9,stroke:#333,stroke-width:2px
    style B fill:#FFE0B2
    style A fill:#FFF9C4
    style L fill:#FFF9C4
    style G fill:#FFE0B2
    style S fill:#FFF9C4
    style D fill:#FFE0B2
    style n2 fill:#FFE0B2
    style E fill:#FFD600
    style H fill:#FFD600,color:#000000
    style C fill:#FFD600
    style n1 fill:#C8E6C9
    style M fill:#00C853,color:#FFFFFF

---
# 运动与血清素合成
---
---
config:
  layout: elk
---
flowchart TB
 subgraph S2["⚡ 核心加速：规律运动"]
        S["🏃‍♂️ 每周3-5次的规律运动<br>慢跑/骑行/游泳"]
        D["分解脂肪释放色氨酸<br>消耗其它氨基酸"]
        BDNF["提升脑源性神经营养因子<br>增强抗抑郁韧性"]
        E["大幅提高血液中<br>色氨酸/LNAA比例"]
        n2@{ label: "<span style=\"font-weight:\">增加血清素受体敏感性<br>阻止血清素被回收</span>" }
  end
 subgraph S1["✨ 必要促进：健康生活习惯"]
        L["🌞规律作息/晒太阳"]
        G["促进维生素D生成/调节生物钟<br>改善血清素合成环境"]
  end
 subgraph s1["常规合成路径"]
        A["饮食摄入色氨酸<br>（禽蛋奶坚果）"]
        B["色氨酸进入血液"]
        C["色氨酸与其它氨基酸<br>竞争穿透脑血屏障进入大脑"]
  end
    S --> D & n2
    L --> G
    A --> B
    B --> C
    C -- 常规路径 --> H["更多色氨酸成功穿过血脑屏障"]
    E -- 运动的关键作用 --> H
    H --> n1["大脑血清素水平提升"]
    G -- 创造有利条件 --> n1
    BDNF -- 长期优化 --> n1
    n1 --> M["白天：情绪稳定、精力充沛<br>夜晚：促进睡眠（合成褪黑素）<br>长期：改善情绪调节能力"]
    D --> E
    n2 --> BDNF
    n2@{ shape: rect}
     S:::keyAction
     D:::process
     BDNF:::keyResult
     E:::keyResult
     L:::keyAction
     G:::process
     A:::source
     B:::source
     C:::process
     H:::keyResult
     n1:::keyResult
     M:::outcome
    classDef source fill:#FFF9C4,stroke:#666
    classDef process fill:#FFE0B2,stroke:#666
    classDef keyAction fill:#6ef,stroke:#333,stroke-width:2px
    classDef keyResult fill:#FFD600,stroke:#666,color:#000
    classDef outcome fill:#00C853,stroke:#666,color:#fff
    style D fill:#FFF9C4
    style n2 fill:#FFF9C4
    style G fill:#FFD600
    style C fill:#FFF9C4
    linkStyle 9 stroke:#000000,fill:none

---
# 为什么他们邪恶
---
---
config:
  layout: elk
---
flowchart TB
 subgraph A["生物基础"]
        A1["自利与生存本能<br>竞争、支配、部落主义"]
  end
 subgraph B["心理机制"]
        B1["共情腐蚀/去人性化<br>认知扭曲与道德脱钩"]
  end
 subgraph C["社会动力"]
        C1["群体极化与意识形态<br>回音室效应/攀比/模仿"]
  end
    A1 -- 提供潜在倾向 --> B
    B1 == 默许 ==> D["具体的“邪恶”行为<br>伤害、剥削、毁灭"]
    D -- 带来 --> E["短期获益与强化<br>权力、资源、归属感"]
    E -- 系统化/合理化 --> C
    C1 -- 进一步驱动 & 正当化 --> B
    C -. 瓦解 .-> F["外部约束<br>共情、道德、法律"]
    B -. 屏蔽 .-> F
    A -. 无视 .-> F
    E -- 多巴胺奖励 --> A
    style B1 fill:#AA00FF,color:#FFFFFF
    style B fill:#E1BEE7,stroke:#333,stroke-width:2px
    style D fill:#FF6D00,color:#FFFFFF
    style E fill:#FF6D00,color:#FFFFFF
    style C fill:#FFE0B2,stroke:#333,stroke-width:2px
    style F color:#000000,fill:#FFD600
    style A fill:#FFF9C4,stroke:#333,stroke-width:2px
    linkStyle 1 stroke:#000000,fill:none
    linkStyle 3 stroke:#FF6D00,fill:none
    linkStyle 5 stroke:#FF6D00,fill:none
    linkStyle 6 stroke:#FF6D00,fill:none
    linkStyle 7 stroke:#FF6D00,fill:none
    linkStyle 8 stroke:#FF6D00,fill:none

---
# 缺爱
---
config:
  layout: elk
---
flowchart LR
 subgraph B["障碍"]
    direction LR
        B1["病态的自我批评与羞耻感<br>“因为我做的不够好所以他们不喜欢我”<br>有人要我总比没人要我好"]
        B2["自我攻击<br>没有固定价值观<br>讨好型人格"]
        B3["未分化的自我<br>无法以自己为原点思考<br>心中空虚/灵魂抽离感"]
        B4["不知道自己想要什么<br>观点和喜好容易随他人而改变<br>在幸福来临前逃离"]
  end
 subgraph C["行为"]
        C1["关系中的自我毁灭模式<br>重复创伤/允许被剥削"]
        C2["情绪调节功能受损<br>情绪惊跳/非黑即白思维"]
        C3["对“存在”本身的困惑<br>慢性空虚感/解离"]
        C4["难以享受成功与快乐<br>自我破坏/不配得感"]
  end
    A["童年缺爱<br>情感忽视/不稳定照料/虐待"] --> B
    B --> C
    C -- 无法真正解决根源问题 --> D{"永远无法填满的空洞<br>（内在结构与功能的缺失）"}
    D -. 持续影响 .-> B & C
    style B1 fill:#FFD600
    style B2 fill:#FFD600
    style B3 fill:#FFD600
    style B4 fill:#FFD600
    style A fill:#BBDEFB,stroke:#333,stroke-width:2px
    style B fill:#FFFFFF
    style C fill:#E1BEE7
    style D fill:#757575,stroke:#333,stroke-width:4px,color:#FFFFFF
    linkStyle 2 stroke:#000000
    linkStyle 3 stroke:#AA00FF,fill:none
    linkStyle 4 stroke:#AA00FF,fill:none



# 解决缺爱
---
---
config:
  layout: elk
  look: neo
---
flowchart LR
 subgraph B["心理障碍"]
    direction LR
        B1["扭曲的自我批评与羞耻感<br>“他们不喜欢我是我的错”<br>“有人要我总比没人要我好”"]
        B2["自我攻击<br>没有固定价值观<br>讨好型人格"]
        B3["未分化的自我<br>无法以自己为原点思考<br>心中空虚/灵魂抽离感"]
        B4["不知道自己想要什么<br>观点和喜好容易随他人而改变<br>在幸福来临前逃离"]
  end
 subgraph C["过度补偿行为"]
        C1["依恋关系中的自残模式<br>重现创伤经历/允许被情感剥削<br>过度亲近/破坏稳定关系"]
        C2["情绪调节功能受损<br>情绪惊跳/非黑即白思维"]
        C3["质疑自身存在的理由<br>背景性空虚感/解离"]
        C4["难以享受成功与快乐<br>自我毁灭/不配得感"]
  end
 subgraph E["解决方法与治愈路径"]
    direction TB
        E1["确立自我边界<br>识别自我情感剥削的行为<br>有意识地做出新选择"]
        E2["哀悼那个从未得到过的温馨童年<br>真正从情感上接受事实<br>不再执着于向过去索取"]
        E3["通过成为自己缺失的那部分<br>重建缺失的内在结构和功能"]
        E4["体验健康的依恋关系<br>内化新的健康的依恋模式"]
  end
    A["童年缺爱<br>情感忽视/不稳定照料/不理解<br>虐待"] --> B
    B --> C
    C == 焦虑型依恋 ==> D{"心中永远无法填满的空洞<br>（内在结构与功能的缺失）"}
    D -. 持续影响 .-> B & C
    E1 -- 打破病态循环 --> C1
    E2 -- 直面并接受悲伤记忆<br>停止向过去索取 --> B1
    E3 == 构建内在结构<br>填补功能缺失 ==> D
    E4 -- 习惯健康依恋关系 --> C
    style A fill:#BBDEFB,color:#000000
    style B fill:#E1BEE7
    style C fill:#E1BEE7
    style D fill:#424242,color:#FFFFFF
    style E fill:#FFD600
    linkStyle 5 stroke:#FFD600,fill:none
    linkStyle 6 stroke:#FFD600,fill:none
    linkStyle 7 stroke:#FFD600,fill:none
    linkStyle 8 stroke:#FFD600,fill:none
