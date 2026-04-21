<div align="center">

# 🌧️ Modelo de Previsão de Chuva
### Random Forest · Previsão em mm · Python

![Python](https://img.shields.io/badge/Python-3.x-3776AB?style=flat-square&logo=python&logoColor=white)
![Scikit-Learn](https://img.shields.io/badge/Scikit--Learn-1.x-F7931E?style=flat-square&logo=scikit-learn&logoColor=white)
![NumPy](https://img.shields.io/badge/NumPy-1.x-013243?style=flat-square&logo=numpy&logoColor=white)
![Google Colab](https://img.shields.io/badge/Google%20Colab-F9AB00?style=flat-square&logo=googlecolab&logoColor=white)

</div>

---

## Sobre o Projeto

Projeto de estudo adaptado de um exercício do treinamento inicial de Machine Learning da **Google for Developers**. O objetivo é prever a **quantidade de chuva em mm** com base em condições climáticas atuais, utilizando **Scikit-Learn** para treinar e avaliar o modelo.

> O código completo para criar e treinar o modelo está disponível neste repositório.

---

## 📊 Estrutura da Base de Dados

| Tipo | Variável | Unidade |
|------|----------|---------|
| **Feature** | Temperatura | °C |
| **Feature** | Pressão atmosférica | hPa |
| **Feature** | Umidade relativa | % |
| **Feature** | Velocidade do vento *(opcional)* | km/h |
| **Feature** | Direção do vento *(opcional)* | graus |
| **Target** | Quantidade de chuva | mm |

---

## ⚙️ Como Funciona

```
Temperatura + Pressão + Umidade → Modelo ML → Chuva prevista (mm)
```

| Etapa | Descrição |
|-------|-----------|
| 1. Coleta | Dados históricos de condições climáticas |
| 2. Preparação | Organização de features e target |
| 3. Treinamento | Modelo treinado com `scikit-learn` |
| 4. Previsão | Estimativa de chuva em mm para novas entradas |

---

## 🛠️ Tecnologias

| Lib | Uso |
|-----|-----|
| **Scikit-Learn** | Treinamento e avaliação do modelo |
| **NumPy** | Manipulação e operações numéricas |

---

## 🚀 Instalação

```bash
pip install scikit-learn numpy
```

---

## 🔗 Conecte-se

Se você gostou do projeto e gostaria de contribuir com uma pequena doação, eu agradeceria muito! Tenha uma ótima semana. 🙏

[![Portfolio](https://img.shields.io/badge/Portfolio-000?style=for-the-badge&logo=ko-fi&logoColor=white)](https://medium.com/@gilnei809/gilnei-azambuja-borges-analista-de-dados-e-administrador-de-banco-de-dados-8774175b0e46)
[![LinkedIn](https://img.shields.io/badge/LinkedIn-0A66C2?style=for-the-badge&logo=linkedin&logoColor=white)](https://www.linkedin.com/in/gilnei-azambuja-borges-1a83432b)
[![Hugging Face](https://img.shields.io/badge/HuggingFace-FFD21E?style=for-the-badge&logo=huggingface&logoColor=black)](https://huggingface.co/bluesky2019)
[![Kaggle](https://img.shields.io/badge/Kaggle-20BEFF?style=for-the-badge&logo=kaggle&logoColor=white)](https://www.kaggle.com/gilneiborges)
[![PayPal](https://img.shields.io/badge/PayPal-00457C?style=for-the-badge&logo=paypal&logoColor=white)](https://www.paypal.com/donate/?hosted_button_id=FW4VNKJWXLTCJ)
