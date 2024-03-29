# Prever Aluguéis

## Descrição do Projeto

Este projeto é um estudo de caso sobre a previsão de aluguel de bicicletas dadas determinadas entradas. Utilizando o Azure Machine Learning, desenvolvemos um modelo capaz de prever a quantidade de bicicletas alugadas em determinado período, baseando-se em dados históricos. O objetivo é fornecer insights valiosos para empresas de compartilhamento de bicicletas, permitindo-lhes otimizar suas operações e melhor atender à demanda dos usuários.

## Tecnologias Utilizadas

Para este projeto, a principal tecnologia utilizada foi o Azure Machine Learning, que nos permitiu treinar, avaliar e implementar o modelo de regressão de forma eficiente e escalável.

## Dados

Os dados utilizados são históricos de aluguel de bicicletas e foram obtidos a partir da seguinte URL: [Bike Rentals Data](https://aka.ms/bike-rentals). Os dados são de natureza tabular e incluem diversas entradas que influenciam o número de aluguéis, como condições climáticas, dia da semana, entre outros.

### Especificações dos Dados:

- **Nome**: Aluguel de Bicicletas
- **Descrição**: Dados históricos de aluguel de bicicletas
- **Tipo**: Tabular

## Modelo

O projeto foca na tarefa de regressão com o objetivo de prever o número de aluguéis (inteiro). Optamos por um conjunto limitado de algoritmos para otimizar o tempo de treinamento e a eficácia do modelo:

- **Tipo de Tarefa**: Regressão
- **Conjunto de Dados**: Aluguel de Bicicletas
- **Coluna de Destino**: Aluguéis
- **Métrica Primária**: Raiz do Erro Quadrático Médio Normalizado
- **Modelos Permitidos**: RandomForest e LightGBM
- **Configurações de Treinamento**:
  - Máximo de Testes: 3
  - Máximo de Testes Simultâneos: 3
  - Máximo de Nós: 3
  - Limite de Pontuação da Métrica: 0,085
  - Tempo Limite: 15 minutos
  - Tempo Limite de Iteração: 15 minutos
  - Habilitar Rescisão Antecipada: Sim
  - Tipo de Validação: Divisão de Validação de Trem
  - Porcentagem de Dados de Validação: 10%

### Resultado do teste de pontos de extremidade

Seguindo todos os passos que a documentação manda chegamos no seguinte resultado

```json
{
  "Results": [
    356.68782294742493
  ]
}
```
