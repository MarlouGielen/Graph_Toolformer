# Graph-Toolformer

### 🟢 May 4: Updates
- **Update 1**: All the datasets and model checkpoints have been publicized, some large-sized data are shared via google drive
    - Datasets and Model Checkpoints (about 5GB): [See this page](https://github.com/jwzhanggy/Graph_Toolformer/tree/main/data)
- **Update 2**: Source code of both Graph-toolformer LLM Tuning and Graph Reasoning Demo are released
    - LLMs Fine-Tuning code with Prompts: [See this page](https://github.com/jwzhanggy/Graph_Toolformer/tree/main/LLM_Tuning)
    - Graph-toolformer Demo code: [See this page](https://github.com/jwzhanggy/Graph_Toolformer/tree/main/Graph_Toolformer_Package)

### 🟢 May 10: Updates
- **Update 1**: The paper has been updated, and the new version of the paper can be found [via this link](http://www.ifmlab.org/files/paper/graph_toolformer.pdf).
- **Update 2**: The prompt dataset has been updated to correct some typos.
- **Update 3**: The LLM fine-tuned checkpoint has been updated to reflect the changes to the prompts.
- **Update 4**: The source code of the graph_toolformer_package has been updated for continuous reasoning with the demo.
************************************************************************************************

![framework](./figures/framework.png)

### Graph-ToolFormer: To Empower LLMs with Graph Reasoning Ability via Prompt Augmented by ChatGPT

Paper URL at IFMLab: http://www.ifmlab.org/files/paper/graph_toolformer.pdf

Paper URL at arxiv: https://arxiv.org/pdf/2304.11116.pdf

Paper description in Chinese: [文章中文介绍](./中文介绍)

### Project Conda Environment

See the shared [environment.yml](./environment.yml) file. Create a local environment at your computer with command 
```
conda env create -f environment.yml
```
For the packages cannot be installed with the above conda command, you may consider to install via pip instead.

### References 
(also add \usepackage{hyperref} into your paper for adding the url address in the reference)

```
@article{zhang2023graph,
    title={Graph-ToolFormer: To Empower LLMs with Graph Reasoning Ability via Prompt Augmented by ChatGPT},
    author={Zhang, Jiawei},
    year={2023},
    eprint={2304.11116},
    archivePrefix={arXiv},
    primaryClass={cs.AI},
}
```

************************************************************************************************
## Organization of the project source code, data and model checkpoints

### Source code

This project source code is divided into two directories:
- **LLM_Tuning [link](https://github.com/jwzhanggy/Graph_Toolformer/tree/main/LLM_Tuning)**: Language model fine-tuning code with graph reasoning prompt dataset
- **Graph_Toolformer_Package [link](https://github.com/jwzhanggy/Graph_Toolformer/tree/main/Graph_Toolformer_Package)**: The Graph-Toolformer reasoning demo code, which will load the fine-tuned LLMs (by the LLM_Tuning code) and the other pre-trained GNN models.

### Dataset

The datasets used in this paper inclode both the the generated graph reasoning prompt datasets, and the benchmark datasets of the graphs
- **Prompt Datasets [link](https://github.com/jwzhanggy/Graph_Toolformer/tree/main/LLM_Tuning/prompt)**: The graph reasoning prompts created in this paper for LLM fine-tuning.
- **Graph Raw Datasets [link](https://github.com/jwzhanggy/Graph_Toolformer/tree/main/Graph_Toolformer_Package/graph_datasets)**: The 15 graph benchmark datasets used in this paper

### Model checkpoints

The pre-trained/fine-tuned model checkpoints released by this project also have two parts
- **Fine-tuned LLM Checkpoint [link](https://github.com/jwzhanggy/Graph_Toolformer/tree/main/Graph_Toolformer_Package/koala/language_models)**: The checkpoint of fine-tuned language model by the above LLM_Tuning code, readers can either tune the LLMs by yourselves or use the provided checkpoint by us.
- **Pre-trained GNN Checkpoints [link](https://github.com/jwzhanggy/Graph_Toolformer/tree/main/Graph_Toolformer_Package/koala/graph_models)**: We use 5 different graph models in this project, the checkpoints of the pre-trained GNNs are also provided

************************************************************************************************

🔴
🟠
⚫
⚪
🟣
🟢
🟡
🔵


## Tasks to be done

- [x] 🟢 Polish the framework: 7/7 done
  - [x] 🟢 add working memory module
  - [x] 🟢 add query parser module
  - [x] 🟢 add query excutor module
  - [x] 🟢 add graph dataset hub
  - [x] 🟢 add graph model hub
  - [x] 🟢 add graph reasoning task hub
  - [x] 🟢 add llm model hub
- [x] 🟢 Expand the framework: 3/3 done
  - [x] 🟢 Include graph datasets: done
    - [x] 🟢 graph property dataset
    - [x] 🟢 bibliographic networks: cora, pubmed, citeseer
    - [x] 🟢 molecular graphs: proteins, nci1, mutag, ptc
    - [x] 🟢 social networks: twitter, foursquare
    - [x] 🟢 recommender system: amazon, last.fm, movielens  
    - [x] 🟢 knowledge graphs: wordnet, freebase 
  - [x] 🟢 Add pre-trained graph models: done
    - [x] 🟢 Toolx
    - [x] 🟢 Graph-Bert
    - [x] 🟢 SEG-Bert
    - [x] 🟢 KMeans Clustering
    - [x] 🟢 BPR
    - [x] 🟢 TransE
  - [x] 🟢 Include graph reasoning tasks: done
    - [x] 🟢 graph property reasoning
    - [x] 🟢 bibliographic paper topic reasoning
    - [x] 🟢 molecular graph function reasoning
    - [x] 🟢 social network community reasoning
    - [x] 🟢 recommender system reasoning
    - [x] 🟢 knowledge graph reasoning
- [x] 🟢 Polish and release the datasets: 4/4 released
  - [x] 🟢 graph raw data: 
  - [x] 🟢 graph reasoning prompt data
  - [x] 🟢 pre-trained graph model checkpoints
  - [x] 🟢 fine-tuned llm model checkpoints
    
- [ ] 🟠 Add and test more LLMs: 1/5 done
  - [x] 🟢 GPT-J
  - [ ] LLaMA
  - [ ] GPT-2
  - [ ] OPT
  - [ ] Bloom
 
- [ ] 🟠 Release the framework and service: 0/5 done
  - [ ] 🟠 Implement the CLI for framework usage
  - [ ] 🟠 Provide the demo for graph reasoning
  - [ ] 🟠 Add API for customerized graph reasoning
  - [ ] 🟠 Release GUI and web access/service


