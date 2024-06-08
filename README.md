# Estudo e Análise do Dataset de Taxi Rides de 2009

Este repositório contém uma série de notebooks que exploram, analisam e comparam diferentes bibliotecas de processamento de dados e modelagem de machine learning usando o dataset de taxi rides de 2009. O objetivo é avaliar a eficiência de diversas bibliotecas para operações de processamento de dados em diferentes amostras do dataset e criar pipelines de machine learning para prever o valor da tarifa (`fare_amt`). A seguir, é apresentada uma descrição detalhada dos notebooks incluídos e as suas respectivas funções.

## Notebooks

### 1. `dask_koalas`
- **Objetivo:** Introdução e estudo comparativo usando as bibliotecas Dask e Koalas.
- **Descrição:** Este notebook fornece uma introdução ao dataset e realiza um estudo detalhado usando Dask e Koalas. Benchmarks são calculados para operações de processamento de dados usando três amostras diferentes do dataset de 2009. Uma avaliação mais profunda é realizada com `cprofile`.
- **Plataforma:** Executado numa Máquina Virtual (VM), criada no Google Cloud Platform.

### 2. `modin_joblib`
- **Objetivo:** Estudo do dataset usando as bibliotecas Modin + Dask e Joblib.
- **Descrição:** Este notebook calcula benchmarks para operações de processamento de dados usando três amostras diferentes (dos três primeiros meses, dos dois primeiros meses e do primeiro mês de 2009). Uma avaliação mais profunda é realizada com `cprofile` para analisar a eficiência das operações.
- **Plataforma:** Executado numa Máquina Virtual (VM), criada no Google Cloud Platform.

### 3. `rapids`
- **Objetivo:** Estudo do dataset usando a biblioteca Dask + RAPIDS.
- **Descrição:** Semelhante ao notebook `modin_joblib`, este notebook calcula benchmarks para operações de processamento de dados usando três amostras diferentes do dataset de 2009. A avaliação de desempenho é aprofundada com `cprofile`.
- **Plataforma:** Executado através do Google Colab.

### 4. `comparacoes`
- **Objetivo:** Comparar as bibliotecas usadas nos estudos anteriores.
- **Descrição:** Este notebook compara a eficiência e desempenho das bibliotecas Dask, Koalas, Modin, Joblib e RAPIDS para operações de processamento de dados. A análise inclui benchmarks e resultados das avaliações feitas com `cprofile`.
- **Plataforma:** Executado numa Máquina Virtual (VM), criada no Google Cloud Platform.

### 5. `ML`
- **Objetivo:** Criar pipelines de machine learning para prever `fare_amt`.
- **Descrição:** Este notebook foca na construção de pipelines de pré-processamento e modelagem para prever o valor da tarifa (`fare_amt`) usando dois modelos de machine learning. O processo inclui a divisão dos dados, pré-processamento, treino, e avaliação dos modelos.
- **Plataforma:** Executado numa Máquina Virtual (VM), criada no Google Cloud Platform.


## Ambiente de Execução

- **Máquina Virtual (VM):** Usada para os notebooks `dask_koalas`, `modin_joblib`, `comparacoes` e `ML`.
- **Google Colab:** Usado para o notebook `rapids`.

## Como Executar

1. **Download dos ficheiros:**
   - Realize o download dos 5 notebooks: `dask_koalas.ipynb`, `modin_joblib.ipynb`, `rapids.ipynb`, `comparacoes.ipynb` e `ML.ipynb` 

2. **Instalar Dependências:**
   - Para notebooks em VM:
     
   - Para notebook em Colab:
     Siga as instruções no próprio notebook `rapids` para instalar as dependências necessárias.

3. **Executar os Notebooks:**
   - Abra os notebooks desejados e execute as células sequencialmente.

## Como ler 
Sugere-se que a leitura dos notebooks seja feita pela ordem indicada acima. Assim, inicie no notebook `dask_koalas`, visto que contém a introdução do trabalho, seguindo-se de `modin_joblib`, `rapids` e `comparacoes`. Por fim, explore a tarefa de Machine Learning no notebook `ML`.

## Resultados dos benchmarks
Os resultados dos benchmarks foram guardados num ficheiro zip `resultados`.