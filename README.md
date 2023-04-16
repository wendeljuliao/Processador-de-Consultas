# Processador-de-Consultas

Implementar um Processador de Consultas
1. Interface gráfica obrigatória mostrando o funcionamento do processador de consultas.
2. Funcionalidades principais:
a. Parser (Análise) de uma consulta SQL;
b. Geração do grafo de operadores da consulta;
c. Ordem de execução da consulta;
d. Exibição dos resultados na interface gráfica;
3. Entidades/estruturas e algoritmos a serem implementadas (sugestão -> usando POO como
padrão):
a. Parser: componente que analisa e separa os componentes principais da string com a
consulta SQL. Pode ser implementado por meio de expressões regulares. Limitaremos o
parse a:
i. Select, From, Where, Join On (duas ou mais tabelas);
ii. Operadores =, >, <, <=, >=, <>, And, In, Not In, ( , ) ;
b. Grafo de operadores: estrutura de dados grafo com a representação interna da consulta,
onde os nós são os operadores/tabelas/constantes e as arestas representam a direção do
fluxo dos resultados intermediários, assim como os predicados que os objetos devem
satisfazer. Representa a estratégia básica de execução da consulta para gerar o resultado.
c. Processador de consultas simples: recebe o grafo de operadores como entrada, percorre o
grafo e gera a ordem de execução correspondente.
4. Banco de Dados:
a. O banco de dados interno a ser representado deve se basear no modelo que segue;
b. Se desejarem criar o banco, serão fornecidos os Scripts para criação e carga do banco de
dados para o MySQL, sendo que os Arquivos devem ser executados na ordem e servem
como exemplo.
5. Heurísticas Básicas a serem usadas
a. Aplicar primeiro as operações que reduzem o tamanho dos resultados intermediários
i. operações de seleção - reduzem o número de tuplas
ii. operações de projeção - reduzem o número de atributos
b. Aplicar primeiro as operações de seleção e de junção mais restritivas
i. reordenar os nós folha da árvore de consulta
ii. evitar a operação de produto cartesiano
iii. ajustar o restante da árvore de forma apropriada
6. Funcionamento:
a. A string com a consulta SQL é entrada na GUI;
b. A string é parseada;
c. O grafo de operadores é construído;
d. O grafo de operadores deve ser mostrado na GUI;
e. A consulta é estruturada usando o grafo como entrada;
f. O resultado da consulta mostrando cada operação e a ordem que será executada, é exibido
na GUI.
