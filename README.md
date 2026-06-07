# ❤️ Heart Disease Prediction with Machine Learning

Projeto desenvolvido para aplicação de técnicas de Machine Learning na predição de doenças cardíacas utilizando a base **Heart Disease** do UCI Machine Learning Repository.

## 📌 Objetivo

Construir e comparar modelos de classificação capazes de identificar a presença de doença cardíaca a partir de características clínicas dos pacientes.

O projeto contempla:

* Pré-processamento dos dados;
* Treinamento de Árvores de Decisão;
* Extração e interpretação de regras;
* Comparação entre diferentes algoritmos de Machine Learning;
* Seleção de atributos;
* Avaliação de desempenho dos modelos.

---

## 📊 Base de Dados

**Dataset:** Heart Disease (UCI Machine Learning Repository)

### Variável Alvo

| Valor | Classe              |
| ----- | ------------------- |
| 0     | Sem doença cardíaca |
| 1–4   | Com doença cardíaca |

Para simplificar o problema, a variável foi transformada em uma classificação binária:

* `0` → Sem doença cardíaca
* `1` → Com doença cardíaca

### Variáveis Preditoras

| Variável | Descrição                        |
| -------- | -------------------------------- |
| age      | Idade                            |
| sex      | Sexo                             |
| cp       | Tipo de dor no peito             |
| trestbps | Pressão arterial em repouso      |
| chol     | Colesterol                       |
| fbs      | Açúcar no sangue em jejum        |
| restecg  | Resultado do eletrocardiograma   |
| thalach  | Frequência cardíaca máxima       |
| exang    | Angina induzida por exercício    |
| oldpeak  | Depressão do segmento ST         |
| slope    | Inclinação do segmento ST        |
| ca       | Número de vasos principais       |
| thal     | Resultado do teste de talassemia |

---

## 🛠 Tecnologias Utilizadas

* Python
* Pandas
* NumPy
* Matplotlib
* Scikit-Learn
* UCI ML Repository (`ucimlrepo`)

---

## 🔄 Fluxo do Projeto

### 1. Carregamento dos Dados

```python
from ucimlrepo import fetch_ucirepo

heart_disease = fetch_ucirepo(id=45)
```

### 2. Pré-processamento

* Conversão de valores ausentes;
* Imputação utilizando média;
* Conversão da variável alvo para classificação binária.

### 3. Divisão dos Dados

* 80% Treinamento
* 20% Teste

```python
train_test_split(test_size=0.2, random_state=42)
```

---

## 🌳 Árvore de Decisão

Foi utilizado o algoritmo **Decision Tree Classifier** para:

* Classificação dos pacientes;
* Visualização da árvore;
* Extração de regras;
* Identificação das variáveis mais importantes.

### Análises realizadas

* Acurácia
* Matriz de Confusão
* Visualização da Árvore
* Importância das Variáveis
* Regras de Decisão

---

## 🤖 Modelos Comparados

Os seguintes algoritmos foram avaliados:

| Modelo                       |
| ---------------------------- |
| Decision Tree                |
| Random Forest                |
| k-Nearest Neighbors (kNN)    |
| Support Vector Machine (SVM) |
| Logistic Regression          |

---

## ⚙️ Experimentos com kNN

Foram realizados testes variando o parâmetro `k`:

```python
k = [1, 3, 5, 7, 9, 11]
```

O objetivo foi analisar o impacto da vizinhança no desempenho do modelo.

---

## 🎯 Seleção de Atributos

Foi aplicada a técnica:

```python
SelectKBest(mutual_info_classif)
```

para identificar os atributos mais relevantes para a classificação.

Foram realizados experimentos utilizando diferentes quantidades de atributos selecionados.

---

## 📈 Métrica de Avaliação

A principal métrica utilizada foi a **Acurácia (Accuracy)**.

[
Accuracy = \frac{Acertos}{Total\ de\ Amostras}
]

A métrica foi escolhida por permitir uma comparação simples e direta entre os modelos avaliados.

---

## 📊 Visualizações Geradas

O projeto gera:

* Matriz de Confusão
* Árvore de Decisão
* Gráfico de Importância das Variáveis
* Comparação entre Modelos
* Desempenho do kNN para diferentes valores de k

---

## 🚀 Como Executar

### Clone o repositório

```bash
git clone https://github.com/seu-usuario/seu-repositorio.git
```

### Entre na pasta do projeto

```bash
cd seu-repositorio
```

### Instale as dependências

```bash
pip install pandas numpy matplotlib scikit-learn ucimlrepo
```

### Execute o projeto

```bash
python projeto_final_tbs5_rls10.py
```

---

## 📚 Conceitos Aplicados

* Machine Learning
* Classificação Supervisionada
* Árvores de Decisão
* Random Forest
* k-Nearest Neighbors (kNN)
* Support Vector Machines (SVM)
* Regressão Logística
* Seleção de Atributos
* Pré-processamento de Dados
* Avaliação de Modelos

---

## 👥 Autores

* Rennan Lino Santos
* Tamyres Bezerra da Silva

---

## 🎓 Contexto Acadêmico

Projeto desenvolvido para fins educacionais, aplicando técnicas de Aprendizado de Máquina em um problema real da área da saúde utilizando uma base pública do UCI Machine Learning Repository.
