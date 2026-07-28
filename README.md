# 📈 Previsão da IBOVESPA — Comparação de Modelos de Série Temporal

![Python](https://img.shields.io/badge/Python-3776AB?logo=python&logoColor=white)
![TensorFlow](https://img.shields.io/badge/TensorFlow-FF6F00?logo=tensorflow&logoColor=white)
![Status](https://img.shields.io/badge/Status-Concluído-brightgreen)

##
![Autor](https://img.shields.io/badge/Autor-Michael%20Jourdain%20Gbedjinou-lightgrey?style=for-the-badge)
## Problema

Modelo preditivo de série temporal para prever diariamente o fechamento do índice **IBOVESPA**, usando 5 anos de dados históricos.

## Stack e abordagem

Três modelos de forecasting foram treinados e comparados no notebook: **LSTM**, **CNN** (via TensorFlow/Keras) e **ARIMA** (via statsmodels), além de teste de estacionariedade (ADF) e análise de autocorrelação (ACF/PACF) para calibrar a ordem do ARIMA.

| Modelo | MSE | MAE | RMSE |
|---|---|---|---|
| **ARIMA** (melhor resultado) | 1.34 | 0.93 | 1.15 |
| LSTM | 11.20 | 2.11 | 3.34 |
| CNN | 9.68 (test) | — | — |

O ARIMA superou as redes neurais nesse caso, com menor erro em todas as métricas.

## Como rodar localmente

```bash
git clone https://github.com/MichaelJourdain93/MichaelIBOVESPA_TECH_CHALLENGE.git
cd MichaelIBOVESPA_TECH_CHALLENGE

pip install pandas numpy scikit-learn statsmodels tensorflow matplotlib seaborn

jupyter notebook notebooks/series_temporais_ibovespa.ipynb
```

## Estrutura

```
MichaelIBOVESPA_TECH_CHALLENGE/
├── README.md
├── data/
│   └── dados_historicos_bovespa_5_anos.csv
└── notebooks/
    └── series_temporais_ibovespa.ipynb
```
