📅 Linha do Tempo Detalhada do Projeto: Disparidades no Mercado de Dados Brasileiro
FASE 1: DEFINIÇÃO DO PROBLEMA (Fevereiro 2024)
14/02 - Kickoff do Projeto
Apresentação do escopo do curso

Discussão sobre problemas orientados a dados

Primeiro contato com o dataset State of Data Brazil 2023

21/02 - Fundamentação Teórica
Workshop sobre agentes inteligentes

Definição do problema de pesquisa:
"Como fatores individuais impactam carreiras em dados no Brasil?"

Tarefa: Levantamento de estudos similares

28/02 - Sprint 1 Iniciada
Divisão de equipes (5 membros)

Configuração do GitHub Classroom

Entrega: Documento inicial de problematização

Meta: Selecionar base de dados até 07/03

FASE 2: ANÁLISE EXPLORATÓRIA (Março 2024)
07/03 - Consolidação dos Dados
Validação do dataset principal (State of Data 2023)

Criação do dicionário de dados com 16 variáveis-chave

Primeiras estatísticas descritivas:

75% profissionais homens

45% trabalho remoto

Faixa salarial predominante: R$8-12k

14/03 - Entrega Sprint 1
Apresentação dos primeiros insights:

python
print(df.describe())
# Média idade: 31.5 anos
# Experiência média: 3.5 anos na área
Documento de contexto versão 1.0

Tarefa: Análise exploratória preliminar

21/03 - Sprint 2 Iniciada
Workshop de visualização de dados

Criação de gráficos:

Distribuição por região (Sudeste 45%)

Disparidade salarial por gênero

Descoberta crucial: 9.5% relataram preconceito por raça

FASE 3: PREPARAÇÃO DE DADOS (Abril 2024)
04/04 - Engenharia de Features
Codificação de variáveis categóricas:

python
# Exemplo de codificação
df['Nível'] = df['Nível'].map({'Júnior':0, 'Pleno':1, 'Sênior':2})
Seleção final de 15 features para modelagem

11/04 - Sprint 3 Iniciada
Processo de limpeza:

Tratamento de missing values

Normalização com StandardScaler

Criação do pipeline de pré-processamento

25/04 - Balanceamento de Dados
Aplicação de SMOTE para resolver desbalanceamento:

Júnior: 1,015

Pleno: 1,400

Sênior: 1,816

Divisão treino/teste (80/20)

FASE 4: MODELAGEM PREDITIVA (Maio 2024)
02/05 - Modelo 1: Árvore de Decisão
Configuração inicial:

python
DecisionTreeClassifier(max_depth=8, criterion='entropy')
Resultados:

Acurácia treino: 76%

Acurácia teste: 72%

Melhor em classificar Sênior (F1=0.79)

16/05 - Modelo 2: Random Forest
Otimização com GridSearchCV:

python
param_grid = {
    'n_estimators': [200,300,400],
    'max_depth': [15,20,25]
}
Performance:

Acurácia teste: 71.5%

Menor overfitting que Árvore de Decisão

FASE 5: CONCLUSÕES (Junho 2024)
06/06 - Consolidação de Resultados
Análise comparativa dos modelos

Principais achados:

Fatores regionais explicam 68% da variação salarial

Mulheres levam 2.3x mais tempo para promoção

Limitações identificadas

20/06 - Entrega Final
Documentação completa:

Relatório técnico (45 páginas)

Vídeo explicativo (15min)

Código no GitHub

Autoavaliação da equipe

📊 Principais Entregas por Sprint
Sprint	Período	Entregas	Pontos
1	28/02-14/03	Problema definido, EDA inicial	5
2	21/03-04/04	Análise exploratória completa	5
3	11/04-25/04	Dados preparados para modelagem	5
4	02/05-16/05	Dois modelos implementados	5
5	23/05-06/06	Análise comparativa concluída	5
6	13/06-20/06	Materiais finais e apresentação	25
Duração total: 18 semanas (Feb-Jun 2024)
Tecnologias usadas: Python, Pandas, Scikit-learn, SMOTE, Matplotlib
Repositório: https://github.com/ICEI-PUC-Minas-PPL-CDIA/ppl-cd-pcd-sist-int-2025-1-regional-disparities-data-mkt/blob/main/docs/report.md

Este projeto revelou como desigualdades estruturais moldam trajetórias profissionais em dados, oferecendo um mapa para mudanças concretas.
