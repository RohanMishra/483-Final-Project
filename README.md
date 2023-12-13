# 483-Final-Project

## How to Use

In this repository, there are two main Jupyter Notebooks that were created. One performs the link prediction task (transe_link_pred.ipynb) and the other does the knowledge graph merging (knowledge_graph_merge.ipynb). These notebooks were written almost entirely from scratch, so they were significantly cleaned up before being deposited here for ease of running and reprodibility.

1. TransE Link Prediction:
   Simply stepping through the notebook cell by cell should generate most of the main results of the paper. The only change required is to change the directory for saving the dataset. I.e. changing wiki5m_dataset = Wikidata5M("/Users/rohan/Documents/483FinalProject/tmp/wiki5m", transform=transform) so that the directory path is appropriate.

   Note, however, that the training for this model will take a very long time. As a result, the outputs of a previous run are left to see. The final few cells simply plot the relevant curves present in the paper - the training loss and MRR curves.

3. Knowledge Graph Merge:
  Similar to before, simply stepping through this notebook cell by cell should generate most of the main results of the paper. The only change required is to change the directory for saving the dataset. I.e. changing wikics_dataset = WikiCS("/Users/rohan/Documents/483FinalProject/tmp/wikics", transform=transform) so that the directory path is appropriate.

  As you step through the notebook, the main results of the paper will be apparent, such as the performance of the embedding model with GraphSAGE Conv layers first (with the loss and AUC curves) and next the performance of the feedforward neural network portion. At the very end, the combining function prints two values - one being the accuracy, the other being the F1 score.
