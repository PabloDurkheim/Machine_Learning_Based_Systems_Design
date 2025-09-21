# Previsão de Preços do Airbnb no Rio de Janeiro com PyTorch

## 📖 Visão Geral do Projeto

Este projeto tem como objetivo desenvolver um modelo de regressão de alta performance para prever os preços de diárias de imóveis na cidade do Rio de Janeiro, utilizando dados da plataforma **Airbnb**. O desenvolvimento segue um pipeline completo de Ciência de Dados, desde a limpeza e o pré-processamento dos dados até a construção de uma rede neural customizada com **PyTorch**, comparando seus resultados com um baseline de modelos de Machine Learning tradicionais.

---

## 🚀 Pipeline do Projeto

O fluxo de trabalho foi estruturado para garantir a qualidade e a robustez do modelo final, seguindo as seguintes etapas:

1.  **Seleção de Features:** Análise e escolha de um conjunto de features relevantes que capturam os principais fatores que influenciam o preço de um aluguel, como atributos do anfitrião, localização, características da propriedade e popularidade.
2.  **Limpeza e Pré-processamento:** Execução de um pipeline de tratamento que incluiu:
    * Correção de tipos e formatos de dados (ex: `price`, `host_response_rate`).
    * Engenharia de features para extrair informações úteis (ex: `bathrooms_text`).
    * Imputação de valores ausentes usando mediana para dados numéricos e moda para categóricos.
    * Conversão de todas as features para um formato numérico através de binarização e *One-Hot Encoding*.
3.  **Tratamento de Outliers:** Utilização do método estatístico **Intervalo Interquartil (IQR)** para identificar e remover dados extremos que poderiam distorcer o treinamento do modelo, resultando em um dataset mais limpo.
4.  **Normalização e Divisão:** Normalização de todas as features para a escala [0, 1] com o `MinMaxScaler` e, em seguida, divisão dos dados em conjuntos de **treino (80%)** e **teste (20%)**.
5.  **Modelagem e Avaliação:**
    * **Baseline:** Criação de um ponto de referência de desempenho com `LazyPredict`, que treinou e avaliou dezenas de modelos de Machine Learning tradicionais.
    * **Modelo Principal:** Desenvolvimento, treinamento e avaliação de uma rede neural customizada com `PyTorch`.

---

## 🛠️ Tecnologias e Bibliotecas Utilizadas

Este projeto foi desenvolvido utilizando as seguintes tecnologias:

-   **Python 3.x**
-   **Jupyter Notebook** como ambiente de desenvolvimento.
-   **Pandas** e **NumPy** para manipulação e análise de dados.
-   **Scikit-learn** para pré-processamento e divisão dos dados.
-   **PyTorch** para a construção e treinamento do modelo de Deep Learning.
-   **LazyPredict** para a criação do baseline de modelos.
-   **Matplotlib** e **Seaborn** para visualização de dados (utilizados na análise exploratória).

---

## ⚙️ Como Executar o Projeto

Para replicar os resultados, siga os passos abaixo:

1.  **Clone o repositório:**
    ```bash
    git clone [https://github.com/seu-usuario/nome-do-repositorio.git](https://github.com/seu-usuario/nome-do-repositorio.git)
    cd nome-do-repositorio
    ```

2.  **Crie um ambiente virtual (recomendado):**
    ```bash
    python -m venv venv
    source venv/bin/activate  # No Windows: venv\Scripts\activate
    ```

3.  **Instale as dependências:**
    O projeto requer algumas bibliotecas. Você pode instalá-las com o pip:
    ```bash
    pip install requirements.txt
    ```
    *Nota: Pode ser necessário instalar o PyTorch seguindo as instruções específicas do site oficial para a sua configuração de hardware (CPU/GPU): https://pytorch.org/*

4.  **Execute o Jupyter Notebook:**
    Abra o arquivo `versão_beta.ipynb` em um ambiente Jupyter para ver todo o processo de desenvolvimento e os resultados.
    ```bash
    jupyter notebook "versão_beta.ipynb"
    ```
5.  **Dados:**
    Certifique-se de que o arquivo `listings.csv` (dataset do Airbnb) esteja no mesmo diretório do notebook.

---
