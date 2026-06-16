1. Este artigo tem uma natureza de pesquisa aplicada, com abordagem quantitativa, com objetivo exploratório e um procedimento experimental.
2. ![[Metodologia-Fluxograma.canvas]]

| Ferramentas/Bibliotecas | Finalidade                                                           | Justificativa                                                                          |
| ----------------------- | -------------------------------------------------------------------- | -------------------------------------------------------------------------------------- |
| Numpy                   | Operações matemáticas                                                | Necessária para uso de *arrays* e multiplicação de matrizes                            |
| Pandas                  | Importação, manipulação e exportação de dados                        | Simplifica o processo de importação e manipulação de dados por meio do panda.DataFrame |
| MatPlotLib              | Criação de gráficos de resultados, erro, etc. Ex: Matriz de Confusão | Simplifica a criação de gráficos que facilitam a interpretação dos resultados          |
| Jupyter Notebook        | Utilizado para realizar a análise e manipulação de dados             | Facilita a análise dos dados por interpretar o código em blocos                        |
| PyCharm                 | IDE selecionada para realizar o desenvolvimento do código            | Facilita o desenvolvimento e *debug* do código                                         |
https://developers.google.com/machine-learning/crash-course/classification/accuracy-precision-recall

https://www.datacamp.com/pt/tutorial/sensitivity-specificity-complete-guide

https://www.geeksforgeeks.org/machine-learning/f1-score-in-machine-learning/

TP: True Positive / Verdadeiro Positivo
FP: False Positive / Falso Positivo
TN: True Negative / Verdadeiro Negativo
FN: False Negative / Falso Negativo

$$
Precisão: \frac{TP}{TP+FP}
$$
$$
Acurácia: \frac{TP+TN}{TP+FP+TN+FN}
$$
$$
Sensibilidade: \frac{TP}{TP+FN}
$$
$$
Especificidade: \frac{TN}{FP+TN}
$$
$$
F1:2\times\frac{Precisão \times Sensibilidade}{Precisão + Sensibilidade}
$$

| Métrica                | Objetivo                                                                                                                                      |
| ---------------------- | --------------------------------------------------------------------------------------------------------------------------------------------- |
| Precisão               | Proporção de resultados corretos em resultados positivos                                                                                      |
| Acurácia               | Proporção de classificações corretas, tanto TP quanto TN                                                                                      |
| Sensibilidade / Recall | Proporção de TP em relação aos positivos reais                                                                                                |
| Especificidade         | Proporção de TN em relação aos negativos reais                                                                                                |
| F1                     | Média harmônica entre a precisão e sensibilidade, útil para balancear dados, precisa que ambas a Precisão e Sensibilidade tenham um bom valor |
