<div align="center">
  <h2>Relatório - MAC0323 Algoritmos e Estruturas de Dados II</h2>
  <h3>Sabrina Araújo - nºUSP 12566182</h3>
</div>

### Tarefas básicas de grafos

#### Entrada do arquivo de texto
O algoritmo lê o arquivo de texto para a entrada da estrutura do grafo na função ```leArquivo```. O nome do arquivo deve ser "grafo.txt" e estar no mesmo diretório do programa.

#### Implementação do Grafo
O grafo foi implementado utilizando a classe ```vector``` para criar V (número de vértices) listas ligadas. Cada lista contém os adjacentes de um dado vértice.

#### Função distancia()
Dado um vértice u, a função calcula a distância de u até todos os vértices do grafo utilizando a função ```bfs(int i)``` que consiste na busca em largura. A ideia dessa função é visitar um vértice i, em seguida seus vizinhos e assim por diante, desse modo, é possível encontrar o menor caminho entre i e os demais vértices.

#### Função compConexas()
Determina o número de componentes conexas e o tamanho de cada componente de um grafo utilizando a função ```dfs()``` que consiste na busca em profundidade. A ideia dessa função é em cada passo examinar um vértice, marco que a busca já o examinou e visito cada um de seus vizinhos que ainda não foi visitado, assim, é possível determinar as componentes conexas.

### Os grafos legais: geradores
No arquivo geradores.cpp há 3 geradores de entrada para o programa principal.
#### simples()
A função ```simples()``` gera um número aleatório para V (número de vértices) e para E (número de arestas) e a partir disso gera uma lista de adjacência aleatória.

#### palavras()
A função ```palavras()``` recebe uma lista com n palavras de um arquivo ```palavras.txt``` e a partir disso cria uma lista de adjacência com números entre 0 e n-1.

#### erdosReniy()
A função ```erdosReniy``` recebe um número de vértices V e uma probabilidade p e a partir disso conecta cada vértice com os outros com probabilidade p.

### Propriedades de grafos: testes

