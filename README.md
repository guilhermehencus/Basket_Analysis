# Basket Analysis  

## *Explicação Breve* 
Supermercados passaram a buscar pela otimização e melhoraria de seu serviço para assim alcançar seus clientes através da tecnologia. 
Este trabalho possui o objetivo de estabelecer um algoritmo Apriori a partir da mineração de dados, 
desenvolvendo um modo capaz de sugerir a um determinado cliente um produto similar a aquele que foi inserido no carrinho de compras, por conseguinte, 
definir uma associação de produtos.  
## *Envolvidos*  
1. [Guilherme Henrique Guimarães Custódio](https://github.com/guilhermehencus)
2. Maria Eduarda da Silva Cabral
3. [Matias Ricardo Muente Castro](https://github.com/MatiasRicardoMuenteCastro)
## *Detalhes*  
Todos os dados foram obtidos de um projeto [INSTACART](https://www.kaggle.com/c/instacart-market-basket-analysis/data) no Kaggle. O projeto foi dividido em quatro fases: 
inicial, procedural, desenvolvimento do algoritmo e a fase final. A fase inicial se trata do entendimento do projeto, da aplicação do Canvas e da apresentação da ideia. 
A seguir, a parte prática se iniciou em união a fase procedural. Nesse ponto, a compreensão de dados tornou-se necessária sobre a base de dados, 
seguida pela mineração e análise de dados - com auxílio de uma linguagem de consulta (SQL) e da tarefa de preparação de dados chamada transpose, 
realizada com o CLI (Command Line Interface) do GITHUB. Já na fase de desenvolvimento do algoritmo, a criação do apriori foi feita. Por fim, a 
revisão do projeto se iniciou em união a implementação e relatório abordando todos os processos do projeto.  

Na primeira tentativa de fazer o algoritmo Apriori foi utilizada a biblioteca Pandas, porém pelo tamanho do Dataset o Pandas não conseguiu 
carregá-lo por completo. Após um tempo com o algoritmo rodando, foi retornado um erro de alocação de Memória RAM, além disso o algoritmo que 
foi pego como base estava fazendo uma contagem de suporte diferentemente do que a convencional, contando ele por inteiros, o que pode ter sido um catalisador do erro.  

Na segunda tentativa foi-se utilizada a Biblioteca Spark, que consegue realizar operações e manipulações de conjuntos de dados de 
forma mais rápida e eficiente quando comparada ao Pandas.  

Nessa tentativa para ser capaz de realizar o processamento do conjunto de dados no algoritmo Apriori, foram reduzidas as linhas do conjunto de dados de 130.000 para 80.000 e diferentemente do outro algoritmo, foi-se adicionado o parâmetro de confiança. Com esse algoritmo, o algoritmo Apriori conseguiu ser executado, porém o tempo de execução era muito elevado e os resultados pegos com o nível de suporte e confiança eram só dois, caso esses níveis fossem de 0.006 de suporte e 0.085 o programa depois de 
um longo tempo de carregamento retornava um erro.  

Houve uma última tentativa, na qual foram utilizadas duas bibliotecas, o Pandas para fazer a leitura do arquivo e o 
Mlxtend que é uma biblioteca focada especialmente em Machine Learning. Essa biblioteca recebia um DataFrame em Pandas, 
o suporte e a confiança mínimos que foram colocados são de 0.006 e 0.085, respectivamente, 
desse modo o tempo de execução foi baixo e retornou 95 resultados no total.  

Houve o desenvolvimento do script [Assosciation.py](https://github.com/guilhermehencus/Basket_Analysis/blob/master/Assosciation.py) para substituir os ID’s dos 
produtos pelo seu nome, além disso esse script, com ID do corredor irá pegar o corredor em que esse produto se encontra, para assim substituir os ID’s dos 
produtos pelos seus nomes e determinar seus corredores. Como existem colunas para os ID’s dos produtos antecedentes e consequentes, 
serão criadas as colunas para os corredores dos produtos antecedentes e consequentes. No final de tudo foi gerando
o arquivo csv [FinalAssociation.csv](https://github.com/guilhermehencus/Basket_Analysis/blob/master/Data/FinalAssociation.csv).
## *Resultado* 
 Por fim, uma avaliação foi feita sobre o projeto e analisou-se tudo que fora produzido, para que fosse possível a 
 conclusão do relatório e a sua implementação por parte do SharePoint – uma plataforma da Microsoft que permite a criação 
 de portais e sua aplicação no ambiente Web.  
 
 ![Resultado](https://user-images.githubusercontent.com/111579476/188933871-7207a9f8-561f-4320-8515-af562a9e35d9.png)





