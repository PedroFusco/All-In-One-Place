# All-In-One-Place
Neste trabalho foi criado um programa de fidelidade para a empresa de Outlet multimarcas All In One Place. Esse programa foi criado utilizando a técnica de clusterização e a linguagem R.

-------------------------||------------------------------

A empresa All In One Place
(O contexto a seguir é completamente fictício, a empresa, o contexto, o CEO, as perguntas de negócio existem somente na minha imaginação)

A empresa All in One Place é uma empresa Outlet Multimarcas, ou seja, ela comercializa produtos de segunda linha de várias marcas a um preço menor, através de um e-commerce.

Em pouco mais de 1 anos de operação, o time de marketing percebeu que alguns clientes da sua base, compram produtos mais caros, com alta frequência e acabam contribuindo com uma parcela significativa do faturamento da empresa.

Baseado nessa percepção, o time de marketing vai lançar um programa de fidelidade para os melhores clientes da base, chamado Insiders. Mas o time não tem um conhecimento avançado em análise de dados para eleger os participantes do programa.

Por esse motivo, o time de marketing requisitou ao time de dados uma seleção de clientes elegíveis ao programa, usando técnicas avançadas de manipulação de dados.

Objetivo: Determinar quem são os clientes elegíveis para participar de um programa de fidelidade da empresa All In One Place?

Para o programa de fidelidade queríamos os clientes que mais gastavam dinheiro na empresa e também aqueles que compravam mais produtos. Para encontrarmos esses clientes, após a limpeza dos dados, foi feita uma análise visual da relação das variáveis de interesse. Verificamos que a maior parte dos clientes, tanto os que compravam a maior quantidade de produtos quanto os que mais gastavam, eram do Reino Unido. Vimos também que os produtos mais vendidos não eram necessariamente os mesmos que geravam mais ganho para a empresa. Por fim, o mais importante, descobrimos que os clientes que compravam a maior quantidade de produtos não eram os mesmos que mais gastavam na All In One Place. Decidimos então agrupar os clientes considerando a quantidade total da compra de produtos e também pela quantidade total gasta na loja por cliente. Testamos três algoritmos de cluster diferentes, cluster hierárquico, k-means e o dbscan. Desses escolhemos como o melhor resultado o cluster hierárquico.

O cluster escolhido foi selecionado pela técnica de clusterização hierárquica, foram selecionados 40 clientes, aproximadamente 1% de toda a clientela. Esses tem como característica os maiores compras na empresa, tanto em quantidade de produto quanto em quantidade de dinheiro. Os clientes escolhidos são responsáveis por 31,03% de todo o ganho financeiro da empresa e também por 30.39% da quantidade de produtos vendidos. Espera-se que com o início do programa de fidelidade a quantidade de faturamento da empresa aumente, não só com os clientes escolhidos nesse momento, mas também com clientes que podem acabar sendo aderidos no programa.
Cabe colocar que o time de marketing pode realizar ações para popularizar o programa de fidelidade, principalmente para países fora do Reino Unido, de forma que novos clientes se sintam incentivados a comprar mais na empresa com a finalidade de serem incluidos no programa.

Obs.: É importante pontuar que para inserir novos clientes no programa de fidelidade é necessário repetir o processo de clusterização já que este é um modelo de machine learning não supervisionado e, sendo assim, não permite inferências para clientes futuros.
