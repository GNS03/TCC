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

Definição de um algoritmo de classificação, conceito.
### 2.2.1 *Unsupervised Learning*

Segundo ALNUAIMI (2026) *Unsupervised Learning* "envolve treinar a máquina sem saber a saída, utilizando apenas entradas. A máquina descobre padrões nos dados e cria seus próprios clusters. Existem dois tipos principais e mais comuns de algoritmos de *Unsupervised Learning*, Clustering e Associação", neste trabalho será utilizado um modelo de *Clustering*.

Ester diz que "existem dois tipos básicos de algoritmos de *Clustering* (Kaufman & Rousseeuw 1990): algoritmos de partição e hierárquicos." (mais coisa -> link)

"Algoritmos de partição, o algoritmo constrói uma partição de uma base de dados D, de n objetos em grupos de k *clusters*.", Ester estabelece também a limitação desse tipo de algoritmo em relação as classificações de dados que não se encaixam no padrão que é esperado pelo modelo, "a forma de todos os *clusters* criados pelo algoritmo de partição é convexa, o que é bastante restritivo", esse é o grande problema dos algoritmos de partição, eles não conseguem reconhecer *clusters* que não são convexos, sendo assim esses algoritmos falham em classificar muitos casos reais, aonde a divisão entre uma classificação nem sempre é tão clara. (Fulano,2026)

"Algoritmos hierárquicos criam uma decomposição hierárquica de D. A decomposição hierárquica é representada por um dendrograma, uma árvore que repetidamente divide D em datasets menores até que que cada nó consista de apenas um objeto", Ester destaca também as limitações de algoritmos hierárquicos, que diferente dos algoritmos de partição, possuem um problema de parâmetros, "Até agora o principal problema dos algoritmos hierárquicos tem sido a dificuldade em definir o parâmetro de condição de término, um valor de Dmin que seja pequeno o suficiente para separar os *clusters* 'naturais' e ao mesmo tempo grande o suficiente para dividir *clusters* em duas partes.".

Para resolver os problemas citados anteriormente por Ester, para os algoritmos de partição e hierárquico, Ester desenvolveu o DBSCAN, criando assim um modelo que conseguisse representar *clusters* convexos e não convexos, e pouco dependente de uma correta parametrização para entender os dados.

?Devido a essas características o DBSCAN pode ser classificado como uma evolução dos modelos anteriores.
#### 2.2.1.1 DBSCAN

DBSCAN é descrito por Ester como, "o algoritmo DBSCAN (*Density Based Spatial Clustering of Applications with Noise*) o qual é projetado para descobrir os *clusters* e ruídos em uma base de dados". O DBSCAN se diferencia dos outros algoritmos por não precisar de um número pré definido de *clusters* e por conseguir reconhecer *clusters* não convexos. Devido a essas vantagens o DBSCAN é um ótimo algoritmo de agrupamento quando não se conhece detalhadamente os dados ou precisa-se realizar uma abordagem genérica, capaz de se adaptar a múltiplos bancos de dados.

*SetOfPoints* - toda a base de dados ou *cluster* descoberta na iteração anterior
*Eps*, *MinPts* - são os parâmetros globais de densidade determinados manualmente pelo usuário 

```
ExpandCluster(SetOfPoints, Point, ClId, Eps, MinPts) : Boolean
	seeds := SetOfPoints.regionQuery(Points, Eps);
	IF seeds.size < MinPts THEN // No core point
		SetOfPoint.changeClId(Point, NOISE);
		RETURN False;
	ELSE //all points in seeds are density reachable from Point
		SetOfPoints.changeClIds(seeds, ClId);
		seeds.delete(Point)
		WHILE seeds <> Empty DO
			currentP := seeds.first();
			result := SetOfPoints.regionQuery(currentP, Eps);
			IF result.size >= MinPts THEN
				FOR i FROM 1 TO result.size DO
					resultP : = result.get(i);
					IF resultP.ClId IN {UNCLASSIFIED, NOISE} THEN
						iF resultP.ClId = UNCLASSIFIED THEN
							seeds.append(resultP);
						END IF;
						SetOfPoints.change.ClId(resultP, ClId);
					END IF; // UNCLASSIFIED or NOISE
				END FOR;
			END IF; // result.size >= MinPts
			seeds.delete(currentP);
		END WHILE; // seeds <> empty
		RETURN True;
	END IF;
END; // ExpandCluster				

DBSCAN (SetOfPoints, Eps, MinPts)

	//SetOfPoints is UNCLASSIFIED
	CluterId := nextId(NOISE);
	FOR i FROm 1 to SetOfPoints.size DO
		Point := SetOfPoints.get(i);
		IF Point.ClId = UNCLASSIFIED THEN
			IF ExpandCluster(SetOfPoints, Point, ClusterId, Eps, MinPts) THEN
				ClusterId := nextId(ClusterId)
			END IF;
		END IF;
	END FOR;
END; // DBSCAN
```

### 2.2.2 *Supervised Learning*

Segundo Mueller (2016), "Supervised Learning é uma técnica de *Machine Learning* que utiliza de dados rotulados para educar o sistema em previsões baseadas em seu treinamento. Esse processo quase imita o processo humano de aprendizagem.", o grande diferencial entre *Unsupervised* e *Supervised Learning* é que no primeiro os dados não são previamente rotulados e o modelo apenas os separa em grupos devido as características presentes nos dados, já no outro caso os dados precisam de rótulos pré-definidos para que o modelo aprenda que certas características definem um rotulo, o resultado pode ser tanto uma classe quanto contínuo como em casos de regressão.

#### 2.2.2.1 Perceptron

Segundo Rosenblatt, o criador do perceptron, em seu *report* de 1957 "*The Perceptron A Perceiving and Recognizing Automation*", "Podemos considerar o perceptron como uma caixa preta, com uma camera de TV como entrada, e uma impressora alfabética o um grupo de luzes como saída. Sua performance pode ser descrita como um processo de aprender a dar o mesmo sinal (saída) para todo estímulo óptico que pertence a mesma classe arbitrária.", essa é a proposta do perceptron, ele é treinado para dar a mesma saída para uma entrada todas as vezes, definindo assim, que aquela entrada pertence a aquela classe observações, porém, como citado anteriormente, o Perceptron é um modelo supervisionado e precisa que as entradas estejam rotuladas antes do treinamento.

Outro ponto importante que foi citado anteriormente, é a incapacidade do Perceptron de resolver problemas não lineares, para resolver essa falha o próximo modelo foi desenvolvido, para ser uma evolução do Perceptron.

pseudocódigo
##### 2.2.2.1.1 MultiLayerPerceptron

Segundo Rumelhart e cia, em seu artigo de 1986, "Nós descrevemos um novo procedimento de aprendizagem, *back-propagation*, para redes que utilizam unidades similares a neurônios. O procedimento repetidamente ajusta os pesos das conexões da rede para minimizar a diferença entre a saída do modelo e a saída esperada. Como um resultado dos ajustes de pesos, unidades internas que não parte da camada de entrada ou saída, vem a representar características importantes do domínio da tarefa e os padrões da tarefa são capturados pela interação entre essas unidades. A habilidade de criar novas e úteis características diferencia o *back-propagation* dos métodos mais simples antigos.". 

A partir da pesquisa e desenvolvimento, realizados por Rumelhart e cia, para a criação do método de *back-propagation* as redes neurais evoluíram e o back-propagation foi utilizado e é até hoje para desenvolver o MultiLayerPerceptron, permitindo que essa rede neural consiga ter outputs não lineares, além de se adaptar muito melhor as características e nuâncias dos dados de entrada.

## 2.3 Python

O Python foi criado e desenvolvido por Guido Van Rossum na década de 90, o python é uma linguagem dinamicamente tipada, interpretada, que tem como objetivo ser uma linguagem simples de aprender e ler, porém capaz de realizar muitas funções.

### 2.3.1 Python aplicado ao Machine Learning

Por essas características o Python se tornou uma linguagem muito utilizada na área de dados, por matemáticos que utilizavam o matlab ou o R anteriormente, devido a facilidade e capacidade do python muitos desses profissionais e cientistas decidiram utilizá-lo como linguagem principal para processos com dados, como mineração de dados, tratamento de dados, desenvolvimento de modelos, criação de gráficos. Por isso, várias bibliotecas foram desenvolvidas pela comunidade ao longo dos anos para facilitar o tratamento de dados em Python, como o Pandas, NumPy, Polars, entre outros. Definindo assim, que o Python fosse a principal linguagem para tratamento de dados atualmente.



