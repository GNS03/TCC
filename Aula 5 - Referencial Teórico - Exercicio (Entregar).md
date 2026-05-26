1. Crie uma tabela de Justificativa Metodológica, contendo duas colunas: 
Na primeira coluna escreva um algoritmo/ modelo/ software/ 
hardware , etc. 
Na segunda coluna escreva a premissa científica da escolha dessa 
ferramenta.

2. Descreva e elabore um mapa mental ou um esqueleto de tópicos 
(sumário provisório) do seu capítulo de referencial. (Grande área, 
subárea, tecnologias: pelo menos 3 sub tópicos em cada)

3. Escolha um conceito central (de qualquer um dos sub tópicos citados 
no exercício 2) e escreva um parágrafo explicando o funcionamento em 
nível conceitual juntamente com definição técnica e acrescente pelo 
menos uma citação indireta.

- 1
modelo, dados, python, bibliotecas

| Ferramenta           | Justificativa                                                                                                                                                                                                                      |
| -------------------- | ---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| Python               | Familiaridade com o processo de desenvolvimento, presença de bibliotecas que agilizam e facilitam o processo de processamento dos dados.                                                                                           |
| Numpy                | Biblioteca do python para manipulação de *arrays* e matrizes, necessária para realizar as multiplicações que ocorrem nos modelos.                                                                                                  |
| Pandas               | Biblioteca muito útil para manipulação de dados, importação, formatação e exportação de dados.                                                                                                                                     |
| Jupyter Notebook     | Ferramenta boa para códigos que utilizam dataframes e matrixes, permitindo que o desenvolvedor acompanhe a saída de cada linha de código separadamente.                                                                            |
| PyCharm              | IDE utilizada por ser estável e facilmente configurável.                                                                                                                                                                           |
| Dados (fígado)       | Os dados foram obtidos online e são interessantes para o projeto pois possui multiplas classes, podendo ser utilizado para testar a performance dos modelos desenvolvidos.                                                         |
| DBSCAN               | Modelo de classificação *unsupervised* , o modelo se destaca por não precisar de parâmetros como n_clusters, podendo ser utilizado com quase qualquer base de dados e tendo resultados consistentes.                               |
| MultiLayerPerceptron | Modelo de classificação *supervised* , o modelo utiliza de estruturas parecidas com neurônios humanos para realizar cálculos e comparações dos dados e assim classificá-los, sendo a base para a área de redes neurais atualmente. |
- 2 
Grande area: Machine Learning - 
	Supervisionado e Não supervisionado - 
	Sub Area: 
		Algoritmos de classificação (descrever os modelos, sem cálculo, pseudocódigo) - 
		Modelos de classificação (calculo) (2-3) - X, descrever mais
		Comparar modelos de classificação  (como serão comparados) X
	tecnologias: 
		dados - X
		python - 
		biblioteca X
	
- 3 Algoritmos de classificação são algoritmos de machine learning que aprendem com os dados para identificar padrões, especificamente em algoritmos de classificação o objetivo é classificar os dados, de acordo com as características presentes neles, em diferentes classes, a partir dos padrões aprendidos pelo modelo na fase de treinamento, esse tipo de algoritmo precisa de dados numéricos e alguns dos modelos são limitados a um certo número de classes possíveis, por exemplo o Perceptron consegue apenas classificar em 2 classes, 0 e 1, limitando muito a sua funcionalidade em cenários reais.