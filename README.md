<div align="center">
  
# 🐟 Cubo Gelatinoso — Concentração de Mercúrio em Peixes 🐟

Entrega individual introdutória da disciplina de Aprendizado de Máquina, ministrada pelo Prof. Dr. Daniel R. Cassar, no curso de Ciência e Tecnologia, Ilum Escola de Ciência (segundo semestre de 2026).

O projeto utiliza o algoritmo **k-Nearest Neighbours ($k$-NN)** para induzir um modelo preditivo capaz de estimar a concentração de mercúrio (ng/g) em peixes a partir de atributos como peso, comprimento, espécie, estado e local de coleta. O dataset utilizado é proveniente da *National Coastal Condition Assessment* (NCCA), conduzida pela *U.S. Environmental Protection Agency* (EPA).

Ao longo do trabalho, diferentes conjuntos de hiperparâmetros foram testados — variando o número de vizinhos ($k$), a métrica de distância (euclidiana, manhattan e chebyshev) e a estratégia de normalização dos atributos numéricos (`StandardScaler` e `MinMaxScaler`) — a fim de identificar a configuração com melhor desempenho preditivo, avaliada por meio do erro absoluto médio (MAE) e do coeficiente de determinação (R²).

# 🛠️ Ferramentas Utilizadas 🛠️

### Nota sobre o uso de IA

Foram utilizadas ferramentas de Inteligência Artificial generativa, Claude (Anthropic) e Copilot (Microsoft), em conjunto para: auxílio no uso das bibliotecas `pandas`, `NumPy` e `scikit-learn`, esclarecimento de dúvidas conceituais sobre aprendizado de máquina; formulação do código dos gráficos comparativos, depuração de erros durante o desenvolvimento e revisão gramatical dos textos em Markdown. As decisões técnicas finais - como a escolha de atributos, hiperparâmetros, métricas de avaliação e interpretação dos resultados - são de autoria própria.

</div>

### Bibliotecas e Módulos

* [pandas](https://pandas.pydata.org/)
* [scikit-learn](https://scikit-learn.org/)
* [seaborn](https://seaborn.pydata.org/)
* [Matplotlib](https://matplotlib.org/)
* [NumPy](https://numpy.org/)

#### Versão do Python

* Python 3.13

<div align="center">
  
# 💻 Instalação e Instruções 💻

### Instalação do Código

O código principal deste projeto é o arquivo `Cubo\_gelatinoso.ipynb`. Junto com ele, é necessário o arquivo `ncca20\_hg\_fishplug.csv`, que contém os dados de mercúrio em tecido de peixe utilizados no trabalho.

Ao realizar o download, é possível perceber que o arquivo é um Jupyter Notebook, ou seja, deve ser rodado em programas que possuam um Jupyter Kernel, como o JupyterLab ou o Visual Studio Code.

⚠️ IMPORTANTE ⚠️

Para o funcionamento correto do código, é essencial que o arquivo `ncca20\_hg\_fishplug.csv` esteja salvo no mesmo diretório do notebook.

### Instalação das Bibliotecas

Antes de executar o notebook, é preciso garantir que as bibliotecas citadas anteriormente estejam instaladas no ambiente Python utilizado. Caso alguma delas não esteja, basta criar uma nova célula no notebook, digitar **pip install** *(nome da biblioteca)* e executar. Por exemplo, para instalar o scikit-learn, basta digitar `pip install scikit-learn`.

### Como Usar:

</div>

1. Abra o `Cubo\_gelatinoso.ipynb` e execute as células em ordem (recomenda-se "Restart Kernel and Run All" para garantir reprodutibilidade).
2. O notebook realiza, em sequência: carregamento e tratamento dos dados, análise exploratória e seleção de atributos, divisão treino/teste, codificação e normalização, indução do modelo baseline e do modelo $k$-NN sob diferentes hiperparâmetros.
3. Ao final, são exibidos gráficos comparando o desempenho das configurações testadas, além do gráfico de valores previstos *vs.* valores reais para o modelo final selecionado.

<div align="center">
  
# 📂 Sobre o Dataset 📂

O dataset (`ncca20\_hg\_fishplug.csv`) é proveniente da *National Coastal Condition Assessment* (NCCA), conduzida pela *U.S. Environmental Protection Agency* (EPA), e contém medições de concentração de mercúrio em tecido de peixes coletados em diferentes estados e corpos d'água dos Estados Unidos.

# ⚠️ Limitações do Modelo ⚠️

</div>

* O modelo final explica cerca de um terço (R² ≈ 0,337) da variação da concentração de mercúrio, indicando que outros fatores não capturados pelo dataset (idade do peixe, posição na cadeia alimentar, características específicas de cada corpo d'água) provavelmente influenciam a contaminação observada.
* Foi identificada uma subestimação das concentrações mais altas de mercúrio, um comportamento característico de algoritmos baseados em vizinhança quando a distribuição do alvo é concentrada em valores baixos.

<div align="center">
  
Uma discussão mais detalhada está disponível na seção de Conclusões do próprio notebook.

# 👤 Desenvolvedor do Projeto 👤

[<img src="https://github.com/PangioAAA.png" width=200><br><sub>✨Giovanni de Almeida Moreira✨</sub>](https://github.com/PangioAAA)

**Giovanni A. Moreira** (2610060)

Aluno do curso de Ciência e Tecnologia, Ilum Escola de Ciência

</div>

* Desenvolveu integralmente o pipeline de tratamento de dados, seleção de atributos e indução do modelo $k$-NN
* Testou e comparou diferentes hiperparâmetros (número de vizinhos, métrica de distância) e estratégias de normalização
* Interpretou os resultados obtidos à luz das limitações do algoritmo e do contexto de avaliação de risco ambiental

<div align="center">
  
Agradecimento especial ao professor da disciplina de Aprendizado de Máquina, por todo o aprendizado:

⭐ Professor Daniel Roberto Cassar

</div>

# 📚 Referências 📚

\[1] CASSAR, Daniel Roberto. ATP-203 2.1 - Aprendizado de máquina, k-NN e métricas. Notebook de aula, disciplina de Aprendizado de Máquina, Ilum, Escola de Ciência, 2026. Disponibilizado pelo docente.

\[2] CASSAR, Daniel Roberto. LMA-203 1.0. Notebook de aula, disciplina de Aprendizado de Máquina, Ilum, Escola de Ciência, 2026. Disponibilizado pelo docente.

\[3] CASSAR, Daniel Roberto. ATP-203 2.2 - Divisão de dados em treino e teste. Notebook de aula, disciplina de Aprendizado de Máquina, Ilum, Escola de Ciência, 2026. Disponibilizado pelo docente.

\[4] CASSAR, Daniel Roberto. ATP-203 3.0 - Modelo linear e baseline. Notebook de aula, disciplina de Aprendizado de Máquina, Ilum, Escola de Ciência, 2026. Disponibilizado pelo docente.

\[5] UNITED STATES ENVIRONMENTAL PROTECTION AGENCY (EPA). National Coastal Condition Assessment (NCCA): mercury in fish fillet plug tissue samples, 2020-2022 (ncca20\_hg\_fishplug.csv). Washington, D.C.: U.S. EPA, 2024. Disponível em: https://www.epa.gov/national-aquatic-resource-surveys/data-national-aquatic-resource-surveys. Acesso em: 5 set. 2026.

\[6] AGENCY FOR TOXIC SUBSTANCES AND DISEASE REGISTRY (ATSDR). ToxFAQs for Mercury. Atlanta: U.S. Department of Health and Human Services, 2022. Disponível em: https://wwwn.cdc.gov/TSP/ToxFAQs/ToxFAQsDetails.aspx?faqid=113&toxid=24. Acesso em: 20 set. 2026.

\[7] FACELI, Katti; LORENA, Ana Carolina; GAMA, João; et al. Inteligência Artificial: uma abordagem de Aprendizado de Máquina. 2. ed. Rio de Janeiro: LTC, 2021.
