# 1 - All In One Place (Projeto solucionado utilizando técnicas de clusterização na linguagem R)
Neste trabalho foi criado um programa de fidelidade para a empresa de Outlet multimarcas All In One Place. Esse programa foi criado utilizando a técnica de clusterização e a linguagem R.

-------------------------||------------------------------

A empresa All In One Place
(O contexto a seguir é completamente fictício, a empresa, o contexto, o CEO, as perguntas de negócio existem somente na minha imaginação)

A empresa All in One Place é uma empresa Outlet Multimarcas, ou seja, ela comercializa produtos de segunda linha de várias marcas a um preço menor, através de um e-commerce.

Em pouco mais de 1 anos de operação, o time de marketing percebeu que alguns clientes da sua base, compram produtos mais caros, com alta frequência e acabam contribuindo com uma parcela significativa do faturamento da empresa.

Baseado nessa percepção, o time de marketing vai lançar um programa de fidelidade para os melhores clientes da base, chamado Insiders. Mas o time não tem um conhecimento avançado em análise de dados para eleger os participantes do programa.

Por esse motivo, o time de marketing requisitou ao time de dados uma seleção de clientes elegíveis ao programa, usando técnicas avançadas de manipulação de dados.

Objetivo: Determinar quem são os clientes elegíveis para participar de um programa de fidelidade da empresa All In One Place?

Para o programa de fidelidade a empresa queria os clientes que mais gastavam dinheiro na All In One Place e também aqueles que compravam mais produtos. Para encontrarmos esses clientes, após a limpeza dos dados, decidimos agrupar os clientes considerando a quantidade total da compra de produtos e também pela quantidade gasta por produto por cliente. Testamos três algoritmos de cluster diferentes k-means, cluster hierárquico e o dbscan. 

- O método de clusterização baseado em densidade, DBSCAN, não se mostrou um bom método para o nosso propósito. Ele selecionou a parte mais densa da nossa base de dados, que eram os clientes que menos gastavam e menos compravam na empresa All In One Place e colocou os outros clientes como outliers. Por este motivo decidimos descartar a análise por este método.

- Para a utilização do método k-means, que é um método baseado em centróides, utilizamos o método da silhueta e o método elbow para encontrarmos o número ideal de clusters. O método da silhueta indicou que o deveríamos selecionar 2 clusters e o método elbow indicou que poderiam ser 2 ou 4 clusters. Após uma análise visual decidimos que o ideal seriam 2 clusters. Analisando os dois clusters selecionados escolhemos aquele de nosso interesse. Verificamos que, para nosso propósito, foram selecionados 19 clientes, o correspondente a  0.44 % da base de dados e que esses clientes foram responsáveis por 21.64% dos produtos comprados e por 72.63% do dinheiro gasto na loja.

- Para o método de clusterização hierárquico construimos um dendograma utilizando a distância euclidiana e o método de aglomeração de Ward, isto levando em conta a quantidade e a aproximação entre os dados em um gráfico de Quantidade X Valor Gasto por cliente. Tendo a visualização do dendograma, pelas distâncias das formações dos clusters, optamos por separar a base em dois clusters. Analisando os clusters formados escolhemos o cluster de nosso interesse. O método hieráquico selecionou 807 clientes, o que corresponde a 18.6% do total, estes clientes foram responsáveis pela compra de 68.7% dos produtos e por 96.77% do dinheiro gasto na empresa.

Concluindo:

- Fica indicado para o programa de fidelidade os clientes selecionados pelo método hieráquico, pois, neste caso temos uma boa porcentagem dos clientes 18.6%. O método k-means selecionou apenas 0.44% dos clientes, não vale a pena para a empresa investir em um programa de fidelidade para atingir tão poucos clientes e outos clientes que verão poucos selecionados não se sentirão incentivados a se esforçar para entrar no programa. Além disso o cluster hieráquico selecionou os clientes responsáveis por 96,77% dos ganho da empresa, de fato esses clientes merecem estar em um programa de fidelidade. 


- É importante pontuar que, para inserir novos clientes no programa de fidelidade, é necessário repetir o processo de clusterização já que este é um modelo de machine learning não supervisionado e, sendo assim, não permite inferências para clientes futuros.
