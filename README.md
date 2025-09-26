# Otimizacao_de_Portifolio
## Propriedades Comuns dos assets
- Sem estacionariedade -> estátisticas de séries temporais financeiras mudam ao longo do tempo (retornos passados != perfomances futuras)
- Cluster de volatilidade -> Variacoes grandes/pequenas do preço tendem a ter variações grandes/pequenas seguidas
- Sem autocorrelação -> Hipótese dos mercados eficientes (HME)
- Caudas longas -> Dados financeiros não seguem distribuição normal
- Assimetria de retorno -> Distribuição de retornos não são simétricos
- Correlação positiva de assets -> Assets movem junto com o mercado

## Preços e retornos
- Na modelagem, o log(pt) é mais conveniente de ser usado, já que os sinais de preço podem ser representados (preços pequenso são amplificados e preços grandes são atenuados)
- Desse modo, o modelo mais simples é: yt = u + yt-1 + et; u = drift, et = ruido aleatório

- O retorno é medido pela variação do preço, desse modo rt = (pt - pt-1) / pt-1 e é aditivo entre os assets
- E o log-retorno é definido como rlogt = yt - yt-1 = log(pt / pt-1) e é aditivo no domínio de tempo.
- Além disso, pelo modelo mais simples, temos que: rlogt = yt - yt-1 = u + et, que é estacionário.

### Volatilidade
- Entre 12-20% - baixa volatilidade
- Acima de 30% - alta volatilidade

### Retornos com estrutura linear
- Medem a dependência no período temporal, que pela HME, é insignificante.
- FAC - Correlação entre o sinal durante um tempo e um tempo anterior
- FACP - Elimina o efeito do sinal nos últimos dois períodos

### Retornos com estrutura não linear
- Dado a pouca significância dos retornos lineares, pode-se pensar que não da para explorar a estrutura temporal do Asset.
- Mas pode-se notar estruturas no envelopamento da volatilidade do sinal, que é algo não linear

### Estrutura do Asset
- Além da estrutura temporal, que pode ser usada para forecasting e modelagem, há a estrutura do Asset em si.
- Desse modo, pode-se escolher o Asset a partir de outros Assets.
- Isso é importante para ver o risco de um portfolio, dado que as ações podem ter diferentes correlações, então diversificar pode ser bom ou ruim para o portfolio.
- Se eles estão correlacionados, então diversificar não reduz o risco.

## Modelagem IID
- Por HME, o preço de um seguro é uma estimativa para o seu valor intrínseco.
- Ou seja, qualquer informação sobre seu preço futuro já está encorporado no preço atual.
- Ou seja, o preço é um passeio aleatório e o seu retorno é uma sequência de variáveis aleatórias iid.

### Modelo IID
- Seja N Assets, os quais podem ser bonds, equities, commodities, fundos ou moedas, e seja xt E R^N os retornos aleatórios dos Assets no tempo t.
- Assim, os retornos são: xt = u + et, sendo u o retorno esperado e et um componente residual com média = 0 e com covariância
