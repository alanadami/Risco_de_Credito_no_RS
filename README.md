Análise do Risco de Crédito no Rio Grande do Sul a partir do SCR

Este repositório apresenta uma análise exploratória e temporal do risco de crédito no Rio Grande do Sul, utilizando dados agregados do Sistema de Informações de Crédito (SCR) do Banco Central do Brasil. O objetivo do projeto é compreender a relação entre inadimplência e ativo problemático, bem como posicionar o comportamento do estado em relação ao agregado nacional, adotado como benchmark.

O trabalho é dividido em dois notebooks, cada um com um papel analítico distinto e complementar.

📊 Objetivos do Projeto

Compreender a estrutura e o significado das principais métricas do SCR

Avaliar o nível de risco da carteira de crédito do RS em comparação ao Brasil

Investigar a relação entre ativo problemático e inadimplência

Analisar se o ativo problemático atua como indicador contemporâneo ou antecedente da inadimplência

Construir uma análise honesta, interpretável e alinhada às limitações dos dados agregados

🗂 Estrutura do Repositório<br>
<br>
├── EDA_rs.ipynb   # Análise exploratória e conceitual (mês específico – RS)<br>
├── analise_rs_br.ipynb   # Análise temporal e comparativa (2024–2025 – RS x Brasil)<br>
└── README.md<br>

📘 Notebook 01 - EDA_rs — Análise Exploratória e Conceitual (RS)

O primeiro notebook tem como foco o entendimento profundo do dataset e das métricas do SCR, utilizando um recorte mensal do Rio Grande do Sul.

Principais atividades:

Interpretação conceitual das variáveis do SCR

Identificação de variáveis identificadoras e métricas

Análise da carteira ativa, vencida, inadimplente e ativo problemático

Justificativa do uso de percentuais em vez de valores absolutos

Leitura econômica das métricas à luz da literatura do Banco Central

Objetivo central:

Garantir que as métricas sejam corretamente compreendidas antes de qualquer análise temporal ou comparação regional.

📕 Notebook 02 — analise_rs_br — Análise Temporal e Comparativa (RS × Brasil)

O segundo notebook desenvolve a análise principal do projeto, utilizando uma série mensal contínua de janeiro de 2024 a outubro de 2025.

Principais etapas:

Consolidação de múltiplos arquivos mensais do SCR

Conversão correta de tipos numéricos antes da agregação

Construção de séries mensais por UF e do agregado nacional

Criação de indicadores percentuais:

% inadimplência

% ativo problemático

Comparação temporal entre RS e Brasil

Análises gráficas:

colunas clusterizadas

<img width="1389" height="590" alt="image" src="https://github.com/user-attachments/assets/3f2c4a3d-c15e-41ee-9956-1c7872f14196" />

<img width="1389" height="590" alt="image" src="https://github.com/user-attachments/assets/b1184131-0f56-40bc-b9f9-35df5af29179" />

dispersão

<img width="590" height="490" alt="image" src="https://github.com/user-attachments/assets/06a32e14-ef63-4e5b-89da-99e3ac8b588d" />

<img width="589" height="490" alt="image" src="https://github.com/user-attachments/assets/d8d9907f-e1c0-4db2-9cbe-366bf7e3bfc9" />


Análise contemporânea (t) e defasada (t → t+1)

<img width="590" height="490" alt="image" src="https://github.com/user-attachments/assets/ebc1a296-c4d8-4e59-a313-fd662fba35fd" />

<img width="1589" height="590" alt="image" src="https://github.com/user-attachments/assets/f375d229-e875-491d-8e6f-68735c0a9af6" />


🔍 Principais Resultados

O Rio Grande do Sul apresentou, de forma consistente, níveis de inadimplência inferiores ao agregado nacional, embora acompanhe as oscilações do ciclo macroeconômico.

O ativo problemático apresenta forte associação contemporânea com a inadimplência, funcionando como um termômetro da saúde da carteira.

Ao introduzir uma defasagem de um mês, a relação entre ativo problemático e inadimplência futura permanece positiva, porém mais fraca, indicando antecedência parcial, mas não capacidade preditiva forte.

A análise sugere que o ativo problemático não deve ser interpretado como preditor determinístico, mas como indicador de risco latente e estresse financeiro da carteira.

🤔 Por que não foi utilizado um modelo preditivo?

Optou-se deliberadamente por não empregar modelos preditivos formais neste projeto pelas seguintes razões:

Série temporal curta (22 observações mensais), insuficiente para estimativas robustas sem risco elevado de overfitting

Dados altamente agregados, que limitam a identificação de relações causais e reduzem a eficácia de abordagens preditivas

Objetivo analítico voltado à compreensão econômica e prudencial dos indicadores, e não à previsão operacional

A priorização de uma análise exploratória rigorosa garante maior interpretabilidade e alinhamento com as limitações do dado disponível.

🧠 Conclusão

O projeto demonstra que o ativo problemático é um indicador relevante para o monitoramento prudencial do risco de crédito, refletindo o grau de fragilidade financeira presente na carteira em determinado momento. Sua utilidade reside principalmente como termômetro contemporâneo, e não como instrumento de previsão isolada da inadimplência futura.

Análises futuras poderiam aprofundar o estudo por meio da desagregação por unidade federativa, da incorporação de séries temporais mais longas ou da inclusão de variáveis macroeconômicas adicionais.

## Dados

Os dados utilizados neste projeto são provenientes do Sistema de Informações de Crédito (SCR) do Banco Central do Brasil.
Devido ao volume dos arquivos, os dados brutos não estão versionados neste repositório.
Os dados podem ser baixados no seguinte link:
https://www.bcb.gov.br/pda/desig/scrdata_{ANO}.zip (Substituindo a expressão ANO, pelo ano desejado, no caso deste notebook, 2024 e 2025, este até outrubo)

🛠 Tecnologias Utilizadas

Python

Pandas

NumPy

Matplotlib

Jupyter Notebook

👤 Autor

Projeto desenvolvido como estudo aplicado em Análise de Dados e Risco de Crédito, com foco em dados regulatórios do sistema financeiro brasileiro.
