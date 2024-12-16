# Análise de Funil de Eventos e Teste A/A/B

## Sobre o Projeto

Este projeto tem como objetivo principal analisar o comportamento dos usuários de um aplicativo de uma startup de produtos alimentícios. A análise é dividida em dois aspectos principais:

- **Funil de Vendas**: Identificar como os usuários progridem até a etapa de compra, determinar onde há maior desistência e compreender o comportamento dos usuários em diferentes etapas.
- **Teste A/A/B**: Avaliar os efeitos de alterações no design do aplicativo sobre os usuários, utilizando dois grupos de controle (fontes antigas) e um grupo de teste (fontes novas).

## Objetivos

1. Estudar o funil de vendas para entender o comportamento dos usuários e identificar gargalos.
2. Avaliar se os grupos de controle A/A possuem diferenças significativas que possam indicar distorções.
3. Verificar o impacto da mudança de design entre o grupo de teste e os grupos de controle.
4. Realizar testes estatísticos para garantir a confiabilidade dos resultados e ajustar o nível de significância apropriado.

---

## Dados

- **Fonte**: `logs_exp_us.csv`
- **Composição**:
  - `EventName`: Nome do evento realizado pelo usuário.
  - `DeviceIDHash`: Identificador exclusivo do usuário.
  - `EventTimestamp`: Data e hora do evento.
  - `ExpId`: Identificador do experimento (246 e 247 para os grupos de controle, 248 para o grupo de teste).
  - **Período**: A ser identificado na etapa de análise exploratória, com exclusão de dados incompletos, se necessário.

---

## Método

### Etapas de Trabalho

#### **Preparação dos Dados**
- Renomear colunas para padronização.
- Identificar e corrigir valores ausentes e tipos de dados inconsistentes.
- Criar colunas de data/hora e data separadas.

#### **Análise Exploratória**
- Identificar a quantidade de eventos e usuários.
- Calcular a média de eventos por usuário.
- Definir o período de dados mais completos para análise.

#### **Análise do Funil de Eventos**
- Classificar eventos por frequência de ocorrência e proporção de usuários que realizaram cada evento.
- Identificar sequência de eventos e calcular a proporção de usuários que passam de uma etapa para outra.
- Determinar o ponto de maior desistência.

#### **Análise do Teste A/A/B**
- Verificar a distribuição de usuários entre os grupos experimentais.
- Testar diferenças estatísticas entre os grupos de controle (A/A).
- Comparar os resultados do grupo de teste com os grupos de controle.
- Ajustar o nível de significância considerando os testes realizados.

---

## Ferramentas Utilizadas

- **Python 3.x**
- **Pandas**: Manipulação e análise de dados.
- **NumPy**: Operações matemáticas e estatísticas.
- **Matplotlib e Seaborn**: Visualização de dados.
- **SciPy**: Testes estatísticos.
- **Jupyter Notebook**: Ambiente de desenvolvimento interativo.

---

### Como Executar o Projeto  
1. Clone o repositório;  
2. Navegue até o diretório do projeto;  
3. Abra o projeto no seu IDE favorito;  
4. Instale as dependências;  
5. Execute o script principal.  

---

### Licença  
Este projeto está licenciado sob a Licença MIT - consulte o arquivo [LICENSE](LICENSE) para mais detalhes.

----------------------

# Event Funnel Analysis and A/A/B Testing

## About the Project

This project aims to analyze user behavior in an application from a food product startup. The analysis is divided into two main aspects:

- **Sales Funnel**: Identify how users progress to the purchase stage, determine where most users drop off, and understand user behavior at various stages.
- **A/A/B Testing**: Evaluate the effects of design changes in the app on users, using two control groups (old fonts) and one test group (new fonts).

## Objectives

1. Study the sales funnel to understand user behavior and identify bottlenecks.
2. Assess whether the A/A control groups have significant differences that could indicate distortions.
3. Evaluate the impact of the design change between the test group and the control groups.
4. Perform statistical tests to ensure reliable results and adjust the appropriate significance level.

---

## Data

- **Source**: `logs_exp_us.csv`
- **Composition**:
  - `EventName`: Name of the event performed by the user.
  - `DeviceIDHash`: Unique user identifier.
  - `EventTimestamp`: Date and time of the event.
  - `ExpId`: Experiment identifier (246 and 247 for control groups, 248 for the test group).
  - **Period**: To be identified during exploratory analysis, excluding incomplete data if necessary.

---

## Method

### Workflow

#### **Data Preparation**
- Rename columns for standardization.
- Identify and fix missing values and inconsistent data types.
- Create separate columns for datetime and date.

#### **Exploratory Analysis**
- Identify the number of events and users.
- Calculate the average number of events per user.
- Define the period with the most complete data for analysis.

#### **Event Funnel Analysis**
- Classify events by occurrence frequency and the proportion of users who performed each event.
- Identify the sequence of events and calculate the proportion of users moving from one stage to the next.
- Determine the stage with the highest drop-off.

#### **A/A/B Test Analysis**
- Verify the distribution of users across experimental groups.
- Test for statistical differences between the control groups (A/A).
- Compare the test group results with the control groups.
- Adjust the significance level considering the number of tests performed.

---

## Tools Used

- **Python 3.x**
- **Pandas**: Data manipulation and analysis.
- **NumPy**: Mathematical and statistical operations.
- **Matplotlib and Seaborn**: Data visualization.
- **SciPy**: Statistical tests.
- **Jupyter Notebook**: Interactive development environment.
  
---

### How to Run the Project  
1. Clone the repository;  
2. Navigate to the project directory;  
3. Open the project in your favorite IDE;  
4. Install dependencies;  
5. Run the main script.  

---

### License  
This project is licensed under the MIT License - see the [LICENSE](LICENSE) file for more details.
