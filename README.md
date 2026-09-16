# Análise de Eficiência Financeira e Conversão de Votos nas Eleições Presidenciais de 2022

![Python](https://img.shields.io/badge/Python-3.x-blue.svg)
![Pandas](https://img.shields.io/badge/Pandas-Tratamento%20de%20Dados-orange.svg)
![Seaborn](https://img.shields.io/badge/Seaborn-Visualização-green.svg)

## 📌 Visão Geral do Projeto

Este projeto consiste em uma análise de dados ponta a ponta voltada a auditar, cruzar e diagnosticar o impacto do financiamento de campanha no desempenho das urnas no 1º turno das Eleições Presidenciais de 2022. 

O objetivo principal foi responder se o volume financeiro dita o vencedor e extrair a métrica de **"Custo por Voto"** de cada candidatura, identificando as estratégias de captação de recursos dos líderes e os principais *outliers* de mercado (campanhas ineficientes).

---

## 📊 Perguntas de Negócio Respondidas

1. O volume de dinheiro dita o vencedor no cenário presidencial?
2. Qual foi o "custo de eficiência" (R$ por voto conquistado) de cada candidato?
3. Qual a principal fonte de financiamento (público vs. privado) dos candidatos que avançaram ao segundo turno?
4. Existem *outliers* gritantes de investimento que resultaram em baixa conversão de votos?

---

### Resumo Executivo: Os Principais Candidatos

| Candidato | Valor de Receita | Votos Nominais | Custo por Voto |
| :--- | :--- | :--- | :--- |
| **Lula** | R$ 135.5M | 57.2M | R$ 2.37 |
| **Bolsonaro** | R$ 126.1M | 51.0M | R$ 2.47 |
| **Simone Tebet** | R$ 38.8M | 4.9M | R$ 7.90 |
| **Ciro Gomes** | R$ 36.0M | 3.5M | R$ 10.01 |
| **Soraya Thronicke**| R$ 36.6M | 0.6M | R$ 61.03 |

---

## 🛠️ Tecnologias e Conceitos Aplicados

*   **Python 3** como linguagem base.
    *   **Pandas** para todo o pipeline de engenharia e modelagem de dados:
    *   Saneamento de strings e conversão de tipos de dados (`astype`, substituição de caracteres).
    *   Manipulação de séries temporais (`to_datetime`).
    *   Agregações complexas e agrupamentos multicolunas (`groupby` + `sum`).
    *   Matrizes dinâmicas de cruzamento (`pivot_table`).
    *   Junção de bases de dados heterogêneas (`merge`/JOIN estrutural).
*   **Seaborn & Matplotlib** para análise exploratória visual (Gráficos de Barras e Gráficos de Dispersão/*Scatter Plots*).

---

## 📈 Principais Insights Extraídos

*   **Concentração de Mercado (Market Share):** Os dois candidatos que avançaram ao segundo turno (Lula e Bolsonaro) concentraram sozinhos **69,11%** de todo o dinheiro que circulou na eleição presidencial, evidenciando um forte abismo financeiro para o restante do pelotão.

*   **Eficiência dos Líderes:** Houve um empate técnico na eficiência de conversão das duas maiores campanhas. O candidato Luiz Inácio Lula da Silva operou a um custo de **R$ 2,37** por voto obtido, enquanto Jair Messias Bolsonaro registrou **R$ 2,47** por voto. Ambos atuaram muito abaixo da linha de base/mediana nacional, que foi de **R$ 14,52**.
  
*   **Outliers de Ineficiência:** Soraya Thronicke (UNIÃO) figurou como o maior ralo de conversão financeira, movimentando mais de R$ 36 milhões para obter cerca de 600 mil votos, o que gerou um custo proibitivo de **R$ 61,03** por voto conquistado.

*   **Polarização de Estratégias de Captação:** O cruzamento via matriz revelou caminhos opostos de receita: o PT focou majoritariamente no Fundo Especial público (mais de R$ 125 milhões), enquanto o PL baseou o grosso de sua estrutura em "Outros Recursos" (doações privadas, pessoas físicas e financiamento coletivo, superando R$ 94 milhões). Podemos ver esse comparativo no gráfico abaixo:
  
![Comparativo de Fontes de Receita](img/comparativo_fontes_receita_agrupado.png)

---

## Análise visual de Outliers

![Análise de Outliers](img/grafico_dispersao_eleicoes.png)

---

## 📂 Estrutura do Repositório

```text
├── img/                # Visualizações gráficas e plots do projeto
│   ├── comparativo_fontes_receita_agrupado.png
│   └── grafico_dispersao_eleicoes.png
├── notebooks/          # Jupyter Notebook com o pipeline de código
│   └── analise_eleitoral.ipynb
└── README.md           # Documentação e relatório do projeto
