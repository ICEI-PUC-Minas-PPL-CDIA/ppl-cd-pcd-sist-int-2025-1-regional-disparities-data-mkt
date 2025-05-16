# Modelos do sistema

* modelo final 1
* modelo final 2

---
* Modelo 2(Versão Preliminar):

import pandas as pd
import numpy as np
from sklearn.model_selection import train_test_split, GridSearchCV
from sklearn.preprocessing import StandardScaler
from sklearn.neighbors import KNeighborsClassifier
from sklearn.metrics import (
    accuracy_score,
    confusion_matrix,
    classification_report,
    f1_score,
)
import matplotlib.pyplot as plt
import seaborn as sns

# Carregar os dados (substitua pelo seu caminho)
df = pd.read_excel('state_of_data_updated_Limpa.xlsx')

# Selecionar features relevantes e target
features = [
    'Investimento em milhões',
    "('P1_a ', 'Idade')",  # Idade
    "('P1_b ', 'Genero')_Num",  # Gênero (codificado)
    "('P1_c ', 'Cor/raca/etnia')_Num",  # Raça/Etnia (codificado)
    "('P1_l ', 'Nivel de Ensino')_Num",  # Nível de Ensino (codificado)
    "('P2_a ', 'Qual sua situação atual de trabalho?')_Num",  # Situação de trabalho
    "('P2_h ', 'Faixa salarial')_Num",  # Faixa salarial
    "('P2_i ', 'Quanto tempo de experiência na área de dados você tem?')_Num",  # Experiência
    "('P2_r ', 'Atualmente qual a sua forma de trabalho?')_Num"  # Modelo de trabalho
]

target = "('P2_g ', 'Nivel')"  # Nível (Júnior=0, Pleno=1, Sênior=2)

# Filtrar dados e remover possíveis NaNs
df_clean = df[features + [target]].dropna()

X = df_clean[features]
y = df_clean[target]

# Verificar balanceamento das classes
print("Contagem por classe:")
print(y.value_counts())

# Dividir em treino (70%) e teste (30%)
X_train, X_test, y_train, y_test = train_test_split(
    X, y, test_size=0.3, random_state=42
)

# Padronizar as features (importante para KNN)
scaler = StandardScaler()
X_train_scaled = scaler.fit_transform(X_train)
X_test_scaled = scaler.transform(X_test)

# Definir os valores de k para testar
param_grid = {'n_neighbors': range(1, 21)}

# Usar GridSearchCV para encontrar o melhor k
knn = KNeighborsClassifier()
grid_search = GridSearchCV(knn, param_grid, cv=5, scoring='accuracy')
grid_search.fit(X_train_scaled, y_train)

# Melhor valor de k
best_k = grid_search.best_params_['n_neighbors']
print(f"\nMelhor valor de k: {best_k}")

# Treinar o modelo com o melhor k
best_knn = KNeighborsClassifier(n_neighbors=best_k)
best_knn.fit(X_train_scaled, y_train)

# Previsões no conjunto de teste
y_pred = best_knn.predict(X_test_scaled)

# Métricas de avaliação
accuracy = accuracy_score(y_test, y_pred)
print(f"\nAcurácia: {accuracy:.2f}")

# Matriz de confusão
conf_matrix = confusion_matrix(y_test, y_pred)
print("\nMatriz de Confusão:")
print(conf_matrix)

# Relatório de classificação
print("\nRelatório de Classificação:")
print(classification_report(y_test, y_pred))

# Plot da matriz de confusão
plt.figure(figsize=(8, 6))
sns.heatmap(
    conf_matrix,
    annot=True,
    fmt="d",
    cmap="Blues",
    xticklabels=["Júnior", "Pleno", "Sênior"],
    yticklabels=["Júnior", "Pleno", "Sênior"],
)
plt.xlabel("Predito")
plt.ylabel("Real")
plt.title("Matriz de Confusão - KNN")
plt.show()

# Testar diferentes valores de k para visualização
k_values = range(1, 21)
accuracies = []

for k in k_values:
    knn_temp = KNeighborsClassifier(n_neighbors=k)
    knn_temp.fit(X_train_scaled, y_train)
    y_pred_temp = knn_temp.predict(X_test_scaled)
    accuracies.append(accuracy_score(y_test, y_pred_temp))

# Plotar a acurácia vs. k
plt.figure(figsize=(10, 6))
plt.plot(k_values, accuracies, marker='o')
plt.xlabel("Número de Vizinhos (k)")
plt.ylabel("Acurácia")
plt.title("Acurácia do KNN para Diferentes Valores de k")
plt.axvline(x=best_k, color='r', linestyle='--', label=f'Melhor k = {best_k}')
plt.legend()
plt.grid()
plt.show()

---

O código pode estar no formato original da ferramenta utilizada. 
Pode ser um processo do Orange ou um Jupyter Notebook.
