Escolher 3 trabalhos que falem sobre os pilares do trabalho (Machine learning, algoritmos de classificação, Python)

Machine learning (teórico)
Algoritmos de classificação (conceitos)

# 2. Trabalhos Relacionados

Nesta seção serão apresentados trabalhos que explicam a importância e o avanço da área de *Machine Learning* (ML), o funcionamento teórico e exemplos de modelos de classificação utilizados neste trabalho, bem como a importância da linguagem de programação Python no desenvolvimento de modelos modernos de *Machine Learning*.

## 2.1 Machine Learning

A área de *Machine Learning* existe há muito tempo. Segundo o *California Learning Resource Network*, o gênesis da área de Machine Learning remonta ao início da década de 1920, com grande influência de um dos pais da computação moderna, *Alan Turing*.

Durante a década de 1950, o desenvolvimento e a pesquisa na área produziram novos algoritmos e descobertas quase anualmente. Uma das contribuições mais relevantes foi o desenvolvimento do *Teste de Turing* em 1950. Segundo o site *UncoverIE*, *Alan Turing* descreveu um teste chamado *The Imitation Game* em seu artigo *Computing Machinery and Intelligence*. O teste propunha métodos para identificar se uma máquina poderia exibir inteligência comparável à humana.

Como forma de demonstrar o avanço das inteligências artificiais na atualidade, pode-se destacar o artigo *Large Language Models Pass the Turing Test*, de Cameron R. Jones e Benjamin K. Bergen.No qual os autores discutem experimentos em que modelos de linguagem modernos, como *ChatGPT-4.5* e *LLaMa-3.1-405B*, apresentaram desempenho compatível com os critérios do teste proposto por Turing. Entretanto, os próprios autores ressaltam que ainda existe debate acadêmico sobre o real significado de “passar” no Teste de Turing, visto que o artigo original não estabelece métricas ou limites objetivos bem definidos.

Já em 1957 o primeiro modelo de Redes Neurais Artificiais é desenvolvido por *Frank Rosenblatt*, o *Perceptron*, segundo o *California Learning Resource Network* o Perceptron é um "Classificador linear, considerado uma das primeiras redes neurais artificiais, criando a base para futuras arquiteturas de redes neurais". "O Perceptron apesar de limitado em suas capacidades, por ser apenas classificador **linear** (2 classes), se tornou um símbolo de otimismo para a era e impulsionou mais pesquisas sobre redes neurais. Porém a sua inabilidade em resolver problemas não lineares foi exposta depois de pouco tempo.", por isso outros modelos foram desenvolvidos com o passar do tempo.

## 2.2 Algoritmos de Classificação

Este artigo utilizará dois modelos de classificação, o DBSCAN (*Density Based Spatial Clustering of Applications with Noise*) e o *MultiLayerPerceptron* (MLP), para melhor explicar a funcionalidade e motivo de escolha desses modelos é preciso definir alguns conceitos de *Machine Learning*, como o *Supervised* e o *Unsupervised Learning*.

Segundo ALNUAIMI *Unsupervised Learning* "envolve treinar a máquina sem saber a saída, utilizando apenas entradas. A máquina descobre padrões nos dadol.s e cria seus próprios clusters. Existem dois tipos principais e mais comuns de algoritmos de *Unsupervised Learning*, Clustering e Associação", neste trabalho será utilizado um modelo de *Clustering*.

Ester diz que "existem dois tipos básicos de algoritmos de *Clustering* (Kaufman & Rousseeuw 1990): algoritmos de partição e hierárquicos." 

"Algoritmos de partição, constrói uma partição de uma base de dados D, de n objetos em grupos de k *clusters*.", "a forma de todos os *clusters* criados pelo algoritmo de partição é convexa, o que é bastante restritivo", esse é o grande problema dos algoritmos de partição, eles não conseguem reconhecer *clusters* que não são convexos.

"Algoritmos hierárquicos criam uma decomposição hierárquica de D. A decomposição hierárquica é representada por um dendrograma, uma árvore que repetidamente divide D em datasets menores até que que cada nó consista de apenas um objeto", "Até agora o principal problema dos algoritmos hierárquicos tem sido a dificuldade em definir o parâmetro de condição de término, um valor de Dmin que seja pequeno o suficiente para separar os *clusters* 'naturais' e ao mesmo tempo grande o suficiente para dividir *clusters* em duas partes.".

Para resolver os problemas citados anteriormente por Ester, para os algorimos de partição e hierárquico, Ester desenvolveu o DBSCAN.

DBSCAN é descrito por Ester como, "o algoritmo DBSCAN (*Density Based Spatial Clustering of Applications with Noise*) o qual é projetado para descobrir os *clusters* e ruídos em uma base de dados". O DBSCAN se diferencia dos outros algoritmos por não precisar de um número pré definido de *clusters* e por conseguir reconhecer *clusters* não convexos.

Supervised
	Perceptron
		MultiLayerPerceptron (David E. Rumelhari, Geoffrey E. Hintont & Ronald J. Williams)

## 2.3 Python aplicado ao Machine Learning

(Adicionar aqui o terceiro trabalho relacionado — uso do Python)



