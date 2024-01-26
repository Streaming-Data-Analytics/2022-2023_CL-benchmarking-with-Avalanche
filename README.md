# CL benchmarking with Avalanche

Optional project of the [Streaming Data Analytics](http://emanueledellavalle.org/teaching/streaming-data-analytics-2022-23/) course provided by [Politecnico di Milano](https://www11.ceda.polimi.it/schedaincarico/schedaincarico/controller/scheda_pubblica/SchedaPublic.do?&evn_default=evento&c_classe=811164&polij_device_category=DESKTOP&__pj0=0&__pj1=1b82965d3c68857e2087d3f3b98a9e40).

Student: **Reza Paki**

The project will use the Python library Avalanche ([Home page](https://avalanche.continualai.org/), [API](https://avalanche-api.continualai.org/en/v0.3.1/)), presented in the [Continual Learning course](https://course.continualai.org/). The aim is to compare different Continual Learning strategies on two standard benchmarks in an Incremental Task Learning scenario.

The following strategies will be of interest:
- Baseline strategies: [Naive Strategy](https://avalanche-api.continualai.org/en/v0.3.1/generated/avalanche.training.Naive.html#avalanche.training.Naive) and [Joint Training](https://avalanche-api.continualai.org/en/v0.3.1/generated/avalanche.training.JointTraining.html#avalanche.training.JointTraining). 
- Replay strategies: Random Replay, [GDUMB](https://arxiv.org/abs/1809.05922). 
- Regularization strategies: [Learning Without Forgetting (LWF)](https://arxiv.org/pdf/1606.09282.pdf), [Elastic Weight Consolidation (EWC)](https://arxiv.org/pdf/1612.00796.pdf
  ). 
- Architectural Strategies: [Copy Weights with Re-Init (CWR)](https://arxiv.org/pdf/1907.03799.pdf), [Progressive Neural Networks (PNNs)](https://arxiv.org/abs/1606.04671
). 
- One hybrid strategy you choose (see module 7 of the CL course).

While it is not necessary to delve deeply into these strategies, it is important to have an intuition of how they work. Please note that Avalanche implements all of them, so you do not need to implement them yourself. Since we are not interested in the best model configuration, you can use [SimpleMLP](https://avalanche-api.continualai.org/en/v0.3.1/generated/avalanche.models.SimpleMLP.html) as the base model for all the strategies.

Strategies comparison must be made based on the following metrics (computed on each experience):
- Accuracy. 
- Forward Transfer, Backward Transfer. 
- Time. 
- CPU and RAM usage.
The project must also include plots and reasoning on Forward and Backward Transfer, as seen during the SDA course.

Experiments must be run separately in an Incremental Task Learning scenario on two different benchmarks, each containing 5 experiences:
- [SplitCIFAR10](https://avalanche-api.continualai.org/en/v0.3.1/generated/avalanche.benchmarks.classic.SplitCIFAR10.html
). 
- [SplitMNIST](https://avalanche-api.continualai.org/en/v0.3.1/generated/avalanche.benchmarks.classic.SplitMNIST.html).

For each benchmark, you are required to create a single ipynb file. You must include comments for the principal instructions, and you are allowed to import external py modules. Additionally, ensure you thoroughly comment on the comparison results using various plots associated with the different metrics. Finally, again, within each ipynb file, briefly discuss the conclusions that can be drawn from the experiment.
