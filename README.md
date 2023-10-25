# Fine Tuning Dolly model through PEFT/LoRA

The demand for using Large Language Models (LLMs) with billions of parameters has increased significantly. This poses a challenge due to the computational resources required for efficient model training and deployment. Here we present a practical approach to leverage the Low-Rank Adaptation (LoRA) based Parameter-Efficient Fine-Tuning (PEFT) to enable training and deploying LLMs on lower GPU resources. 

### Dolly Model 

<p align="center"><img src="https://github.com/yfgit2012/PEFT-Fine-Tuning-LLM/blob/main/assets/dolly.jpeg" width=300/></p>

We present case studies using the open source, instruction-following LLM [Dolly](https://github.com/databrickslabs/dolly) - a set of instruction-following large language models trained by [Databricks](https://databricks.com/). Dolly-v2-12b is a 12 billion parameter causal language model created by Databricks that is derived from [EleutherAI’s](https://www.eleuther.ai/) [Pythia-12b](https://huggingface.co/EleutherAI/pythia-12b) and fine-tuned on a [~15K record instruction corpus](https://github.com/databrickslabs/dolly/tree/master/data) generated by Databricks employees and released under a permissive license (CC-BY-SA). We evaluation results to illustrate the quantitative comparisons between LLMs of varying sizes, ranging from 3 billion to 12 billion parameters. By systematically evaluating the tradeoff between model performance and the compute resources required for fine-tuning, we provide insights into the scalability, efficiency and cost effectiveness of fine-tuning LLMs.    

We present case studies of fine tuning dolly-v2 models with PEFT/LoRA in Hugging Face, and quantitative comparison between the models of varying sizes ranging from 3 billion to 12 billion parameters. The systematic evaluation illustrates the tradeoff between model performance and the compute resources required for fine-tuning.

### What is LoRA  

LoRA - Low Rank Adaption - is to fine tune a foundation model that does not require updating all the parameters of the LLM. The training is conducted ona  low dimension matrix that represents the space of the training task with very high accuracy, instead of the full weights. During the inference, the weights of the LoRA model are added or integrated into the main LLM.

<img src="https://github.com/yfgit2012/PEFT-Fine-Tuning-LLM/blob/main/assets/lora.png" width=500>

### Dolly 3B 

Fine tuning (Full weights vs LoRA) 

![image](https://github.com/yfgit2012/PEFT-Fine-Tuning-LLM/blob/main/assets/dolly_3bloraft_1.png)

![image](https://github.com/yfgit2012/PEFT-Fine-Tuning-LLM/blob/main/assets/dolly_3bloraft_2.png)

![image](https://github.com/yfgit2012/PEFT-Fine-Tuning-LLM/blob/main/assets/dolly_3bloraft_3.png)

![image](https://github.com/yfgit2012/PEFT-Fine-Tuning-LLM/blob/main/assets/dolly_3bloraft_4.png)

Inference (Full weights vs LoRA) 

![image](https://github.com/yfgit2012/PEFT-Fine-Tuning-LLM/blob/main/assets/dolly_3blorainf_1.png)

![image](https://github.com/yfgit2012/PEFT-Fine-Tuning-LLM/blob/main/assets/dolly_3blorainf_2.png)

![image](https://github.com/yfgit2012/PEFT-Fine-Tuning-LLM/blob/main/assets/dolly_3blorainf_3.png)

### Dolly 3B vs 7B vs 12B LoRA tuning

![image](https://github.com/yfgit2012/PEFT-Fine-Tuning-LLM/blob/main/assets/dolly_3b7b12b_1.png)

![image](https://github.com/yfgit2012/PEFT-Fine-Tuning-LLM/blob/main/assets/dolly_3b7b12b_2.png)





