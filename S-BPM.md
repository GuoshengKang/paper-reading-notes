## S-BPM
1. **Albert Fleischmann, Stephan Borgert, Matthes Elstermann, Florian Krenn, and Robert Singer. "*An overview to S-BPM oriented Tool Suites*". Proceedings of S-BPM ONE. pp. 30-31, 2017.**  
摘要：文章给出了目前已公布的S-BPM工具，其中介绍了7个工具，有的只适合建模，有的既可以建模也可以执行。可惜没有开源本地执行的工具，具体介绍如下表：<div align=center><img width="500" height="400" src="resources/S-BPM_tool_overview_execution.jpg"/></div>还好，在github上有搜索到开源的[S-BPM建模与实现工具](https://github.com/stefanstaniAIM/IPPR2016)。

2. **Robert Singer. "*Business Process Modeling and Execution--A Compiler for Distributed Microservices*". arXiv preprint arXiv:160105976, Vol. No., pp., 2016.**  
摘要：文章提出BPMS的一些缺点，目前的BPMS主要都是建立在事实的BPMN标准上。然而已有的工具并不是直接支持业务流程模型的执行，而是BPMN向BPLE转化再执行。这意味着概念模型和执行表示之间有一道鸿沟。再者，BPMN建模需要的分析技术和在形式化语言抽象上的经验。这种能力在很多大公司是难以获得的，尤其是在以些小型、中型企业当中。因此，为了克服这些弱点，出现了S-BPM。S-BPM将业务流程看成松散的执行者网络，每个可看成一个微服务。主题（执行者）其实就是流程执行的资源，可以是人也可以是机器。本文回顾了典型的工作流系统架构，并提出了基于执行者的工作流系统架构，如下图所示，这种架构适合流程的内部通信，流程之间通信，及不同企业的流程之间的通信。<div align=center><img width="600" height="350" src="resources/architecture_of_distributed_S-BPM.jpg"/></div>本文讨论了概念模型的如何变成执行代码问题，给出了概念模型编译的工作过程，如下图所示：<div align=center><img width="500" height="300" src="resources/compilation_work_flow_for_S-BPM.jpg"/></div>最后也指出了一些研究问题，都是和实际应用密切相关的。

3. **Matthias Eduard Geisriegler. *Process Mining of Business Process Choreographies*[D], FH JOANNEUM - University of Applied Sciences, Graz, Austria, 2017.**  
摘要：以往的流程挖掘产生的模型是一个编制模型，而这篇硕士论文主要的贡献是可通过流程挖掘产生S-BPM建模方式的流程编排模型，并对其进行了系统集成，S-BPM系统执行平台的体系结构[1]如下图所示：<div align=center><img width="500" height="300" src="resources/architecture_of_S-BPM_execution_platform.jpg"/></div>**[1] Matthias Geisriegler, Maksym Kolodiy, Stefan Stani, and Robert Singer. "*Actor Based Business Process Modeling and Execution: A Reference Implementation Based on Ontology Models and Microservices*". Proceedings of 2017 43rd Euromicro Conference on Software Engineering and Advanced Applications (SEAA). IEEE, pp. 359-362, 2017.**  
[**知识补充**]: [Bipartite graph](https://en.wikipedia.org/wiki/Bipartite_graph)的定义：指顶点可以分成两个不相交的集U和V（U和V皆为独立集（independent sets），使得在同一个集内的顶点不相邻（没有共同边）的图。难怪业务流程的文章中一直提到Workflow net是二分图。工作流模块是能建模流程，使其能够与环境通信。类似的概念——开放工作流亡也提出来了。  
**主要思路**：
   + （1）扩充事件日志属性信息，使其包含通信的信息如下：<div align=center><img width="500" height="120" src="resources/event_log_of_S-BPM.jpg"/></div>
   + （2）使用开源的流程挖掘工具[ProM](http://www.promtools.org)，对挖掘的Petri Net编制流程进行编辑，添加通信接口，从而将WF Net描述的流程（PNML格式）扩充为oWFN或Workflow Module（EPNML格式）一个例子如下：<div align=center><img width="500" height="300" src="resources/compatible_worflow_modules.jpg"/></div>
   + (3) 将EPNML描述的流程映射为OWL描述的流程，使其变为可执行的S-BPM模型。

4. **Albert Fleischmann, Werner Schmidt, and Christian Stary. ''*Subject-oriented business process management*''.  Handbook on Business Process Management 2 Springer, pp. 601-621, 2015.**  
摘要：这篇文章是对S-BPM建模方式与实现介绍比较全面的一篇论文，适合初步了解S-BPM的人看，内容既全面又较新。S-BPM的建模主要分3三个步骤：(1)定义主题；(2)主题交互图；(3)主题行为建模。鉴于对初步了解的人来说，该文献非常重要，因此已对该文献翻译了[中文版本](resources/面向主题的业务流程管理.pdf)。

5. **Albert Fleischmann, Werner Schmidt, and Christian Stary. "Requirements Specification as Executable Software Design-A Behavior Perspective". Proceedings of REFSQ Workshops. pp. 9-18, 2015.**  
摘要：这篇文章给出了一个例子，当需求变化时可通过引入事件消息来扩展和改编主题行为以满足需求或异常处理。该改编例子在以下文献也被提及：  
**Albert Fleischmann, Werner Schmidt, and Christian Stary. ''*Subject-oriented business process management*''.  Handbook on Business Process Management 2 Springer, pp. 601-621, 2015.**  

6. **Peter Forbrig. "*Reuse of models in S-BPM process specifications*". Proceedings of the 7th International Conference on Subject-Oriented Business Process Management. ACM, pp. 6, 2015.**  
摘要：毫无疑问，领域的建模有诸多优势。现也有不同的符号的建模工具，比如：BPMN、S-BPM。尽管有很多工具支持，创建模型依然是一个挑战。从头创建模型非常耗时和易错。使用已有的模型也有一些问题。有时没有完全的执行正确，导致结果错误；也常常模型的一部分忘记改编到新的上下文。因此，重用模型已有部分的工具支持将非常有益。文章首先介绍了BPMN中如何将组件一般化，形成可以复用的组件。基本思想就是将具体业务的用参数进行泛化，使其可以描述通用的流程模型。然后，类似地将通用组件的概念引入到S-BPM中，使其模型可以重用，如下图所示：<div align=center><img width="400" height="300" src="resources/Generic_model_component_for_customer_interaction.jpg"/></div>同时，文章还讨论了不同的组件改编策略，如下图所示：<div align=center><img width="400" height="300" src="resources/Instances_of_the_generic_model_component_presented.jpg"/></div>最后，给出了开发工具支持的需求分析：  
   + 支持浏览和实例化；
   + 支持静态和动态的实例；
   + 支持设计时的决策；
   + 支持模拟。  
1. **A Fleischmann, and W Schmidt. "*S-BPM as a new impetus in Business Process Management: A survey*". BUSINESS INFORMATICS INTERDISCIPLINARY ACADEMIC JOURNAL, Vol. 32, No. 2, pp. 7, 2015.**  
摘要：这是一篇俄文期刊的文章。简单介绍了S-BPM方法的属性，详细介绍了对BPM生命周期活动的影响。这是S-BPM提出者写的一篇综述性文章，值得初了解S-BPM的人读，有简单介绍S-BPM的由来，以及无论在工业界还是学术界引起的轩然大波，文章大张旗鼓S-BPM的优势。文章提到了两个商用的图形符号建模工具：基于Java的[Metasonic Suite](http://www.metasonic.de/)和基于.net的[InFlow](www.strict-solutions.at)。S-BPM的生命周期可以是开放性的，如下图所示：<div align=center><img width="400" height="300" src="resources/linear_and_non-linear_S-BPM-based_organizational_development.jpg"/></div>

1. **Robert Singer, and Stefan Raß. ''*Embodying Business Rules in S-BPM*''.  S-BPM in the Wild Springer, pp. 187-199, 2015.**  
摘要：文章提出在S-BPM中的添加业务规则，增强系统的敏捷度，减少流程适应性的工作。增加了一个业务规则引擎做为外部服务来调用，将规则的评估结果作为主题控制流的决策指导。可能和传统BPM的区别就是，原来的决策是建模在模型当中，有具体的决策点，而现在是独立出来作为一个规则引擎作为服务来调用。

3. **Stephan Schiffner, Thomas Rothschädl, and Nils Meyer. "*Towards a subject-oriented evolutionary business information system*". Proceedings of Enterprise Distributed Object Computing Conference Workshops and Demonstrations (EDOCW), 2014 IEEE 18th International. IEEE, pp. 381-388, 2014.**  
摘要： 这篇文章对演化业务信息系统EBIS和S-BPM进行了比较，目的是提出实现基于S-BPM的演化业务信息系统的软件需求。通过比较，S-BPM基本可以满足演化信息系统的需求属性，因此认为S-BPM是一个恰当的方法来建立演化业务信息系统。文章中对的S-BPM的初步介绍非常简洁且全面，是一个值得借鉴的写法。可惜文章引用的很多关于流程变化管理方面的文献都是德文的，没法阅读。查看其引用的文献又几乎没有，无法真正了解具体的工作。鉴于对S-BPM驱动的演化业务信息系统的软件需求描述比较完整，还给出了S-BPM驱动的EBIS的概念设计如下图所示，这对流程的变化管理非常重要，因此已对该文献翻译了[中文版本](resources/面向主题的演化业务信息系统.pdf)。<div align=center><img width="400" height="350" src="resources/Conceptual_Design_S-BPM-driven_EBIS.jpg"/></div>


3. **Patrick Garon, Arnd Neumann, and Frank Bensberg. "*Design of a Subject-Oriented Reference Model for Change Management*". Proceedings of International Conference on Subject-Oriented Business Process Management. Springer, pp. 74-88, 2014.**  
摘要： 文章以S-BPM的建模方式提出了一个变化管理流程的参考模型，介绍了各个subject的职责，从变化的提出、审核及实现等环节，参考模型如下图所示：<div align=center><img width="400" height="300" src="resources/SIDforChangeManagementProcess.jpg"/></div>

3. **Robert Singer, Johannes Kotremba, and Stefan Raß. "*Modeling and execution of multienterprise business processes*". Proceedings of 2014 IEEE 16th Conference on Business Informatics (CBI). IEEE, pp. 68-73, 2014.**  
摘要：业务流程不只是规则系统的工作流（输入、黑盒、输出），它们常常有很深的社会方面，只要有人工参与的涉入。文章讨论了分布式的BPM，定义为多代理的系统，这和S-BPM的理念如出一辙，并给出了实现的体系结构，用服务交互的例子来阐述体系结构的功能，以说明S-BPM是一个很自然的方式来建模和执行分布式流程。

2. **Albert Fleischmann, Werner Schmidt, Christian Stary, Stefan Obermeier, and Egon Börger. *Subject-oriented business process management*. Springer Science & Business Media, 2012.**   
摘要：这本书对S-BPM建模、验证、优化、实现、监控、建模工具进行全面的介绍。

6. **Robert Gottanka, and Nils Meyer. "*ModelAsYouGo:(re-) design of S-BPM process models during execution time*". Proceedings of International Conference on Subject-Oriented Business Process Management. Springer, pp. 91-105, 2012.**  
摘要：文章引入了一个新方法（即，ModelAsYouGo）来建模S-BPM业务流程，使得执行者们在执行实例时可以记录他们的主题通信和内部行为。主题 的每个用户可以建模自己的内部行为，发送和接收信息。当流程涉及多个参与者时，这时协作就发生了。ModelAsYouGo使得流程执行者们可以以一种容易和社会化的方式设计可靠的模型。因此，执行者将成为业务世界的主角。可惜文章从头到尾连一个图和一个例子都没有，全是文字介绍，各种空白喊白话该方法可以干嘛干嘛，但是读之后就是不知道具体是怎么干的。文章将方法的评估的案例的系统实现作为了未来工作。不过，文章提到结构化流程的概念，值得提一下：
   + 结构化流程：是指流程模型描述从端到端严格地预定义好，不存在会偏离流程模型的实例；
   + 半结构化流程：是指生命周期没有被一个形式化模型完全定义好的业务或系统流程。通常该流程具有不完全的流程视图，流程只是以流程图，流图或抽象状态机的形式给出，其流程执行不完全被中心实体所控制。相反，使用了各种IT和人工的机制，包括email、内容管理系统、基于WEB的表单、定制应用或者这些的组合。
   + 非结构化流程：是指不可预测的流程。该流程敏感依赖于外部因素，这些因素超越了流程上下文的控制。因此，这样的流程不能根据内部状态而固化起来。

7. **Robert Singer, and Erwin Zinser. "*Business Process Management—S-BPM a New Paradigm for Competitive Advantage?*". Proceedings of International Conference on Subject-Oriented Business Process Management. Springer, pp. 48-70, 2009.**  
摘要：本文提出了业务和IT之间的鸿沟，BPMN这个建模符号标准依然不是一个好理解的东西。尤其是一些移动行为（比如：发邮件）不能容易地在传统的工作流引擎中建模和实现。因此需要一种新的建模方法来适应移动行为的环境，即S-BPM。文章还大谈教育中如何设置S-BPM课程，以对比与传统BPMN建模的各样优势，以推广这样的研究到企业当中去。这篇文章给出S-BPM是一个具有前景的方法几个事实：  
   + 面向消息的集成  
   + 面向行为建模型方法  
   + 简洁的建模符号集合  
   + 流程可以采用自然语言建立  
   + 流程模型本质上是严格形式化定义的，不需要人工干预即可执行

8. **Jan Vom Brocke, and Michael Rosemann. *Business Process Management*. Springer, 2015.**  
摘要：
