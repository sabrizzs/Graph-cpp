<div align="center">
  <h2>Relatório - MAC0323 Algoritmos e Estruturas de Dados II</h2>
  <h3>Sabrina Araújo - nºUSP 12566182</h3>
</div>

#### Entrada do arquivo de texto
O algoritmo lê o arquivo de texto para a entrada da estrutura do grafo na função ```leArquivo```. O nome do arquivo deve ser "grafo.txt" e estar no mesmo diretório do programa.

#### Implementação do Grafo
O grafo foi implementado utilizando a classe ```vector``` para criar V (número de vértices) listas ligadas. Cada lista contém os adjacentes de um dado vértice.

#### Função distancia()
Dado um vértice u, a função calcula a distância de u até todos os vértices do grafo utilizando a função ```bfs(int i)``` que consiste na busca em largura. A ideia dessa função é visitar um vértice i, em seguida seus vizinhos e assim por diante, desse modo, é possível encontrar o menor caminho entre i e os demais vértices.

#### Função compConexas()
Determina o número de componentes conexas e o tamanho de cada componente de um grafo utilizando a função ```dfs()``` que consiste na busca em profundidade. A ideia dessa função é em cada passo examinar um vértice, marco que a busca já o examinou e visito cada um de seus vizinhos que ainda não foi visitado, assim, é possível determinar as componentes conexas.
