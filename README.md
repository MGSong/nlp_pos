# 词表示论文资源

|    论文题目    |   关键词＋概述   | 资源路径 | 说明（创新点） |
| ----------- | ------------------- | ----- | -------|
|[Exploiting Similarities among Languages for Machine Translation](https://arxiv.org/pdf/1309.4168.pdf)| 词向量，双语翻译baseline||1. 使用简单线性矩阵乘法学习语言A到语言B的映射 2. 构造评测集以及构造对照组的方法。如使用编辑距离，Word Co-occurrence构造的对照组|
|[Word Translation Without Parallel Data](https://arxiv.org/pdf/1710.04087.pdf)| 多语言的Embedding，对抗学习|[代码地址](https://github.com/facebookresearch/MUSE)|用对抗学习语言A到语言B的映射 |
|[Transfer Learning for Deep Sentiment Analysis](http://www.aclweb.org/anthology/P18-1235)|带情感信息的Embedding，迁移学习||误差函数的设计，加了正则，该正则使得学到网络对已知情感标签的词效果好；可借鉴评测方式|
|[Normalized Word Embedding and Orthogonal Transform for Bilingual Word Translation](http://www.aclweb.org/anthology/N15-1104)| Normalized Word Embedding以及Orthogonal Transform可提高Bilingual分类性能||提高模型训练效率以及稳定性的方法（normalize+正则），容易工程实现|
|[Training Neural Word Embeddings For Transfer Learning And Translation](http://scholar.sun.ac.za/handle/10019.1/98758)|迁移学习的Embedding|||
|[Wiktionary-Based Word Embeddings](http://www.mt-archive.info/15/MTS-2015-DeMelo.pdf)|wiki字典，多语言全局embedding||基于词与词之间的关系（使用加权内积）建模|
|[Adversarial Network Embedding](https://arxiv.org/pdf/1711.07838.pdf)|对抗网络Embedding|||
|[Interpretable Adversarial Perturbation in Input Embedding Space for Text](https://www.ijcai.org/proceedings/2018/0601.pdf)|对抗扰动生成方式，此对抗样本||对抗扰动生成方式增加限制，另其仅在有实际意义的word的方向变动，而非随机任意方向变动（后续或者可以加入更强限制，比如lm模型）|
|[Enriching Word Vectors with Subword Information](https://research.fb.com/wp-content/uploads/2017/06/tacl.pdf)|char n-gram，形态学词向量||使用char级别的 n-gram 特征建模，得到表征词形态的词向量|
|[Linguistic Regularities in Sparse and Explicit Word Representations](http://www.aclweb.org/anthology/W14-1618)|||nothing special|
|[Advances in Pre-Training Distributed Word Representations](https://arxiv.org/pdf/1712.09405)|词向量训练优化手段||词频为Zipf分布，需要提高高频词的discard probability；类似attention的加权context embedding；可以用mutual information criterion从数量爆炸的n-gram中选择少部分信息量大的|
|[Learning to Compose Words into Sentences with Reinforcement Learning](https://arxiv.org/pdf/1611.09100)|tree-structured representations,增强学习|||
|[Recent Trends in Deep Learning Based Natural Language Processing](http://2www.sentic.net/deep-learning-for-nlp-review.pdf)|多个nlp任务 state of art 方法||多个nlp任务最新进展，参考价值很大|
|[Invariant Variation Problems](https://arxiv.org/pdf/physics/0503066)|经典不变量分析|[其他链接](http://www.neo-classical-physics.info/uploads/3/0/6/5/3065888/noether_-_invariant_variational_problems.pdf)|最经典论文,可以参考https://en.wikipedia.org/wiki/Noether%27s_theorem|
|[Lexicon infused phrase embeddings for named entity resolution](https://arxiv.org/pdf/1404.5367.pdf)|词典，Phrase Embeddings||改装skip-gram，除了预测上下文的context外，还预测辞典中与改词关联的context|
|[Improved Word and Symbol Embedding for Part-of-Speech Tagging](https://denero.org/content/pubs/snl17_altieri_tagging.pdf)|词向量的使用技巧||byte-pair encoding|
|[Unsupervised POS Induction with Word Embeddings](http://www.aclweb.org/anthology/N15-1144)|HMM、多元高斯分布||skip-gram减小window size更利于获取语法信息；假设某个tag对应的词向量符合多元高斯分布|
|[Improving the Accuracy of Pre-trained Word Embeddings for Sentiment Analysis](https://arxiv.org/ftp/arxiv/papers/1711/1711.08609.pdf)|通过简单concat的方法改进词向量||直接简单concat word2vec、glove、pos2vec、leicon2vec，缺点是需要引入外部有监督数据|
|[Part-Of-Speech Tag Embedding for Modeling Sentences and Documents](https://escholarship.org/uc/item/0vk28220)|POS Embedding||nothing special|
|[Diagnosing and Enhancing VAE Models](https://openreview.net/pdf?id=B1e0X3C9tQ)|ICLR 2019接收论文| ||
|[使用生成式对抗网络进行远距离监督关系抽取](https://arxiv.org/pdf/1805.09929)||[其他链接](https://mp.weixin.qq.com/s/mEwJs3ayo9iSg0S2uEfWdQ)|用对抗网络进行样本去噪，generator和discriminator目标相反，generator尽可能预测样本干净度，预测出来的标签取反放入discriminator训练，训练直到discriminator性能下降最大为止（discriminator初始时和generator的目标一样）。|
|[Phrase-Based & Neural Unsupervised Machine Translation](https://arxiv.org/pdf/1804.07755.pdf)|非监督机器翻译|||
|[Unsupervised Part-of-Speech Taggingwith Bilingual Graph-Based Projections](https://aclanthology.info/pdf/P/P11/P11-1061.pdf)|非监督 POS Tagging|||
|[Distinguishing Antonyms and Synonyms in a Pattern-based Neural Network](https://arxiv.org/pdf/1701.02962.pdf)|有监督训练word pair关系||借助 parse tree 特征有监督训练反义word pair，基本假设是在同一句话里，反义词同时出现的概率大于同义词同时出现的概率|
|[Integrating Distributional Lexical Contrast into Word Embeddings for Antonym–Synonym Distinction](https://arxiv.org/pdf/1605.07766.pdf)|训练能区分同义词的embedding|[代码地址](https://github.com/nguyenkh/AntSynDistinction)|两种方法，方法一是在普通的词向量的目标函数中加上同义词和反义词的正则；方法二是给词向量的各个特征re－weight，能区分反义词的特征加大权重|
|[Evaluating semantic relations in neural word embeddings with biomedical and general domain knowledge bases](https://www.ncbi.nlm.nih.gov/pmc/articles/PMC6069806/)|评测词向量捕捉到的各种语义或语法关系|[代码地址](https://github.com/zwChan/Wordembedding-and-semantics)|评测三种词向量在semantic task的效果；词向量捕捉的关系有8种|
|[Refining Word Embeddings for Sentiment Analysis](https://www.aclweb.org/anthology/D17-1056)|2018，使用单词极性信息进行有监督refine||取一个词的top k个最近的词向量，然后使用对应的极性分数对词进行重排序，并将这个重排序的作用反馈到原向量|
|[Retrofitting Word Vectors to Semantic Lexicons](https://arxiv.org/pdf/1411.4166.pdf)|2014，使用辞典的语义信息进行词向量的refine|  [代码地址](https://github.com/mfaruqui/retrofitting) [代码地址2](https://github.com/mfaruqui/eval-word-vectors) [代码地址3](https://github.com/mfaruqui/non-distributional)|和这篇Refining Word Embeddings for Sentiment Analysis基本一样|
|[Refining Pretrained Word Embeddings Using Layer-wise Relevance Propagation](http://citeseerx.ist.psu.edu/viewdoc/download?doi=10.1.1.780.435&rep=rep1&type=pdf)|2018|[其他地址](http://www.aclweb.org/anthology/D18-1520)|让特征相关分数按layer进行后向传播进行refine词向量；|
|[SeVeN: Augmenting Word Embeddings with Unsupervised Relation Vectors](https://arxiv.org/pdf/1808.06068)|2018||1、基于PMI构造无监督特征，进而得到无监督关系；2、使用AutoEncoder进行去噪。 3、方法思路挺好，但是感觉效果提升不大|
|[Black-box Generation of Adversarial Text Sequences to Evade Deep Learning Classifiers](https://arxiv.org/pdf/1801.04354.pdf)|2018|||
|[Adversarial Training for Relation Extraction](http://www.aclweb.org/anthology/D17-1187)|2017，对抗学习|  [代码地址](https://github.com/jxwuyi/AtNRE)|使用对抗样本提高分类器的稳定性|
|[Adversarial Feature Matching for Text Generation](https://arxiv.org/pdf/1706.03850.pdf)|2017,文本生成||在标准的gan loss中加入了 Maximum Mean Discrepancy 项。通过将文本map到某个feature空间，然后再通过RKHS技术进行相似度的度量|
|[From Word to Sense Embeddings: A Survey on Vector Representations of Meaning](https://arxiv.org/pdf/1805.04032.pdf)|2018||写的比较凌乱|
|[Jointly Learning Word Embeddings and Latent Topics](https://arxiv.org/pdf/1706.07276.pdf)|2017，联合训练特定topic的embedding ||借鉴LDA的思想，给标准的skip-gram模型加上主题因子，用EM算法进行迭代优化|
|[Distilled Wasserstein Learning for Word Embedding and Topic Modeling](http://120.52.51.16/papers.nips.cc/paper/7443-distilled-wasserstein-learning-for-word-embedding-and-topic-modeling.pdf)|2018|||
|[Multi-Task Label Embedding for Text Classification](http://aclweb.org/anthology/D18-1484)|2018||多任务学习，label embedding|
|[Factors Influencing the Surprising Instability of Word Embeddings](https://arxiv.org/pdf/1804.09692.pdf)|2018|||
|[The Interplay of Semantics and Morphology in Word Embedding](https://arxiv.org/pdf/1704.01938.pdf)|2017| [代码地址1](https://github.com/oavraham1/prop2vec)  [代码地址2](https://github.com/oavraham1/ag-evaluation)|词的相似性分为语义相似性和词态相似性；若想增加semantic similarity，可以使用lemma，但会损害 morphology similarity|
|[Joint Embedding of Words and Labels for Text Classification](https://arxiv.org/pdf/1805.04174.pdf)|2018 有监督| [代码地址](https://github.com/guoyinwang/LEAM)|将label嵌入到词向量空间，通过label和词的相似度矩阵构建attention权值|
|[Domain Separation Networks](http://120.52.51.17/papers.nips.cc/paper/6254-domain-separation-networks.pdf)|2016|||
|[RAND-WALK: A Latent Variable Model Approach to Word Embeddings](https://arxiv.org/pdf/1502.03520)|2016| [代码地址](https://github.com/YingyuLiang/SemanticVector)||
|[Linear Algebraic Structure of Word Senses, with Applications to Polysemy](https://arxiv.org/pdf/1601.03764)|2016|  [代码地址](https://github.com/YingyuLiang/SemanticVector)||
|[Querying Word Embeddings for Similarity and Relatedness](http://aclweb.org/anthology/N18-1062)|2018|||
|[A Rank-Based Similarity Metric for Word Embeddings](https://arxiv.org/pdf/1805.01923.pdf)|2018|||
|[Improving Word Embeddings with Convolutional Feature Learning and Subword Information](https://www.aaai.org/ocs/index.php/AAAI/AAAI17/paper/download/14724/14187)|2017||
|[Computing Text Similarity using Tree Edit Distance](http://www.cic.ipn.mx/~sidorov/sngrams_ted_2015.pdf)|2015|||
|[Normalisation of Historical Text Using Context-Sensitive Weighted Levenshtein Distance and Compound Splitting](http://120.52.51.13/www.ep.liu.se/ecp/085/017/ecp1385017.pdf)|2013|||
|[Explicit Retrofitting of Distributional Word Vectors](http://www.aclweb.org/anthology/P18-1004)|2018||使用nn拟合一个新的度量空间映射，使得在新的度量空间里满足同义反义词距离条件，且保持愿空间的拓扑结构；还可借鉴一种数据增强方法|
|[Unsupervised Learning of Style-sensitive Word Vectors](http://aclweb.org/anthology/P18-2091)|2018，可捕捉 Stylistic Similarity版的CBOW||为捕捉 semantic and syntactic similarities，使用context预测target；为了捕捉Stylistic Similarity，使用非context预测target|
|[Adversarial Propagation and Zero-Shot Cross-Lingual Transfer of Word Vector Specialization](https://arxiv.org/pdf/1809.04163.pdf)|2018，对抗学习，词向量微调|[代码地址](https://github.com/cambridgeltl/adversarial-postspec)|它先使用外部辞典进行词向量refine，得到一部分词的refined词向量；利用前一步的结果作为训练集，使用gan进行原始词向量到refine词向量映射的学习|
|[Using pseudo-senses for improving the extraction of synonyms from word embeddings](http://aclweb.org/anthology/P18-2056)|2018 acl||创新点在于将一句话拆成context－target的方式，在原有方式基础上，增加一个target在同一句话整体的context描述方式。refine词向量的方式有paragram和Retrofitting两种，它这里使用paragram|
|[Auto-Encoding Dictionary Definitions into Consistent Word Embeddings](http://aclweb.org/anthology/D18-1181)|2018 emnlp||仅仅使用辞典定义来训练词向量，可以更好捕获词的similarity；refine词向量时也可以考虑将辞典定义这种关系考虑进去|
|[Gromov-Wasserstein Alignment of Word Embedding Spaces](http://aclweb.org/anthology/D18-1214)|2018 emnlp|||
|[Word Relation Autoencoder for Unseen Hypernym Extraction Using Word Embeddings](http://aclweb.org/anthology/D18-1519)|2018 emnlp||为了避免对训练样本过拟合（即在训练集出现对pair效果好），从对（w1，w2）建模转为 （w1，w2-w1）建模，并使用AutoEncoder|
|[Learning Gender-Neutral Word Embeddings](https://aclanthology.info/papers/D18-1521/d18-1521)|2018 emnlp|||
|[Specialising Word Vectors for Lexical Entailment](http://aclweb.org/anthology/N18-1103)|2018 naacl||使用外部关系词进行映射训练|
|[DeepAlignment: Unsupervised Ontology Matching with Refined Word Vectors](https://aclanthology.info/papers/N18-1072/n18-1072)|2018 naacl|||
|[Enhanced Word Representations for Bridging Anaphora Resolution](https://aclanthology.info/papers/N18-2001/n18-2001)|2018 naacl|||
|[Relation Induction in Word Embeddings Revisited](https://aclanthology.info/papers/C18-1138/c18-1138)|2018 coling|||
|[Encoding Sentiment Information into Word Vectors for Sentiment Analysis](http://aclweb.org/anthology/C18-1085)|2018 coling|||
|[Word Sense Disambiguation Based on Word Similarity Calculation Using Word Vector Representation from a Knowledge-based Graph](https://aclanthology.info/papers/C18-1229/c18-1229)|2018 coling|||
|[Learning Hierarchical Similarity Metrics](http://www.cs.toronto.edu/~vnair/cvpr12.pdf)|2012|||
|[Poincaré Embeddings for Learning Hierarchical Representations](http://papers.nips.cc/paper/7213-poincare-embeddings-for-learning-hierarchical-representations.pdf)|2017|||
|[PME: Projected Metric Embedding on Heterogeneous Networks for Link Prediction](http://shichuan.org/hin/time/2018.KDD%202018%20PME_Projected%20Metric%20Embedding%20on%20Heterogeneous%20Networks%20for%20Link%20Prediction.pdf)|2018, 异构网络结构 embedding||对于异构的关系，先将原始向量进行与relation相关的特定的映射；双向（一个edge的两个node）负采样|
|[Scalable Graph Embedding for Asymmetric Proximity](https://www.aaai.org/ocs/index.php/AAAI/AAAI17/paper/viewFile/14696/14500)|2017, 非对称结构的图embedding|||
|[Hierarchical Embeddings for Hypernymy Detection and Directionality](https://arxiv.org/pdf/1707.07273.pdf)|2017 acl|||
|[Imposing Hard Constraints on Deep Networks: Promises and Limitations](https://arxiv.org/pdf/1706.02025.pdf)|2017|||
|[Large-Scale Embedding Learning in Heterogeneous Event Data](http://hanj.cs.illinois.edu/pdf/icdm16_hgui.pdf)|2018 aaai|||
|[Relation Structure-Aware Heterogeneous Information Network Embedding](https://www.aaai.org/Papers/AAAI/2019/AAAI-LuY.5171.pdf)|2019 aaai||将所有异构关系简化从属关系和交互关系；从属关系的距离直接使用欧里几得距离（相当于在同一类别）；交互关系距离在原始L1距离中加入表征relation的向量Yr（|X2-X1-Yr|）|
|[Unseen Word Representation by Aligning Heterogeneous Lexical Semantic Spaces](https://arxiv.org/pdf/1811.04983.pdf)|aaai 2019||先使用外部辞典图进行random walk，生成人造句子，进行词向量训练得到v1；再学习v1到普通词向量v2的映射，目标函数是最大化CCA(Canonical Correlation Analysis)|

# 文本分类论文
|    论文题目    |   关键词＋概述   | 资源路径 | 说明（创新点） |
| ----------- | ------------------- | ----- | -------|
|||||

# 几种NLP任务state of the art水平
|    任务名称    |   数据集+描述   | 目前别人最优值 | 描述及链接 | 现状值|
| ----------- | ------------------- | -------- | -------|--------|
|Word Similarity|RG-65|spearman cor 0.920|Pilehvar and Navigli (2015) Knowledge-based (Wiktionary) https://github.com/vecto-ai/word-benchmarks|0.8177|
|Word Similarity|WordSimilarity-353|spearman cor 0.828|https://github.com/vecto-ai/word-benchmarks ConceptNet Numberbatch Hybrid	Speer et al. (2017)	|0.6278|
|Word Similarity|SimLex-999|spearman cor 0.642|https://github.com/vecto-ai/word-benchmarks SVR4 combine Banjade et al. (2015)[5]|0.4960|
|Syntactic Relations|Google Analogy中的morphological relations|69.3	|https://github.com/vecto-ai/word-benchmarks http://llcao.net/cu-deeplearning15/presentation/nn-pres.pdf|67.0|
|Synonym Selection|TOEFL Synonym Questions|100.00%|Bullinaria and Levy (2012)	|95%|
|Sentiment Analysis|IMDb|Accuracy 95.4|https://arxiv.org/abs/1801.06146 https://ai.stanford.edu/~ang/papers/acl11-WordVectorsSentimentAnalysis.pdf https://github.com/akzaidi/fine-lm||
|Named entity recognition|CoNLL 2003 (English)|f1值 93.09|https://drive.google.com/file/d/17yVpFA7MmXaQFTe-HDpZuqw9fJlmzg56/view https://github.com/zalandoresearch/flair|91.9|

## 两个可以看效果的链接地址
- https://aclweb.org/aclwiki/RG-65_Test_Collection_(State_of_the_art)
- https://github.com/sebastianruder/NLP-progress

## 论文工具链接地址
- [查询论文latex bib地址](https://www.bibsonomy.org/search/Specializing%20Word%20Embeddings%20for%20Similarity%20or%20Relatedness)

# 几个数据集源
|    数据集    |   关键词＋概述   | 
| ----------- | ------------------- | 
|https://github.com/airshipcloud/dictionary-seed/tree/master/wordnet/Thesaurus||

# 2018 NIPS Best Paper
|    论文题目    |   关键词＋概述   | 下载路径 | 说明（创新点） |
| ----------- | ------------------- | -------- | -------|
|Non-delusional Q-learning and Value-iteration||http://120.52.51.17/www.cs.toronto.edu/~cebly/Papers/nondelusionalQ_nips18.pdf||
|Optimal Algorithms for Non-Smooth Distributed Optimization in Networks||https://papers.nips.cc/paper/7539-optimal-algorithms-for-non-smooth-distributed-optimization-in-networks.pdf||
|Nearly Tight Sample Complexity Bounds for Learning Mixtures of Gaussians via Sample Compression Schemes||https://papers.nips.cc/paper/7601-nearly-tight-sample-complexity-bounds-for-learning-mixtures-of-gaussians-via-sample-compression-schemes.pdf||
|Neural Ordinary Differential Equations||https://arxiv.org/pdf/1806.07366||

# 其他资源
|    论文题目    |   关键词＋概述   | 资源路径 | 说明（创新点） |
| ----------- | ------------------- | ----- | -------|
|[Adversarial Learning for Neural Dialogue Generation](https://arxiv.org/pdf/1701.06547.pdf)|2017|||
|[Long Text Generation via Adversarial Training with Leaked Information](https://www.aaai.org/ocs/index.php/AAAI/AAAI18/paper/download/16360/16061)|2018|||
|[Adversarial Feature Matching for Text Generation](https://arxiv.org/pdf/1706.03850)|2017|||
|[Distance metric learning, with application to clustering with side-information](https://ai.stanford.edu/~ang/papers/nips02-metric.pdf)|2003 metric learning 聚类|||
|[A Survey on Metric Learning for Feature Vectors and Structured Data](https://arxiv.org/pdf/1306.6709.pdf)|2014 metric learning 调研|||
