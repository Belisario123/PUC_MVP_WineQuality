# 🧪 MVP — Sprint: Machine Learning & Analytics (PUC-Rio)

**Autor:** Eduardo Belisario Nicolau  
**Turma:** 40530010056_20250_01  
**Data:** 28/09/2025  

## 🎯 Tema
Predição da qualidade de vinhos (*regressão*) utilizando o dataset **Wine Quality** do UCI Machine Learning Repository.

## 📚 Descrição
Este projeto é parte do MVP da disciplina **Machine Learning & Analytics** da PUC-Rio.  
O objetivo foi construir um fluxo completo de **aprendizado de máquina supervisionado** para prever a **nota de qualidade (0–10)** de vinhos a partir de medições físico-químicas.

A solução implementa:

- Preparação do ambiente e **reprodutibilidade** com sementes (`seed`) fixas.  
- **Carregamento direto dos dados** a partir do UCI Repository ou do próprio GitHub, garantindo que qualquer pessoa consiga rodar o notebook sem downloads manuais.  
- **Exploração, limpeza e engenharia de atributos**, incluindo criação da variável `alcohol_squared` para capturar efeitos não lineares e da variável categórica `type` (tinto/branco).  
- **Treinamento e validação de modelos**: Linear Regression, Ridge, Random Forest e Gradient Boosting, com pipelines que integram `StandardScaler` e `OneHotEncoder`.  
- **Otimização de hiperparâmetros** com `RandomizedSearchCV`, ajustando parâmetros essenciais para Random Forest e Gradient Boosting.  
- **Análise de importância de variáveis** usando *Permutation Importance*, identificando os atributos mais relevantes (por exemplo, teor alcoólico e acidez).  
- **Conclusões, limitações e próximos passos**, cobrindo hipóteses, interpretação de métricas e sugestões para melhorias futuras.

## 📂 Estrutura do repositório
```text
PUC_MVP_WineQuality/
├── PUC_MVP_WineQuality.ipynb   # Notebook completo e reprodutível
├── winequality-red.csv         # Dataset de vinhos tintos
├── winequality-white.csv       # Dataset de vinhos brancos
└── README.md                   # Este arquivo
```

## 🔗 Links de reprodutibilidade
- **Notebook final no Google Colab**  
  [Abrir no Colab](https://colab.research.google.com/drive/1iyPTI1fOxS4LK0ZygMe2QqDL3KbkYDPJ?usp=sharing)
- **Repositório no GitHub**  
  [PUC_MVP_WineQuality](https://github.com/Belisario123/PUC_MVP_WineQuality)

## ⚙️ Requisitos de execução
Para rodar localmente, é necessário ter:

- Python 3.12 ou superior
- Bibliotecas:
  - `pandas`
  - `numpy`
  - `scikit-learn`
  - `matplotlib`

No **Google Colab**, basta abrir o notebook e executar **Runtime → Run all** para que tudo funcione automaticamente (os dados são baixados via URLs do GitHub).

## 🏁 Resultados principais
- **Melhor modelo:** Random Forest ajustado via `RandomizedSearchCV`
- **Desempenho final:**
  - RMSE ≈ 0,70
  - MAE baixo
  - R² estável no conjunto de teste
- **Variáveis mais importantes:** atributos relacionados a teor alcoólico e acidez destacaram-se como determinantes para a previsão da qualidade.

## 📄 Licença
- **Dataset original:** [Cortez et al., 2009 — UCI Machine Learning Repository](https://doi.org/10.24432/C56S3T), licenciado sob [Creative Commons Attribution 4.0 (CC BY 4.0)](https://creativecommons.org/licenses/by/4.0/).
- **Código do notebook:** disponibilizado publicamente neste repositório para fins acadêmicos e educacionais.

---

> 💡 Este README garante que o avaliador consiga entender rapidamente o objetivo do trabalho, os resultados alcançados e como reproduzir cada passo sem esforço.
