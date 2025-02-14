Cálculo de Métricas de Avaliação de Aprendizado

Neste projeto, vamos calcular as principais métricas de avaliação de modelos de classificação de dados. As métricas a serem calculadas são:

    Acurácia
    Sensibilidade (Recall)
    Especificidade
    Precisão
    F-score

Essas métricas são essenciais para entender o desempenho de um modelo de Machine Learning (ML) ao classificar dados em diferentes categorias. Vamos utilizar as fórmulas e métodos correspondentes a cada uma dessas métricas para calcular os resultados, utilizando uma matriz de confusão como base para os cálculos.
Objetivo

O objetivo do projeto é implementar funções que calculem as métricas mencionadas a partir de uma matriz de confusão. A matriz de confusão será fornecida como entrada para as funções, e você pode escolher valores arbitrários para os elementos da matriz (VP, VN, FP, FN) para facilitar o entendimento de como cada métrica funciona.
Tabela 1: Visão Geral das Métricas de Avaliação
Métrica	Fórmula	Descrição
Acurácia	VP+VNVP+FN+VN+FPVP+FN+VN+FPVP+VN​	Proporção de previsões corretas (verdadeiros positivos e negativos) em relação ao total de previsões.
Sensibilidade (Recall)	VPVP+FNVP+FNVP​	Capacidade do modelo de identificar corretamente as instâncias positivas.
Especificidade	VNVN+FPVN+FPVN​	Capacidade do modelo de identificar corretamente as instâncias negativas.
Precisão	VPVP+FPVP+FPVP​	Proporção de previsões positivas que são realmente positivas.
F-score	2×Precisa˜o×SensibilidadePrecisa˜o+Sensibilidade2×Precisa˜o+SensibilidadePrecisa˜o×Sensibilidade​	Média harmônica entre a precisão e a sensibilidade.
Onde:

    VP (Verdadeiros Positivos): Casos positivos corretamente classificados.
    VN (Verdadeiros Negativos): Casos negativos corretamente classificados.
    FP (Falsos Positivos): Casos negativos classificados incorretamente como positivos.
    FN (Falsos Negativos): Casos positivos classificados incorretamente como negativos.
    P (Precisão): A precisão do modelo ao classificar as instâncias positivas.
    S (Sensibilidade): A capacidade do modelo de identificar corretamente as instâncias positivas.
    N (Total de elementos): Total de dados no conjunto de teste.

Como Usar

    Escolha uma matriz de confusão: Escolha uma matriz de confusão com valores arbitrários de VP, VN, FP, FN. Essa matriz será usada para calcular as métricas.
    Implementação das funções: Implemente funções para calcular cada métrica com base na matriz de confusão fornecida.
    Cálculos: Utilize as fórmulas da Tabela 1 para calcular as métricas de avaliação.

Exemplo de matriz de confusão:
	Predito Positivo	Predito Negativo
Real Positivo	VP	FN
Real Negativo	FP	VN
Funções:

    calcular_acuracia(VP, VN, FP, FN): Calcula a acurácia do modelo.
    calcular_sensibilidade(VP, FN): Calcula a sensibilidade (recall).
    calcular_especificidade(VN, FP): Calcula a especificidade.
    calcular_precisao(VP, FP): Calcula a precisão.
    calcular_fscore(precisao, sensibilidade): Calcula o F-score.

Exemplo de Cálculo

Dada a seguinte matriz de confusão:
	Predito Positivo	Predito Negativo
Real Positivo	50	10
Real Negativo	5	100

Temos:

    VP = 50
    FN = 10
    FP = 5
    VN = 100

Utilizando as fórmulas da Tabela 1, podemos calcular as métricas:

    Acurácia = 50+10050+10+100+5=150165=0.90950+10+100+550+100​=165150​=0.909
    Sensibilidade (Recall) = 5050+10=5060=0.83350+1050​=6050​=0.833
    Especificidade = 100100+5=100105=0.952100+5100​=105100​=0.952
    Precisão = 5050+5=5055=0.90950+550​=5550​=0.909
    F-score = 2×0.909×0.8330.909+0.833=2×0.7581.742=0.8692×0.909+0.8330.909×0.833​=2×1.7420.758​=0.869

Conclusão

Este projeto oferece uma maneira prática de entender e calcular as principais métricas de avaliação de um modelo de classificação, utilizando a matriz de confusão como base. Aprofundar-se no cálculo dessas métricas ajudará a avaliar o desempenho dos modelos de forma mais eficiente e a escolher a melhor abordagem para resolver um problema de classificação.
