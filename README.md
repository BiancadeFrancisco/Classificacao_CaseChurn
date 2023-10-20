# Classificacao_CaseChurn

## Descrição Projeto

**Conjunto de dados:**
Conjunto de dados com informações de clientes de uma plataforma de streaming.

**Arquivo:** .excel

**Objetivo:**
Através da metodologia CRISP-DM, realizar uma análise exploratória em um dataset com características de usuários churn e não churn. Testar e avaliar algoritmos para prever possíveis ocorrências de churn, levando em consideração características distribuídas no dataset explorado.
- Churn é uma métrica que indica a quantidade de clientes que cancelaram um produto ou serviço em um determinado período de tempo.

**IDE:** Colab

**Linguagem:** Python

**Principais bibliotecas utilizadas:**
•	Pandas, para manipulação e tratamento dos dados;
•	Seaborn, para criação e visualização de gráficos;
•	Matplotlib, para criação e visualização de gráficos;
•	Scikit-learn, aprendizado de máquina;

**Algoritmos utilizados:**
•	Regressão Logística;
•	Random Forest.

**CRISP-DM:** 
- Importação bibliotecas;
- Importação dataset.

1° Entendimento Negócio;

2° Entendimento dos Dados;
Leitura dos dados disponibilizados no dataset:

•	Target: variável “chave” a ser analisada.

Churn — Cliente deu churn ou não

•	Variáveis explicativas: variáveis numéricas e/ou categóricas que podemos utilizar para explicar o nosso Target.

*Variáveis numéricas:*

Tenure — Número de meses que o cliente está na base;
MonthlyCharges — A quantia consumida por cliente mensalmente;
TotalCharges — A quantia consumida por cliente total;

*Variáveis categóricas:*

CustomerID - Id do cliente;
Gender — M/F;
SeniorCitizen — Se o cidadão é ou não idoso (0,1);
Partner — Se o cliente é ou não casado;
Dependents — Cliente tem dependentes (Yes, No);
PhoneService — Cliente tem serviço telefonico (Yes, No);
MulitpleLines — Se o cliente tem várias linhas ou não (Yes, No, No Phone Service);
InternetService — Tipo do serviço de internet (DSL, Fiber Optic, None).
OnlineSecurity — Se o cliente tem segurança online (Yes, No, No Internet Service);
OnlineBackup — WSe o cliente tem Backup Online (Yes, No, No Internet Service);
DeviceProtection — Se o cliente tem proteção do dispositivo (Yes, No, No Internet Service);
TechSupport — Se o cliente tem suporte tecnológico (Yes, No, No Internet Service);
StreamingTV — Se o cliente tem streaming de TV (Yes, No, No Internet Service);
StreamingMovies — Se o cliente tem serviço de streaming de filmes (Yes, No, No Internet Service);
Contract — Termo de contrato do cliente (Monthly, 1-Year, 2-Year);
PaperlessBilling — Se o cliente tem ou não boleto sem papel (Yes, No);
PaymentMethod — Método de pagamento do cliente(E-Check, Mailed Check, Bank Transfer (Auto), Credit Card (Auto)).

Obs: Nessa etapa realizou-se descrições informativas para verificar tipos dos dados, verificar descrição analítica dos dados numéricos, verificado se há dados nulos, realizado algumas agregações para gerar insights na análise.

3° Preparação dos Dados;
Nessa etapa realizou-se distribuição das variáveis em X (variáveis explicativas) e Y (variável target). Realizou-se a través do Label Enconder a transformação dos dados target em formato binário. Transformou-se variáveis explicativas categóricas em Dummies e, através do MinMaxScaler, normalizou-se as variáveis explicativas para que não houvesse impactos diferentes ao testar o modelo. 

4° Modelagem dos Dados;
Separou-se a base de dados em: variáveis explicativas para treino e teste e, variável target para treino e teste.
Aplicou-se o algoritmo de Logistic Regression na base de treino. Para mensurar a performance desse algoritmo aplicou-se a Matriz de Confusão e as seguintes métricas: acurácia, acurácia balanceada, precisão, recall, F1 e ROC AUC.
Após aplicou-se o algoritmo de Random Forest Classifier, também na base de treino. E da mesma maneira, para mensurar a sua performance, aplicou-se a Matriz de Confusão e as seguintes métricas: acurácia, acurácia balanceada, precisão, recall, F1 e ROC AUC. 
Para testar melhor performance, aplicou-se o algoritmo Random Forest com seus parâmetros tunados e após, repetiu-se a aplicação da métricas para verificar sua performance.

5° Validação;
Foi possível aplicar os algoritmos na base de dados, conseguiu-se mensurar suas performances.
Avaliado o desempenho dos modelos para verificar se foram atendidas todas as necessidades que foram definidas inicialmente, mensurando suas performances

**Resultado:**
O resultado final comparado teve melhor performance: algoritmo de classificação Random Forest.

