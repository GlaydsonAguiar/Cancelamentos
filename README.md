📉 Projeto – Análise de Cancelamento de Clientes
🧠 Objetivo
Analisar dados de clientes de uma empresa para entender padrões de cancelamento, identificando possíveis fatores que influenciam a decisão de sair, com base em variáveis como tipo de contrato, serviços utilizados e perfil de cliente.

📁 Dataset
Arquivo: cancelamentos.csv

Contém informações como:

Tipo de contrato

Serviços contratados

Tempo como cliente

Se o cliente cancelou ou não (cancelou)

🔧 Tecnologias Utilizadas
Python

Pandas – Leitura, limpeza e manipulação de dados

Plotly Express – Visualizações interativas

Jupyter Notebook – Desenvolvimento do projeto

📌 Etapas do Projeto
Importação e Leitura dos Dados

pd.read_csv("cancelamentos.csv")

Remoção da coluna CustomerID

Limpeza de Dados

Verificação de nulos e uso de dropna()

Análise Exploratória

Frequência de cancelamento (absoluto e %)

Comparações por tipo de contrato

Outras variáveis associadas

Visualizações com Plotly

Gráficos de barra, pizza e histogramas interativos

📈 Exemplo de Código
python
Copiar
Editar
import pandas as pd
import plotly.express as px

tabela = pd.read_csv("cancelamentos.csv")
tabela = tabela.drop("CustomerID", axis=1).dropna()

# Gráfico de cancelamento por tipo de contrato
grafico = px.histogram(tabela, x="tipo_contrato", color="cancelou")
grafico.show()
💡 Principais Insights
Cancelamentos são mais comuns em contratos mensais.

Clientes com planos de longo prazo têm maior retenção.

A análise ajuda a orientar estratégias de fidelização.

🚀 Próximos Passos
Modelagem preditiva com Machine Learning

Agrupamento de clientes com clustering

Criação de dashboard interativo
