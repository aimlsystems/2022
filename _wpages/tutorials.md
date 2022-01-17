---
layout: other
title: Tutorials
---

{:.text-center}
## 24th of October, 2021

<br><br>

<a id="t-1"></a>

# Tutorial 1

### Machine Learning for Databases

#### Speakers
* Guoliang Li, Tsinghua University
* Xuanhe Zhou, Tsinghua University
* Lei Cao, CSAIL, MIT

#### Description

{:.text-justify}
Machine learning techniques have been proposed to optimize the databases. For example, traditional empirical database optimization techniques (e.g., cost estimation, join order selection, knob tuning, index and view advisor) cannot meet the high-performance requirement for large-scale database instances, various applications and diversified users, especially on the cloud.  Fortunately, machine learning based techniques can alleviate this problem by judiciously selecting optimization strategy. In this tutorial, we categorize database tasks into three typical problems that can be optimized by different machine learning models, including NP-hard problems (e.g., knob space exploration, index/view selection, partition-key recommendation for offline optimization; query rewrite, join order selection for online optimization), regression problems (e.g., cost/cardinality estimation, index/view benefit estimation, query latency prediction), and prediction  problems (e.g., query workload prediction). We review existing machine learning based techniques to address these problems and provide research challenges.

<a id="t-2"></a>

# Tutorial 2

### Tutorial on Human Assisted ML

#### Speaker
* Abir De, Assistant Professor, Dept. of CSE, IIT Bombay.

#### Description

{:.text-justify}
In a wide range of high stake and critical applications, societies often rely on the judgement of human experts to make consequential decisions, which have significant impacts. However, the timeliness and the quality of these decisions are often compromised by shortage of experts. For example, in any hospital with limited resources, patients may have to wait for a long time. On the other hand, simple mistakes made by common works in a factory can lead to a heavy loss. To overcome this challenge, there is a recent line of works which describe how machine and humans can work together to achieve superior performance to what they individually could have achieved.

{:.text-justify}
The goal of this tutorial is introduce these techniques as well as describing the consequence of the outcome of machine learning on society at large— the pitfalls and the possibly remedy to overcome them. More specifically, we aim to teach the possibility of designing human assisted machine learning models in two classical machine learning setups— supervised learning and sequential decision making, where the machine learning task is distributed between humans and machines in such a way, so that, together human and machine perform better than than what they would achieve on their own.

Summarizing the goals of the tutorial evolve about the following problem:

{:.text-justify}
1. Human assisted supervised learning, where given both human annotations and ground truth labels, we learn how to outsource samples to humans to achieve better performance.
1. Human assisted reinforcement learning, where, for example in autonomous driving, a machine wants to take quick control in an emergency situation, or vice-versa. For example, in collision avoidance systems in cars, the machine takes control during a potential threat, whether in other aeroplanes, humans takes control if there is a possibility of mid-air collisions.

<a id="t-3"></a>

# Tutorial 3

### Compression of Deep Learning Models for NLP

#### Speaker
* Manish Gupta, Principal Applied Scientist, Microsoft

#### Description

{:.text-justify}
In recent years, the fields of NLP and information retrieval have made tremendous progress thanks to deep learning models like RNNs and LSTMs, and Transformer based models like BERT. But these models are humongous in size: BERT (340M parameters), GPT-2 (1.5B parameters), T5 (11B parameters, 21.7GB) and so on. Real world applications however demand small model size, low response times and low computational power wattage. We will discuss six different types of methods (pruning, quantization, knowledge distillation, parameter sharing, matrix decomposition, and other Transformer based methods) for compression of such models to enable their deployment in real industry NLP  projects.  Given the critical need of building applications with efficient and small models, and the large amount of recently published work in this area, we believe that this tutorial is very timely. We will organize related work done by the 'deep learning for NLP' community in the past few years and present it as a coherent story.

