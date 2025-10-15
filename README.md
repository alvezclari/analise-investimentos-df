# Análise de Projetos de Investimento - Distrito Federal

## Sobre o Projeto
Este projeto tem como objetivo principal demonstrar a capacidade de construir um pipeline de processamento de dados (ETL - Extração, Transformação e Carga) e realizar uma análise exploratória sobre dados públicos de projetos de investimento no Distrito Federal.  
Os dados foram extraídos da **API ObrasGov.br**, especificamente do endpoint `/projeto-investimento`, filtrados para a Unidade Federativa (UF) do Distrito Federal (DF).

**Objetivos Específicos:**
1. Integrar-se com uma API pública (ObrasGov.br) para extrair dados de forma paginada.  
2. Tratar e normalizar dados complexos.  
3. Persistir os dados tratados em um banco de dados relacional (PostgreSQL).  
4. Gerar insights e visualizações que respondam a perguntas de negócio sobre os investimentos no DF.  

---

## Instalação
Para configurar e executar o projeto localmente, siga os passos abaixo:

1. **Clonar repositório:**
   ```bash
   git clone <(https://github.com/alvezclari/analise-investimentos-df.git)>
   cd analise-investimentos-df
2. **Criar ambiente virtual:** 
    ```bash
    python3 -m venv venv
    source venv/bin/activate  # No Linux/macOS
    venv\Scripts\activate  # No Windows
3. **Instalar dependências:** 
    ```bash
    pip install -r requirements.txt

## Como Executar 
O projeto é desenvolvido em um Jupyter Notebook, que guia através das etapas de extração, tratamento e análise dos dados. 

1. **Ativar o ambiente virtual** (se ainda não estiver ativo):
    ```bash
    source venv/bin/activate
2. **Iniciar o Jupyter Notebook:**
    ```bash
    jupyter notebook
3. No navegador, navegue até o diretório notebooks e abra o arquivo analise_completa.ipynb. Siga as células do notebook para executar a análise passo a passo.


## Estrutura do Projeto
   ```bash
analise-investimentos-df/
├── .env
├── .git/
├── notebooks/
│   ├── analise_completa.ipynb
│   ├── data/
│   │   ├── processed/
│   │   │   └── projetos_df_clean.csv
│   │   └── raw/
│   │       └── projetos_df_raw.json
│   └── visualizacoes/
│       ├── 01_distribuicao_valores.png
│       ├── 02_top_orgaos_barras.png
│       ├── 03_proporcao_orgaos_pizza.png
│       ├── 04_evolucao_temporal.png
│       ├── 05_box_status.png
│       ├── 06_contagem_status.png
│       └── 07_distribuicao_tipos_projeto.png
├── README.md
└── requirements.txt
```
## Tecnologias Utilizadas

- **Python**  
- **Pandas**  
- **Plotly**  
- **Jupyter Notebook**  
- **Requests** (para consumo da API)  
- **SQLAlchemy** (para persistência em banco de dados)  
- **PostgreSQL** (como banco de dados de destino)

