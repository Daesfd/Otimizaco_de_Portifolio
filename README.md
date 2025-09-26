# Otimizacao_de_Portifolio
## Propriedades Comuns
- Sem estacionariedade -> estátisticas de séries temporais financeiras mudam ao longo do tempo (retornos passados != perfomances futuras)
- Cluster de volatilidade -> Variacoes grandes/pequenas do preço tendem a ter variações grandes/pequenas seguidas
- Sem autocorrelação -> Hipótese dos mercados eficientes
- Caudas longas -> Dados financeiros não seguem distribuição normal
- Assimetria de retorno -> Distribuição de retornos não são simétricos
- Correlação positiva de assets -> Assets movem junto com o mercado

## Preços e retornos
- Na modelagem, o log(pt) é mais conveniente de ser usado, já que os sinais de preço podem ser representados (preços pequenso são amplificados e preços grandes são atenuados)
- Desse modo, o modelo mais simples é: yt = u + yt-1 + et; u = drift, et = ruido aleatório

- O retorno é medido pela variação do preço, desse modo 
