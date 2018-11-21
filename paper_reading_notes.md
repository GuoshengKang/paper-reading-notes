文献阅读笔记
1.	Yiren Wang, Dominic Seyler, Shubhra Kanti Karmaker Santu et al., "A Study of Feature Construction for Text-based Forecasting of Time Series Variables." pp. 2347-2350.
摘要：从文本提取词的词语重要性及主题作为预测的输入特征，对于一些受舆情影响的预测有效。

2.	Tsan-Ming Choi, Chi-Leung Hui, Na Liu et al., “Fast fashion sales forecasting with limited data and time,” Decision Support Systems, vol. 59, pp. 84-92, 2014.
摘要：ELM+GM=3F (Fast Fashion Forecasting)。实验仅用了3个周期数据预测4个周期。ELM：学习速度快，但要求一定数量的训练数据才能有比较合理的预测。GM：适用数据非常少的情况，对有一定趋势的变量预测较准，但是对预测变量波动的情况效果很差。

3.	Qi Wu, “The forecasting model based on wavelet ν-support vector machine,” Expert Systems with Applications, vol. 36, no. 4, pp. 7604-7610, 2009.
摘要：针对小样本数据的季节、非线性、不确定性（随机）特征，提出了一种新的小波支持向量机方法WN v-SVM，利用小波核函数进行线性的空间转换，PS算法用来选择WN v-SVM的最优参数。因而整个模型称为PSWN v-SVM。其中，语言描述的特征通过模糊预处理（具体不详）。特征有权重，但不知道怎么来的以及后续如何处理的？需查看其它的文献。案例：汽车销量预测
 
4.	Zhi-Ping Fan, Yu-Jie Che, and Zhen-Yu Chen, “Product sales forecasting using online reviews and historical sales data: A method combining the Bass model and sentiment analysis,” Journal of Business Research, vol. 74, pp. 90-100, 2017.
摘要：利用朴素贝叶斯计算在线评论的情感指数。将情感指数用于扩展Bass/Norton模型的模仿系数从而进行汽车的销量预测。

5.	Real Carbonneau, Kevin Laframboise, and Rustam Vahidov, “Application of machine learning techniques for supply chain demand forecasting,” European Journal of Operational Research, vol. 184, no. 3, pp. 1140-1154, 2008.
摘要：比较了不同方法在供应链中协同需求预测中的优劣，实验结果显示RNN和SVM较优。（Naı¨ve Forecast、Average、 Moving Average、 Trend、 Multiple Linear Regression、 Neural Networks、 Recurrent Neural Networks、Support Vector Machines）。具体特征考虑未提及，模型的具体使用也不详细。

6.	Nengbao Liu, Vahan Babushkin, and Afshin Afshari, “Short-term forecasting of temperature driven electricity load using time series and neural network model,” Journal of Clean Energy Technologies, vol. 2, no. 4, pp. 327-331, 2014.
摘要：ANN和SARIMAX用来预测短期的电力消耗。利用“预白燥”处理温度对电力消耗的影响期数，并将季节性因素（日、周、年）考虑进来，最后采用SARIMAX进行预测。数据预处理和模型过程介绍不清楚。

7.	Mirko Mazzoleni, S Formentin, Fabio Previdi et al., “Control-oriented modeling of SKU-level demand in retail food market,” IFAC-PapersOnLine, vol. 50, no. 1, pp. 13003-13008, 2017.
摘要：提出了销量因素的考虑，讲不同的销量分成不同的类型考虑；同样，将一年中不同的时间划分成6段，成为6个类别变量。最后，使用线性模型进行拟合。优点：考虑了过去两期的预测误差；缺点：只能预测2期。

8.	https://stats.stackexchange.com/questions/114385/what-is-the-difference-between-convolutional-neural-networks-restricted-boltzma
摘要：讨论CNN、RBM、Auto-encoder的区别如下：
All three models have their use cases, pros and cons, but probably the most important properties are:
1.	Autoencoders are simplest ones. They are intuitively understandable, easy to implement and to reason about (e.g. it's much easier to find good meta-parameters for them than for RBMs).
2.	RBMs are generative. That is, unlike autoencoders that only discriminate some data vectors in favour of others, RBMs can also generate new data with given joined distribution. They are also considered more feature-rich and flexible.
3.	CNNs are very specific model that is mostly used for very specific task (though pretty popular task). Most of the top-level algorithms in image recognition are somehow based on CNNs today, but outside that niche they are hardly applicable (e.g. what's the reason to use convolution for film review analysis?).

9.	姜艳梅, and 卜庆凯, “基于数据挖掘的超市商品销量预测,” Hans Journal of Data Mining, vol. 8, no. 02, pp. 74, 2018.
摘要：论文提出采用LightGBM预测模型进行短期超市商品的销量预测，LightGBM是结合了分类树和回归树的一种组合模型，发现结果比单一的模型效果要好。文中提到的特征工程师值得参考的：静态特征提取+动态特征；静态特征提取是指一些统计特征，而动态特征是通过基本特征和销售特征作为训练数据，利用用 SVR 模型进行处理，提取商品销售的商品销量周期性指数，用来作为商品销量的动态特征。缺点：论文描述过于简单，难以清除的具体特征处理及LightGBM方法原理和实现。

10.	Maria Elena Nenni, Luca Giustiniano, and Luca Pirolo, “Demand forecasting in the fashion industry: a review,” International Journal of Engineering Business Management, vol. 5, no. Godište 2013, pp. 5-36, 2013.
摘要：本文提出了需求分类的指标

11.	Rafael S Gutierrez, Adriano O Solis, and Somnath Mukhopadhyay, “Lumpy demand forecasting using neural networks,” International Journal of Production Economics, vol. 111, no. 2, pp. 409-420, 2008.
摘要：本文提出了使用neural network来解决lumpy类型的销量预测，输入为（前一期的销量，前一期最近零销量的间隔天数）。个人感觉特征取得很有代表性，但是感觉特征数量有点少。

12.	A Nasiri Pour, B Rostami Tabar, and A Rahimzadeh, “A hybrid neural network and traditional approach for forecasting lumpy demand,” Proc. World Acad. Sei. Eng. Technol, vol. 30, pp. 384-389, 2008.
摘要：论文引用了上一篇论文，提出了hybrid proposed method (HPM) (HPM)，首先使用MLP预测销量是否发生(0/1)；然后针对发生的销量，使用exponential smoothing预测具体销量数值。实验比较了SBA、MLP、GRNN、RNN集中方法，结果表明HPM方法有较好的综合预测精度。各模型的输入介绍比较清楚，可以借鉴。其中，HPM的输入如下：
1. The demand at the end of the immediately preceding target period (lag 1).
2. The number of periods separating the last two nonzero demand transactions as of the end of the immediately preceding target period.
3. The number of period(s) between target period and first nonzero demand immediately preceding target period.
4. The number of period(s) between target period and first zero demand immediately preceding target period.

13.	毕建涛, and 魏红芹, “改进的 BP 神经网络及其在销量预测中的应用,” 山东理工大学学报: 自然科学版, vol. 25, no. 6, pp. 29-33, 2011.
摘要：本文提出基于PCA的PSO-BP销量预测模型，具体过程是：首先使用PCA对输入数据进行降维，简化BP的结构；然后使用PSO搜索较优的BP初始化参数，加速BP的收敛和更小的概率陷入局部最优解；最后，BP进行训练模型。实验使用S品牌服装为例，与标准的BP和基于PCA的BP进行比较，结果较优。该文献可以参考的一点是实验中有给出考虑的特征，但是没有给出具体的数据处理：促销价格折扣、促销活动天数、广告活动投入、竞争对手的促销活动、产品需求的季节性、产品所处的生命周期、社会消费品零售总额、消费者价格指数
