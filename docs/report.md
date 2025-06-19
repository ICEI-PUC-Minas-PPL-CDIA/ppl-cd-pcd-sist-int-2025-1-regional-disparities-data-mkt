#  Diferenças no mercado de Ciência de Dados do Brasil a nível de indivíduo.  
  
Alunos: 
Álvaro Oliveira Soares de Souza - alvaro.souza.1213824@sga.pucminas.br

Guilherme Amintas Lopes Magalhaes - guilherme.amintas@sga.pucminas.br 

Izabela Dobscha Santos Borges - idsborges@sga.pucminas.br

Luiz Eduardo Araújo de Medeiros - leamedeiros@sga.pucminas.br 

Walker Junio Gonzaga Rocha - walker.gonzaga@sga.pucminas.br    

---

Professores:

* Prof. Hugo Bastos de Paula.  
* Prof. Hayala Nepomuceno Curto.  

---

_Curso de Ciência de Dados, Unidade Praça da Liberdade_

_Instituto de Informática e Ciências Exatas – Pontifícia Universidade de Minas Gerais (PUC MINAS), Belo Horizonte – MG – Brasil_

---

##  Índice

- [Resumo](#resumo)
- [Introdução](#introdução)
- [Contextualização](#contextualização)
- [Problema](#problema)
- [Objetivo Geral](#objetivo-geral)
- [Objetivos Específicos](#objetivos-específicos)
- [Justificativas](#justificativas)
- [Público Alvo](#público-alvo)
- [Análise Exploratória dos Dados](#análise-exploratória-dos-dados)
  - [1. Introdução](#1-introdução)
  - [2. Atributos Analisados (Dicionário de Dados)](#2-atributos-analisados-dicionário-de-dados)
  - [3. Estatísticas Descritivas](#3-estatísticas-descritivas)
  - [4. Principais Insights](#4-principais-insights)
  - [5. Gráficos Adicionais](#5-gráficos-adicionais)
- [Preparação dos Dados](#preparação-dos-dados)
- [Tabela de Variáveis e Codificações](#tabela-de-variáveis-e-codificações)
- [Indução de Modelos](#indução-de-modelos)
  - [Modelo 1: Classificação com Árvore de Decisão](#modelo-1-classificação-com-árvore-de-decisão)
  - [Modelo 2: Random Forest](#modelo-2-random-forest)
- [Treinamento e Otimização do Modelo](#treinamento-e-otimização-do-modelo)
- [Análise Comparativa dos Modelos](#análise-comparativa-dos-modelos)
- [Conclusão](#conclusão)
- [Apêndices](#apêndices)

---

### Resumo

Este estudo analisa como fatores individuais (formação, habilidades técnicas e socioeconômicos) impactam carreiras em dados no Brasil, utilizando o State of Data 2023 como base principal. Aplicando métodos estatísticos, identificaremos:

-Quais habilidades mais influenciam salários e empregabilidade

-Como diferentes trajetórias de capacitação (graduação, cursos livres) afetam a progressão

-Barreiras enfrentadas por grupos sub-representados

Os resultados fornecerão um guia prático para profissionais e instituições, promovendo maior equidade no mercado de dados brasileiro. 

---

## Introdução

Apesar do crescimento acelerado do mercado de dados no Brasil, as oportunidades e trajetórias profissionais nessa área são profundamente desiguais, influenciadas não apenas por fatores econômicos e regionais, mas também por características individuais, como formação acadêmica. Enquanto alguns profissionais conseguem ascender rapidamente a cargos bem remunerados em empresas inovadoras, outros enfrentam barreiras persistentes, mesmo possuindo qualificações aparentemente similares. Essas disparidades sugerem que, além das dinâmicas macro do mercado, aspectos individuais desempenham um papel crucial na definição do sucesso profissional em ciência de dados.

Este estudo busca investigar como variáveis a nível individual—como formação educacional, habilidades técnicas (ex: domínio de Python, machine learning), competências não técnicas (ex: comunicação, resolução de problemas), participação em bootcamps ou cursos extracurriculares, e acesso a mentorias—impactam:

Remuneração: Diferenças salariais entre profissionais com perfis semelhantes, mas trajetórias distintas;

Empregabilidade: Velocidade de inserção no mercado e acesso a vagas de alto valor agregado;

Progressão de carreira: Fatores que aceleram (ou limitam) a ascensão a cargos sênior e de liderança.

Ao focar no nível individual, esta pesquisa visa não apenas entender as desigualdades no mercado de dados, mas também fornecer ferramentas práticas para que profissionais possam navegar e superar barreiras em suas carreiras—independentemente de seu contexto regional ou socioeconômico inicial.

---

###    Contextualização

O mercado de dados no Brasil vive um momento de expansão, aimpulsionado pelo uso de tecnologias como inteligência artificial, machine learning e análise de big data. No entanto, por trás dessa demanda aquecida por profissionais qualificados, há uma realidade desigual: as oportunidades e trajetórias na área são profundamente moldadas por fatores individuais, como formação acadêmica, habilidades técnicas e comportamentais, acesso a redes profissionais e condições socioeconômicas.

Enquanto alguns cientistas de dados conseguem alcançar salários elevados e posições estratégicas em poucos anos, outros, mesmo com qualificações técnicas semelhantes, enfrentam dificuldades para ingressar no mercado ou progredir na carreira. Essa disparidade não se explica apenas por diferenças regionais (como a concentração de vagas no Sudeste), mas também por barreiras individuais, como:

- Divisão técnica: Profissionais com domínio em ferramentas avançadas (ex: PySpark, TensorFlow) têm salários até 35% superiores à média (Pesquisa Stack Overflow, 2023), mas muitos não têm acesso a capacitação nessas tecnologias.

- Networking e viés de contratação: 60% das vagas são preenchidas por indicação (LinkedIn, 2023), privilegiando quem já está inserido em ambientes corporativos da área tecnológica.

- Educação formal vs. cursos alternativos: Profissionais com pós-graduação têm 20% mais chances de alcançar cargos sênior, mas bootcamps e certificações podem acelerar a entrada no mercado para quem não tem diploma na área (Data Science Academy, 2023).

Além disso, habilidades não técnicas—como comunicação, pensamento crítico e capacidade de traduzir dados em decisões, são frequentemente subestimadas, mas determinam até 40% da progressão para cargos de liderança (Harvard Business Review, 2022).

Nesse cenário, este estudo busca entender como variáveis individuais—e não apenas macroeconômicas ou regionais—influenciam:

-A disparidade salarial entre profissionais com habilidades técnicas equivalentes;

-O acesso a oportunidades em empresas de ponta vs. barreiras impostas por falta de networking ou viés de seleção;

-A velocidade de crescimento na carreira, analisando o peso de pós-graduações, cursos livres e experiências práticas.

-Quais combinações de habilidades (técnicas e comportamentais) têm maior impacto em cada estágio da carreira;

-O papel de certificações alternativas na competitividade do profissional;

-Como as condições (background) socioeconômicas influenciam o acesso à capacitação e à empregabilidade.

Os resultados visam orientar tanto profissionais (em estratégias personalizadas de qualificação) quanto empresas e instituições de ensino (na redução de vieses e adaptação de programas de treinamento). O objetivo final é democratizar as oportunidades em dados, garantindo que o potencial da área seja acessível não apenas a quem está nos polos tradicionais ou tem determinados privilégios iniciais, mas a todos os talentos—independentemente de sua origem ou trajetória prévia.

---

###    Problema

*Pergunta orientada a dados: Como o nível profissional do indivíduo afeta o mercado de trabalho de Ciência de Dados?*

O crescimento do mercado de ciência de dados no Brasil, embora promissor, é marcado por disparidades significativas no nível individual, onde fatores como formação, habilidades, acesso a networking e condições socioeconômicas determinam quem consegue ingressar, progredir e se manter competitivo na área. Enquanto alguns profissionais alcançam cargos bem remunerados e oportunidades em empresas inovadoras, outros—mesmo com qualificações técnicas semelhantes—enfrentam barreiras persistentes devido a:

*Desigualdades Estruturais no Nível Individual*

- Divisão de habilidades: Profissionais com domínio em ferramentas avançadas (MLOps, engenharia de dados) têm salários até 50% maiores, mas muitos não têm acesso a capacitação nessas tecnologias (Stack Overflow, 2023).

- Networking e viés de contratação: 60% das vagas são preenchidas por indicação (LinkedIn, 2023), excluindo quem não está inserido em ambientes corporativos da área tecnológica.

- Educação formal vs. alternativas: Pós-graduação aumenta em 30% as chances de alcançar cargos sênior, mas bootcamps e certificações são a única via para muitos sem diploma na área (Data Science Academy, 2023).

- Habilidades não técnicas negligenciadas: Competências como comunicação e storytelling impactam 40% das promoções (Harvard Business Review, 2022), mas são pouco desenvolvidas em cursos técnicos.

*Impactos Diretos na Carreira:*

Para profissionais:

- Iniciantes sem acesso a mentorias ou cursos especializados levam 2x mais tempo para conseguir o primeiro emprego na área.

- Quem não domina inglês ou ferramentas em alta demanda (ex: LLMs, cloud) fica excluído de vagas globais e bem remuneradas.

- Profissionais de grupos sub-representados (mulheres, negros, periféricos) enfrentam maior dificuldade para alcançar cargos de liderança.

Para empresas e instituições:

- Empresas perdem talentos qualificados por não identificarem potenciais além do currículo tradicional.

- Instituições de ensino formam profissionais desalinhados com demandas reais do mercado, gerando desemprego técnico.

*Lacuna Crítica*

Não existe hoje um sistema que analise como variáveis individuais, e não apenas regionais, impactam:

-A disparidade salarial entre profissionais com habilidades equivalentes;

-O acesso a oportunidades em empresas de ponta vs. barreiras impostas por falta de networking;

-A efetividade de diferentes rotas de capacitação (graduação, bootcamps, cursos livres).

*Solução Proposta:*

Um modelo analítico baseado em dados individuais que cruze:

- Perfis profissionais → Quais experiências levam a melhores salários e empregabilidade.

- Pesquisas salariais e de recrutamento → Viéses de contratação e gaps de competências.

- Trajetórias de sucesso → Rotas alternativas de capacitação (ex.: certificações X pós-graduação).

*Objetivo final:*

Para profissionais: Identificar as habilidades e estratégias mais eficazes para sua realidade.

Para empresas: Reduzir vieses e encontrar talentos subutilizados.

Para instituições de ensino: Adaptar currículos às demandas do mercado.

---

###    Objetivo geral

Desenvolver um modelo analítico baseado no State of Data Brazil 2023 para identificar e mensurar como fatores individuais (formação, habilidades técnicas e comportamentais, background socioeconômico e acesso a networking) influenciam as disparidades de oportunidades, remuneração e progressão de carreira no mercado brasileiro de ciência de dados.

###   Objetivos Específicos

*1-Mapear o perfil individual dos profissionais*

- Analisar a distribuição de formação acadêmica (STEM vs não-STEM), modalidades de capacitação (graduação, pós, cursos livres) e sua correlação com níveis salariais;

- Avaliar o impacto de fatores socioeconômicos.

*2-Mensurar como variáveis como gênero, raça, região de origem e tipo de instituição de formação afetam:*

- Tempo para ingresso no mercado;

- Acesso a oportunidades em empresas de elite.

---

###    Justificativas

A investigação sobre como fatores individuais impactam a carreira de cientistas de dados no Brasil justifica-se por três questões críticas:

*1. Desigualdade Oportunidades Ocultas*

Dados do State of Data Brazil 2023 revelam que:

-Profissionais com formação em STEM (Ciência, Tecnologia, Engenharia e Matemática) têm 30% mais chances de alcançar cargos sênior;

-Quem domina inglês avançado recebe propostas até 50% melhores em empresas globais;

-Mulheres e negros ocupam apenas 25% dos cargos de liderança em dados, mesmo com qualificação equivalente.

Essas disparidades não são explicadas apenas por competência técnica, mas por barreiras invisíveis: acesso a networking, viés em processos seletivos e falta de mentoria.

*2. Capacitação Desalinhada com o Mercado*

-62% dos profissionais aprendem ferramentas por conta própria (cursos online, bootcamps), mas muitos não sabem quais habilidades priorizar para crescer na carreira;

-Empresas  precisam de profissionais que possuem habilidades não técnicas (comunicação, gestão), mas poucos cursos focam nisso;

-Quem vem de instituições menos prestigiadas ou regiões periféricas enfrenta dificuldades para ser reconhecido, mesmo com conhecimento equivalente.

*3. Falta de Dados para Decisões Estratégicas*

Não há sistemas que cruzem:

- Perfil individual → Habilidades mais valorizadas no mercado;

- Trajetórias alternativas → Como profissionais sem diploma tradicional alcançaram sucesso;

- Barreiras socioeconômicas → Quais fatores (além da técnica) impedem a progressão.

Isso prejudica:

- Profissionais: Escolhem capacitações que não trazem retorno financeiro ou oportunidades reais;

- Empresas: Perdem talentos qualificados por focarem apenas em currículos tradicionais;

- Instituições de ensino: Não adaptam cursos às demandas reais do mercado.

Impacto Social

Este estudo visa transformar dados em ações práticas:

 Para profissionais:

-Identificar quais habilidades (técnicas e comportamentais) priorizar;

-Mostrar rotas alternativas de capacitação com base em trajetórias reais de sucesso;

-Ajudar grupos sub-representados a superar barreiras de acesso.

 Para empresas:

-Reduzir vieses em contratações e valorizar habilidades além do diploma;

-Criar programas de mentoria para talentos em início de carreira.

---

##    Público alvo

Este estudo tem como público-alvo profissionais em diferentes estágios da carreira em ciência de dados no Brasil, cujas trajetórias são profundamente influenciadas por seu perfil individual e condições de acesso a oportunidades. Nosso foco principal são iniciantes que enfrentam dificuldades para entrar no mercado devido à falta de experiência prática e orientação sobre quais habilidades priorizar; profissionais em transição de carreira, que precisam validar seus conhecimentos sem formação tradicional na área; e trabalhadores subempregados, que mesmo atuando com análise de dados não conseguem alcançar posições melhor remuneradas. Também damos atenção especial a grupos sub-representados, como mulheres, negros e pessoas de baixa renda, que enfrentam barreiras adicionais no acesso a ecossistemas tech qualificados e processos seletivos. A pesquisa visa fornecer a esses grupos dados concretos sobre as habilidades mais valorizadas pelo mercado, estratégias eficazes de capacitação e cases de sucesso que possam servir como referência, ajudando a transformar a ciência de dados em uma carreira mais acessível e democrática. Ao cruzar informações sobre trajetórias reais de profissionais com diferentes backgrounds, buscamos criar um guia prático que mostre não apenas o caminho ideal, mas as múltiplas rotas possíveis para o sucesso na área, considerando as diversas realidades existentes no país.

---
## Análise exploratórida dos dados


##  1. Introdução
O projeto utiliza o dataset da planilha unificada da State_of_data_2023 com Microdados(MCTI) como principal fonte de dados, que relaciona os estados brasileiros com o mercado de dados, incluindo informações sobre investimentos, características demográficas dos profissionais e condições de trabalho.

##  2. Atributos Analisados (Dicionário de Dados)

| Atributo | Descrição | Escala do Dado | Tipo de Dado |
|----------|-----------|----------------|--------------|
| ESTADO | Estado brasileiro onde o profissional atua | Nominal | Texto (Categórico) |
| INVESTIMENTO EM MILHÕES | Valor investido no estado (em milhões de R$) | Contínuo | Float |
| IDADE | Idade dos participantes em anos completos | Discreta | Inteiro |
| GÊNERO | Identificação de gênero (Masculino, Feminino, etc.) | Nominal | Texto (Categórico) |
| REGIÃO ONDE MORA | Região geográfica do Brasil | Nominal | Texto (Categórico) |
| MUDOU DE ESTADO | Se já mudou de estado (0 = Não, 1 = Sim) | Nominal | Inteiro (Binário) |
| NÍVEL DE ENSINO | Grau de escolaridade | Ordinal | Texto (Ordinal) |
| SITUAÇÃO DE TRABALHO | Situação atual de emprego | Nominal | Texto (Categórico) |
| NÍVEL | Nível profissional (Júnior, Pleno, Sênior) | Ordinal | Texto (Ordinal) |
| FAIXA SALARIAL | Faixa de remuneração mensal | Ordinal | Texto (Ordinal) |
| TEMPO NA ÁREA DE DADOS | Anos de experiência na área | Discreta | Texto (Ordinal) |
| PRETENDE MUDAR DE EMPREGO | Intenção de mudança em 6 meses | Nominal | Texto (Categórico) |
| FORMA DE TRABALHO | Modalidade de trabalho (Remoto, Híbrido, Presencial) | Nominal | Texto (Categórico) |
| COR/RAÇA/ETNIA | Autoidentificação racial/étnica | Nominal | Texto (Categórico) |
| EXPERIÊNCIA PROFISSIONAL AFETADA | Percepção sobre impacto na experiência | Nominal | Inteiro (Binário) |
| EXPERIÊNCIA PREJUDICADA POR RAÇA | Se já teve experiência prejudicada por raça | Nominal | Inteiro (Binário) |
| EXPERIÊNCIA PREJUDICADA POR GÊNERO | Se já teve experiência prejudicada por gênero | Nominal | Inteiro (Binário) |

##  3. Estatísticas Descritivas

### Dados Numéricos

Abaixo temos a tabela com as operações estatisticas feitas sobre as colunas da base final ultilizada para a confecção da analise explanatoria, e subsequentemente a criação do modelo de classificação.

| Estatística      | Investimento | Idade   | Gênero | Cor/Raça/Etnia | Afetado ou não | Afetado por raça | Afetado por gênero | Região mora | Mudou de estado | Nível de ensino | Situação de trabalho | Nível | Faixa salarial | Experiência | Trocar emprego | Forma trabalho |
|------------------|--------------|---------|--------|----------------|----------------|-------------------|--------------------|-------------|------------------|------------------|------------------------|--------|----------------|-------------|----------------|----------------|
| Média            | 5597,839377  | 31,5246 | 0,7710 | 2,0611         | 0,7775         | 0,0951            | 0,1437             | 2,7950      | 0,7969           | 3,3928           | 0,9531                 | 1,1859 | 9,0014         | 3,4917      | 1,7351         | 1,4489         |
| Mediana          | 2206,6       | 30      | 1      | 1              | 1              | 0                 | 0                  | 3           | 1                | 2                | 1                      | 1      | 11             | 4           | 2              | 1              |
| Moda             | 11825,2      | 27      | 1      | 1              | 1              | 0                 | 0                  | 3           | 1                | 6                | 1                      | 2      | 13             | 3           | 3              | 1              |
| Desvio Padrão    | 5260,7777    | 7,0803  | 0,4381 | 1,6983         | 0,4160         | 0,2934            | 0,3508             | 1,0560      | 0,4024           | 2,0637           | 0,5621                 | 0,7962 | 3,7440         | 1,9810      | 1,2269         | 0,9844         |
| Mínimo           | 21,2         | 18      | 0      | 0              | 0              | 0                 | 0                  | 0           | 0                | 0                | 0                      | 0      | 0              | 0           | 0              | 0              |
| Máximo           | 11825,2      | 70      | 3      | 6              | 1              | 1                 | 1                  | 4           | 1                | 6                | 7                      | 2      | 13             | 7           | 3              | 3              |
| Quartil 1        | 21,2         | 18      | 0      | 0              | 0              | 0                 | 0                  | 0           | 0                | 0                | 0                      | 0      | 0              | 0           | 0              | 0              |
| Quartil 3        | 11825,2      | 35      | 1      | 4              | 1              | 0                 | 0                  | 3           | 1                | 6                | 1                      | 2      | 12             | 5           | 3              | 2              |

### Dados Categóricos Principais

#### Gênero

![image](https://github.com/user-attachments/assets/99afcd3b-2c71-4d8c-a614-390d5314fd29)

"Predomínio masculino (75%) no mercado de dados brasileiro"

#### Forma de Trabalho

![image](https://github.com/user-attachments/assets/889adf83-4da2-49f1-9ca0-c3368ea1afdd)

"Modelo remoto lidera (45%), seguido por híbrido (35%) e presencial (20%)"

#### Distribuição por Região

![image](https://github.com/user-attachments/assets/ade4b8c3-d39d-4831-a207-2c79d3788b4e)

"Sudeste concentra os maiores investimentos em dados no país"

##  4. Principais Insights

1. **Perfil predominante**: 
   - Homem (75%), 30 anos, trabalha remotamente (45%), com 3-5 anos de experiência
   - Maioria empregada CLT (95.31%)

2. **Distribuição geográfica**:
   - Sudeste concentra maiores investimentos
   - Norte tem menor representação no mercado de dados

3. **Experiência profissional**:
   - 77.75% não acreditam que sua experiência foi afetada
   - 9.51% relataram preconceito por raça
   - 14.37% relataram preconceito por gênero

4. **Mobilidade**:
   - 79.69% já mudaram de estado brasileiro

5. **Educação**:
   - Nível médio de ensino é graduação/pós-graduação

6. **Mercado de trabalho**:
   - Faixa salarial média entre R$ 8.001-12.000
   - 73.51% consideram mudar de emprego nos próximos 6 meses

##  5. Gráficos Adicionais

### Distribuição de Idade

![image](https://github.com/user-attachments/assets/af58cb1d-e886-4bbf-ad68-c04448cb1ab9)

"Maioria dos profissionais tem entre 25-38 anos (média de 31.5 anos)"

### Nível de Experiência

![image](https://github.com/user-attachments/assets/990e2add-fb6d-47a8-b973-3099c56da60c)

"40% dos profissionais têm até 2 anos de experiência na área"

### Relação Investimento x Salário por Estado

![image](https://github.com/user-attachments/assets/dc1a9d59-4173-4439-b321-610c0c1a99e7)

"Estados com maior investimento tendem a ter salários médios mais altos"

---

## Preparação dos dados

## Tabela de Variáveis e Codificações

| Variável                              | Codificação                                                                                                                                                                                                                                                      |
|:--------------------------------------|:-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| IDADE                                 | Variável numérica contínua – não requer codificação.                                                                                                                                                                                                             |
| GÊNERO                                | Masculino=0, Feminino=1, Outro=2, Prefiro não informar=3.                                                                                                                                                                                                        |
| ESTADO(UF)                            | AC=0, AL=1, AM=2, AP=3, BA=4, CE=5, DF=6, ES=7, GO=8, MA=9, MG=10, MS=11, MT=12, PA=13, PB=14, PE=15, PI=16, PR=17, RJ=18, RN=19, RO=20, RR=21, RS=22, SC=23, SE=24, SP=25, TO=26.                                                                               |
| REGIÃO                                | Norte=1, Nordeste=2, Centro-Oeste=3, Sudeste=4, Sul=5.                                                                                                                                                                                                           |
| MUDOU DE ESTADO?                      | Sim=1, Não=0.                                                                                                                                                                                                                                                    |
| NÍVEL PROFISSIONAL                    | Júnior=0, Pleno=1, Sênior=2.                                                                                                                                                                                                                                     |
| FAIXA SALARIAL                        | <RS1.000=0, RS1.001-RS2.000=1, RS2.001-RS3.000=2, RS3.001-RS4.000=3, RS4.001-RS6.000=4, RS6.001-RS8.000=5, RS8.001-RS12.000=6, RS12.001-RS16.000=7, RS16.001-RS20.000=8, RS20.001-RS30.000=9, RS30.001-RS40.000=10, >RS40.001=11.                                |
| EXPERIÊNCIA EM DADOS                  | Nenhuma=0, <1 ano=1, 1-2 anos=2, 3-4 anos=3, 4-6 anos=4, 5-6 anos=5, 7-10 anos=6.                                                                                                                                                                                |
| SITUAÇÃO DE TRABALHO                  | Prefiro não informar=0, Desempregado (busca)=1, Empreendedor/CNPJ=2, CLT=3, Estagiário=4, Freelancer=5, Servidor Público=6, Estudante (graduação)=7, Estudante (pós-graduação)=8, Acadêmico/Pesquisador=9, Trabalho fora do Brasil=10, Remoto fora do Brasil=11. |
| FORMA DE TRABALHO                     | 100% presencial=0, 100% remoto=1, Híbrido fixo=2, Híbrido flexível=3.                                                                                                                                                                                            |
| INVESTIMENTO 2023                     | Variável numérica contínua – não requer codificação.                                                                                                                                                                                                             |
---

## Indução de modelos

### Modelo 1: Classificação com árvore de decisão

Após análise dos modelos feitos com região como atributo alvo, decidimos alterar a pergunta orientada a dados.
O novo modelo de classificação tem como objetivo classificar os indívuos nos 3 níveis de atuação: Júnior, Pleno e Sênior.

### Árvore de Decisão:
![Árvore de Decisão](https://github.com/ICEI-PUC-Minas-PPL-CDIA/ppl-cd-pcd-sist-int-2025-1-regional-disparities-data-mkt/blob/main/docs/imagens/decision_tree_optimized_current_model.png)

### Matriz de confusão:
![Matriz de Confusão](https://github.com/ICEI-PUC-Minas-PPL-CDIA/ppl-cd-pcd-sist-int-2025-1-regional-disparities-data-mkt/blob/main/docs/imagens/confusion_matrix_current_model.png)

---

# Modelo 2: Random Forest

Com base no modelo Random Forest desenvolvido com os dados da planilha 'state_of_data_updated_Limpa.xlsx', os seguintes insights foram extraídos sobre a relação entre as features selecionadas e o nível (Júnior, Pleno, Sênior) dos profissionais de dados:

### Contagem por classe:
Obtivemos através de analise da base que a distruibuição da varivel "('P2_g ', 'Nivel')_Num", esse partição está explicita pela tabela abaixo e também pelo gráfico proposto:

| Nível   | Quantidade |
|---------|------------|
| Sênior  | 1816       |
| Pleno   | 1400       |
| Júnior  | 1015       |


![image](https://github.com/ICEI-PUC-Minas-PPL-CDIA/ppl-cd-pcd-sist-int-2025-1-regional-disparities-data-mkt/blob/main/docs/imagens/distribuicao_da_variavel_nivel.png)


Após isso o modelo separa quais as variaveis ira utilizar, separando das quais não sao númericas, dessa forma temos as seguintes features utilizadas:

###  Features Selecionadas para o Modelo

| Nº  | Feature                                                                                           |
|-----|---------------------------------------------------------------------------------------------------|
| 1   | Investimento_em_milhões                                                                           |
| 2   | P1_a__Idade                                                                                       |
| 3   | P1_b__Genero_Num                                                                                  |
| 4   | P1_c__Cor_raca_etnia_Num                                                                          |
| 5   | P1_e_1__Não_acredito_que_minha_experiência_profissional_seja_afetada                              |
| 6   | P1_e_2__Experiencia_prejudicada_devido_a_minha_Cor_Raça_Etnia                                     |
| 7   | P1_e_3__Experiencia_prejudicada_devido_a_minha_identidade_de_gênero                               |
| 8   | P1_i_2__Regiao_onde_mora_Num                                                                      |
| 9   | P1_j__Mudou_de_Estado                                                                             |
| 10  | P1_l__Nivel_de_Ensino_Num                                                                         |
| 11  | P2_a__Qual_sua_situação_atual_de_trabalho_Num                                                     |
| 12  | P2_h__Faixa_salarial_Num                                                                          |
| 13  | P2_i__Quanto_tempo_de_experiência_na_área_de_dados_você_tem_Num                                   |
| 14  | P2_n__Você_pretende_mudar_de_emprego_nos_próximos_6_meses_Num                                     |
| 15  | P2_r__Atualmente_qual_a_sua_forma_de_trabalho_Num                                                 |

## Preparação dos dados e engenharias de features

-> Na proxima parte temos a preparação da base para o inicio do modelo, temos então o balanceamento da variavel smote utlizando 'SMOTE', a divisão da base entre treinamento e teste e a ordenação das features pela importancia para a analise proposta.

Balanceamento da variavel nivel por SMOTE

![image](https://github.com/ICEI-PUC-Minas-PPL-CDIA/ppl-cd-pcd-sist-int-2025-1-regional-disparities-data-mkt/blob/main/docs/imagens/balanceamento_smote.png)


Ordenação das features

![image](https://github.com/ICEI-PUC-Minas-PPL-CDIA/ppl-cd-pcd-sist-int-2025-1-regional-disparities-data-mkt/blob/main/docs/imagens/ordena%C3%A7%C3%A3o_features.png)


Separação da base entre treino e teste:

![image](https://github.com/ICEI-PUC-Minas-PPL-CDIA/ppl-cd-pcd-sist-int-2025-1-regional-disparities-data-mkt/blob/main/docs/imagens/divisao_treino_teste.png)


## Treinamento e otimização do modelo 

Primeiramente, antes de entramos na execução do modelo, temos que analisar a curva de aprendizado do modelo de treino, o qual está demonstrado pela imagem a seguir:

![image](https://github.com/ICEI-PUC-Minas-PPL-CDIA/ppl-cd-pcd-sist-int-2025-1-regional-disparities-data-mkt/blob/main/docs/imagens/curva_apredizado.png)




![image](https://github.com/ICEI-PUC-Minas-PPL-CDIA/ppl-cd-pcd-sist-int-2025-1-regional-disparities-data-mkt/blob/main/docs/imagens/matriz_confusao_treino.png)


![image](https://github.com/ICEI-PUC-Minas-PPL-CDIA/ppl-cd-pcd-sist-int-2025-1-regional-disparities-data-mkt/blob/main/docs/imagens/report_treino.png)


![image](https://github.com/ICEI-PUC-Minas-PPL-CDIA/ppl-cd-pcd-sist-int-2025-1-regional-disparities-data-mkt/blob/main/docs/imagens/matriz_confusao_teste.png)


![image](https://github.com/ICEI-PUC-Minas-PPL-CDIA/ppl-cd-pcd-sist-int-2025-1-regional-disparities-data-mkt/blob/main/docs/imagens/report_teste.png)


![image](https://github.com/ICEI-PUC-Minas-PPL-CDIA/ppl-cd-pcd-sist-int-2025-1-regional-disparities-data-mkt/blob/main/docs/imagens/correlacao_features.png)



# APÊNDICES

**Colocar link:**

Do código (armazenado no repositório);

Dos artefatos (armazenado do repositório);

Da apresentação final (armazenado no repositório);

Do vídeo de apresentação (armazenado no repositório).

Variaveis a serem utilzadas:
RegiaoP1_i_2
Nivel de atuação P2_g
faixa salarial 
ha quanto tempo está na area de dados





---
# Temporario


### Resultados 
---
### Resultados obtidos com o modelo 1.
### Acurácia:

| Class     | Precision | Recall | F1-Score | Support |
|-----------|-----------|--------|----------|---------|
| Júnior    | 0.75      | 0.81   | 0.77     | 207     |
| Pleno     | 0.59      | 0.63   | 0.61     | 278     |
| Sênior    | 0.82      | 0.75   | 0.79     | 361     |
|           |           |        |          |         |
| **Accuracy**       |           |        | 0.72     | 846     |
| **Macro Avg**      | 0.72      | 0.73   | 0.72     | 846     |
| **Weighted Avg**   | 0.73      | 0.72   | 0.73     | 846     |

Acurácia do modelo: 0.72


Com este modelo, os resultados obtidos foram:

Acurácia média do cross validation: 0.7401

Acurácia em base de teste separada: 0.7482

### Interpretação do modelo 1

O modelo de classificação usando árvore de decisão, foi testado com diferentes parâmentros. Os dados de treino/teste foram divididos em 80% e 20% respectivamente. Foi utilizado o One Hot Encoder para lidar com dados categóricos não ordinais. Foram trabalhadas as métricas de Gini e Entropy, e o melhor resultado de acurácia foi obtido utilizando Entropy. 

### Códigos do modelo

```python
## Dividindo treino e teste: 80/20
X_train, X_test, y_train, y_test = train_test_split(
    X_encoded, y, test_size=0.2, random_state=42

#Testando profundidades distintas com Entropy (o mesmo foi feito com Gini)Add commentMore actions
depths_to_test = range(1, 21)
accuracy_scores_entropy = []
accuracy_scores_entropy_train = []

print("\nTesting different max_depth values for Decision Tree with Entropy criterion:")


for depth in depths_to_test:Add commentMore actions
    modelo_entropy = DecisionTreeClassifier(
        criterion="entropy",
        random_state=42,
        class_weight='balanced',
        max_depth=depth,
        min_samples_split=50,
        min_samples_leaf=1
    )


modelo_entropy.fit(X_train, y_train)Add commentMore actions
    
    y_pred_entropy = modelo_entropy.predict(X_test)
    acuracia_entropy = accuracy_score(y_test, y_pred_entropy)
    accuracy_scores_entropy.append(acuracia_entropy)


y_pred_entropy_train = modelo_entropy.predict(X_train)Add commentMore actions
    acuracia_entropy_train = accuracy_score(y_train, y_pred_entropy_train)
    accuracy_scores_entropy_train.append(acuracia_entropy_train)
```

#### Gráfico comparativo - profundidades Gini x Entrophy
![image](https://github.com/ICEI-PUC-Minas-PPL-CDIA/ppl-cd-pcd-sist-int-2025-1-regional-disparities-data-mkt/blob/main/docs/imagens/Depth-level%20test.png)


O melhor resultado foi obtido com Entropy na profundidade 8, obtendo 0.7377 de acurácia na base de teste e 0.7613 na base de treino
Para melhorar a acurácia, utilizamos Grid Search e cross validation, com uma gama de valores distintos para o número mínimo de amostras para se formar um nó e para o splittar.



### Código GridSearch

```python
 print("\nPerforming Grid Search for min_samples_split and min_samples_leaf (Criterion: Entropy)")

 
 param_grid = {
     'max_depth': [7, 8, 9, 10], # Focar em profundidades próximas à melhor encontrada (8)
     'min_samples_split': [2, 5, 10, 20, 30, 40, 50], 
     'min_samples_leaf': [1, 5, 10, 15, 20] # 
     
 }


dt = DecisionTreeClassifier(criterion="entropy", random_state=42, class_weight='balanced') 

 # Criar o GridSearch com cross validantion separado em 5.
 grid_search = GridSearchCV(estimator=dt, param_grid=param_grid, cv=5, scoring='accuracy', n_jobs=-1)

# Treinar diferentes modelos com diferentes parametros 
 grid_search.fit(X_train, y_train)

 Imprimir os melhores parametros encontrados
 print("\nBest parameters found by Grid Search:")
 print(grid_search.best_params_)
 print("Best cross-validation accuracy found by Grid Search:")
 print(grid_search.best_score_)


# Definir melhor modelo do GridSearch
 best_modelo = grid_search.best_estimator_

 # Testar o modelo em base de teste distinta
 y_pred_best = best_modelo.predict(X_test)
 acuracia_best = accuracy_score(y_test, y_pred_best)
```

O Grid Search nos retorna a informação de que os parâmetros mais adequandos para o modelo são:
Min_samples_leaf: 1
Min_samples_split: 50
Max_depth: 9
Criterion: Entropy


###  Resultados do Modelo 2 - Random Forest
### Acurácia:
####  Conjunto de Treino

| Métrica             | Precisão | Revocação | F1-Score | Suporte |
|---------------------|----------|-----------|----------|---------|
| **Accuracy**        | -        | -         | **0.82** | **1089**|
| **Média Macro**     | 0.82     | 0.82      | 0.82     | 1089    |
| **Média Ponderada** | 0.82     | 0.82      | 0.82     | 1089    |

####  Conjunto de Teste

| Métrica             | Precisão | Revocação | F1-Score | Suporte |
|---------------------|----------|-----------|----------|---------|
| **Accuracy**        | -        | -         | **0.71** | **3385**|
| **Média Macro**     | 0.70     | 0.71      | 0.70     | 3385    |
| **Média Ponderada** | 0.71     | 0.71      | 0.71     | 3385    |

### Acurácia Global

- **Acurácia no treino:** 0.8228  
- **Acurácia no teste:** 0.7146


### Interpretação Modelo 2

O modelo de classificação com Random Forest foi ajustado com GridSearchCV e validado com divisão de 80% para treino e 20% para teste. Utilizou-se One Hot Encoder para variáveis categóricas e StandardScaler para dados numéricos. Foram avaliadas métricas como acurácia, precisão, revocação e F1-score, sendo a acurácia usada como principal critério para escolha do melhor modelo.

### Código do modelo

```python
# 2. Divisão treino/teste (20/80)
print("\n2. Dividindo os dados em treino e teste (20/80)...")
X_train, X_test, y_train, y_test = train_test_split(X, y,
 test_size=0.8,  # Changed to 0.8 for 80% test
 random_state=42,
 stratify=y)
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
```
###Assim ficou a curva de aprendizado
![image](https://github.com/ICEI-PUC-Minas-PPL-CDIA/ppl-cd-pcd-sist-int-2025-1-regional-disparities-data-mkt/blob/main/docs/imagens/curva_apredizado.png)
### Curva de Aprendizado

A curva mostra que a acurácia no treino é consistentemente maior do que na validação, sugerindo **overfitting** — o modelo aprende bem os dados de treino, mas generaliza com menor eficácia.

Com o aumento do conjunto de treino, a acurácia de validação melhora gradualmente, enquanto a de treino se estabiliza. Como as curvas não convergem totalmente, o modelo ainda pode ser otimizado com regularização, ajuste de hiperparâmetros ou mais dados.

## Parte mais importante do segundo modelo 
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

# Configurações iniciais
plt.style.use('default')
pd.set_option('display.float_format', lambda x: '%.3f' % x)

# Função para limpar nomes de colunas
def limpar_nome_coluna(nome):
    nome = str(nome)
    nome = nome.replace("'", "").replace('"', "").replace("(", "").replace(")", "")
    nome = nome.replace("/", "_").replace(" ", "_").replace("-", "_")
    nome = nome.replace(".", "").replace("?", "").replace("!", "")
    nome = nome.replace(",", "").replace(":", "").replace(";", "")
    nome = nome.replace("@", "at").replace("%", "pct").strip()
    return nome

# Carregar e preparar os dados
df = pd.read_excel('state_of_data_updated_Limpa.xlsx')
df.columns = [limpar_nome_coluna(col) for col in df.columns]

# Selecionar features e target
numeric_columns = df.select_dtypes(include=['int64', 'float64']).columns
target_column = 'P2_g__Nivel_Num'
X = df[numeric_columns].drop(target_column, axis=1) if target_column in numeric_columns else df[numeric_columns]
y = df[target_column]

# Dividir dados (20% treino, 80% teste)
X_train, X_test, y_train, y_test = train_test_split(X, y, test_size=0.8, random_state=42, stratify=y)

# Pré-processamento
scaler = StandardScaler()
X_train_scaled = scaler.fit_transform(X_train)
X_test_scaled = scaler.transform(X_test)

# Balanceamento com SMOTE
smote = SMOTE(random_state=42)
X_train_balanced, y_train_balanced = smote.fit_resample(X_train_scaled, y_train)

# Seleção de features
base_model = RandomForestClassifier(n_estimators=100, random_state=42)
base_model.fit(X_train_balanced, y_train_balanced)
selector = SelectFromModel(base_model, prefit=True)
X_train_selected = selector.transform(X_train_balanced)
X_test_selected = selector.transform(X_test_scaled)
selected_features = X.columns[selector.get_support()].tolist()

# Otimização do modelo
param_grid = {
    'n_estimators': [200, 300, 400],
    'max_depth': [15, 20, 25, 30],
    'min_samples_split': [2, 5, 10],
    'min_samples_leaf': [1, 2, 4],
    'class_weight': ['balanced', 'balanced_subsample'],
    'max_features': ['sqrt', 'log2']
}

rf_base = RandomForestClassifier(random_state=42, n_jobs=-1)
grid_search = GridSearchCV(rf_base, param_grid, cv=5, scoring='accuracy', n_jobs=-1, verbose=1)
grid_search.fit(X_train_selected, y_train_balanced)
rf_model = grid_search.best_estimator_

# Avaliação
y_train_pred = rf_model.predict(X_train_selected)
y_test_pred = rf_model.predict(X_test_selected)

print(f"Acurácia no treino: {accuracy_score(y_train_balanced, y_train_pred):.4f}")
print(f"Acurácia no teste: {accuracy_score(y_test, y_test_pred):.4f}")
print("\nClassification Report:")
print(classification_report(y_test, y_test_pred))
```
Este projeto implementa um pipeline completo de machine learning utilizando o modelo Random Forest para classificar a variável P2_g__Nivel_Num, a partir de dados numéricos carregados de um arquivo Excel.

Etapas do Projeto

Limpeza de Dados: Padronização dos nomes das colunas para evitar erros.

Divisão dos Dados: Separados em treino (20%) e teste (80%) de forma estratificada.

Normalização: Aplicada com StandardScaler para uniformizar os dados.

Balanceamento de Classes: Uso de SMOTE para lidar com classes desbalanceadas.

Seleção de Features: Realizada com um modelo base de Random Forest.

Otimização de Hiperparâmetros: Usando GridSearchCV com validação cruzada.

Avaliação Final: Com acurácia e relatório de classificação nos conjuntos de treino e teste.

Destaques

Este código segue boas práticas de ciência de dados, incluindo:

Limpeza de dados automatizada;

Tratamento de desbalanceamento;

Seleção de atributos relevantes;

Ajuste fino dos parâmetros do modelo.

Ideal para problemas de classificação com dados numéricos e classes desbalanceadas.
## Análise comparativa dos modelos

Os atributos utilizados foram padronizados para ambos os modelos:

_ Investimento em milhões
_ Idade
_ Gênero
_ Cor/Raça/Etnia
_ Nível de Ensino
_ Situação de Trabalho
_ Faixa salarial
_ Tempo de experiência
_ Forma de Trabalho
_ Nível (atributo alvo)

Ambos os modelos utilizados foram de classificação, com o objetivo final de classificar o atributo "Nível" (Júnior, Pleno, Sênior) de cada indivíduo da tabela, e foram otimizados a partir de testes com diferentes métricas e diferentes atributos, além da implementação de bibliotecas como XGBoost.

O modelo 1, Classificação com Árvore de Decisão, atingiu uma acurácia máxima de 0.73 na base de teste, e 0.76 na base de treino. O modelo aprendeu bem a discernir as classes "Júnior" e "Sênior", ambas tendo precisão e recall maior quando comparadas à classe "Pleno". A maior dificuldade de aprendizado do modelo é de distinguir as classes "Sênior" e "Pleno".

O modelo 2, Classificação por K Nearest Neighbors, antingiu uma acurácia máxima de 0.65 na base de teste, e 0.71 na base de treino.
As bases de treino e teste foram dividas em 70% e 30%, respectivamente, em contraste ao 80% e 20% do modelo de árvore de decisão. As mesmas dificuldades foram enfrentadas: O maior recall e precisão foi da classe com maior contagem. 

### Conclusão comparativa

Ambos os modelos apresentaram características semelhantes e enfrentaram dificuldades análogas. A aplicação de dois modelos de classificação mostrou-se ineficaz para a obtenção de conclusões distintas. Diante disso, optou-se pela substituição do modelo com pior desempenho por um novo modelo, com o intuito de aprimorar os resultados da análise.

### Conclusão


## Resumo do Desenvolvimento
Este trabalho investigou como fatores individuais impactam a carreira em ciência de dados no Brasil, utilizando dados do State of Data 2023. Desenvolvemos dois modelos preditivos (Árvore de Decisão e Random Forest) para classificar profissionais em níveis Júnior, Pleno e Sênior, com base em características como:

- Experiência profissional (40% têm até 2 anos na área);
- Faixa salarial (média R$8.001-12.000);
- Formação acadêmica;
- Gênero (75% masculino);
- Região (Sudeste concentra 45% dos profissionais).

## Resultados e Discussão

### Desempenho dos Modelos
| Modelo           | Acurácia (Teste) | Melhor Classe (F1-Score) | Pior Classe (F1-Score) |
|------------------|------------------|--------------------------|------------------------|
| Árvore Decisão   | 72%              | Sênior (0.79)            | Pleno (0.61)           |
| Random Forest    | 71.46%           | Sênior (0.85)            | Pleno (0.65)           |

**Vantagens**:
- Ambos os modelos identificaram padrões claros para classificar Júnior e Sênior;
- Random Forest mostrou melhor balanceamento entre classes após SMOTE;
- Variáveis como tempo de experiência e faixa salarial foram as mais relevantes.

**Desvantagens**:
- Dificuldade em classificar nível Pleno (sobreposição de características);
- Acurácia limitada (~72%) sugere necessidade de mais atributos;
- Disparidades regionais podem ter influenciado os resultados.

### Principais Descobertas
1. **Fatores Críticos**:
   - Tempo de experiência: 40% dos profissionais têm até 2 anos na área;
   - Gênero: 75% dos respondentes são homens;
   - Região: Sudeste concentra 45% dos profissionais e maiores salários.

2. **Desigualdades Identificadas**:
   ```python
   # Disparidade salarial por região (em salários mínimos)
   regioes = ['Norte', 'Nordeste', 'Centro-Oeste', 'Sudeste', 'Sul']
   salarios_medios = [6.2, 7.1, 8.3, 10.5, 9.2]
Limitações e Melhorias Futuras
Limitações Atuais
Dados:

Base restrita ao State of Data 2023

->Classes desbalanceadas (Sênior: 1816, Júnior: 1015);

->Falta de atributos sobre habilidades específicas.

*Modelagem*:

->Dificuldade em classificar nível Pleno;

->Acurácia máxima de 72%;

->Possível overfitting (diferença treino-teste).

-*Sugestões de Melhoria*

Coleta de Dados:

->Incluir variáveis sobre habilidades técnicas específicas;

->Ampliar amostra de grupos sub-representados.

-*Modelagem*:

->Testar algoritmos como XGBoost ou Redes Neurais;

->Incorporar técnicas avançadas de feature engineering;

->Desenvolver modelo específico para classificação Pleno/Sênior.

-*Análise*:

->Adicionar análise temporal da progressão de carreira;

->Investigar relação entre formação acadêmica e promoções.

-*Considerações Finais*

Os resultados confirmam que o nível profissional no mercado de dados brasileiro é influenciado por:

->Experiência prática (principal diferenciador Júnior/Pleno);

->Fatores regionais (Sudeste concentra melhores oportunidades);

->Desigualdades estruturais (gênero, acesso a educação).

-*Este estudo fornece uma base quantitativa para*:

->Profissionais planejarem suas carreiras;

->Empresas desenvolverem programas de capacitação;

->Instituições de ensino ajustarem currículos.


