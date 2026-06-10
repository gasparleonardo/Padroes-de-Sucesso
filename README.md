# Análise Preditiva e Padrões de Sucesso no Mercado Global de Videogames

## Descrição do Projeto
Este projeto foi desenvolvido com foco em inteligência de mercado e análise preditiva de dados para a indústria de entretenimento (loja online fictícia *Ice*). O objetivo principal foi consolidar dados históricos de vendas, plataformas, gêneros e avaliações acumulados até 2016 para mapear o comportamento do consumidor, identificar padrões de sucesso comercial e prever tendências de mercado para o ano de 2017, subsidiando o planejamento de campanhas de publicidade direcionadas por dados (*data-driven marketing*).

---

## Tecnologias e Ferramentas Utilizadas
* **Linguagem:** Python
* **Análise e Manipulação de Dados:** Pandas e NumPy
* **Análise Estatística e Testes de Hipóteses:** SciPy (Módulo Stats)
* **Visualização de Dados:** Matplotlib e Seaborn
* **Ambiente de Desenvolvimento:** Jupyter Notebook

---

## Pipeline de Dados e Metodologia

### 1. Limpeza de Dados e Engenharia de Atributos
* Processamento de um dataset com mais de 16.000 registros para padronização de nomes de colunas e tratamento de valores ausentes.
* Investigação e tratamento da string descritiva `"TBD"` (*To Be Determined*) em notas de usuários, convertendo-as logicamente em valores nulos (`NaN`) para viabilizar cálculos estatísticos.
* Conversão de tipos de dados (`Year_of_Release` para inteiro e `User_Score` para float).
* Criação do KPI de **Vendas Globais Totais** por meio do somatório consolidado das métricas de vendas regionais (América do Norte, Europa, Japão e Outras Regiões).

### 2. Análise Exploratória de Dados (AED) & Ciclo de Vida
* Análise cronológica de lançamentos de jogos para compreender a dinâmica histórica da indústria.
* Identificação do **ciclo de vida médio de plataformas de jogos** (constatado em aproximadamente 10 anos de relevância comercial comercial).
* Aplicação de um filtro de recorte temporal estratégico (anos de 2013 a 2016) para mitigar o impacto de dados obsoletos e isolar o período ideal de projeção para o ano de 2017.
* Mapeamento de plataformas líderes em vendas globais (como PS4 e Xbox One) e construção de diagramas de caixa (*boxplots*) para analisar a dispersão de vendas globais por plataforma.

### 3. Fatores de Influência e Análise Regional (Perfis de Consumidores)
* Análise de correlação (através de diagramas de dispersão e coeficientes) para mensurar o impacto das notas de críticos (*Critic Score*) e usuários (*User Score*) no volume final de vendas.
* Desenvolvimento de análises comparativas de lucratividade versus popularidade por gênero de jogo.
* Criação de **Perfis Regionais de Consumo** isolando as 5 principais plataformas, os 5 principais gêneros e o impacto da classificação etária (ESRB Rating) para cada mercado: América do Norte (NA), Europa (EU) e Japão (JP).

### 4. Testes de Hipóteses Estatísticas
Validação científica de premissas de negócios utilizando o **Teste-t de Student** para amostras independentes com nível de significância de 5% ($\alpha = 0.05$):
* **Hipótese 1:** Avaliação se as classificações médias dos usuários das plataformas *Xbox One* e *PC* são iguais.
* **Hipótese 2:** Avaliação se as classificações médias dos usuários para os gêneros *Action* (Ação) e *Sports* (Esportes) diferem entre si.

---

## Principais Insights & Impacto de Negócio
* **Comportamento Regional Assimétrico:** O mercado consumidor de games não é homogêneo. Enquanto o Ocidente (América do Norte e Europa) concentra o faturamento em consoles de mesa (PS4/XOne) e gêneros como *Shooter* e *Action* com classificação madura (M), o mercado Japonês (Oriente) é dominado por plataformas portáteis (Nintendo 3DS) e pelo gênero *Role-Playing* (RPG).
* **Fator de Influência:** Descobriu-se que as notas de críticos profissionais possuem uma correlação positiva muito mais expressiva com o sucesso de vendas do que as notas dadas pelo público geral.
* **Validação Estatística:** O Teste-t confirmou com rigor matemático que a satisfação dos usuários é estatisticamente idêntica entre Xbox One e PC, mas varia significativamente entre os gêneros Action e Sports.
* **Direcionamento Comercial:** O diagnóstico gerou recomendações de alocação de orçamento de marketing customizadas: campanhas focadas em grandes produções do gênero *Shooter* no Ocidente e manutenção do ecossistema de RPGs portáteis para o mercado asiático.

---
