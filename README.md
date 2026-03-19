# Previsão de Energia Gerada em Usina com Regressão Linear

Este projeto foi feito para a prática do curso Data Science Alura e tem como objetivo prever a energia elétrica gerada (PE) em uma usina com base em variáveis ambientais utilizando regressão linear.

## Dataset

O conjunto de dados contém as seguintes variáveis:

- AT: Temperatura ambiente  
- V: Vácuo de exaustão  
- AP: Pressão atmosférica  
- RH: Umidade relativa  
- PE: Energia elétrica gerada (variável alvo)  

## Preparação dos Dados

Os dados foram separados em variáveis explicativas (X) e variável alvo (y):

- X: AT, V, AP, RH  
- y: PE  

Em seguida, foi realizada a divisão em treino e teste:

- 70% para treino  
- 30% para teste  

## Modelagem

Foi utilizado o modelo de regressão linear com a biblioteca statsmodels.

A constante foi adicionada manualmente ao modelo.

### Modelo 1

Variáveis utilizadas:

- AT  
- V  
- AP  
- RH  

O modelo foi ajustado utilizando Ordinary Least Squares (OLS).

## Avaliação do Modelo

O desempenho foi avaliado utilizando o coeficiente de determinação R².

O modelo apresentou bom ajuste aos dados de treino, indicando boa capacidade de explicação da variável alvo.

## Multicolinearidade

Foi utilizado o Variance Inflation Factor (VIF) para verificar a presença de multicolinearidade entre as variáveis explicativas.

Resultados do modelo inicial:

- AT apresentou VIF acima de 5, indicando possível multicolinearidade  
- V apresentou valor moderado  
- AP e RH apresentaram valores baixos  

Para reduzir esse problema, foi criado um segundo modelo.

### Modelo 2

Variáveis utilizadas:

- V  
- AP  
- RH  

A variável AT foi removida para reduzir a multicolinearidade.

## Comparação entre Modelos

O modelo 2 foi comparado com o modelo 1 para avaliar o impacto da remoção da variável AT.

A análise considerou:

- R²  
- estabilidade dos coeficientes  
- comportamento dos resíduos  

## Análise de Previsão

Foram gerados gráficos de comparação entre valores reais e previstos.

Isso permite avaliar visualmente o desempenho do modelo.

## Análise de Resíduos

Os resíduos foram analisados para verificar a qualidade do modelo.

Resíduo é definido como:

resíduo = valor real − valor previsto

Foram gerados gráficos de:

- resíduos versus valores previstos  

## Interpretação dos Resíduos

Um bom modelo apresenta:

- resíduos distribuídos de forma aleatória  
- ausência de padrões  
- variância constante  

## Resultados Observados

Os gráficos indicam:

- boa proximidade entre valores reais e previstos  
- alguns padrões nos resíduos que podem indicar limitações do modelo  

## Conclusão

O modelo de regressão linear foi capaz de capturar a relação entre variáveis ambientais e geração de energia.

Pontos positivos:

- boa capacidade preditiva  
- modelo interpretável  
- aplicação direta em dados reais  

Limitações:

- presença inicial de multicolinearidade  
- necessidade de ajuste nas variáveis  
- possíveis padrões nos resíduos  

## Possíveis Melhorias

- testar novos modelos além da regressão linear  
- incluir novas variáveis explicativas  
- aplicar transformações nos dados  
- validar com dados de teste  

Este projeto demonstra a aplicação de técnicas de regressão linear e análise estatística para previsão de geração de energia em usinas.
