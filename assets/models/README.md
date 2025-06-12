# Modelos do sistema

* modelo final 1
* modelo final 2

---

# Modelo 1 - Árvore de Decisão

## Bloco 1 - Importação das bibliotecas

```python
import pandas as pd
from sklearn.model_selection import train_test_split, GridSearchCV
from sklearn.tree import DecisionTreeClassifier
from sklearn.metrics import confusion_matrix, classification_report, accuracy_score
import seaborn as sns
import matplotlib.pyplot as plt
````
## Bloco 2 - Carregamento e limpeza de dados

```python
df = pd.read_excel("/content/state of data 1 (1).xlsx", header=[0, 1], engine='openpyxl')

# Selecionar os atributos e o alvo com nomes exatos
colunas_usadas = [
    "('P1_a ', 'Idade')",
    "('P1_b ', 'Genero')",
    "('P2_h ', 'Faixa salarial')",
    "('P2_i ', 'Quanto tempo de experiência na área de dados você tem?')",
    "('P2_r ', 'Atualmente qual a sua forma de trabalho?')",
    "('P1_i_2 ', 'Regiao onde mora')",
    "Investimento em milhões",
    "('P2_g ', 'Nivel')" # alvo
]

df = df[colunas_usadas]

# Renomear as colunas para facilitar o código
df.columns = [
    "Idade", "Genero", "FaixaSalarial", "TempoExperiencia",
    "FormaTrabalho", "Regiao", "Investimento", "Nivel"
]

# Checar valores faltantes
print("Missing values before handling:\n", df.isnull().sum())
print(f"Shape before dropping NaNs: {df.shape}")

# Remover linhas com valores faltantes
df.dropna(inplace=True) # Removes rows with any NaN values

```

## Bloco 3 - Testando e otimizando o modelo

```python
# Separar X (atributos) e y (alvo)
X = df.drop("Nivel", axis=1)
y = df["Nivel"]

# Codificar variáveis categóricas
X_encoded = pd.get_dummies(X)

# Dividir em treino e teste
X_train, X_test, y_train, y_test = train_test_split(
    X_encoded, y, test_size=0.2, random_state=42

# Testar diferentes profundidades 

depths_to_test = range(1, 21) # Profundidades de 1 a 20
accuracy_scores_entropy = [] 
accuracy_scores_entropy_train = []

print("\nTesting different max_depth values for Decision Tree with Entropy criterion:")

for depth in depths_to_test:
    modelo_entropy = DecisionTreeClassifier(
        criterion="entropy",  
        random_state=42,
        class_weight='balanced',
        max_depth=depth,  
        min_samples_split=50, 
        min_samples_leaf=1
    )

    modelo_entropy.fit(X_train, y_train)
    # Calcular acurácias de treino e de teste
    y_pred_entropy = modelo_entropy.predict(X_test)
    acuracia_entropy = accuracy_score(y_test, y_pred_entropy)
    accuracy_scores_entropy.append(acuracia_entropy)
    y_pred_entropy_train = modelo_entropy.predict(X_train)
    acuracia_entropy_train = accuracy_score(y_train, y_pred_entropy_train)
    accuracy_scores_entropy_train.append(acuracia_entropy_train)
```

## Bloco 4 - Otimização com GridSearch

```python
 #Definir os parametros a serem testados
 param_grid = {
     'max_depth': [7, 8, 9, 10], # Profundidades próximas à ideal encontrada
     'min_samples_split': [2, 5, 10, 20, 30, 40, 50],
     'min_samples_leaf': [1, 5, 10, 15, 20] 
 }

 dt = DecisionTreeClassifier(criterion="entropy", random_state=42, class_weight='balanced')

 # Partir a base em 5 (cv=5)
 grid_search = GridSearchCV(estimator=dt, param_grid=param_grid, cv=5, scoring='accuracy', n_jobs=-1)

 grid_search.fit(X_train, y_train)

 print("\nBest parameters found by Grid Search:")
 print(grid_search.best_params_)
 print("Best cross-validation accuracy found by Grid Search:")
 print(grid_search.best_score_) # This is the average cross-validation score

 best_modelo = grid_search.best_estimator_

 # Avaliar o melhor modelo na base de teste intependente
 y_pred_best = best_modelo.predict(X_test)
 acuracia_best = accuracy_score(y_test, y_pred_best)
 print(f"\nAccuracy of the best model (from Grid Search) on the test set: {acuracia_best:.4f}")

```

## Bloco 5 - Visualização final dos resultados

```python

 #Treinar o modelo final com os melhores parâmetros encontrados (por exemplo, usando Entropy, depth 8)
 final_modelo = DecisionTreeClassifier(
      criterion="entropy",
      random_state=42,
      class_weight='balanced',
      max_depth=8,
      min_samples_split=50, # Número ideal encontrado pelo GridSearch
      min_samples_leaf=1 # Número ideal encontrado pelo GridSearch
 )
 final_modelo.fit(X_train, y_train)

 # Fazer previsões com o modelo final
 y_pred_final = final_modelo.predict(X_test)

 # Avaliar o modelo final
 matriz_final = confusion_matrix(y_test, y_pred_final)

 # Visualizar a matriz de confusão do modelo final
 plt.figure(figsize=(8,6))
 sns.heatmap(matriz_final, annot=True, fmt="d", cmap="Blues",
             xticklabels=final_modelo.classes_, yticklabels=final_modelo.classes_)
 plt.xlabel("Previsto")
 plt.ylabel("Real")
 plt.title("Matriz de Confusão (Modelo Final)")
 plt.savefig("confusion_matrix_final.png")
 plt.show()
 files.download("confusion_matrix_final.png")


 # Relatório com métricas do modelo final
 print("\nRelatório de Classificação (Modelo Final):")
 print(classification_report(y_test, y_pred_final))

 # Mostrar acurácia do modelo final
 acuracia_final = accuracy_score(y_test, y_pred_final)
 print(f"\nAcurácia do modelo Final: {acuracia_final:.4f}")
```
*modelo 2 versão preliminaro

```python
from IPython import get_ipython
from IPython.display import display
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
```
### Carregar os dados (substitua pelo seu caminho)
```python
df = pd.read_excel('state_of_data_updated_Limpa.xlsx')
```
### Selecionar features relevantes e target
```python
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
```
### Filtrar dados e remover possíveis NaNs
```python
df_clean = df[features + [target]].dropna()

X = df_clean[features]
y = df_clean[target]
```

### Verificar balanceamento das classes
```python
print("Contagem por classe:")
print(y.value_counts())
```

### Dividir em treino (70%) e teste (30%)
```python
X_train, X_test, y_train, y_test = train_test_split(
    X, y, test_size=0.3, random_state=42
)
```
### Padronizar as features (importante para KNN)
```python
scaler = StandardScaler()
X_train_scaled = scaler.fit_transform(X_train)
X_test_scaled = scaler.transform(X_test)
```
### Definir os valores de k para testar
```python
param_grid = {'n_neighbors': range(1, 21)}
```

### Usar GridSearchCV para encontrar o melhor k
```python
knn = KNeighborsClassifier()
grid_search = GridSearchCV(knn, param_grid, cv=5, scoring='accuracy')
grid_search.fit(X_train_scaled, y_train)
```

### Melhor valor de k
```python
best_k = grid_search.best_params_['n_neighbors']
print(f"\nMelhor valor de k: {best_k}")
```

### Treinar o modelo com o melhor k
```python
best_knn = KNeighborsClassifier(n_neighbors=best_k)
best_knn.fit(X_train_scaled, y_train)
```

### Previsões no conjunto de teste
```python
y_pred_test = best_knn.predict(X_test_scaled)
```

# Métricas de avaliação
```python
accuracy_test = accuracy_score(y_test, y_pred_test)
print(f"\nAcurácia de Teste: {accuracy_test:.2f}")
```

### Calcular a acurácia de treino
```python
y_pred_train = best_knn.predict(X_train_scaled)
accuracy_train = accuracy_score(y_train, y_pred_train)
print(f"Acurácia de Treino: {accuracy_train:.2f}")
```

### Matriz de confusão
```python
conf_matrix = confusion_matrix(y_test, y_pred_test)
print("\nMatriz de Confusão:")
print(conf_matrix)
```

### Relatório de classificação
```python
print("\nRelatório de Classificação:")
print(classification_report(y_test, y_pred_test))
```

### Plot da matriz de confusão
```python
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
```

### Plotar a acurácia vs. k
```python
plt.figure(figsize=(10, 6))
plt.plot(k_values, accuracies, marker='o')
plt.xlabel("Número de Vizinhos (k)")
plt.ylabel("Acurácia")
plt.title("Acurácia do KNN para Diferentes Valores de k")
plt.axvline(x=best_k, color='r', linestyle='--', label=f'Melhor k = {best_k}')
plt.legend()
plt.grid()
plt.show()

```
---
# Modelo 2 Random forest versão final
Abaixo estará disponível a visualização do código de Random forest utilizado no modelo 2, ele estará divido por blocos e com uma explicação de suas features e ferramentas usadas para a criação do mesmo:

## Blocos 1: Importação das Bibliotecas.

```python
# Importando as bibliotecas necessárias
import pandas as pd
import numpy as np
from sklearn.model_selection import train_test_split, GridSearchCV, learning_curve
from sklearn.ensemble import RandomForestClassifier
from sklearn.metrics import accuracy_score, classification_report, confusion_matrix
from sklearn.preprocessing import StandardScaler
from imblearn.over_sampling import SMOTE
import matplotlib.pyplot as plt
from sklearn.feature_selection import SelectFromModel

# Configurando o estilo dos gráficos
plt.style.use('default')

# Configurando warnings e formato de exibição dos números
import warnings
warnings.filterwarnings('ignore')
pd.set_option('display.float_format', lambda x: '%.3f' % x)
```

## Bloco 2: Carregamento e limpeza de dados.

```python


# Carregando e explorando os dados
print("="*50)
print("CARREGAMENTO E ANÁLISE EXPLORATÓRIA DOS DADOS")
print("="*50)

# Carregando os dados do arquivo Excel
print("\n1. Carregando o dataset...")
df = pd.read_excel('state_of_data_updated_Limpa.xlsx')

# Limpando os nomes das colunas
def limpar_nome_coluna(nome):
    # Remove caracteres especiais e espaços extras
    nome = str(nome)
    nome = nome.replace("'", "")
    nome = nome.replace('"', "")
    nome = nome.replace("(", "")
    nome = nome.replace(")", "")
    nome = nome.replace("/", "_")
    nome = nome.replace(" ", "_")
    nome = nome.replace("-", "_")
    nome = nome.replace(".", "")
    nome = nome.replace("?", "")
    nome = nome.replace("!", "")
    nome = nome.replace(",", "")
    nome = nome.replace(":", "")
    nome = nome.replace(";", "")
    nome = nome.replace("@", "at")
    nome = nome.replace("%", "pct")
    nome = nome.strip()
    return nome

# Aplicando a limpeza nos nomes das colunas
df.columns = [limpar_nome_coluna(col) for col in df.columns]

# Mostrando os novos nomes das colunas
print("\nNomes das colunas após limpeza:")
for col in df.columns:
    print(f"- {col}")

# Análise inicial do dataset
print("\n2. Informações gerais do dataset:")
print(f"- Número total de registros: {df.shape[0]}")
print(f"- Número de features: {df.shape[1]}")

# Exibindo as primeiras linhas
print("\n3. Primeiras 5 linhas do dataset:")
display(df.head())

# Estatísticas descritivas das features numéricas
print("\n4. Estatísticas descritivas das features numéricas:")
display(df.describe())

# Verificando valores únicos e distribuição da variável alvo
print("\n5. Distribuição da variável alvo (P2_g__Nivel_Num):")
target_dist = df['P2_g__Nivel_Num'].value_counts(normalize=True).round(3) * 100
print(target_dist, "%")

# Visualização da distribuição da variável alvo
plt.figure(figsize=(10, 6))
plt.hist(df['P2_g__Nivel_Num'], bins=3, rwidth=0.8)
plt.title('Distribuição da Variável Alvo')
plt.xlabel('Nível')
plt.ylabel('Contagem')
plt.show()

# Verificando valores missing
print("\n6. Verificação de valores missing:")
missing_values = df.isnull().sum()
if missing_values.sum() > 0:
    print("\nColunas com valores missing:")
    print(missing_values[missing_values > 0])
else:
    print("Não há valores missing no dataset.")
```

## Bloco 3: Preparação dos dados.

```python
# PREPARAÇÃO DOS DADOS E ENGENHARIA DE FEATURES
print("="*50)
print("PREPARAÇÃO DOS DADOS E ENGENHARIA DE FEATURES")
print("="*50)

# 1. Seleção de Features
print("\n1. Selecionando features numéricas...")
numeric_columns = df.select_dtypes(include=['int64', 'float64']).columns
target_column = 'P2_g__Nivel_Num'  # Ajuste aqui se o nome da coluna alvo for diferente após a limpeza
X = df[numeric_columns].drop(target_column, axis=1) if target_column in numeric_columns else df[numeric_columns]
y = df[target_column]

print("\nFeatures selecionadas para o modelo:")
for col in X.columns:
    print(f"- {col}")

# 2. Divisão treino/teste (20/80)
print("\n2. Dividindo os dados em treino e teste (20/80)...")
X_train, X_test, y_train, y_test = train_test_split(X, y,
                                                test_size=0.8,  # Changed to 0.8 for 80% test
                                                random_state=42,
                                                stratify=y)

# Visualização da divisão dos dados
plt.figure(figsize=(10, 5))
plt.subplot(1, 2, 1)
plt.pie([0.2, 0.8], labels=['Treino (20%)', 'Teste (80%)'], autopct='%1.1f%%') # Updated labels
plt.title('Divisão Treino/Teste')

plt.subplot(1, 2, 2)
train_dist = pd.Series(y_train).value_counts()
test_dist = pd.Series(y_test).value_counts()
width = 0.35
plt.bar(np.arange(len(train_dist)) - width/2, train_dist/len(y_train), width, label='Treino')
plt.bar(np.arange(len(test_dist)) + width/2, test_dist/len(y_test), width, label='Teste')
plt.title('Distribuição das Classes')
plt.xlabel('Classe')
plt.ylabel('Proporção')
plt.legend()
plt.tight_layout()
plt.show()

# 3. Normalização dos dados
print("\n3. Normalizando os dados...")
scaler = StandardScaler()
X_train_scaled = scaler.fit_transform(X_train)
X_test_scaled = scaler.transform(X_test)

# 4. Balanceamento das classes com SMOTE
print("\n4. Aplicando SMOTE para balancear as classes...")
smote = SMOTE(random_state=42)
X_train_balanced, y_train_balanced = smote.fit_resample(X_train_scaled, y_train)

# Visualização do balanceamento
plt.figure(figsize=(10, 5))
plt.subplot(1, 2, 1)
plt.hist(y_train, bins=3, rwidth=0.8)
plt.title('Distribuição Original (Treino)')
plt.xlabel('Nível')
plt.ylabel('Contagem')

plt.subplot(1, 2, 2)
plt.hist(y_train_balanced, bins=3, rwidth=0.8)
plt.title('Distribuição após SMOTE')
plt.xlabel('Nível')
plt.ylabel('Contagem')
plt.tight_layout()
plt.show()

# 5. Seleção de features importantes
print("\n5. Selecionando features mais importantes...")
base_model = RandomForestClassifier(n_estimators=100, random_state=42)
base_model.fit(X_train_balanced, y_train_balanced)

selector = SelectFromModel(base_model, prefit=True)
X_train_selected = selector.transform(X_train_balanced)
X_test_selected = selector.transform(X_test_scaled)

# Resumo das dimensões
print("\nDimensões dos conjuntos de dados após processamento:")
print(f"X_train: {X_train_selected.shape}")
print(f"X_test: {X_test_selected.shape}")

# Features selecionadas
selected_features = X.columns[selector.get_support()].tolist()
print("\nFeatures selecionadas para o modelo:")
for col in selected_features:
    print(f"- {col}")

# Visualização da importância das features
feature_importance = pd.DataFrame({
    'feature': X.columns,
    'importance': base_model.feature_importances_
})
feature_importance = feature_importance.sort_values('importance', ascending=True)

plt.figure(figsize=(10, 6))
plt.barh(range(len(feature_importance)), feature_importance['importance'])
plt.yticks(range(len(feature_importance)), feature_importance['feature'])
plt.xlabel('Importância')
plt.title('Importância das Features')
plt.tight_layout()
plt.show()
```

## Bloco 4: Otimização do Modelo

```python
# TREINAMENTO E OTIMIZAÇÃO DO MODELO
print("="*50)
print("TREINAMENTO E OTIMIZAÇÃO DO MODELO")
print("="*50)

# 1. Definição dos hiperparâmetros para otimização
print("\n1. Configurando grid de hiperparâmetros...")
param_grid = {
    'n_estimators': [200, 300, 400],      # Número de árvores
    'max_depth': [15, 20, 25, 30],        # Profundidade máxima das árvores
    'min_samples_split': [2, 5, 10],      # Número mínimo de amostras para split
    'min_samples_leaf': [1, 2, 4],        # Número mínimo de amostras em folhas
    'class_weight': ['balanced', 'balanced_subsample'],  # Pesos das classes
    'max_features': ['sqrt', 'log2']       # Número de features a considerar
}

# 2. Criação e configuração do modelo base
print("\n2. Criando modelo base...")
rf_base = RandomForestClassifier(random_state=42, n_jobs=-1)

# 3. Configuração e execução do GridSearchCV
print("\n3. Iniciando busca em grade com validação cruzada...")
grid_search = GridSearchCV(
    estimator=rf_base,
    param_grid=param_grid,
    cv=5,                  # 5-fold cross-validation
    scoring='accuracy',    # Métrica para otimização
    n_jobs=-1,            # Usar todos os cores disponíveis
    verbose=1             # Mostrar progresso
)

# 4. Treinamento com GridSearchCV
print("\n4. Treinando modelo com os melhores parâmetros...")
grid_search.fit(X_train_selected, y_train_balanced)

# 5. Obtendo e exibindo os melhores parâmetros
rf_model = grid_search.best_estimator_
print("\nMelhores parâmetros encontrados:")
for param, value in grid_search.best_params_.items():
    print(f"{param}: {value}")

# 6. Gerando previsões
print("\n5. Gerando previsões...")
y_train_pred = rf_model.predict(X_train_selected)
y_test_pred = rf_model.predict(X_test_selected)

# 7. Plotando curva de aprendizado
print("\n6. Gerando curva de aprendizado...")
train_sizes, train_scores, test_scores = learning_curve(
    rf_model, X_train_selected, y_train_balanced,
    cv=5, n_jobs=-1, train_sizes=np.linspace(0.1, 1.0, 10)
)

train_mean = np.mean(train_scores, axis=1)
train_std = np.std(train_scores, axis=1)
test_mean = np.mean(test_scores, axis=1)
test_std = np.std(test_scores, axis=1)

plt.figure(figsize=(10, 6))
plt.plot(train_sizes, train_mean, label='Treino', color='blue', marker='o')
plt.fill_between(train_sizes, train_mean - train_std, train_mean + train_std, alpha=0.15, color='blue')
plt.plot(train_sizes, test_mean, label='Validação', color='green', marker='o')
plt.fill_between(train_sizes, test_mean - test_std, test_mean + test_std, alpha=0.15, color='green')
plt.xlabel('Tamanho do Conjunto de Treino')
plt.ylabel('Acurácia')
plt.title('Curva de Aprendizado')
plt.legend(loc='lower right')
plt.grid(True)
plt.show()
```
## Bloco 5: Avaliação do Modelo.

```python
# AVALIAÇÃO E VISUALIZAÇÃO DOS RESULTADOS
print("="*50)
print("AVALIAÇÃO E VISUALIZAÇÃO DOS RESULTADOS")
print("="*50)

def plot_confusion_matrix(y_true, y_pred, title):
    """
    Plota uma matriz de confusão usando matplotlib
    """
    cm = confusion_matrix(y_true, y_pred)
    plt.figure(figsize=(10, 8))
    plt.imshow(cm, interpolation='nearest', cmap=plt.cm.Blues)
    plt.title(f'Matriz de Confusão - {title}')
    plt.colorbar()

    # Adiciona os valores na matriz
    thresh = cm.max() / 2.
    for i in range(cm.shape[0]):
        for j in range(cm.shape[1]):
            plt.text(j, i, format(cm[i, j], 'd'),
                    ha="center", va="center",
                    color="white" if cm[i, j] > thresh else "black")

    plt.ylabel('Real')
    plt.xlabel('Previsto')
    plt.tight_layout()
    plt.show()

def plot_classification_report(y_true, y_pred, title):
    """
    Cria uma visualização do classification report usando matplotlib
    """
    report = classification_report(y_true, y_pred, output_dict=True)
    report_df = pd.DataFrame(report).transpose()

    plt.figure(figsize=(10, 6))
    plt.imshow(report_df.iloc[:-1, :].astype(float), cmap=plt.cm.RdYlGn, aspect='auto')
    plt.colorbar()

    # Adiciona os valores na matriz
    for i in range(len(report_df.index[:-1])):
        for j in range(len(report_df.columns)):
            text = f'{report_df.iloc[i, j]:.3f}'
            plt.text(j, i, text, ha="center", va="center")

    plt.xticks(range(len(report_df.columns)), report_df.columns)
    plt.yticks(range(len(report_df.index[:-1])), report_df.index[:-1])
    plt.title(f'Classification Report - {title}')
    plt.tight_layout()
    plt.show()

def display_metrics(y_true, y_pred, title):
    """
    Função principal para exibir todas as métricas e visualizações
    """
    print(f"\n{'-'*20} {title} {'-'*20}")

    # 1. Acurácia
    acc = accuracy_score(y_true, y_pred)
    print(f"\n1. Acurácia: {acc:.4f}")

    # 2. Classification Report textual
    print("\n2. Classification Report detalhado:")
    print(classification_report(y_true, y_pred))

    # 3. Matriz de Confusão
    print("\n3. Gerando Matriz de Confusão...")
    plot_confusion_matrix(y_true, y_pred, title)

    # 4. Classification Report Visual
    print("\n4. Gerando Classification Report Visual...")
    plot_classification_report(y_true, y_pred, title)

# Avaliando resultados no conjunto de treino
print("\nAVALIANDO RESULTADOS NO CONJUNTO DE TREINO")
display_metrics(y_train_balanced, y_train_pred, "Conjunto de Treino")

# Avaliando resultados no conjunto de teste
print("\nAVALIANDO RESULTADOS NO CONJUNTO DE TESTE")
display_metrics(y_test, y_test_pred, "Conjunto de Teste")

# Resumo final
print("\nRESUMO FINAL DO MODELO")
print("="*50)
print(f"Acurácia no treino: {accuracy_score(y_train_balanced, y_train_pred):.4f}")
print(f"Acurácia no teste: {accuracy_score(y_test, y_test_pred):.4f}")
print("\nObservações importantes:")
print("1. Diferença entre acurácia de treino e teste indica o nível de overfitting")
print("2. Matriz de confusão mostra onde o modelo mais acerta/erra")
print("3. Classification report fornece métricas detalhadas por classe")
```
Bloco 6: Analise e importancia das features.

```python
import pandas as pd
import matplotlib.pyplot as plt
from sklearn.metrics import confusion_matrix
# ANÁLISE FINAL DAS FEATURES E IMPORTÂNCIA
print("="*50)
print("ANÁLISE FINAL DAS FEATURES E IMPORTÂNCIA")
print("="*50)

# 1. Criando DataFrame com importância das features e formatando nomes
feature_importance = pd.DataFrame({
    'feature': [limpar_nome_coluna(feat) for feat in selected_features],
    'importance': rf_model.feature_importances_
})
feature_importance = feature_importance.sort_values('importance', ascending=False)

# Criando um dicionário para mapear nomes formatados para nomes mais legíveis
nome_legivel = {col: col.replace('_', ' ').title() for col in feature_importance['feature']}

# 2. Visualização da importância das features
plt.figure(figsize=(12, 8))
plt.barh(range(len(feature_importance)), feature_importance['importance'])
plt.yticks(range(len(feature_importance)), feature_importance['feature'])
plt.title('Importância das Features no Modelo Final')
plt.xlabel('Importância Relativa')
plt.ylabel('Features')
plt.tight_layout()
plt.show()

# 3. Análise detalhada das top 5 features mais importantes
print("\nAnálise detalhada das top 5 features mais importantes:")
top_5_features = feature_importance.head()
for idx, row in top_5_features.iterrows():
    print(f"\n{row['feature']}:")
    print(f"- Importância relativa: {row['importance']:.4f}")
    print(f"- Contribuição percentual: {(row['importance']/feature_importance['importance'].sum()*100):.2f}%")

# 4. Estatísticas das features numéricas selecionadas
print("\nEstatísticas descritivas das features selecionadas:")
selected_stats = df[selected_features].describe()
display(selected_stats)

# 5. Correlação entre as features selecionadas
plt.figure(figsize=(12, 8))
correlation_matrix = df[selected_features].corr()
plt.imshow(correlation_matrix, cmap=plt.cm.coolwarm, aspect='auto')
plt.colorbar()

# Adiciona os valores na matriz de correlação
for i in range(correlation_matrix.shape[0]):
    for j in range(correlation_matrix.shape[1]):
        plt.text(j, i, f'{correlation_matrix.iloc[i, j]:.2f}',
                ha='center', va='center')

plt.xticks(range(len(selected_features)), selected_features, rotation=45, ha='right')
plt.yticks(range(len(selected_features)), selected_features)
plt.title('Matriz de Correlação das Features Selecionadas')
plt.tight_layout()
plt.show()

# 6. Resumo final das features
print("\nRESUMO FINAL DAS FEATURES")
print("="*50)
print(f"Número total de features originais: {len(X.columns)}")
print(f"Número de features selecionadas: {len(selected_features)}")
print(f"Redução de dimensionalidade: {((len(X.columns) - len(selected_features))/len(X.columns)*100):.2f}%")
print("\nObservações sobre as features:")
print("1. As features mais importantes indicam os principais fatores preditivos")
print("2. A correlação entre features pode indicar redundância de informação")
print("3. A redução de dimensionalidade ajuda a evitar overfitting")
```
Bloco 7:

```python
# Visualização da Importância das Features
feature_importance = pd.DataFrame({
    'feature': selected_features,
    'importance': rf_model.feature_importances_
})
feature_importance = feature_importance.sort_values('importance', ascending=False)

# Criando o gráfico de barras com matplotlib
plt.figure(figsize=(12, 6))
plt.barh(range(len(feature_importance)), feature_importance['importance'])
plt.yticks(range(len(feature_importance)), feature_importance['feature'])
plt.xlabel('Importância')
plt.title('Importância das Features Selecionadas')
plt.tight_layout()
plt.show()

# Imprimindo importância das features
print("\nImportância das features selecionadas:")
for idx, row in feature_importance.iterrows():
    print(f"{row['feature']}: {row['importance']:.4f}")

# Imprimindo métricas finais
print("\nMétricas finais do modelo otimizado:")
print(f"Acurácia no conjunto de treino: {accuracy_score(y_train_balanced, y_train_pred):.4f}")
print(f"Acurácia no conjunto de teste: {accuracy_score(y_test, y_test_pred):.4f}")

```

Bloco 8: 

```python
from sklearn.model_selection import GridSearchCV

# Definindo os parâmetros para otimização
param_grid = {
    'n_estimators': [100, 200, 300],
    'max_depth': [10, 20, 30, None],
    'min_samples_split': [2, 5, 10],
    'min_samples_leaf': [1, 2, 4],
    'max_features': ['sqrt', 'log2']
}

# Criando o objeto GridSearchCV
grid_search = GridSearchCV(
    estimator=RandomForestClassifier(random_state=None),
    param_grid=param_grid,
    cv=5,
    n_jobs=-1,
    verbose=2,
    scoring='accuracy'
)

# Executando a busca
grid_search.fit(X_train, y_train)

# Imprimindo os melhores parâmetros
print("Melhores parâmetros:", grid_search.best_params_)
print("Melhor score:", grid_search.best_score_)

```




