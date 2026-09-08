---
layout: archive
permalink: /projects/
author_profile: true
---

{% include base_path %}

# Learning, representations, and scientific discovery

What we already know helps us learn, but it can also limit what we notice or consider. I study this relationship in human decision making and large language models, and I am extending it to scientific communities. I also ask how the models we use to study these learners shape our explanations of their behavior.

## How do people learn and change their decisions?

During my PhD, I used neural networks to study how people make decisions as they gain experience. Traditional models describe behavior through a few quantities, such as how strongly a new outcome changes someone's expectations. These frameworks are useful, but they can become conceptual bottlenecks: any behavior that does not fit is dismissed as noise. I used more flexible models to identify patterns these descriptions miss, then translated those patterns into interpretable models of decision making.

![Overview of my research on human decision making]({{ site.baseurl }}/images/work.png)

### Data-driven discovery of behavioral patterns

Neural networks fit to behavior revealed structure in human exploration that standard models overlook, characterized through [decision boundaries](https://www.2023.ccneuro.org/view_paper52a7.html?PaperNum=1437&talk), [behavioral dimensionality and symbolic formulas](https://openreview.net/forum?id=xW5JQo6TXO), and [attractor geometry](https://2024.ccneuro.org/pdf/615_Paper_authored_ccn2024_horizon_rnn_dynamics_authored.pdf). These include context-dependent value integration, context-dependent uncertainty modulation, and correlated value updates across options, and they generate hypotheses about the underlying neural implementations. On the method side, I showed that the usual way of fitting cognitive models can return [very different parameters with identical fit](https://www.biorxiv.org/content/10.1101/2025.03.21.644663), and that deep learning recovers these parameters more reliably.

I also use LLMs to interpret people's own descriptions of their decisions, extracting [decision traits](https://openreview.net/forum?id=fEoemPDicz) and [programs](https://openreview.net/forum?id=1Tny4KgGO2) from think-aloud text, and to generate and evaluate explanations of human [think-aloud](https://osf.io/preprints/psyarxiv/6ta3z_v2) and [behavior](https://www.nature.com/articles/s41586-025-09215-4) at scale.

### Cognition as online learning

![follow gradient]({{ site.baseurl }}/images/rl_params_score_landscape.png)

A central question is how people change their learning strategies over time. Previous models assume a fixed strategy. I developed [DynamicRL](https://osf.io/4xumc_v2) to estimate strategy parameters from one decision to the next, and found that [human strategy adaptation resembles policy gradient ascent](https://www.biorxiv.org/content/10.1101/2025.07.28.667308): people adjust their strategy in the direction that improves expected outcomes. Applied to ten datasets, the model approaches the predictive ceiling of recurrent neural networks while remaining interpretable. Related work extends model-agnostic meta-learning to infer human learning rules, giving [a normative account of why people weight evidence unevenly over time](https://osf.io/gf5cp_v2).

Together, these projects develop an online learning perspective on cognition. Many existing cognitive models can be rewritten as online learning processes operating under different objectives and representations. A Q-learning model, for instance, is an online prediction problem that minimizes the Bellman error under a one-hot representation of options. This view clarifies what objective each model assumes, and it suggests treating individual and task differences as consequences of the representation on which the learner performs gradient descent.

## What can language models learn from context?

![neurofeedback]({{ site.baseurl }}/images/llm_nf.png)

Large language models can learn from information in a prompt without changing their trained parameters. I study what makes this possible and what limits it. My work shows how [existing representations constrain learning and reorganize during it](https://arxiv.org/abs/2605.28854), and how [memories interfere when they share representations](https://arxiv.org/abs/2604.09670), producing capacity limits that resemble human working memory. I also investigate how models [generate and update hypotheses](https://arxiv.org/abs/2605.05851): they evaluate hypotheses better than they generate them, and the hypotheses they generate stay close to what they already know.

Other projects examine how models [use evidence and seek information under uncertainty](https://arxiv.org/abs/2607.26845), finding that "thinking" mostly sharpens the use of existing evidence rather than driving exploration, and why they [struggle to locate the last few items in a sequence](https://arxiv.org/abs/2605.07127), where fine-tuning on this single primitive transfers broadly to long-context tasks.

### Metacognition and superposition

To understand why LLMs sometimes fail to explain their own computations, I introduced [a neuroscience-inspired neurofeedback paradigm to quantify their metacognition](https://arxiv.org/abs/2505.13763), their ability to report and control internal activation patterns. This capacity is limited by the semantic meaningfulness and variance of the activations, and spans a metacognitive space much smaller than the model's neural space. The work also identified adversarial vectors that let models evade monitoring.

A key constraint behind these limits is superposition: models represent more features than they have dimensions, producing polysemantic neurons analogous to mixed selectivity in neuroscience. This compression enables generalization across related concepts at the cost of interference. I ask how the geometry of superposition, the representation learned in training, shapes in-context learning, the online optimization that runs on top of it, and whether it explains failures in tasks such as Bayesian evidence integration, where features cannot be factorized.

## How do scientific communities learn?

![science progress]({{ site.baseurl }}/images/science_progress.png)

With James Evans at the University of Chicago, I am extending these questions to science itself. A research paradigm is a shared vocabulary within a community, and it shapes which hypotheses a field considers and which it overlooks. This includes examining my own tools for studying humans and AI.

My current questions concern the inductive biases that humans and AI bring to generating hypotheses. Which possibilities do they overlook? Does AI extend the space of hypotheses or interpolate within it? How can we build systems that help scientists develop and test the alternatives? This work connects the study of learning with the design of AI tools for scientific discovery.
