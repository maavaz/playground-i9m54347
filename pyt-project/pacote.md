# Pacotes Python

No arquivo <b>Programação Python</b> (https://www.codingame.com/playgrounds/52499/programacao-python-intermediario---prof--marco-vaz/biblioteca-padrao), foi mostrado como deve-se utilizar (importar) os módulos componentes da biblioteca padrão, bem como as suas funções. 
Módulos são programas que tipicamente contêm funções, variáveis, classes e objetos que provêm alguma funcionalidade comum e que podem ser usadas em outros programas. Um pacote (biblioteca) é basicamente outro tipo de módulo que contém um conjunto de módulos. Enquanto um módulo é armazenado em um arquivo (com a extensão de nome de arquivo .py), um pacote é um diretório contendo vários módulos.   
Existem vários pacotes python muito úteis, pois são voltados para as diversas áreas de aplicação científica, mas em alguns casos, para serem utilizados, precisam ser instalados (como instalá-los está fora do contexto desse documento). 
Se você possui o ambiente Anaconda (https://www.anaconda.com/) instalado em sua máquina, não se preocupe, pois já possui instalados os pacotes que iremos apresentar aqui (pandas, Numpy e MatPlotLib).  
Como já adiantado, não iremos abordar todos os pacotes, apenas os seguintes:

+ <b>NumPy</b> (https://numpy.org/) - Pacote básico da linguagem Python (precisa instalá-lo) que permite trabalhar com arranjos, vetores e matrizes de N dimensões, de uma forma comparável e com uma sintaxe semelhante ao software proprietário Matlab, mas com muito mais eficiência, e com toda a expressividade da linguagem. 

+ <b>pandas</b> (https://pandas.pydata.org/) - Pacote Python (precisa instalá-lo) que fornece estruturas de dados de alto nível e uma grande variedade de ferramentas para análise. A grande característica deste pacote é a capacidade de traduzir operações bastante complexas com dados em um ou dois comandos. O Pandas contêm muitos métodos internos para agrupar, filtrar e combinar dados, bem como a funcionalidade de séries temporais. Tudo isso é seguido por indicadores de velocidade impressionantes.

+ <b>matplotlib</b> (http://matplotlib.org/) - Biblioteca do Python para criação de gráficos em 2D, bastante utilizada para visualização de dados e que apresenta uma série de possibilidades gráficas, como gráficos de barra, linha, pizza, histogramas, entre muitos outros.

**OBS:** Os termos **Pacote** e **Biblioteca** serão usados como sinônimos.

### <b> Métodos X Funções </b>

Convém relembrar que, apesar dos métodos e das funções terem funcionalidades semelhantes, as sintaxes de ambos diferem um pouco.
As funções agem como segmentos de código independentes que geralmente recebem uma entrada, executam algum processamento e retornam alguma saída. O formato geral das funções será:

**nome_da_função(objeto)**

Por outro lado, métodos são funções especiais que pertencem a um tipo específico de objeto (os pacotes são objetos Python). Isso significa que, por exemplo, quando trabalhamos com um determinado objeto, existem funções ou métodos especiais que podem ser usados apenas com aquele objeto.  A forma geral dos métodos é:

**objeto.nome_do_método([parâmetros])**
