# Desafio: Detecção de Fraude em Cartão de Crédito

Trabalho prático desenvolvido como parte da disciplina de Aprendizado de Máquina no **Web Academy — Instituto de Computação / UFAM**.

## Sobre o Projeto
Este notebook aplica o fluxo completo de Machine Learning a um problema clássico de dados fortemente desbalanceados: a detecção de fraudes em transações de cartão de crédito utilizando o dataset do Kaggle (*Credit Card Fraud Detection*).

## Tecnologias e Ferramentas
* **Python**
* **Pandas & NumPy** (Manipulação e estruturação de dados)
* **Scikit-learn** (Modelagem preditiva, divisão estratificada, padronização e métricas)
* **Matplotlib & Seaborn** (Visualização de dados e matriz de confusão)

## Fluxo de Trabalho Implementado
1. **Análise Exploratória (EDA):** Verificação estrutural, estatísticas descritivas e análise da distribuição da variável alvo (*Class*), evidenciando o forte desequilíbrio (aprox. 0,17% de fraudes).
2. **Engenharia de Features:** Seleção das variáveis (componentes `V1` a `V28` e `Amount`) e padronização isolada do conjunto de treino para evitar vazamento de dados (*data leakage*).
3. **Divisão Estratificada:** Aplicação do `train_test_split` com `stratify=y` para garantir proporções idênticas da classe minoritária.
4. **Modelagem:** Treinamento utilizando **Regressão Logística** com o parâmetro `class_weight='balanced'` para penalizar os erros na classe de fraude.
5. **Avaliação Crítica:** Análise de desempenho indo além da acurácia, utilizando **Precision, Recall, F1-score** e a **Matriz de Confusão**, além de discussões sobre o impacto de negócio (*Falsos Positivos* vs *Falsos Negativos*) e ajuste de limiar (*threshold*).
