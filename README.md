# Previsão de Preços de Ações com LSTM

Este projeto utiliza um modelo de LSTM (Long Short-Term Memory) para prever os preços futuros de ações com base em dados históricos. O modelo foi treinado usando indicadores técnicos e dados de candles para prever movimentos futuros de preços.

## Tabela de Conteúdos

- [Visão Geral](#visão-geral)
- [Tecnologias Utilizadas](#tecnologias-utilizadas)
- [Como Usar](#como-usar)
- [Estrutura dos Dados](#estrutura-dos-dados)
- [Resultados](#resultados)
- [Licença](#licença)

## Visão Geral

O objetivo deste projeto é prever se o preço de fechamento de um ativo financeiro (neste caso, o WDO - Mini Índice) será maior ou menor em relação ao preço de abertura do próximo candle, utilizando uma rede neural do tipo LSTM. 

## Tecnologias Utilizadas

- Python
- Pandas
- NumPy
- Matplotlib
- Keras
- TensorFlow
- Joblib

## Como Usar

1. **Clone o repositório**:
   ```bash
   git clone https://github.com/Kelme108/Training-LSTM.git
   cd seurepositorio
   ```

2. **Instale as dependências**:
   ``` bash
   pip install -r Python Pandas, NumPy, Matplotlib, Keras, TensorFlow, Joblib
   ```

3. **Execute o script**:
  O script principal pode ser executado diretamente, mas certifique-se de que você tenha o arquivo CSV com os dados históricos de candles (WDO_candles_07.csv) na mesma pasta do script.
  ``` bash
  python seu_script.py
  ```

## **Estrutura dos Dados**
O projeto utiliza um arquivo CSV (WDO_candles_07.csv) com a seguinte estrutura:

| Coluna       | Descrição                                  |
|--------------|--------------------------------------------|
| time         | Timestamp do candle                        |
| open         | Preço de abertura                          |
| close        | Preço de fechamento                        |
| high         | Preço mais alto do candle                 |
| low          | Preço mais baixo do candle                |
| spread       | Diferença entre o preço de compra e venda |
| tick_volume  | Volume em ticks                           |
| real_volume  | Volume real                                |


## Resultados

O modelo é avaliado usando métricas como Erro Absoluto Médio (MAE) e Erro Quadrático Médio (MSE). As previsões são plotadas em comparação com os valores reais para visualizar a precisão do modelo.

![Previsões vs Valores Reais](/previsao_vs_reais.png)
