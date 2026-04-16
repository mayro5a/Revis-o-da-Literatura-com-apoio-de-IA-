# Resumo Estruturado

## 1. Técnicas de aprendizado de máquina mais utilizadas
A literatura demonstra o uso extenso de algoritmos supervisionados clássicos de Machine Learning (ML), sendo os mais proeminentes:
- Random Forest (RF)
- Support Vector Machine (SVM)
- Regressão Logística (LR)
- K-Nearest Neighbors (KNN)
- Árvores de Decisão (DT)

Mais recentemente, destacam-se:
- Métodos de ensemble: XGBoost, AdaBoost, Gradient Boosting (GBM), LightGBM
- Estratégias de Stacking

O uso de Deep Learning (DL) também cresce rapidamente:
- Redes Neurais Artificiais (ANN)
- Redes Neurais Convolucionais (CNN)
- Long Short-Term Memory (LSTM)

---

## 2. Atributos (features) mais frequentes
A maioria das predições baseia-se em:
- Registros Eletrônicos de Saúde (EHR)
- Exames de rotina

Principais atributos:
- Idade
- Índice de Massa Corporal (IMC)
- Glicose / glicemia de jejum (FPG)
- Pressão arterial (sistólica/diastólica)
- Hemoglobina glicada (HbA1c)
- Sexo
- Insulina
- Triglicerídeos (TG)

Outros atributos relevantes:
- Exercício físico
- Tabagismo
- Consumo de álcool
- Histórico familiar

---

## 3. Principais desafios
Os principais desafios incluem:

- **Dados:**
  - Pequeno tamanho de amostra
  - Dados ausentes
  - Desbalanceamento de classes

- **Validação:**
  - Falta de validação externa
  - Baixa generalização

- **Interpretabilidade:**
  - Modelos caixa-preta

- **Aspectos éticos:**
  - Privacidade de dados médicos

---

## 4. Técnicas de pré-processamento
Principais técnicas utilizadas:

- **Imputação de dados:**
  - Média
  - Mediana
  - KNN
  - MICE

- **Normalização:**
  - Min-Max

- **Balanceamento:**
  - SMOTE
  - Random Under-Sampling

- **Redução de dimensionalidade / seleção de features:**
  - Algoritmos Genéticos
  - LASSO
  - PCA
  - Boruta
  - RFE
  - Correlação de Spearman

---

## 5. Métricas de avaliação
Principais métricas utilizadas:

- **Globais:**
  - Acurácia
  - AUC / AUROC

- **Detalhadas:**
  - Sensibilidade (Recall)
  - Especificidade
  - Precisão
  - F1-score

- **Outras:**
  - Brier Score
  - Decision Curve Analysis (DCA)

---

# Tabela Comparativa de Estudos na Literatura

| Artigo / Referência | Técnicas Utilizadas | Atributos Utilizados | Tipo de Tarefa | Pré-processamento | Métricas | Principais Contribuições |
|--------------------|-------------------|----------------------|----------------|-------------------|----------|--------------------------|
| Mohsen et al. (Revisão de Escopo sobre Predição de T2DM) | ML clássico (RF, SVM, LR, DT), Deep Learning | Dados multimodais (EHR, multi-ômica, imagens); Idade, IMC, Glicose, histórico familiar | Classificação | SMOTE, subamostragem, imputação por média/mediana, remoção de linhas | AUC, Acurácia, Sensibilidade, Especificidade, Precisão, F1-Score | Demonstrou superioridade de modelos multimodais e destacou desafios clínicos como validação externa e explicabilidade |
| Zaferani et al. (Modelo Ensemble Transparente) | Ensemble Stacking e Voting (LR, RF, KNN, Redes Neurais) | Glicose, Pressão Arterial, Espessura da pele, Insulina, IMC, Idade | Classificação | Imputação pela média, Normalização Min-Max, Seleção de Features (Spearman) | Acurácia, Precisão, Recall, Especificidade, F1-score, AUROC, Brier Score, ECE | Criou modelo altamente calibrado e interpretável usando LIME e SHAP |
| Nazirun et al. (Revisão Sistemática em Progressão de T2DM) | LR, SVM, DT, RF, Bagging, Boosting (XGBoost, AdaBoost, LightGBM), CNN, LSTM | FPG, FBG, HbA1c, dados demográficos, histórico médico e estilo de vida | Classificação, Regressão, Agrupamento | Imputação (MICE, k-NN), padronização, PCA, SMOTE, Information Gain | Acurácia, AUC-ROC, Sensibilidade, Especificidade, Precisão, RMSE, MCC | Propôs taxonomia e melhores práticas, incluindo desafios éticos |
| Liu et al. (Risco de Progressão de Pré-diabetes para Diabetes) | XGBoost, LR, DT, RF | FPG, TG, Circunferência da Cintura, IMC, ALT, Educação | Classificação | LASSO, Otimização Bayesiana | AUC, Sensibilidade, Especificidade, Acurácia, F1-score | XGBoost teve melhor desempenho; SHAP identificou variáveis mais importantes |
| Abdollahi et al. (Ensemble Híbrido com Algoritmos Genéticos) | Stacking, AdaBoost, Bagging, RF, KNN, MLP, SVM, NB, Extra Trees | Idade, exames laboratoriais, diagnósticos, medicamentos, tempo de internação | Classificação | Imputação pela mediana, Algoritmos Genéticos | Acurácia, Sensibilidade, Especificidade | Alta acurácia (98.8–99%) com otimização evolutiva |
| Lu et al. (Predição de Trombose Venosa em Osteoartrite) | XGBoost, LR, RF, AdaBoost, GBDT, LGBM | Grau K-L, Idade, Hipertensão, Ácido Úrico, Anti-CCP, Glicose | Classificação | RFE, SMOTE, imputação por mediana | ROC, AUC | Identificou relações clínicas relevantes usando SHAP e XGBoost |
