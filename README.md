English description below

Olivetti Faces e Modelo de Mistura Gaussiana

Descrição do Projeto

Este repositório contém dois arquivos principais que exploram técnicas de detecção de anomalias e agrupamento no conjunto de dados Olivetti faces, 
utilizando métodos como KMeans clustering e Modelos de Mistura Gaussiana (GMM).

Olivetti Faces

O arquivo Olivetti Faces foca na aplicação de várias técnicas de aprendizado de máquina no conjunto de dados Olivetti faces. 
O conjunto de dados consiste em imagens em escala de cinza de rostos humanos, e o projeto inclui os seguintes passos:

Preparação dos Dados

O conjunto de dados foi dividido em conjuntos de treinamento, validação e teste, com a aplicação de escalonamento para normalizar as características.

KMeans Clustering

O KMeans clustering foi utilizado para identificar padrões e agrupar os rostos em clusters. Uma análise do índice de silhueta ajudou a determinar o número ideal de clusters.

Visualização dos Clusters

Os rostos dentro de cada cluster foram visualizados para inspecionar a qualidade do agrupamento e identificar quais rostos foram considerados semelhantes pelo algoritmo KMeans.

Classificador Random Forest

Um classificador Random Forest foi treinado usando as características originais para classificar os rostos e avaliado com base na precisão no conjunto de validação.

Redução de Dimensionalidade com KMeans

O KMeans foi utilizado para reduzir a dimensionalidade dos dados, e o desempenho do modelo foi avaliado com base na precisão da validação. 

A melhor estratégia de redução de dimensionalidade foi determinada comparando diferentes valores de K (número de clusters).

Combinação de Características do KMeans com Características Originais

Explorei a combinação das características geradas pelo KMeans com os dados originais para melhorar a precisão da classificação. 
A combinação das características resultou em uma melhoria no desempenho do modelo.

Avaliação Final do Modelo

O modelo final, combinando as características originais com as características do KMeans, foi testado no conjunto de teste, e o desempenho foi avaliado. 

A melhor combinação de características resultou na maior precisão no teste.






Modelo de Mistura Gaussiana nas Olivetti Faces

O arquivo Modelo de Mistura Gaussiana nas Olivetti Faces aplica um Modelo de Mistura Gaussiana (GMM) para análise e detecção de anomalias no conjunto de dados Olivetti Faces. 

O objetivo principal é agrupar as imagens de rostos e identificar imagens que se desviam significativamente dos padrões (anomalias), além de gerar faces sintéticas. 

Os seguintes passos foram realizados:

Preparação dos Dados e Escalonamento

O conjunto de dados Olivetti Faces foi carregado e pré-processado, com escalonamento das imagens usando PCA (Análise de Componentes Principais) para reduzir a dimensionalidade, preservando a maior parte da variação dos dados.

Treinamento do GMM

O Modelo de Mistura Gaussiana (GMM) foi treinado com 40 componentes para modelar a distribuição dos dados. 

O GMM foi ajustado aos dados transformados por PCA, permitindo uma representação mais eficiente das imagens.

Detecção de Anomalias

O modelo GMM foi utilizado para detectar anomalias comparando a verossimilhança dos dados originais com as imagens modificadas, como imagens invertidas ou escurecidas. 

Para isso, foram calculadas as log-verossimilhanças das imagens normais e das modificadas, como imagens viradas horizontalmente ou escurecidas.

Visualização das Imagens Geradas pelo GMM

O GMM gerou faces sintéticas, que foram reconstruídas a partir da transformação PCA. 

Essas faces geradas foram visualizadas em uma grade de imagens para inspecionar os resultados do agrupamento e gerar faces baseadas nos padrões encontrados.

Análise de Erro de Reconstrução

O erro de reconstrução foi calculado comparando as imagens originais com as reconstruídas a partir de PCA. 

Este erro foi visualizado para diferentes tipos de imagens (normais, invertidas, e escurecidas) para avaliar a qualidade da reconstrução.

Avaliação do Modelo e Resultados

As imagens modificadas (invertidas e escurecidas) apresentaram maior erro de reconstrução, 
o que indica que o GMM conseguiu identificar essas anomalias com base na discrepância entre as log-verossimilhanças e os erros de reconstrução.

Principais Resultados

O Modelo de Mistura Gaussiana foi eficaz para detectar anomalias, identificando imagens modificadas (invertidas e escurecidas) com base na probabilidade de suas distribuições.

As faces geradas pelo GMM mostraram boa qualidade, sendo capazes de recriar rostos a partir dos padrões aprendidos.

O uso do PCA ajudou a reduzir a dimensionalidade e facilitou o treinamento do GMM, além de fornecer uma forma eficiente de visualizar e reconstruir as imagens.

A análise do erro de reconstrução indicou que o modelo é sensível a modificações nas imagens, como inversões e escurecimento, permitindo identificar essas mudanças como anomalias.




Olivetti Faces and Gaussian Mixture Model

Project Description

This repository contains two main files that explore anomaly detection and clustering techniques on the Olivetti Faces dataset, using methods like KMeans clustering and Gaussian Mixture Models (GMM).

Olivetti Faces

The Olivetti Faces file focuses on applying several machine learning techniques to the Olivetti Faces dataset. The dataset consists of grayscale images of human faces, and the project includes the following steps:

Data Preparation

The dataset was split into training, validation, and test sets, with scaling applied to normalize the features.

KMeans Clustering

KMeans clustering was used to identify patterns and group the faces into clusters. A silhouette score analysis helped determine the ideal number of clusters.

Cluster Visualization

The faces within each cluster were visualized to inspect the clustering quality and identify which faces were considered similar by the KMeans algorithm.

Random Forest Classifier

A Random Forest classifier was trained using the original features to classify the faces and was evaluated based on accuracy on the validation set.

Dimensionality Reduction with KMeans

KMeans was used for dimensionality reduction, and the model's performance was evaluated based on validation accuracy. The best dimensionality reduction strategy was determined by comparing different values of K (number of clusters).

Combining KMeans Features with Original Features

I explored combining the features generated by KMeans with the original data to improve classification accuracy. Combining features resulted in an improvement in model performance.

Final Model Evaluation

The final model, combining original features with KMeans features, was tested on the test set, and performance was evaluated. The best feature combination resulted in the highest accuracy on the test set.

Gaussian Mixture Model on Olivetti Faces

The Gaussian Mixture Model on Olivetti Faces file applies a Gaussian Mixture Model (GMM) for anomaly analysis and detection on the Olivetti Faces dataset. 
The main objective is to cluster the face images and identify images that deviate significantly from the patterns (anomalies), as well as generate synthetic faces. 

The following steps were performed:

Data Preparation and Scaling

The Olivetti Faces dataset was loaded and preprocessed, with scaling applied to the images using PCA (Principal Component Analysis) to reduce dimensionality while preserving most of the data's variance.

GMM Training

The Gaussian Mixture Model (GMM) was trained with 40 components to model the data distribution. The GMM was fitted to the PCA-transformed data, allowing a more efficient representation of the images.

Anomaly Detection

The GMM model was used to detect anomalies by comparing the likelihood of the original data with modified images, such as flipped or darkened images. Log-likelihoods of both normal and modified images (e.g., horizontally flipped or darkened) were calculated.

Visualization of Generated Faces by GMM

The GMM generated synthetic faces, which were reconstructed from the PCA transformation. These generated faces were visualized in a grid of images to inspect the clustering results and generate faces based on the patterns found.

Reconstruction Error Analysis

Reconstruction error was calculated by comparing the original images with the reconstructed ones from PCA. This error was visualized for different types of images (normal, flipped, and darkened) to assess reconstruction quality.

Model Evaluation and Results

Modified images (flipped and darkened) exhibited higher reconstruction error, indicating that the GMM successfully identified these anomalies based on the discrepancy between log-likelihoods and reconstruction errors.

Key Results

The Gaussian Mixture Model was effective in detecting anomalies, identifying modified images (flipped and darkened) based on the likelihood of their distributions.

The faces generated by the GMM were of good quality, being able to recreate faces based on the learned patterns.

Using PCA helped reduce dimensionality and facilitated GMM training, providing an efficient way to visualize and reconstruct images.

The reconstruction error analysis indicated that the model is sensitive to image modifications, such as flipping and darkening, allowing it to identify these changes as anomalies.
