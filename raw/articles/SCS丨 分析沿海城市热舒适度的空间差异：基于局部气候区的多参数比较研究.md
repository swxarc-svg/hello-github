---
title: "SCS丨 分析沿海城市热舒适度的空间差异：基于局部气候区的多参数比较研究"
source: "https://mp.weixin.qq.com/s/XHbxdpp-3EmBDdG8VwzefQ"
author:
  - "[[戈多]]"
published:
created: 2026-04-09
description: "Sustainable Cities and Society——分析沿海城市热舒适度的空间差异：基于局部气候区的多参数比较研究"
tags:
  - "clippings"
---
戈多 *2026年2月20日 11:30*

**点击蓝字 关注我们**

![Image](https://mmbiz.qpic.cn/mmbiz_png/eDXiba58htLfOcA4peXicHXUxebfBWLCSDge6iaF4ibIfYoOdSg8xL0JHgCOicicy5wT92YXibRgtoddibeB704QKPycIHS1Jw71ab0ZpvzIgricJES8/640?wx_fmt=png&tp=webp&wxfrom=5&wx_lazy=1#imgIndex=1)

**01**

**研究背景**

在全球变暖和城市热岛效应的双重压力下，城市公共空间的户外热舒适（OTC）问题日益凸显，直接关系到居民的健康、福祉以及城市空间的使用效率。尽管已有大量研究证实城市形态（如天空开阔度、街道宽高比）是影响微气候和热舒适的关键物理因素，但这些研究多依赖于数值模拟，且常常忽略了人的主观能动性。事实上，个体的热感知是一个复杂的多维度过程，不仅受物理环境的直接影响，还受到个人生理特征、社会背景乃至心理状态（如活动目的、停留时长、同伴关系）的深刻调节。尤其在气候独特的沿海城市，海陆风等特殊气象条件可能改变城市形态与热舒适之间的传统关系。然而，目前缺乏大规模、跨建成环境类型的实证研究，特别是那些能够整合客观物理测量与主观问卷调查，并系统性探讨物理、生理、社会和心理等多重因素耦合作用机制的研究。因此，本研究旨在通过对沿海城市大连的多个典型公共空间进行综合性实地调研，以“局地气候区”（LCZ）为分类框架，深入解析夏季不同建成环境下热舒适的空间分异规律，建立适用于当地的热舒适基准，并揭示影响居民热感知的多维度主导因素及其作用机制。

**02**

**研究方法**

研究构建了一个包含数据采集、描述性分析、多变量分析和机器学习建模四个步骤的综合研究框架，旨在系统解析沿海城市户外热舒适的空间差异及其多维度影响机制（图1）。

![Image](data:image/svg+xml,%3C%3Fxml version='1.0' encoding='UTF-8'%3F%3E%3Csvg width='1px' height='1px' viewBox='0 0 1 1' version='1.1' xmlns='http://www.w3.org/2000/svg' xmlns:xlink='http://www.w3.org/1999/xlink'%3E%3Ctitle%3E%3C/title%3E%3Cg stroke='none' stroke-width='1' fill='none' fill-rule='evenodd' fill-opacity='0'%3E%3Cg transform='translate(-249.000000, -126.000000)' fill='%23FFFFFF'%3E%3Crect x='249' y='126' width='1' height='1'%3E%3C/rect%3E%3C/g%3E%3C/g%3E%3C/svg%3E)

图 1.实验流程图

**研究区域选择与现场测量：** 研究地点为中国北方沿海城市大连。基于前期的LCZ地图绘制工作，研究团队选取了五种主要的、社会活动频繁的LCZ类型（LCZ 1-2, LCZ 4, LCZ 5, LCZ 6, LCZ A），并在每种类型下选择了2-3个具有代表性的公共空间，共计14个研究样点（图2）。在2023年8月的一个典型夏季时段，研究团队在这些样点同步进行了实地微气候测量和问卷调查。微气候测量使用了包含温度、湿度、风速、黑球温度和太阳辐射等多个传感器的综合性热舒适监测仪，以1分钟的频率连续记录数据（图3，表2）。

![Image](data:image/svg+xml,%3C%3Fxml version='1.0' encoding='UTF-8'%3F%3E%3Csvg width='1px' height='1px' viewBox='0 0 1 1' version='1.1' xmlns='http://www.w3.org/2000/svg' xmlns:xlink='http://www.w3.org/1999/xlink'%3E%3Ctitle%3E%3C/title%3E%3Cg stroke='none' stroke-width='1' fill='none' fill-rule='evenodd' fill-opacity='0'%3E%3Cg transform='translate(-249.000000, -126.000000)' fill='%23FFFFFF'%3E%3Crect x='249' y='126' width='1' height='1'%3E%3C/rect%3E%3C/g%3E%3C/g%3E%3C/svg%3E)

图 2.研究区域及各测量点的卫星图像

![Image](data:image/svg+xml,%3C%3Fxml version='1.0' encoding='UTF-8'%3F%3E%3Csvg width='1px' height='1px' viewBox='0 0 1 1' version='1.1' xmlns='http://www.w3.org/2000/svg' xmlns:xlink='http://www.w3.org/1999/xlink'%3E%3Ctitle%3E%3C/title%3E%3Cg stroke='none' stroke-width='1' fill='none' fill-rule='evenodd' fill-opacity='0'%3E%3Cg transform='translate(-249.000000, -126.000000)' fill='%23FFFFFF'%3E%3Crect x='249' y='126' width='1' height='1'%3E%3C/rect%3E%3C/g%3E%3C/g%3E%3C/svg%3E)

图 3.实验测量方法

**问卷调查设计：** 问卷（图4）分为两大部分。第一部分收集受访者的个人基本信息（如年龄、性别）、社会经济背景（如收入、教育程度）、个人行为特征（如着装、活动水平）以及与空间使用相关的心理因素（如到访目的、停留时长、同伴情况）。第二部分则采用多级李克特量表，记录受访者对当前环境的主观热感知，包括总体舒适度（OCV）、热感觉（TSV）、热舒适度（TCV）和热可接受度（TAF）等。

![Image](data:image/svg+xml,%3C%3Fxml version='1.0' encoding='UTF-8'%3F%3E%3Csvg width='1px' height='1px' viewBox='0 0 1 1' version='1.1' xmlns='http://www.w3.org/2000/svg' xmlns:xlink='http://www.w3.org/1999/xlink'%3E%3Ctitle%3E%3C/title%3E%3Cg stroke='none' stroke-width='1' fill='none' fill-rule='evenodd' fill-opacity='0'%3E%3Cg transform='translate(-249.000000, -126.000000)' fill='%23FFFFFF'%3E%3Crect x='249' y='126' width='1' height='1'%3E%3C/rect%3E%3C/g%3E%3C/g%3E%3C/svg%3E)

图 4.室外热舒适度问卷

**数据分析与热基准建立：** 首先，利用SPSS和Origin软件对收集到的数据进行描述性统计分析，揭示不同LCZ类型下微气候参数的差异以及受访者属性的分布特征。随后，采用单因素方差分析（ANOVA）和Tukey事后检验来确定不同LCZ类型之间的气象参数是否存在显著差异。核心步骤是建立热舒适基准，研究选取了国际通用的通用热气候指数（UTCI）作为评价指标，通过线性回归分析受访者的平均热感觉投票（MTSV）与UTCI之间的关系，确定了每个LCZ类型乃至每个具体样点的中性UTCI（NUTCI）及其舒适范围（NUTCIR）。

**影响因素的多元分析与机器学习建模：** 为了解析多维度因素对热感知的影响，研究首先采用有序逻辑回归（Ordinal Logistic Regression）模型，分别在每个样点和每个LCZ类型的层面上，分析物理、个人、社会和心理四大类因素对各项热感知投票（OCV, TSV, TCV, TAV）的综合影响。最后，为了进一步探究各因素的非线性作用机制和相对重要性，研究采用了CatBoost机器学习模型来预测总体舒适度（OCV），并结合SHAP（SHapley Additive exPlanations）可解释性分析方法，直观地展示了在不同LCZ类型中，各个影响因素对模型预测结果的贡献方向和大小，从而识别出主导因素。

**03**

**主要结果**

热舒适感知的空间分异显著：不同LCZ类型的建成环境下，居民的夏季热舒适感知存在显著差异。整体而言，绿地和水体丰富的LCZ A（公园）以及高品质的LCZ 4（开敞高层住宅）表现出较高的热舒适度。相比之下，LCZ 1-2（紧凑高/中层）商业区由于建筑密集、通风不畅，热不适感最为强烈。有趣的是，LCZ 5（开敞中层）区域的热舒适度也相对较低，这可能与其较高的空间暴露度和较少的绿化有关（图6）。

![Image](data:image/svg+xml,%3C%3Fxml version='1.0' encoding='UTF-8'%3F%3E%3Csvg width='1px' height='1px' viewBox='0 0 1 1' version='1.1' xmlns='http://www.w3.org/2000/svg' xmlns:xlink='http://www.w3.org/1999/xlink'%3E%3Ctitle%3E%3C/title%3E%3Cg stroke='none' stroke-width='1' fill='none' fill-rule='evenodd' fill-opacity='0'%3E%3Cg transform='translate(-249.000000, -126.000000)' fill='%23FFFFFF'%3E%3Crect x='249' y='126' width='1' height='1'%3E%3C/rect%3E%3C/g%3E%3C/g%3E%3C/svg%3E)

图 6.不同建筑环境中的主观热感知投票 (a) OCV (b) TSV (c) TCV (d) TAV

**热舒适基准的异质性：** 尽管LCZ分类为城市形态提供了标准化框架，但研究发现即便是同一LCZ类型内部，其热舒适基准也存在显著的空间差异；而不同LCZ类型之间的基准差异反而相对有限。这表明单一空间样本不足以代表整个LCZ类型的热特征。具体来看，LCZ 5（开敞中层）区域展现出最高的中性UTCI阈值（NUTCI = 23.28 °C），表明该区域在夏季体感上更热。与之形成鲜明对比的是，LCZ 4（开敞高层）区域的中性UTCI最低（NUTCI = 20.46 °C），反映了其相对凉爽的微气候环境（图7）。

![Image](data:image/svg+xml,%3C%3Fxml version='1.0' encoding='UTF-8'%3F%3E%3Csvg width='1px' height='1px' viewBox='0 0 1 1' version='1.1' xmlns='http://www.w3.org/2000/svg' xmlns:xlink='http://www.w3.org/1999/xlink'%3E%3Ctitle%3E%3C/title%3E%3Cg stroke='none' stroke-width='1' fill='none' fill-rule='evenodd' fill-opacity='0'%3E%3Cg transform='translate(-249.000000, -126.000000)' fill='%23FFFFFF'%3E%3Crect x='249' y='126' width='1' height='1'%3E%3C/rect%3E%3C/g%3E%3C/g%3E%3C/svg%3E)

图 7.不同建筑环境和 LCZ 类型中的 NUTCI 和 NUTCIR

**影响因素的多维度与空间变异性：** 有序逻辑回归和机器学习分析揭示，居民的热感知是物理、心理、社会和个人等多维度因素复杂交互作用的结果，且主导因素因空间（LCZ类型）而异。

物理因素（如气温Ta、太阳辐射G）的基石作用被普遍证实，但在不同空间其影响程度和方式各异。例如，风速（Va）在LCZ 6（开敞低层）中对缓解热感有显著作用，但在建筑密集的LCZ 1-2中则效果不彰。

个人因素中，“年龄”和“活动水平”是关键调节变量。老年人普遍表现出对高温更高的耐受力，热感觉更低。

社会因素如“教育程度”和“收入”也显示出重要影响，尤其是在LCZ 4中，高收入群体由于居住环境品质更高，其热舒适感也更强。

心理因素，特别是“到访频率”（FoV）和“到访目的”（PoV），在旅游休闲导向的空间（如LCZ 6和LCZ A）中扮演了极其重要的角色，高频率的到访和以休闲为目的的活动能显著提升个体的热舒适体验（图8，图9）。

![Image](data:image/svg+xml,%3C%3Fxml version='1.0' encoding='UTF-8'%3F%3E%3Csvg width='1px' height='1px' viewBox='0 0 1 1' version='1.1' xmlns='http://www.w3.org/2000/svg' xmlns:xlink='http://www.w3.org/1999/xlink'%3E%3Ctitle%3E%3C/title%3E%3Cg stroke='none' stroke-width='1' fill='none' fill-rule='evenodd' fill-opacity='0'%3E%3Cg transform='translate(-249.000000, -126.000000)' fill='%23FFFFFF'%3E%3Crect x='249' y='126' width='1' height='1'%3E%3C/rect%3E%3C/g%3E%3C/g%3E%3C/svg%3E)

图 8.不同建成环境下的有序逻辑回归模型回归估计结果

![Image](data:image/svg+xml,%3C%3Fxml version='1.0' encoding='UTF-8'%3F%3E%3Csvg width='1px' height='1px' viewBox='0 0 1 1' version='1.1' xmlns='http://www.w3.org/2000/svg' xmlns:xlink='http://www.w3.org/1999/xlink'%3E%3Ctitle%3E%3C/title%3E%3Cg stroke='none' stroke-width='1' fill='none' fill-rule='evenodd' fill-opacity='0'%3E%3Cg transform='translate(-249.000000, -126.000000)' fill='%23FFFFFF'%3E%3Crect x='249' y='126' width='1' height='1'%3E%3C/rect%3E%3C/g%3E%3C/g%3E%3C/svg%3E)

图 9.不同LCZ 类型中有序逻辑回归模型回归估计的结果

**机器学习模型的可解释性洞察：** CatBoost与SHAP的结合分析进一步量化了各因素的贡献。例如，在LCZ 1-2中，街道宽高比（H/W）是导致热不适的最主要形态因素；而在LCZ 5中，风速（Va）则成为提升舒适度的关键有利因素；在LCZ A（公园）中，绿视率（GVI）和个人活动水平成为影响舒适度的核心变量（图11）。

![Image](data:image/svg+xml,%3C%3Fxml version='1.0' encoding='UTF-8'%3F%3E%3Csvg width='1px' height='1px' viewBox='0 0 1 1' version='1.1' xmlns='http://www.w3.org/2000/svg' xmlns:xlink='http://www.w3.org/1999/xlink'%3E%3Ctitle%3E%3C/title%3E%3Cg stroke='none' stroke-width='1' fill='none' fill-rule='evenodd' fill-opacity='0'%3E%3Cg transform='translate(-249.000000, -126.000000)' fill='%23FFFFFF'%3E%3Crect x='249' y='126' width='1' height='1'%3E%3C/rect%3E%3C/g%3E%3C/g%3E%3C/svg%3E)

图 11.基于SHAP 值的 LCZ 类别之间的 OCV 预测模型

**04**

**研究创新点**

**热舒适基准的精细化建立与比较：** 不仅为大连市不同LCZ类型建立了精细化的夏季热舒适基准（NUTCI），还通过与西安等内陆城市的比较，首次实证揭示了沿海城市由于其特殊气候条件（如海陆风），其热舒适基准范围显著窄于内陆城市（图10）。

**先进分析方法的综合应用：** 本研究综合运用了有序逻辑回归、CatBoost机器学习和SHAP可解释性分析等多种先进统计与AI方法，不仅准确预测了热舒适，更深入、直观地揭示了不同建成环境下各影响因素的非线性作用和相对重要性，为精准的城市设计干预提供了科学依据。

**05**

**实验所用的具体技术、壁垒与仪器信息**

**具体技术与壁垒：**

**大规模协同调查的组织能力：** 在14个分散的城市地点同步开展高强度的微气候测量和问卷调查，需要精密的组织协调、大量训练有素的调查员以及严格的质量控制流程，这是研究实施的主要难点。

**多源数据整合与分析技术：** 研究需要处理和分析两大类异构数据：高频的客观物理测量数据和大规模的主观问卷数据。将这两者在时空上精确匹配，并运用有序逻辑回归、机器学习等高级统计方法进行综合分析，对研究者的数据处理和建模能力提出了很高要求。

**LCZ框架的应用与解读：** 将实地样点准确地对应到LCZ分类框架中，并基于此进行差异化分析和基准建立，需要对LCZ理论有深刻的理解和实践经验。

**可解释性AI技术的应用：** 使用SHAP等前沿技术来解释复杂的CatBoost模型，将“黑箱”模型的预测结果转化为设计师和规划师可以理解的、具有指导意义的洞察，是本研究在方法上的一个技术亮点和难点。

**所用仪器及其型号（见表2）：**

**综合热舒适仪：** JTR10 WBGT仪，用于测量黑球温度。

**太阳辐射计：** HD2102.2。

**风速计：** Kestrel 5500手持气象站。

**温湿度记录仪：** HOBO MX2301。

**其他设备：** 用于拍摄鱼眼照片以计算天空开阔度（SVF）的相机和镜头。

**论文信息**

Zhang, H., Wang, Y., Chen, B., Bai, J., Zhao, J., Guo, F., & Zhu, P. (2025). Analyzing spatial disparities in thermal comfort in a coastal city: A multi-parameter comparative study based on local climate zones. Sustainable Cities and Society, 107031.

https://doi.org/10.1016/j.scs.2025.107031

本文仅为笔者对论文内容的初步理解，不代表原论文的官方观点。如您对该研究感兴趣，欢迎点击文末【阅读原文】阅读完整文献。  

Read more

继续滑动看下一个

城市热环境研究前沿

向上滑动看下一个