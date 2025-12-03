---
layout: archive
permalink: /projects/
author_profile: true
---

{% include base_path %}

# How to understand complex behaviors?

My work focuses on uncovering the mechanisms underlying human decision-making. Understanding this inherently complex process often relies on explanatory frameworks such as reinforcement learning (RL) models or decision-making traits. However, these frameworks can also become conceptual bottlenecks that limit our ability to capture the full richness of biological behavior.

In my PhD research, I use neural networks to model biological behavioral data and identify novel patterns that traditional frameworks may overlook. These insights, in turn, help us design improved explanatory models that better represent the underlying decision processes.

![research interest]({{ site.baseurl }}/images/work.png)

## Data-driven discovery of novel behavioral patterns

Normative conceptual frameworks such as RL have long provided valuable insights into the principles of decision-making. However, these frameworks often produce incomplete characterizations due to modeling biases, subjective parameter tuning, or reliance on idealized assumptions. I addresses this challenge by leveraging the flexibility of neural networks to discover novel behavioral patterns and construct interpretable explanatory frameworks. I characterize individual differences in human exploration through [decision boundaries](https://www.2023.ccneuro.org/view_paper52a7.html?PaperNum=1437&talk), [behavioral dimensionality and symbolic formula](https://openreview.net/forum?id=xW5JQo6TXO), and [attractor geometry](https://2024.ccneuro.org/pdf/615_Paper_authored_ccn2024_horizon_rnn_dynamics_authored.pdf). These explanatory interfaces uncover behavioral patterns that previous models fail to capture, including context-dependent value integration, context-dependent uncertainty modulation, and correlated value update across options. They also generate hypotheses about the underlying neural implementations of these patterns. I also use LLMs to interpret human descriptions of their decision processes through [decision traits](https://openreview.net/forum?id=fEoemPDicz) and [programs](https://openreview.net/forum?id=1Tny4KgGO2). I further leverage LLMs to generate and evaluate explanations of human [think-aloud](https://osf.io/preprints/psyarxiv/6ta3z_v2) and [behaviors](https://www.nature.com/articles/s41586-025-09215-4) at scale. These findings enhance behavioral prediction and interpretation while generating testable hypotheses for future experiments.

## Meta-learning as a unified framework for understanding behavior. 

![follow gradient]({{ site.baseurl }}/images/rl_params_score_landscape.png)

Although previous explanations for decision-making provide useful insights, they remain fragmented, raising a key question: can we unify them under a normative framework that generalizes across different contexts? Meta-learning offers a promising unifying framework, wherein agents optimize their ongoing learning strategies to adapt to dynamic environments. However, because its normative formulation is inherently goal-optimal, meta-learning cannot directly account for biological behavior, which is often suboptimal. I use neural networks to address this issue in two complementary directions. First, I model how humans adapt RL strategies through experience by estimating RL parameters over time, overcoming limitations of previous models that assume static strategies. Analysis of parameter dynamics reveals a meta-learning process in human decision-making --- specifically, [a real-time refinement of learning strategies that resembles policy gradient ascent](https://www.biorxiv.org/content/10.1101/2025.07.28.667308) used in AI. I then apply this method to ten datasets, where it approaches ceiling performance that recurrent neural network achieves while [maintaining interpretability. In the second direction, I model human strategy adaptation in experiments as a meta-learning process, specifically formulating perceptual integration as a dynamic strategy shaped by ongoing error-driven learning. I extend model-agnostic meta-learning to infer human learning rules, providing [a normative account of uneven evidence-integration kernels](https://osf.io/gf5cp_v2) observed in behavior. Together, this work positions meta-learning as a model of human behavior, captures dynamic strategy adaptation --- an underexplored dimension in prior work --- and bridges learning-to-learn in psychology with meta-learning in AI.

I also demonstrate that many existing cognitive models and their variants can be reformulated as MAML processes (online learning) operating under different objective functions and representations. For instance, a Q-learning model, which integrates the values of different options in multi-armed bandit tasks, can be equivalently viewed as an online prediction problem that minimizes the Bellman error (predicting the next reward) under a one-hot representation of options. This approach will offer novel insights into cognitive models and provide a normative understanding of these tasks by clarifying what objectives should be optimized. Second, building on my prior work, I will demonstrate these strategies can be interpreted as online gradient descent processes induced by different representation spaces, which can be estimated by ANNs. This model can jointly predict behavior and neural activity, providing causal links to behavior. The model estimates a unique representation for each subject, upon which it performs a linear gradient descent, allowing us to analyze individual and task differences as consequences of their underlying representations. 

## Neuroscience-inspired frameworks to understand LLM metacognition.

![follow gradient]({{ site.baseurl }}/images/llm_nf.png)

To understand why LLMs sometimes fail to explain their own computational processes, I introduced [a neuroscience-inspired neurofeedback paradigm to quantify their metacognition](https://arxiv.org/abs/2505.13763)—specifically, their ability to explicitly report and control internal activation patterns. I demonstrated that an LLM's metacognitive capacity is limited by the semantic meaningfulness and variance of its neural activations \citep{ji-an_language_2025}. This work not only identified potential adversarial vectors that allow models to evade monitoring but also established a hypothesis regarding the fundamental factors required for robust AI metacognition.

A key neural constraint in LLMs is superposition, where models represent more features than their dimensions. This results in 'polysemantic' neurons analogous to 'mixed selectivity' in neuroscience. This compression affects representational geometry, enabling generalization across related concepts at the cost of interference. This aim investigates how neural constraints in LLMs shape learning and asks how the geometry of superposition (the outer loop's representations) influences ICL (the inner online optimization). I will also examine whether neural geometry constraints on learning cause failures in tasks such as Bayesian evidence integration , as such failures could arise because features cannot be factorized. I extend our Neurofeedback ICL paradigm, which defines features as arbitrary directions in neural activation. This allows me to observe how online learning on selected features interferes with learning on others. I will design experiments using combined features (e.g., 'smart and hardworking' or 'optimistic and depressed') to investigate how ICL is performed when features are correlated and if this correlation is factored out. 

## What is an explanation and how to optimize better explanation?

![follow gradient]({{ site.baseurl }}/images/science_progress.png)

Understanding is an evolving process that involves developing increasingly refined explanatory concepts. Just as scientific progress depends on improving abstractions, understanding AI requires new conceptual tools.
