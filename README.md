# Análise Exploratória de Dados (EDA) - World Happiness Report 2019

**Candidato:** João Carlos Oliveira da Silva  
**Processo Seletivo:** SYNAPTA - Análise de Dados  

## Objetivo e Problema de Negócio
O objetivo deste projeto é identificar e quantificar os fatores macroeconómicos e sociais que exercem maior impacto no grau de felicidade e bem-estar global. A análise procura responder à seguinte questão central: *Quais são os pilares sociais e económicos que determinam a prosperidade de uma nação, e como se manifesta a desigualdade interna entre as diferentes regiões do globo?* 

Foi adotada uma abordagem estritamente descritiva e focada na governança da informação, abdicando de modelos preditivos em prol de uma comunicação clara de *insights* reais.

## Fonte dos Dados
Os dados utilizados nesta análise têm origem no estudo anual global de bem-estar.
* **Dataset:** [World Happiness Report 2019](https://www.kaggle.com/datasets/unsdsn/world-happiness)
* **Plataforma:** Kaggle (licença pública respeitada conforme as diretrizes originais).

## Dicionário de Variáveis
* **Overall rank:** Posição geral do país no ranking mundial.
* **Country or region:** Nome do país ou região avaliada.
* **Score:** Pontuação total de felicidade (métrica principal).
* **GDP per capita:** Riqueza económica (Produto Interno Bruto por pessoa).
* **Social support:** Rede de amparo estatal, familiar ou comunitária.
* **Healthy life expectancy:** Expectativa de vida com saúde de qualidade.
* **Freedom to make life choices:** Nível de liberdade individual para a tomada de decisões.
* **Generosity:** Disposição da população para doações e ajuda mútua.
* **Perceptions of corruption:** Confiança da população nas instituições e perceção de corrupção.
* **Continente:** Variável derivada, criada via código para permitir a análise de disparidades regionais.

## Ferramentas e Tecnologias
* **Linguagem:** Python
* **Manipulação de Dados:** Pandas, pycountry_convert
* **Visualização:** Matplotlib, Seaborn
* **Ambiente de Desenvolvimento:** Google Colab (prototipagem e formatação executiva via nbconvert) e Visual Studio Code.
* **Versionamento:** Git e GitHub

## Limpeza e Preparação dos Dados
1. **Auditoria Estrutural:** Verificação inicial da volumetria (156 países e 9 variáveis).
2. **Validação de Qualidade:** Confirmação da ausência de valores nulos (NaN) e de registos duplicados no *dataset*.
3. **Engenharia de Recursos (Feature Engineering):** Implementação de uma função de mapeamento utilizando a biblioteca `pycountry_convert` para categorizar cada "Country or region" no seu respetivo "Continente", permitindo a agregação espacial dos dados.
4. **Cálculo de Disparidade:** Extração simultânea da Média e da Mediana global e continental para detetar assimetrias e "falsas prosperidades" inflacionadas por elites regionais.

## Resultados e Principais Conclusões
A exploração visual e matemática dos indicadores consolidou cinco *insights* executivos:
1. **Confiança Institucional:** A transparência governamental impulsiona positivamente o desempenho de todos os restantes indicadores sociais.
2. **Impacto na Solidariedade:** A perceção de alta corrupção combinada com baixa liberdade individual está diretamente associada à queda sistêmica da generosidade.
3. **Saúde e Amparo:** A expectativa de vida com qualidade depende intrinsecamente de uma forte rede de amparo social (Social support), superando o peso isolado da infraestrutura clínica.
4. **O Peso da Liberdade:** A liberdade de escolha e o apoio comunitário possuem um impacto superior ao PIB per capita isolado na determinação do topo do ranking mundial.
5. **Generosidade como Sobrevivência:** Em regiões com grave déficit de apoio estatal (ex: África Subsaariana), a alta generosidade manifesta-se como um mecanismo essencial de sobrevivência estruturado pela própria comunidade.

## Limitações da Análise
* **Correlação vs. Causalidade:** As associações matemáticas e visuais apresentadas representam tendências de correlação fortes, e não provas absolutas de causalidade direta.
* **Corte Temporal:** O conjunto de dados reflete exclusivamente o cenário sociopolítico e económico de 2019, não contemplando impactos sistémicos posteriores (como a pandemia global).
* **Fatores Ocultos:** A base de dados é estritamente quantitativa, carecendo de variáveis qualitativas que traduzam as nuances culturais, históricas e climáticas intrínsecas a cada nação.

## Declaração de Uso de Inteligência Artificial Generativa
Declaro que ferramentas de Inteligência Artificial Generativa foram utilizadas estritamente como assistentes de produtividade durante o desenvolvimento deste projeto (suporte na sintaxe, diagramação visual do Markdown e organização do versionamento via Git). Toda a lógica de programação exploratória, escolha de cruzamentos analíticos (Média vs. Mediana) e a formulação das conclusões e limitações metodológicas são de minha autoria intelectual direta.

## Instruções de Execução
Para replicar esta análise localmente:
1. Clone este repositório: `git clone https://github.com/JoaoCarlos-collab/nome-do-repositorio.git`
2. Certifique-se de ter o Python 3 instalado.
3. Instale as dependências executando: `pip install -r requirements.txt`
4. O *dataset* `World Happiness Report 2019.csv` já se encontra na raiz do projeto (ou na pasta `/Data`).
5. Abra o ficheiro `World_Happiness_Report_2019.ipynb` no Visual Studio Code, Jupyter Notebook ou faça o upload para o Google Colab para executar as células passo a passo.
6. O relatório executivo final pode ser consultado diretamente abrindo o ficheiro PDF anexado neste repositório.
