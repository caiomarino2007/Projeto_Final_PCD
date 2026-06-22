<img src="Cabeçalho e Rodapé - Ilum/Cabecalho - Ilum.png" width="100%"/>

# Projeto Final PCD - Jogo da Cobrinha
### Aluno: Caio Guimarães Marino - Turma 2026
### Docentes: Daniel R. Cassar, James Moraes de Almeida, Leandro Nascimento Lemos
### Ilum, Escola de Ciência, Centro Nacional de Pesquisa em Energia e Materiais (CNPEM), Brasil.

### **Descrição**
Este projeto consiste em uma tentativa de produzir o jogo da cobrinha (Snake) no Python a partir da biblioteca `Pygame`, a qual foi criada para o desenvolvimento de jogos 2D.
Neste jogo, o usuário controla, com as setas direcionais, uma cobrinha que deve comer maçãs que são geradas aleatoriamente pelo campo. O objetivo é conseguir o máximo de pontos possível, ou seja, comer o máximo de maçãs. No entanto, conforme as maçãs são consumidas, a cobrinha vai crescendo de tamanho e o jogo termina quando a cobrinha bater nas bordas do campo ou quando bater no próprio corpo. 

Além do pygame, para o desenvolvimento do projeto foi utilizada também a biblioteca nativa `random` do Python, utilizada para aleatorizar o spawn das maçãs no jogo.

OBS.: O projeto conta com um modo para pessoas com daltonismo, o qual pode ser ativado pressionando a tecla D durante a execução do jogo.

### **Guia de arquivos no repositório**
Neste repositório, o arquivo `Projeto_cobrinha.ipynb` (arquivo Jupyter) é o principal do projeto e contém todo o desenvolvimento, estando organizado em células de código e suas respectivas documentações em células Markdown.
Os arquivos presentes na pasta `Cabeçalho e Rodapé - Ilum` são apenas imagens referentes ao cabeçalho e rodapé da instituição, utilizados na construção deste README.

Para analisar a construção do projeto e o desenvolvimento do código desde o início, analise os commits realizados na branch `dev`.

### **Requisitos**
Para a execução do projeto, é necessário possuir:

- Python 3.10 ou superior
- Biblioteca Pygame (pode ser instalada através do comando `%pip install pygame`, que pode ser executado diretamente em uma célula de código no notebook)
- Ambiente que rode notebooks, como JupyterLab, por exemplo (para executar o arquivo `.ipynb`)

No desenvolvimento do projeto, foi utilizado o seguinte ambiente:

- Python 3.13.7
- Pygame 2.6.1
- VS Code (com extensão do Jupyter)
- Windows 11 64 bits

### **Principais Funções e Estrutura do Projeto**
#### `posicao_maca()`
Essa função é responsável por gerar uma posição aleatória para a maçã dentro dos limites do campo de jogo, utilizando a função `randint()` do módulo `random` para isso. `posicao_maca()`, garante também que a maçã apareça alinhada ao movimento da cobrinha.

#### `reinicia_jogo()`
Essa função é responsável por restaurar todas as variáveis de estado do jogo para seus valores iniciais. Ela é chamada quando o jogador escolhe reiniciar o jogo após perder, redefinindo o tamanho da cobrinha, a posição da maçã, a pontuação, a velocidade da cobrinha e as variáveis auxiliares de controle do jogo.

#### Loop principal (`while rodando`)
Todo o funcionamento do jogo é controlado por um laço de repetição principal que permanece em execução enquanto a variável `rodando` for verdadeira. É nesse laço que as pricipais tarefas do jogo são realizadas, como a captura dos eventos do teclado e da janela, a atualização da direção da cobrinha, a movimentação da mesma, a verificação das colisões (com a maçã, borda e prórpio corpo), o contador de pontuação, a atualização da tela e o controle do FPS.

<img src="Cabeçalho e Rodapé - Ilum/Rodape - Ilum.png" width="100%"/>