<div align="center">
  <h2>Relatório EP3 - MAC0323 Algoritmos e Estruturas de Dados II</h2>
  <h3>Sabrina Araújo - nºUSP 12566182</h3>
</div>

### Tarefas básicas de grafos

#### Entrada do arquivo de texto
O algoritmo lê o arquivo de texto para a entrada da estrutura do grafo na função ```leArquivo```. O nome do arquivo deve ser "grafo.txt" e estar no mesmo diretório do programa. A lista de adjacência deve ter inteiros de 0 e V-1.

#### Implementação do Grafo
O grafo foi implementado utilizando a classe ```vector``` para criar V (número de vértices) listas ligadas. Cada lista contém os adjacentes de um dado vértice.

#### Função distancia()
Dado um vértice u, a função calcula a distância de u até todos os vértices do grafo utilizando a função ```bfs(int i)``` que consiste na busca em largura. A ideia dessa função é visitar um vértice i, em seguida seus vizinhos e assim por diante, desse modo, é possível encontrar o menor caminho entre i e os demais vértices.

#### Função compConexas()
Determina o número de componentes conexas e o tamanho de cada componente de um grafo utilizando a função ```dfs()``` que consiste na busca em profundidade. A ideia dessa função é em cada passo examinar um vértice, marco que a busca já o examinou e visito cada um de seus vizinhos que ainda não foi visitado, assim, é possível determinar as componentes conexas.

#### Exemplo
Seja a seguinte lista de adjacência:

![image](https://i.imgur.com/7Xns7wg.png)

O programa gera a saída:

![image](https://i.imgur.com/ZuKrfkj.png) ![image](https://i.imgur.com/qMoZ2GU.png) ![image](https://i.imgur.com/4bGUrXj.png) ![image](https://i.imgur.com/DK2ifjd.png)

![image](https://i.imgur.com/hMViJZO.png)

### Os grafos legais: geradores
No arquivo geradores.cpp há 3 geradores de entrada para o programa principal.
#### simples()
A função ```simples()``` gera um número aleatório para V (número de vértices) e para E (número de arestas) e a partir disso gera uma lista de adjacência aleatória.

#### palavras()
A função ```palavras()``` recebe uma lista com n palavras de um arquivo ```palavras.txt``` e a partir disso cria uma lista de adjacência com números entre 0 e V-1.

#### erdosReniy()
A função ```erdosReniy()``` recebe um número de vértices V e uma probabilidade p e a partir disso conecta cada vértice com os outros com probabilidade p.

### Propriedades de grafos: testes

#### Grafos de palavras

Nestes grafos, cada vértice é uma palavra de k letras, e duas palavras estão ligadas se diferem em exatamente uma letra.

#### Teste 1
Utilizando as palavras tears–sears–stars–stare–stale–stile–smile como entrada do programa gerador, temos a seguinte lista de adjacência:

![image](https://i.imgur.com/r946LZu.png)

A partir dessa lista criamos um grafo com o programa principal, que gera a saída:

![image](https://i.imgur.com/dQpCLqE.png) ![image](https://i.imgur.com/3enlcm1.png) 

![image](https://i.imgur.com/TmD13EB.png) 

#### Teste 2
Utilizando as palavras word-woad-road-read-real-peal-peat-plat-play como entrada do programa gerador, temos a seguinte lista de adjacência:

![image](https://i.imgur.com/2KCulbi.png)

A partir dessa lista criamos um grafo com o programa principal, que gera a saída:

![image](https://i.imgur.com/A8gHnOn.png) ![image](https://i.imgur.com/K2B8cvo.png) ![image](https://i.imgur.com/cFrAmdw.png) ![image](https://i.imgur.com/ew50C2R.png)

![image](https://i.imgur.com/Zt79b0z.png)

<li> Seis graus de separação </li>

#### Teste 3
Utilizando uma [lista](https://www.dicio.com.br/palavras-com-quatro-letras/) de 1000 palavras de 4 letras em português, temos uma lista de adjacência com 1000 vértices e 2793 arestas (obs: a lista da imagem não está completa):

![image](https://i.imgur.com/BrsZWbd.png)

A partir dessa lista criamos um grafo com o programa principal, que gera a saída (as imagens não representam a saída completa):

![image](https://i.imgur.com/u7lzf7b.png)

É possível observar que há diferentes distâncias entre os vértices, no qual podem estar acima ou abaixo de 6. Diante disso, não dá para afirmar que todos os vértices estão a seis ou menos conexões de outro vértice. Porém, a distância média é menor ou igual a 6:

![image](https://i.imgur.com/X4bsIxT.png)

#### Grafos aleatórios de Erdös-Reniy

<li> Componente gigante </li>

Se p <= (1-e)/n então, com alta probabilidade as componentes conexas são pequenas, com O(log n) elementos, mas se p >= (1+e)/n surge uma componente gigante no grafo.

#### Teste 4

Seja p=0.2 e e=0.01.
Ao criar um grafo com 10 vértices e probabilidade p, temos a seguinte lista de adjacência:

![image](https://i.imgur.com/iveJvYY.png)

A partir dessa lista criamos um grafo com o programa principal, que gera a saída:

![image](https://i.imgur.com/EAgtNwn.png) ![image](https://i.imgur.com/skQ6gVo.png) ![image](https://i.imgur.com/aCB7W5k.png)

![image](https://i.imgur.com/HdusdkX.png)

Neste exemplo, p >= (1+e)/n, assim, como proposto pelo modelo surgiu uma componente gigante no grafo.

#### Teste 5
Seja p=0.01 e e=0.01.
Ao criar um grafo com 20 vértices e probabilidade p, temos a seguinte lista de adjacência:

![image](https://i.imgur.com/L0jrhxD.png)

A partir dessa lista criamos um grafo com o programa principal, que gera a saída:

![image](https://i.imgur.com/b4VLM4B.png)

![image](https://i.imgur.com/BFQHMtD.png)

Neste exemplo, p <= (1-e)/n, assim, como proposto pelo modelo surgiram componentes conexas pequenas com O(log20) elementos.

<li> Seis graus de separação </li>

#### Teste 6

Seja p=0.1.
Ao criar um grafo com 20 vértices e probabilidade p, temos uma lista de adjacência com 42 arestas.

A partir dessa lista criamos um grafo com o programa principal, que gera a saída (a imagem não está completa, pois a saída é grande):

![image](https://i.imgur.com/Z67F4Ce.png)

![image](https://i.imgur.com/RcY0qwi.png)

Neste exemplo, todos os pares de vértices possuem uma distância menor ou igual a 6, com média igual a 2, assim, validando a ideia dos seis graus de separação.

#### Teste 7

Seja p=0.1.
Ao criar um grafo com 50 vértices e probabilidade p, temos uma lista de adjacência com 253 arestas.

A partir dessa lista criamos um grafo com o programa principal, que gera a saída (a imagem não está completa, pois a saída é grande):

![image](https://i.imgur.com/EztfvdC.png)

![image](https://i.imgur.com/dKsi4dC.png)

Neste exemplo, todos os pares de vértices possuem uma distância menor ou igual a 3, com média igual a 2, assim, validando a ideia dos seis graus de separação.
