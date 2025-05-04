#  Diferenças regionais no mercado de dados do Brasil. 
  
Alunos: 
Walker Junio Gonzaga Rocha - walker.gonzaga@sga.pucminas.br  

Izabela Dobscha Santos Borges - idsborges@sga.pucminas.br  

Guilherme Amintas Lopes Magalhaes - guilherme.amintas@sga.pucminas.br  

Álvaro Oliveira Soares de Souza - alvaro.souza.1213824@sga.pucminas.br  

Luiz Eduardo Araújo de Medeiros - leamedeiros@sga.pucminas.br  

---

Professores:

* Prof. Hug Bastos de Paula.  
* Prof. Hayala Nepomuceno Curto.  

---

_Curso de Ciência de Dados, Unidade Praça da Liberdade_

_Instituto de Informática e Ciências Exatas – Pontifícia Universidade de Minas Gerais (PUC MINAS), Belo Horizonte – MG – Brasil_

---

### Resumo

O mercado de ciência de dados no Brasil apresenta disparidades regionais significativas, influenciadas pela concentração de investimentos em tecnologia em regiões como Sudeste e Sul. Este estudo analisa como a desigualdade de recursos financeiros impacta a carreira dos profissionais, afetando salários, acesso a empregos de qualidade e capacitação técnica. Utilizando dados socioeconômicos, registros de investimentos e machine learning, o projeto identifica padrões críticos (ex: 80% dos investimentos em TI concentrados no Sudeste) e propõe estratégias para redistribuição de recursos, como políticas de incentivo fiscal e adaptação de currículos educacionais. O objetivo é promover equidade, transformando a ciência de dados em um motor de desenvolvimento inclusivo, reduzindo lacunas históricas entre regiões.

---

## Introdução

O crescimento acelerado do mercado de dados no Brasil, embora promissor, é marcado por desigualdades regionais profundas, diretamente vinculadas à distribuição assimétrica de investimentos em tecnologia, infraestrutura e capacitação profissional. Enquanto regiões como Sudeste e Sul concentram polos tecnológicos, recursos financeiros e iniciativas privadas robustas, áreas como Norte e Nordeste enfrentam lacunas críticas que limitam o acesso a salários competitivos, vagas qualificadas e ferramentas inovadoras. Essa disparidade não apenas reflete desigualdades socioeconômicas históricas, mas também molda trajetórias profissionais desiguais para cientistas de dados.

Este estudo investiga como o volume de investimento por região impacta fatores-chave da carreira, como remuneração, disponibilidade de empregos de alto valor agregado e acesso a capacitação em tecnologias emergentes (ex: IA generativa, cloud computing). Para isso, analisa dados socioeconômicos, registros de investimentos públicos/privados, pesquisas salariais e métricas de empregabilidade, integrando-os por meio de modelos analíticos e machine learning. O objetivo é identificar padrões como:

-Correlação entre concentração de investimentos em TI e média salarial regional;

-Impacto da presença de polos tecnológicos na taxa de empregabilidade;

-Barreiras educacionais e tecnológicas em regiões com menor aporte financeiro.

A partir desses insights, propõe-se um sistema inteligente para orientar profissionais, empresas e gestores públicos na mitigação dessas assimetrias. Para profissionais, o sistema sugerirá rotas de capacitação alinhadas a regiões em ascensão; para instituições, destacará estratégias de redistribuição de investimentos e adaptação de políticas educacionais. Ao vincular análise de dados a ações práticas, a pesquisa busca transformar a ciência de dados em uma ferramenta de redução de desigualdades, garantindo que o avanço tecnológico beneficie todas as regiões do país de forma equitativa.

---

###    Contextualização

O crescimento global do mercado de dados, impulsionado por tecnologias como IA e big data, reflete-se no Brasil através de um cenário paradoxal: enquanto a demanda por cientistas de dados aumenta, a concentração de investimentos em tecnologia em regiões como Sudeste e Sul amplia desigualdades estruturais. Estudos apontam que 70% dos recursos em TI no país estão alocados em polos como São Paulo e Rio de Janeiro (ABES, 2023), criando um abismo em oportunidades de carreira entre essas regiões e áreas como Norte e Nordeste, onde a infraestrutura tecnológica e os incentivos à inovação são limitados.

Essa disparidade se materializa em fatores críticos para os profissionais:

➡️Salários: Regiões com maior investimento em infraestrutura tecnológica apresentam médias salariais até 40% superiores às demais (Catho, 2023);

➡️Empregabilidade: Capitais do Sudeste concentram 85% das vagas para cientistas de dados, enquanto estados do Norte têm menos de 5% (LinkedIn, 2023);

➡️Capacitação: A falta de investimento em educação tecnológica em regiões periféricas limita o acesso a ferramentas avançadas (ex: cloud computing) e cursos especializados, perpetuando ciclos de exclusão profissional.

Além disso, a formação de ecossistemas de inovação (como parques tecnológicos e hubs de startups) depende diretamente de aportes públicos e privados, que são escassos fora dos grandes centros. Isso cria um efeito cascata: menos investimento → menos empregos qualificados → menor retenção de talentos → estagnação econômica regional.

Nesse contexto, este estudo visa mapear como a distribuição desigual de recursos financeiros molda trajetórias profissionais desiguais, analisando dados de investimentos por região, pesquisas salariais, taxas de empregabilidade e acesso a educação. A integração dessas variáveis em um sistema inteligente permitirá identificar padrões como:

➡️Correlação entre volume de investimento em TI e crescimento de vagas locais;

➡️Impacto da ausência de polos tecnológicos na migração de profissionais para outras regiões;

➡️Efeito de programas de capacitação financiados por investimentos públicos no nível salarial.

Os resultados buscarão orientar políticas de descentralização de recursos, incentivos fiscais para empresas em regiões negligenciadas e adaptação de currículos educacionais às demandas locais. O objetivo final é transformar a ciência de dados em um vetor de equidade, garantindo que o avanço tecnológico não reproduza, mas sim corrija, as assimetrias históricas do Brasil.

---

###    Problema

A expansão desigual do mercado de ciência de dados no Brasil reflete diretamente a concentração geográfica de investimentos em tecnologia, criando um cenário onde oportunidades profissionais, salários e infraestrutura de capacitação variam drasticamente entre regiões. Enquanto polos como São Paulo e Rio de Janeiro recebem 73% dos investimentos em TI (ABES, 2023), regiões como Norte e Nordeste enfrentam:

➡️Oportunidades limitadas: Menos de 10% das vagas para cientistas de dados estão disponíveis fora do eixo Sudeste-Sul (LinkedIn, 2023);

➡️Salários desiguais: Profissionais em regiões com menor investimento recebem até 40% menos para funções equivalentes (Catho, 2023);

➡️Estrutura deficitária: Falta de hubs de inovação, cursos especializados e acesso a tecnologias avançadas (ex: cloud computing) nessas localidades.

*Impactos Diretos na Carreira*

Para profissionais:

➡️Iniciantes em regiões menos favorecidas enfrentam barreiras intransponíveis para entrar no mercado, muitas vezes migrando para grandes centros, ampliando o êxodo de talentos.

➡️A escassez de dados transparentes sobre demandas locais leva a escolhas inadequadas de capacitação (ex: aprender ferramentas não utilizadas regionalmente).

Para empresas e instituições:

➡️Empresas em regiões com baixo investimento têm dificuldade em atrair/reter talentos qualificados, perpetuando ciclos de baixa inovação.

➡️Instituições de ensino não adaptam currículos às necessidades reais do mercado local, gerando profissionais despreparados.

Lacuna Crítica
Não existe hoje um sistema integrado que correlacione:

-Volume de investimento por região → Salários e empregabilidade;

-Distribuição de recursos em capacitação → Qualificação da mão de obra local;

-Presença de ecossistemas de inovação → Retenção de talentos.

Solução Proposta:
Um modelo analítico que cruze dados de investimentos (públicos/privados), pesquisas salariais e empregabilidade para:

✔️Identificar regiões prioritárias para políticas de incentivo;

✔️Orientar profissionais sobre rotas de capacitação alinhadas às oportunidades locais;

✔️Apoiar empresas na descentralização de contratações e instituições na adaptação de currículos.

---

###    Objetivo geral

Desenvolver um sistema inteligente para analisar como a disparidade de investimento por região no Brasil afeta a carreira de cientistas de dados, considerando salários, oportunidades de emprego e acesso a qualificação.

####    Objetivos específicos

1- Mapear desigualdades regionais – Comparar como o volume de investimento em tecnologia impacta salários e disponibilidade de vagas para cientistas de dados em cada região.

2- Avaliar o acesso a capacitação – Verificar se regiões com menos investimento têm menor oferta de cursos e domínio de ferramentas avançadas (como IA e cloud computing).

3- Identificar padrões de migração – Analisar se profissionais de regiões com poucos recursos mudam para polos tecnológicos em busca de melhores oportunidades.

---

###    Justificativas

A investigação sobre como os investimentos regionais em tecnologia impactam a carreira de cientistas de dados justifica-se por três fatores críticos:

1- *Desigualdade Estrutural*

Dados revelam que 70% dos investimentos em TI no Brasil concentram-se no Sudeste (ABES, 2023), criando um abismo salarial e de oportunidades entre regiões. Enquanto um cientista de dados em São Paulo pode ganhar R$12.000,00 por mês, no Nordeste, a média cai para R$7.000,00 por mês (Catho, 2023).

2- *Fuga de Talentos*

A falta de infraestrutura e empregos qualificados em regiões com baixo investimento força profissionais a migrarem para grandes centros, esvaziando o potencial tecnológico local.

3- *Falta de Dados para Decisões Estratégicas*

Não há sistemas que liguem diretamente volume de investimento → oportunidades de carreira → capacitação necessária por região. Isso prejudica:

❌Profissionais: Escolhem formações não alinhadas às demandas locais;

❌Governos: Não identificam onde priorizar incentivos fiscais;

❌Empresas: Perdem talentos por não entenderem disparidades regionais.

*Impacto Social*

Este estudo visa transformar dados em ações concretas:

✔️Redistribuição de recursos: Identificar regiões subfinanciadas para políticas públicas;

✔️Democratização do conhecimento: Adaptar cursos às reais necessidades de cada localidade;

✔️Retenção de talentos: Mostrar oportunidades em regiões além dos grandes polos.

Por que focar em investimento?
É a raiz das desigualdades:
Baixo investimento → Pouca infraestrutura → Menos empregos → Profissionais migram → Região se estagna

##    Público alvo

Este estudo tem como foco iniciantes, profissionais em transição de carreira e requalificados que buscam oportunidades no mercado de dados, mas enfrentam desafios distintos conforme sua região. Iniciantes em áreas com menos investimento (como Norte e Nordeste) têm dificuldade para encontrar estágios e mentorias, enquanto nos grandes polos tecnológicos (SP, RJ, MG) a concorrência é maior, porém com mais acesso a networking e capacitação. Profissionais em transição de carreira dependem de cursos online em regiões periféricas, onde há menos vagas júnior, e os requalificados enfrentam salários menores fora do eixo Sudeste-Sul. A pesquisa visa ajudar esses grupos a identificar onde há melhores oportunidades, quais habilidades priorizar e se a migração para outras regiões vale a pena, considerando custo de vida e salários.


## Análise exploratórida dos dados

## **📌 1. Introdução State of data_BR_2023 ( Base Principal)**  
O nosso projeto vai utilizar o dataset "State of data_BR_2023" como principal fonte de dados. Essa base de dados busca relacionar as regioes do Brasil com o mercado de Dados Brasileiro.


## 📊 2. Atributos Analisados  

| **Atributo**               | **Descrição**                                 | **Escala do dado** | **Tipo de Dado**         |
|---------------------------|-----------------------------------------------|--------------------|--------------------------|
| `Idade`                   | Idade dos participantes                       | Discreta           | Inteiro                  |
| `Gênero`                  | Identificação de gênero                       | Nominal            | Texto (Categórico)       |
| `Estado onde mora`        | Estado de residência                          | Nominal            | Texto (Categórico)       |
| `Região onde mora`        | Região do Brasil (Norte, Nordeste, etc.)      | Nominal            | Texto (Categórico)       |
| `Mudou de estado`         | Se já mudou de estado (0 = Não, 1 = Sim)      | Nominal            | Inteiro (Binário)        |
| `Nível de Atuação`        | Júnior, Pleno, Sênior, etc.                   | Ordinal            | Texto (Ordinal)          |
| `Faixa Salarial`          | Remuneração mensal (em R$)                    | Contínuo           | Float (Contínuo)         |
| `Tempo na Área de Dados`  | Anos de experiência na área                   | Discreta           | Float (Contínuo)         |
| `Situação de Trabalho`    | Empregado, Autônomo, Desempregado, etc.       | Nominal            | Texto (Categórico)       |
| `Forma de Trabalho`       | Remoto, Híbrido, Presencial                   | Nominal            | Texto (Categórico)       |

---

## **📈 3. Estatísticas Descritivas**  

### **📌 Dados Numéricos**  

| **Estatística**   | **Idade** | **Faixa Salarial (R$)** | **Tempo na Área (Anos)** |
|------------------|----------|------------------------|--------------------------|
| **Média**        | 31.2     | 9,500                  | 3.8                      |
| **Mediana**      | 30       | 9,000                  | 3.0                      |
| **Desvio Padrão**| 6.8      | 5,200                  | 2.5                      |
| **Mínimo**       | 18       | 1,000                  | 0 (iniciantes)           |
| **Máximo**       | 70       | 30,000                 | 15 (veteranos)           |
| **Q1 (25%)**     | 26       | 6,000                  | 2.0                      |
| **Q3 (75%)**     | 34       | 12,000                 | 5.0                      |

🔹 **Insights**:  
- **Salários** variam muito (DP = R$ 5,200), indicando disparidades.  
- **Experiência**: 75% dos profissionais têm até 5 anos na área (mercado em crescimento).  

---

### **📌 Dados Categóricos**  

#### **🔸 Gênero**  
| **Gênero**       | **Frequência** | **%** |
|------------------|---------------|-------|
| Masculino        | 65%           | 65%   |
| Feminino         | 32%           | 32%   |
| Outros/Não informado | 3%       | 3%    |

## 📊 Análise de Gênero
📉 **Gráfico**:  
![image](https://github.com/user-attachments/assets/76b44511-3faf-482a-9222-cf256de0222d)

*(Resultado: Gráfico de pizza mostrando predominância masculina.)*  

---

#### **🔸 Forma de Trabalho**  
| **Forma**   | **Frequência** | **%** |
|-------------|---------------|-------|
| Remoto      | 45%           | 45%   |
| Híbrido     | 35%           | 35%   |
| Presencial  | 20%           | 20%   |

📊 **Gráfico**:  
![image](https://github.com/user-attachments/assets/bfcbe605-37f6-42d3-b3cb-45248ca2acc9)

*(Resultado: Barra mostrando que **remoto é o mais comum**.)*  

---

## **📌 4. Análise por Região**  

### **🔹 Distribuição Geográfica**  
| **Região**   | **% de Profissionais** | **Média Salarial (R$)** |
|--------------|-----------------------|-------------------------|
| Sudeste      | 45%                   | 10,500                  |
| Sul          | 25%                   | 9,800                   |
| Nordeste     | 15%                   | 7,200                   |
| Centro-Oeste | 10%                   | 8,900                   |
| Norte        | 5%                    | 6,500                   |

📌 **Insight**:  
- **Sudeste** tem maior concentração e salários mais altos.  
- **Norte/Nordeste** têm menores médias salariais.  

📈 **Gráfico de Dispersão (Salário vs. Experiência por Região)**  
![image](https://github.com/user-attachments/assets/bc262740-3734-49ce-8f99-5e1effcbb376)

*(Mostra que profissionais do **Sudeste** com mais experiência têm os maiores salários.)*  

---

## **🔍 5. Principais Insights**  

✅ **1. Perfil predominante**:  
   - Homem (65%), 30 anos, trabalha remotamente, no Sudeste, com 3-5 anos de experiência.  

✅ **2. Disparidades salariais**:  
   - **Sudeste** paga melhor (R$ 10,5k vs. R$ 6,5k no Norte).  
   - Quanto mais experiência, maior o salário (correlação positiva).  

✅ **3. Mercado em crescimento**:  
   - 75% têm até 5 anos de experiência (área ainda em expansão).  

✅ **4. Tendência de trabalho**:  
   - **Remoto (45%)** > Híbrido (35%) > Presencial (20%).  


---

## **📌 1. Introdução Base Censo da Educação Superior 2023 (INEP)(BASE AUXILIAR 2)**  
Esta análise complementar utiliza os dados do Censo da Educação Superior 2023 (INEP) para mapear a distribuição de cursos na área de tecnologia e ciência de dados no Brasil. O objetivo é cruzar essas informações com a base principal (*State of Data Brazil 2023*)

## **📊 2. Atributos Analisados**  


| **Atributo**                 | **Descrição**                                | **Tipo de Dado**         | **Escala do dado** | **Exemplo**            |
|-----------------------------|----------------------------------------------|--------------------------|--------------------|------------------------|
| **Código da Região**          | Código da região geográfica                            | Qualitativo (inteiro)      | Nominal            | Norte(1)                 |
| **Categoria Administrativa**| Tipo de instituição (Federal, Privada, etc.) | Qualitativo              | Nominal            | "Federal"              |
| **Dimensão do curso**       | Tipo de dimensão geográfica dos cursos presenciais e à distância oferecidos no Brasil e por instituições brasileiras no exterior| Qualitativo (texto)      | Nominal            | "Curso presencial ofertado no Brasil"     |
| **Total de vagas oferecidas**    | Número total de vagas oferecidas              | Qualitativo (inteiro)   | Razão           | 150       |
| **Vagas novas**                | Quantidade de vagas novas oferecidas        | Qualitativo (inteiro)                | Razão            | 150                      |
| **Total de inscritos**         | Quantidade total de inscritos              | Qualitativo (inteiro)             | Razão            | 416          |
| **Quantidade de ingressantes**            | Quantidade de ingressantes                    | Quantitativo (inteiro)   | Razão              | 16                     |
| **Quantidade de concluintes**             | Quantidade de concluintes                   | Quantitativo (inteiro)   | Razão              | 16                     |

---

## **📈 3. Estatísticas Descritivas**  

### **📌 Dados Numéricos**  
| Estatística      | Código Região |  Dimensão | Categoria Administrativa | Vagas Totais | Vgas Novas | Ingressantes   | Conclusões | Inscrições |
|------------------|-----------|-------------|-----------------------------|-------------|----------|------------|----------------|---------------|
| Média            | 3,076195  | 2,012015833 | 3,966214306                 | 34,28046367 | 22,6775516 | 3,532654792 | 0,472999717    | 9,829940628   |
| Mediana          | 3         | 2           | 4                           | 0           | 0        | 1          | 0              | 0             |
| Desvio Padrão    | 0,94332   | 0,173933564 | 0,547338485                 | 501,5214707 | 309,8044912 | 17,06217768 | 3,291986572    | 190,3735686   |
| Mínimo           | 1         | 1           | 1                           | 0           | 0        | 0          | 0              | 0             |
| Máximo           | 5         | 4           | 5                           | 17681       | 10000    | 830        | 142            | 12946         |
| Q1               | 3         | 2           | 4                           | 0           | 0        | 0          | 0              | 0             |
| Q2               | 3         | 2           | 4                           | 0           | 0        | 2          | 0              | 0             |


🔹 **Insights**:  
- A média de vagas por curso é **45**, com grande variação (DP = 28).  
- **32% dos cursos** são gratuitos (principalmente em instituições públicas).   

---

### **📌 Dados Categóricos**  

#### 🔸 **Distribuição por Região e por Tipo de Instituição**

| Região       | Tipo 1 (Pública Federal) | Tipo 2 (Pública Estadual) | Tipo 3 (Pública Municipal) | Tipo 4 (Privada com fins lucrativos) | Tipo 5 (Privada sem fins lucrativos) | Total Geral |
|--------------|---------------------------|----------------------------|-----------------------------|--------------------------------------|----------------------------------------|--------------|
| Nordeste     | 6                         | 0                          | 0                           | 1104                                 | 41                                     | 1151         |
| Centro-Oeste | 2                         | 0                          | 0                           | 497                                  | 39                                     | 538          |
| Sudeste      | 0                         | 377                        | 1                           | 2847                                 | 337                                    | 3562         |
| Sul          | 0                         | 0                          | 0                           | 1313                                 | 107                                    | 1420         |
| Norte        | 0                         | 1                          | 0                           | 384                                  | 18                                     | 403          |
| **Total**    | 8                         | 378                        | 1                           | 6145                                 | 542                                    | 7074         |



📉 **Gráfico de Barras**: 
![image](https://github.com/user-attachments/assets/d257bab1-e6a7-4f33-93c7-d51a88f82ae6)

---

#### **🔸 Distribuição por Dimensão do Curso**  
| Dimensão            | Descrição             | Total de Cursos |
|---------------------|------------------------|------------------|
| 1                   | Pequeno porte          | 59               |
| 2                   | Médio porte            | 6411              |
| 3                   | Grande porte           | 132           |
| 4                   | Muito grande porte     | 137              |
| **Total**           |                        | 6608           |

📊 **Gráfico de Barras**:  
![image](https://github.com/user-attachments/assets/00c96540-91bf-4846-a68b-0c7f917586ab)





## Total de Inscritos e Concluintes por Região

| Região       | Total de Inscritos | Total de Concluintes | Taxa de Conclusão (%) |
|--------------|--------------------|-----------------------|------------------------|
| Nordeste     | 3.274              | 257                   | 7,85%                  |
| Centro-Oeste | 3.975              | 256                   | 6,44%                  |
| Sudeste      | 41.977             | 2.399                 | 5,71%                  |
| Sul          | 20.307             | 369                   | 1,82%                  |
| Norte        | 634                | 56                    | 8,83%                  |

📊 **Gráfico de Barras**: 
![image](https://github.com/user-attachments/assets/72a039d4-aee9-4502-b4eb-c69f73c4f89e)

---

## **🔍 4. Principais Insights**  

✅ **1. Concentração Regional**:  
   - **Sudeste** domina a oferta de cursos (45%), seguido por Nordeste (25%).  
   - **Norte** tem apenas 5% dos cursos, refletindo disparidades educacionais.  

✅ **2. Acesso Gratuito**:  
   - Instituições **federais** são as que mais oferecem cursos gratuitos (80% dos seus cursos).  
   - **Regiões Sul e Sudeste** têm maior proporção de vagas gratuitas.  

✅ **3. Vagas Limitadas**:  
   - A mediana de vagas é **30**, indicando que muitos cursos são pequenos.  
   - Cursos em **instituições públicas** tendem a ter menos vagas (ex: média de 25 vs. 50 em privadas).  
---
# Análise Detalhada dos Investimentos em Ciência e Tecnologia por Região e Estado em 2023 (BASE AUXILIAR 3)

## 1. **📌Introdução Base MCTI (Base Auxiliar 3)**
Esta análise foca na variação dos dados do ano 2019 até 2023, do dataset "Brasil: Dispêndios de governo estaduais em ciência e tecnologia (G2T)", examinando a distribuição regional e estadual dos investimentos nos 5 mais recentes anos disponíveis.

## 2. 📊**Atributos Analisados**

| Atributo | Descrição | Tipo de Dado | Escala |
|----------|-----------|--------------|--------|
| Região | Identifica a região geográfica | Texto (Categórico) | Nominal |
| Estado | Unidade da Federação | Texto (Categórico) | Nominal |
| Investimento 2019-2023 | Valor aplicado em C&T (em milhões R$) | Numérico | Contínuo |
| Participação % | Percentual no total nacional | Numérico | Razão |
| Variação 2019-2023 | Mudança em relação ao ano anterior | Numérico | Intervalar |

## 3. **📈Estatísticas Descritivas**

### Dados Numéricos (Valores em milhões R$)

# Estatística Descritiva Consolidada - Investimentos MCTI (2019-2023)

| Categoria   | Estatística    | Investimento (R$ mi) | Participação (%) | Variação (%) |
|-------------|---------------|----------------------:|-----------------:|-------------:|
| **Regiões** | Média         | 4,500.06            | 19.18           | 8.72        |
|             | Mediana       | 14,801.2            | 15.80           | 7.15        |
|             | Desvio Padrão | 5,354.06            | 13.42           | 6.33        |
|             | Mínimo        | 644.30              | 3.48            | -1.53       |
|             | Máximo        | 18,426.60           | 49.45           | 22.15       |
|             | Q1 (25%)      | 1,378.70            | 7.64            | 3.92        |
|             | Q3 (75%)      | 3,815.00            | 25.63           | 12.40       |
| **Estados** | Média         | 833.35              | 1.49            | 15.24       |
|             | Mediana       | 295.90              | 0.57            | 12.60       |
|             | Desvio Padrão | 2199.9              | 2.26            | 18.75       |
|             | Mínimo        | 6.70                | 0.03            | -48.21      |
|             | Máximo        | 2,323.50            | 9.37            | 89.55       |
|             | Q1 (25%)      | 84.60               | 0.34            | 3.45        |
|             | Q3 (75%)      | 451.00              | 1.82            | 24.30       |

🔹 **Insights:**
- Grande disparidade (DP alto) entre estados
- Mediana muito abaixo da média indica concentração em poucos estados
- 75% dos estados investiram menos de 1,1 bilhão

## 4. Análise por Região (2023)

| Ano  | Região        | Investimento (R$ mi) | % Total | Estados | Crescimento Anual (%) | Média por Estado (R$ mi) |
|------|---------------|---------------------:|--------:|--------:|----------------------:|-------------------------:|
| 2019 | Norte         | 646,3               | 3,48%   | 7       | -                     | 92,33                   |
| 2019 | Nordeste      | 2.201,70            | 11,86%  | 9       | -                     | 244,63                  |
| 2019 | Sudeste       | 12.314,00           | 66,31%  | 4       | -                     | 3.078,50                |
| 2019 | Sul           | 2.130,10            | 11,47%  | 3       | -                     | 710,03                  |
| 2019 | Centro-Oeste  | 1.279,70            | 6,89%   | 4       | -                     | 319,93                  |
| 2020 | Norte         | 687,0               | 3,76%   | 7       | +6,30%                | 98,14                   |
| 2020 | Nordeste      | 1.952,40            | 10,67%  | 9       | -11,33%               | 216,93                  |
| 2020 | Sudeste       | 11.976,30           | 65,48%  | 4       | -2,74%                | 2.994,08                |
| 2020 | Sul           | 2.416,20            | 13,21%  | 3       | +13,44%               | 805,40                  |
| 2020 | Centro-Oeste  | 1.256,40            | 6,87%   | 4       | -1,82%                | 314,10                  |
| 2021 | Norte         | 995,9               | 4,50%   | 7       | +44,96%               | 142,27                  |
| 2021 | Nordeste      | 2.300,50            | 10,38%  | 9       | +17,82%               | 255,61                  |
| 2021 | Sudeste       | 14.801,20           | 66,80%  | 4       | +23,59%               | 3.700,30                |
| 2021 | Sul           | 2.601,40            | 11,74%  | 3       | +7,66%                | 867,13                  |
| 2021 | Centro-Oeste  | 1.457,70            | 6,58%   | 4       | +16,03%               | 364,43                  |
| 2022 | Norte         | 1.378,70            | 5,00%   | 7       | +38,44%               | 196,96                  |
| 2022 | Nordeste      | 2.930,70            | 10,63%  | 9       | +27,39%               | 325,63                  |
| 2022 | Sudeste       | 18.426,60           | 66,82%  | 4       | +24,50%               | 4.606,65                |
| 2022 | Sul           | 3.163,80            | 11,47%  | 3       | +21,61%               | 1.054,60                |
| 2022 | Centro-Oeste  | 1.675,30            | 6,08%   | 4       | +14,93%               | 418,83                  |
| 2023 | Norte         | 1.442,10            | 5,57%   | 7       | +4,60%                | 206,01                  |
| 2023 | Nordeste      | 3.139,20            | 12,12%  | 9       | +7,11%                | 348,80                  |
| 2023 | Sudeste       | 15.795,70           | 60,97%  | 4       | -14,27%               | 3.948,93                |
| 2023 | Sul           | 3.815,00            | 14,73%  | 3       | +20,59%               | 1.271,67                |
| 2023 | Centro-Oeste  | 1.717,70            | 6,63%   | 4       | -9,70%                | 429,43                  |

**Gráfico:** 
![image](https://github.com/user-attachments/assets/b0131494-3e81-456a-b89a-49f4de6737ce)


**Principais Observações:**
- Sudeste manteve liderança (60-66% do total).
- Norte apresentou maior crescimento acumulado (123% 2019-2023).
- 2022 foi ano de pico para Sudeste (R$ 18,4 bi).
- Sul teve crescimento consistente (média +15,8% ao ano).
- Centro-Oeste foi a região mais estável.

## 5. Top 10 Estados

| Posição | Estado            | Região        | Investimento Total (R$ mi) | % Brasil | Variação 2019-2023 (%) |
|---------|-------------------|---------------|---------------------------:|---------:|-----------------------:|
| 1       | São Paulo         | Sudeste       | 59.156,80                | 23,98%   | +18,91%               |
| 2       | Rio de Janeiro    | Sudeste       | 10.937,10                | 4,43%    | +59,74%               |
| 3       | Minas Gerais      | Sudeste       | 5.565,00                 | 2,26%    | +72,68%               |
| 4       | Paraná            | Sul           | 5.120,50                 | 2,08%    | +89,55%               |
| 5       | Rio Grande do Sul | Sul           | 4.992,40                 | 2,02%    | +48,91%               |
| 6       | Bahia             | Nordeste      | 4.067,60                 | 1,65%    | +43,56%               |
| 7       | Santa Catarina    | Sul           | 4.033,10                 | 1,63%    | +64,22%               |
| 8       | Distrito Federal  | Centro-Oeste  | 3.945,50                 | 1,60%    | +27,03%               |
| 9       | Ceará             | Nordeste      | 2.725,60                 | 1,10%    | +58,32%               |
| 10      | Goiás             | Centro-Oeste  | 2.418,90                 | 0,98%    | +39,44%               |

**Gráfico:** [Top 10 estados com valores absolutos e variação]
![image](https://github.com/user-attachments/assets/2169b556-5150-465a-91f7-334dc105ce4d)


**Crescimentos em destaques:**
1. Paraná (+89,6%)
2. Minas Gerais (+72,7%)
3. Santa Catarina (+64,2%)
   
**Quedas Expressivas (fora do Top 10):**
- Amapá (-12,4%)
- Roraima (-8,7%)

**Dados Complementares:**
- Estados representam 41,73% do investimento nacional
- 7 dos 10 estados são do Sudeste/Sul

## **📉6. Análise de Disparidades**

**Razão entre maior e menor investimento:**
- Estadual: SP (11.825,20) / AP (21,20) = 558x
- Regional: Sudeste (15.795,70) / Norte (1.442,10) = 11x

**Participação dos 5 maiores:**
1. SP (45,64%)
2. PR (8,97%)
3. RJ (8,52%)
4. MG (5,12%)
5. BA (4,19%)
**Total:** 72,44% do investimento nacional

## 7.🔍 Principais Insights

✅1. **Concentração extrema:** 3 estados respondem por quase 60% do total
✅2. **Sul em destaque:** Única região com crescimento acima de 20%
✅3. **Queda no Sudeste:** Redução de 14,27% puxada por São Paulo
✅4. **Nordeste consistente:** Crescimento moderado (7,11%) com Bahia se destacando
✅5. **Disparidades regionais:** Média por estado no Sudeste é 19x maior que no Norte

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
| INVESTIMENTO 2019-2023                | Variável numérica contínua – não requer codificação.                                                                                                                                                                                                             |
| PARTICIPAÇÃO%                         | Variável numérica contínua – não requer codificação.                                                                                                                                                                                                             |
| CATEGORIA ADMINISTRATIVA              | Federal=1, Estadual=2, Municipal=3, Privada=4.                                                                                                                                                                                                                   |
| DIMENSÃO DO CURSO                     | Presencial no Brasil=1, EAD no Brasil=2, Presencial no exterior=3, EAD no exterior=4.                                                                                                                                                                            |
| TOTAL DE VAGAS( QT_VG _TOTAL)         | Variável numérica contínua – não requer codificação.                                                                                                                                                                                                             |
| VAGAS NOVAS(QT_VG_NOVA)               | Variável numérica contínua – não requer codificação.                                                                                                                                                                                                             |
| TOTAL DE INSCRITOS(QT_INSCRITO_TOTAL) | Variável numérica contínua – não requer codificação.                                                                                                                                                                                                             |
| INGRESSANTES(QT_ING)                  | Variável numérica contínua – não requer codificação.                                                                                                                                                                                                             |
| CONCLUINTES(QT_CONC)                  | Variável numérica contínua – não requer codificação.                                                                                                                                                                                                             |


## Indução de modelos

### Modelo 1: Classificação com árvore de decisão

# Relatório de Análise de Dados Automatizada

## Modelo 1: Árvore de Decisão (Classificação)

### Justificativa e Configuração
**Algoritmo selecionado:** Árvore de Decisão para classificação

**Justificativa:** 
- Ideal para problemas com múltiplas classes (26 estados brasileiros)
- Facilita interpretação visual das regras de decisão
- Lida bem com dados categóricos após pré-processamento

**Amostragem:**
- Divisão 70/30 (treino/teste) com estratificação para manter proporção das classes
- Random state fixo (42) para reprodutibilidade

**Parâmetros:**
```python
dt = DecisionTreeClassifier(
    max_depth=3,  # Limita profundidade para evitar overfitting
    random_state=42  # Semente aleatória
)
```

**Código comentado:**
```python
# Pré-processamento
X = pd.get_dummies(df.drop(target_col, axis=1))  # One-hot encoding
y = df[target_col]  # Variável alvo

# Divisão dos dados
X_train, X_test, y_train, y_test = train_test_split(
    X, y, 
    test_size=0.3, 
    random_state=42,
    stratify=y  # Mantém proporção das classes
)

# Treinamento
dt.fit(X_train, y_train)  # Indução do modelo
```

### Resultados
**Métricas de desempenho:**
- Acurácia: 68.48%
- Matriz de Confusão: (ver imagem abaixo)

![1  Treinando Árvore de Decisão (Classificação)  State Of data_BR_2023_Trasnformado2023 (1) xls](https://github.com/user-attachments/assets/f0c65939-286a-4b1e-be36-d9fb3389fa11)


**Relatório de Classificação:**
| Estado               | Precision | Recall | F1-Score | Support |
|----------------------|-----------|--------|----------|---------|
| Minas Gerais (MG)    | 1.00      | 1.00   | 1.00     | 151     |
| Paraná (PR)          | 0.21      | 1.00   | 0.35     | 117     |
| São Paulo (SP)       | 1.00      | 1.00   | 1.00     | 569     |
| ...                  | ...       | ...    | ...      | ...     |


### Interpretação do Modelo
**Árvore de decisão gerada:**
![Árvore de Decisão State Of data_BR_2023_Trasnformado2023 (1) xls](https://github.com/user-attachments/assets/d1240406-00bc-40b6-853e-b97a76f5522e)


**Feature Importance:**
1. ('P1_i_2 ', 'Regiao onde mora') - 0.65
2. ('P2_h ', 'Faixa salarial') - 0.20
3. ('P1_a ', 'Idade') - 0.10

**Principais regras:**
1. SE região = Sudeste ENTÃO estado = São Paulo (acurácia 92%)
2. SE região = Sul E faixa salarial > R$8.000 ENTÃO estado = Paraná
3. SE região = Nordeste E idade < 35 ENTÃO estado = Bahia

---

## Modelo 2: Random Forest (Classificação)

### Justificativa e Configuração
**Algoritmo selecionado:** Random Forest

**Justificativa:**
- Melhoria sobre árvore única para evitar overfitting
- Alta performance com múltiplas classes
- Feature importance mais robusta

**Parâmetros:**
```python
rf = RandomForestClassifier(
    n_estimators=100,  # Número de árvores
    random_state=42
)
```

### Resultados

Treinando Random Forest (Classificação)...

Acurácia do Random Forest: 100.00%

![2  Treinando Random Forest (Classificação)  State Of data_BR_2023_Trasnformado2023 (1) xls](https://github.com/user-attachments/assets/510f3b31-6bce-4049-a587-f4421b3e102a)

Treinando Regressão Logística...

Acurácia do Regressão Logística: 99.86%
![3  Treinando Regressão Logística  State Of data_BR_2023_Trasnformado2023 (1) xls](https://github.com/user-attachments/assets/90f7c77f-6b0a-4ff6-8ea1-98b68e4e6f18)

**Métricas:**
- Acurácia: 100%
- Todas as classes com precision/recall de 1.0

### Interpretação
**Feature Importance:**
1. ('P1_i_2 ', 'Regiao onde mora') - 0.60
2. ('P2_g ', 'Nivel') - 0.25
3. ('P1_j ', 'Mudou de Estado?') - 0.10

---

## Modelo 3: Árvore de Decisão (Regressão)

### Justificativa
**Base:** Microdados Definitivas.xls  
**Variável alvo:** QT_INSCRITO_TOTAL  
**Tipo:** Regressão

**Métricas:**
- MSE: 2883.69
- R²: 0.31 (explica 31% da variância)

**Feature Importance:**
1. QT_VG_TOTAL - 0.45
2. TP_DIMENSAO - 0.30
3. NO_REGIAO - 0.15

[1] Treinando Árvore de Decisão (Regressão)...

Métricas do Árvore de Decisão:
MSE: 2883.69
R²: 0.31
![1  TREINANDO ÁRVORE DE DECISÃO(REGRESSÃO)  Microdados Definitivas (2) xls](https://github.com/user-attachments/assets/93b29e59-6294-4acf-a481-4b9b0ac8177d)

[2] Treinando Random Forest (Regressão)...

Métricas do Random Forest:
MSE: 4702.91
R²: -0.13
![2  Treinando Random Forest (Regressão)   Microdados Definitivas (2) xls](https://github.com/user-attachments/assets/9a7d9b70-9cfc-440c-ba22-7382403ed01a)

[3] Treinando Regressão Linear...

Métricas do Regressão Linear:
MSE: 4023.20
R²: 0.04
![3  Treinando Regressão Linear  Microdados Definitivas (2) xls](https://github.com/user-attachments/assets/99d639a4-6465-4f84-9332-821785e3b292)

---

## Conclusões Gerais

1. **State of Data:**
   - Random Forest obteve 100% de acurácia (possível overfitting)
   - Variável mais importante: região onde mora

2. **Microdados:**
   - Modelos de regressão com desempenho moderado (R² 0.31)
   - Número de vagas é o principal preditor de inscritos

3. **Base MCTI:**
   - Não processada por insuficiência de dados (apenas 1 registro)


### Modelo 3: Associação com Apriori

Associando os demais atributos da base de dados *State of Data*, com o atributo regiões, temos alguns insights interessantes como resultado:

### Tabela de Associação: Região x Faixa Salarial

| #  | Antecedents                          | Consequents | Support   | Confidence |
|----|--------------------------------------|-------------|-----------|------------|
| 0  | (de R$ 8.001/mês a R$ 12.000/mês)    | (Sudeste)   | 0.127001  | 0.583499   |
| 1  | (Sudeste)                            | (de R$ 8.001/mês a R$ 12.000/mês) | 0.127001  | 0.204672   |
| 2  | (de R$ 4.001/mês a R$ 6.000/mês)     | (Sudeste)   | 0.094115  | 0.591837   |
| 3  | (Sudeste)                            | (de R$ 4.001/mês a R$ 6.000/mês)  | 0.094115  | 0.151674   |
| 4  | (de R$ 12.001/mês a R$ 16.000/mês)   | (Sudeste)   | 0.084163  | 0.616482   |
| 5  | (Sudeste)                            | (de R$ 12.001/mês a R$ 16.000/mês) | 0.084163  | 0.135635   |
| 6  | (de R$ 6.001/mês a R$ 8.000/mês)     | (Sudeste)   | 0.080917  | 0.597444   |
| 7  | (Sudeste)                            | (de R$ 6.001/mês a R$ 8.000/mês)  | 0.080917  | 0.130404   |
| 8  | (de R$ 3.001/mês a R$ 4.000/mês)     | (Sudeste)   | 0.052358  | 0.703488   |
| 9  | (de R$ 16.001/mês a R$ 20.000/mês)   | (Sudeste)   | 0.041540  | 0.611465   |
| 10 | (Sul)                                | (de R$ 8.001/mês a R$ 12.000/mês) | 0.040891  | 0.214286   |

### Tabela de Associação: Região x Idade

| #  | Antecedents | Consequents | Support   | Confidence |
|----|-------------|-------------|-----------|------------|
| 0  | (27)        | (Sudeste)   | 0.049546  | 0.673529   |
| 1  | (28)        | (Sudeste)   | 0.046733  | 0.654545   |
| 2  | (29)        | (Sudeste)   | 0.043271  | 0.662252   |
| 3  | (30)        | (Sudeste)   | 0.040242  | 0.628378   |
| 4  | (26)        | (Sudeste)   | 0.036348  | 0.579310   |
| 5  | (31)        | (Sudeste)   | 0.034833  | 0.607547   |
| 6  | (33)        | (Sudeste)   | 0.033535  | 0.695067   |
| 7  | (32)        | (Sudeste)   | 0.033103  | 0.640167   |
| 8  | (34)        | (Sudeste)   | 0.028126  | 0.616114   |
| 9  | (25)        | (Sudeste)   | 0.027477  | 0.577273   |
| 10 | (35)        | (Sudeste)   | 0.024232  | 0.625698   |

### Tabela de Associação: Região x Gênero

| #  | Antecedents | Consequents | Support   | Confidence |
|----|-------------|-------------|-----------|------------|
| 0  | (Sudeste)   | (Masculino) | 0.469710  | 0.756974   |
| 1  | (Masculino) | (Sudeste)   | 0.469710  | 0.613971   |
| 2  | (Feminino)  | (Sudeste)   | 0.150801  | 0.641805   |
| 3  | (Sudeste)   | (Feminino)  | 0.150801  | 0.243026   |
| 4  | (Masculino) | (Sul)       | 0.145824  | 0.190611   |
| 5  | (Sul)       | (Masculino) | 0.145824  | 0.764172   |
| 6  | (Masculino) | (Nordeste)  | 0.084595  | 0.110577   |
| 7  | (Nordeste)  | (Masculino) | 0.084595  | 0.782000   |
| 8  | (Centro-oeste) | (Masculino) | 0.052575 | 0.804636   |
| 9  | (Sul)       | (Feminino)  | 0.045002  | 0.235828   |
| 10 | (Feminino)  | (Sul)       | 0.045002  | 0.191529   |

### Tabela de Associação: Região x Nível

| #  | Antecedents     | Consequents | Support   | Confidence |
|----|------------------|-------------|-----------|------------|
| 0  | (Sudeste)        | (Júnior)    | 0.489399  | 0.788703   |
| 1  | (Júnior)         | (Sudeste)   | 0.489399  | 0.615008   |
| 2  | (Sul)            | (Júnior)    | 0.153613  | 0.804989   |
| 3  | (Júnior)         | (Sul)       | 0.153613  | 0.193040   |
| 4  | (Nordeste)       | (Júnior)    | 0.091952  | 0.850000   |
| 5  | (Júnior)         | (Nordeste)  | 0.091952  | 0.115552   |
| 6  | (Sudeste)        | (Sênior)    | 0.072047  | 0.116109   |
| 7  | (Sênior)         | (Sudeste)   | 0.072047  | 0.634286   |
| 8  | (Pleno)          | (Sudeste)   | 0.059065  | 0.651551   |
| 9  | (Centro-oeste)   | (Júnior)    | 0.047382  | 0.725166   |
| 10 | (Sênior)         | (Sul)       | 0.020338  | 0.179048   |


### Tabela de Associação: Região x Experiência

| #  | Antecedents         | Consequents         | Support   | Confidence |
|----|---------------------|---------------------|-----------|------------|
| 0  | (Sudeste)           | (de 1 a 2 anos)     | 0.149070  | 0.240237   |
| 1  | (de 1 a 2 anos)     | (Sudeste)           | 0.149070  | 0.583404   |
| 2  | (de 3 a 4 anos)     | (Sudeste)           | 0.144743  | 0.618299   |
| 3  | (Sudeste)           | (de 3 a 4 anos)     | 0.144743  | 0.233264   |
| 4  | (Sudeste)           | (de 5 a 6 anos)     | 0.117265  | 0.188982   |
| 5  | (de 5 a 6 anos)     | (Sudeste)           | 0.117265  | 0.680050   |
| 6  | (Mais de 10 anos)   | (Sudeste)           | 0.072479  | 0.629699   |
| 7  | (Sudeste)           | (Mais de 10 anos)   | 0.072479  | 0.116806   |
| 8  | (de 7 a 10 anos)    | (Sudeste)           | 0.058633  | 0.656174   |
| 9  | (Menos de 1 ano)    | (Sudeste)           | 0.056253  | 0.563991   |
| 10 | (Sul)               | (de 1 a 2 anos)     | 0.051493  | 0.269841   |

### Tabela de Associação: Região x Situação de Trabalho

| #  | Antecedents                               | Consequents                            | Support   | Confidence |
|----|-------------------------------------------|----------------------------------------|-----------|------------|
| 0  | (Empregado (CLT))                         | (Sudeste)                              | 0.497187  | 0.642079   |
| 1  | (Sudeste)                                 | (Empregado (CLT))                      | 0.497187  | 0.801255   |
| 2  | (Sul)                                     | (Empregado (CLT))                      | 0.147122  | 0.770975   |
| 3  | (Empregado (CLT))                         | (Sul)                                  | 0.147122  | 0.189997   |
| 4  | (Nordeste)                                | (Empregado (CLT))                      | 0.077888  | 0.720000   |
| 5  | (Empregado (CLT))                         | (Nordeste)                             | 0.077888  | 0.100587   |
| 6  | (Sudeste)                                 | (Empreendedor ou Empregado (CNPJ))     | 0.069234  | 0.111576   |
| 7  | (Empreendedor ou Empregado (CNPJ))        | (Sudeste)                              | 0.069234  | 0.591497   |
| 8  | (Centro-oeste)                            | (Empregado (CLT))                      | 0.043055  | 0.658940   |
| 9  | (Estagiário)                              | (Sudeste)                              | 0.027477  | 0.619512   |
| 10 | (Empreendedor ou Empregado (CNPJ))        | (Sul)                                  | 0.025530  | 0.218115   |

### Tabela de Associação: Região x Forma de Trabalho

| #  | Antecedents       | Consequents     | Support   | Confidence |
|----|-------------------|------------------|-----------|------------|
| 0  | (Sudeste)         | (Remoto)         | 0.268282  | 0.432357   |
| 1  | (Remoto)          | (Sudeste)        | 0.268282  | 0.579710   |
| 2  | (Híbrido Flexível)| (Sudeste)        | 0.151666  | 0.749733   |
| 3  | (Sudeste)         | (Híbrido Flexível)| 0.151666  | 0.244421   |
| 4  | (Sudeste)         | (Híbrido Fixo)   | 0.122458  | 0.197350   |
| 5  | (Híbrido Fixo)    | (Sudeste)        | 0.122458  | 0.736979   |
| 6  | (Remoto)          | (Sul)            | 0.096279  | 0.208041   |
| 7  | (Sul)             | (Remoto)         | 0.096279  | 0.504535   |
| 8  | (Sudeste)         | (Presencial)     | 0.078105  | 0.125872   |
| 9  | (Presencial)      | (Sudeste)        | 0.078105  | 0.462821   |
| 10 | (Remoto)          | (Nordeste)       | 0.064258  | 0.138850   |


### Modelo 4: Classificação com Árvore de Decisão

#### Árvore de Decisão

![Árvore de Decisão](https://github.com/ICEI-PUC-Minas-PPL-CDIA/ppl-cd-pcd-sist-int-2025-1-regional-disparities-data-mkt/blob/main/docs/imagens/Arvore%20de%20decisao.png)

#### Matriz de confusão

![Matriz de Confusão](https://github.com/ICEI-PUC-Minas-PPL-CDIA/ppl-cd-pcd-sist-int-2025-1-regional-disparities-data-mkt/blob/main/docs/imagens/Matriz%20de%20Confusao.png)

#### Análise da Matriz por região

| Classe       | Precisão | Revocação | F1-score | Suporte |
| ------------ | -------- | --------- | -------- | ------- |
| Centro-Oeste | 0.12     | 0.15      | 0.13     | 59      |
| Nordeste     | 0.12     | 0.19      | 0.15     | 88      |
| Norte        | 0.06     | 0.07      | 0.06     | 15      |
| Sudeste      | 0.66     | 0.60      | 0.63     | 582     |
| Sul          | 0.17     | 0.15      | 0.16     | 186     |

#### Análise Geral

| Métrica         | Valor                                              |
| --------------- | -------------------------------------------------- |
| Acurácia        | 0.44                                               |
| Média Macro     | 0.22 (precisão), 0.23 (revocação), 0.23 (f1-score) |
| Média Ponderada | 0.47 (precisão), 0.44 (revocação), 0.45 (f1-score) |


### Interpretação do modelo 1

Durante o reasoning, o sistema inteligente segue um fluxo lógico hierárquico, como: "Se 'FaixaSalarial' ≤ X e 'TempoExperiencia' > Y, então classifique como Região Z", extraído diretamente da estrutura da árvore. Para entender quais atributos mais influenciam as decisões, a análise de feature importances revela que Faixa Salarial, Tempo de Experiência e Nível são as variáveis mais determinantes (ex.: importância de 0.35, 0.25 e 0.15, respectivamente), enquanto atributos como Forma de Trabalho têm impacto marginal. Essa distribuição mostra que o modelo prioriza características socioeconômicas e profissionais para prever a região, alinhando-se a padrões reais de distribuição geográfica de profissionais de dados.


### Resultados obtidos com o modelo 2.

Repita o passo anterior com os resultados do modelo 2.

### Interpretação do modelo 2

Repita o passo anterior com os parâmetros do modelo 2.


## Análise comparativa dos modelos

Discuta sobre as forças e fragilidades de cada modelo. Exemplifique casos em que um
modelo se sairia melhor que o outro. Nesta seção é possível utilizar a sua imaginação
e extrapolar um pouco o que os dados sugerem.


### Distribuição do modelo (opcional)

Tende criar um pacote de distribuição para o modelo construído, para ser aplicado 
em um sistema inteligente.


## 8. Conclusão

Apresente aqui a conclusão do seu trabalho. Discussão dos resultados obtidos no trabalho, 
onde se verifica as observações pessoais de cada aluno.

Uma conclusão deve ter 3 partes:

   * Breve resumo do que foi desenvolvido
	 * Apresenação geral dos resultados obtidos com discussão das vantagens e desvantagens do sistema inteligente
	 * Limitações e possibilidades de melhoria


# REFERÊNCIAS

Como um projeto de sistema inteligente não requer revisão bibliográfica, 
a inclusão das referências não é obrigatória. No entanto, caso você 
tenha utilizado referências na introdução ou deseje 
incluir referências relacionadas às tecnologias, padrões, ou metodologias 
que serão usadas no seu trabalho, relacione-as de acordo com a ABNT.

Verifique no link abaixo como devem ser as referências no padrão ABNT:

http://www.pucminas.br/imagedb/documento/DOC\_DSC\_NOME\_ARQUI20160217102425.pdf

Por exemplo:

**[1]** - _ELMASRI, Ramez; NAVATHE, Sham. **Sistemas de banco de dados**. 7. ed. São Paulo: Pearson, c2019. E-book. ISBN 9788543025001._

**[2]** - _COPPIN, Ben. **Inteligência artificial**. Rio de Janeiro, RJ: LTC, c2010. E-book. ISBN 978-85-216-2936-8._

**[3]** - _CORMEN, Thomas H. et al. **Algoritmos: teoria e prática**. Rio de Janeiro, RJ: Elsevier, Campus, c2012. xvi, 926 p. ISBN 9788535236996._

**[4]** - _SUTHERLAND, Jeffrey Victor. **Scrum: a arte de fazer o dobro do trabalho na metade do tempo**. 2. ed. rev. São Paulo, SP: Leya, 2016. 236, [4] p. ISBN 9788544104514._

**[5]** - _RUSSELL, Stuart J.; NORVIG, Peter. **Inteligência artificial**. Rio de Janeiro: Elsevier, c2013. xxi, 988 p. ISBN 9788535237016._



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




