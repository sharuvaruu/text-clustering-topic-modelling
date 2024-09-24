# **Text Clustering and Topic Modeling** 🗂️

## **Project Overview**  
This repository contains an in-depth notebook focused on text clustering and topic modeling, utilizing a dataset of ideas provided in an Excel sheet. The project explores data preprocessing, dimensionality reduction, and multiple clustering algorithms to extract meaningful insights from textual data. 🌟

## **Achievements** ✅  
- Successfully preprocessed and cleaned a dataset of textual ideas.
- Implemented various clustering algorithms to group similar ideas.
- Conducted exploratory data analysis (EDA) to understand the characteristics of the dataset.
- Generated visualizations to represent text length and sentence length distributions.
- Achieved a clear understanding of data preprocessing techniques essential for text analysis.

## **Dataset** 📊  
The dataset used in this project is a collection of textual "ideas" stored in an Excel file. Each idea is a short text input, which is preprocessed, analyzed, and clustered. The primary focus is on the 'Idea' column for text analysis.

### **Key Columns**  
- `Idea`: Contains the main text data for clustering and topic modeling.

## **Steps Involved** 🔍  

### **1. Exploratory Data Analysis (EDA)**  
We begin with an exploration of the textual data, analyzing:
- **Text Length Distribution:** Understanding the length of each idea.
- **Sentence Length Distribution:** Analyzing the distribution of sentence lengths by splitting ideas into sentences.
- **Text Length Distribution:** ![image](https://github.com/user-attachments/assets/a4403af0-d2fd-472f-bab5-a738f1bf7659)
- **Sentence Length Distribution:** ![image](https://github.com/user-attachments/assets/c33b0f80-a934-4c15-bec5-f38c232fe6a3)

---

### **2. Text Preprocessing**  
Text preprocessing is crucial for effective clustering. It involves the following steps:
- **Tokenization:** Splitting text into individual tokens (words).
- **Stopword Removal:** Removing common stopwords, with specific customizations for this dataset.
- **Lemmatization:** Reducing words to their base form.
- **Part-of-Speech Tagging (POS):** Filtering words based on their grammatical role (nouns, verbs, adjectives, etc.).
- **Distribution of Word Length:** ![image](https://github.com/user-attachments/assets/92900c31-78af-4170-a0fc-06208d71050d)
- **Word Cloud of Most Frequent Words:** ![image](https://github.com/user-attachments/assets/11637f80-956a-4909-b639-39debfa5f40b)

#### **Hierarchical Clustering using Agglomerative Clustering**  
This section outlines the implementation of hierarchical clustering using the Agglomerative Clustering algorithm. The primary goal is to cluster the data based on the features extracted from the TF-IDF matrix.

#### **Overview**  
Hierarchical clustering is a method of cluster analysis that seeks to build a hierarchy of clusters. In this implementation, we use the **Ward's method**, which minimizes the variance within clusters. The dendrogram function visualizes the hierarchical clustering as a tree structure. This visual representation helps in understanding how clusters are formed.
- **Dendrogram:** ![image](https://github.com/user-attachments/assets/d03b0baa-b5f6-4687-8a13-c29f2b2776d5)

#### **Plotting Word Clouds for Top Words per Cluster** 🌈  
This section describes how to visualize the top words from each cluster using word clouds. Word clouds provide a visual representation of word frequency, where larger words indicate higher importance.

#### **Code Overview** 📝  
The function `plot_word_clouds` takes a dictionary of top words for each cluster and generates word clouds for visual analysis. Each cluster's prominent words are displayed in separate subplots.

#### **Key Components** 🔑  
- **WordCloud**: This library generates word cloud images based on word frequencies, making it easy to see which words are most significant in each cluster. 🌟
- **Matplotlib Subplots**: The function uses subplots to arrange multiple word clouds side by side, allowing for easy comparison between clusters. 📊
- **Frequency Dictionary**: The top words and their scores are converted into a dictionary format, which is essential for creating the word clouds. 📚

#### **Example Output** 🎉  
The resulting visualization displays word clouds for each cluster, with the size of each word representing its frequency. This helps in quickly assessing the main themes within each cluster.
**Top words of cluster:** ![image](https://github.com/user-attachments/assets/f2d375aa-69fd-4ba1-8963-547900ab5b20)

### **3. Dimensionality Reduction** 📉  
To improve clustering performance, we apply techniques such as:
- **TF-IDF Vectorization**: Converting text into numerical format. 📊
- **PCA (Principal Component Analysis)**: Reducing dimensionality while preserving variance. 🔍

### **4. Clustering Algorithms** 🤖  
We implemented multiple clustering algorithms, including:
- **K-Means Clustering** ⚙️
- **Hierarchical Clustering** 📚
- **DBSCAN (Density-Based Spatial Clustering of Applications with Noise)** 🌌

### **5. Model Evaluation** 📈  
We evaluated the performance of our clustering models using two key metrics: **Silhouette Score** and **Davies-Bouldin Index**. These metrics help in understanding the quality of clusters formed by the algorithm. 🔍

#### **Evaluation Metrics:**  
- **Silhouette Score**: Measures how similar an object is to its own cluster compared to other clusters. A higher Silhouette score indicates better-defined clusters (range: -1 to +1). 🌟
- **Davies-Bouldin Index**: Measures the average similarity ratio of each cluster with the cluster that is most similar to it. A lower value indicates better clustering quality. 📏

#### **Results:**
##### **K-Means Clustering:**
- **Silhouette Score**: 0.9144  
  - A high Silhouette score, indicating that clusters are well-separated. 👍
  
- **Davies-Bouldin Index**: 0.2947  
  - A very low Davies-Bouldin index, suggesting that clusters are compact and well-separated. 🔒

![image](https://github.com/user-attachments/assets/b179975d-9f78-4aee-84c4-299b40bac0ac)

- **Number of Clusters**: 2 🔢

##### **Top Words per Cluster:**
- **Cluster 1**:
  - applicant eg decent (0.0426) 📝
  - action system (0.0407) ⚙️
  - based alerting active (0.0377) 🚨
  - aiding change (0.0355) 🔄
  - application also highlight (0.0327) ✨
  - bank (0.0326) 🏦
  - ai suggestion (0.0321) 🤖
  - based personal (0.0252) 👤
  - available web (0.0236) 🌐
  - based pet (0.0229) 🐾

- **Cluster 2**:
  - appropriate position effectively (0.1254) 🎯
  - assigned (0.1226) 📌
  - analysis comparison (0.1138) 📊
  - action system (0.0788) ⚙️
  - based personal (0.0616) 👤
  - attack technique (0.0530) ⚔️
  - accident rescue (0.0490) 🚑
  - ai suggestion (0.0488) 🤖
  - analyzes machine (0.0414) 🖥️
  - application analytics (0.0410) 📈

##### **Hierarchical Clustering:**
- **Silhouette Score**: 0.5943  
  - This score suggests moderate cluster separation. ⚖️
  
- **Davies-Bouldin Index**: 0.5588  
  - A relatively low index, indicating reasonable cluster separation, though not as compact as K-Means. 📏

![image](https://github.com/user-attachments/assets/effb5e23-540c-47e1-ab75-5018aed432eb)  
![image](https://github.com/user-attachments/assets/2bbbe063-456b-4363-bf61-dd426934a5e2)  

---

### **Summary:**  
- **K-Means** performed better with a high Silhouette score of 0.91 and a very low Davies-Bouldin index of 0.29, indicating tight and well-separated clusters. 🏆
- **Hierarchical Clustering** showed moderate results with a Silhouette score of 0.59 and a Davies-Bouldin index of 0.56, indicating less compact clusters compared to K-Means. 📉

### **Tech Stack** 🛠️  
- **Programming Language**: Python 🐍
- **Libraries Used**:
  - Pandas for data manipulation 📅
  - Numpy for numerical operations ➗
  - Scikit-learn for machine learning and clustering 📚
  - Matplotlib and Seaborn for data visualization 🎨
  - NLTK or SpaCy for text processing ✍️
  - Jupyter Notebook Environment 🌐

---

### **Future Work** 🚀  
- **Enhanced Preprocessing**: Further fine-tuning of text preprocessing techniques and experimenting with different vectorization methods (e.g., Word2Vec, FastText).
- **More Clustering Techniques**: Exploring additional clustering algorithms and ensemble methods to improve results.
- **Deeper Insights**: Implementing methods for interpreting clusters and gaining deeper insights from the data.

## **License** 📝  
This project is licensed under the MIT License. See the [LICENSE](./LICENSE) file for more details.

## **Contact** 📧  
For any questions or collaborations, feel free to reach out via [GitHub](https://github.com/sharuvaruu) or connect with me on [LinkedIn](https://www.linkedin.com/in/sharvari-salodkar-587b611a5/).

---

*Thank you for visiting this repository! 😊*
