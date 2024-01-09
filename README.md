# Jogo de Tiro em OpenGL

Este é um jogo simples desenvolvido em OpenGL, utilizando a biblioteca GLUT. O objetivo do jogo é controlar um canhão e atirar em inimigos que se movem na tela. O código está estruturado em C++ e utiliza a biblioteca TinyXML para a manipulação de dados XML.

## Estrutura do Código

### Principais Estruturas de Dados

- **Círculo (`circle`):** Representa um círculo no jogo, contendo informações como coordenadas (`cx`, `cy`), raio (`r`), cor e identificador.

- **Retângulo (`rectangle`):** Representa um retângulo no jogo, com informações sobre posição (`x`, `y`), largura (`width`), altura (`height`), cor de preenchimento e identificador.

- **Tiro (`tiro`):** Estrutura para armazenar informações sobre os tiros no jogo, incluindo coordenadas (`x`, `y`) e direção (`teta`).

### Funções Principais

- **`init()`:** Função de inicialização do jogo.

- **`desenha()`:** Função para renderizar os elementos do jogo.

- **`teclado(tecla, x, y)`:** Função para capturar eventos de teclado e controlar o canhão.

- **`recebeValores()`:** Função para receber valores de entrada.

- **`distanciaEuclidiana(x, y)`:** Calcula a distância euclidiana entre duas coordenadas.

- **`desenhaTiro()`:** Desenha os tiros disparados pelo jogador.

- **`atualizaMovimentosInimigos()`:** Atualiza os movimentos dos inimigos na tela.

- **`desenhaTiroInimigo1()`, `desenhaTiroInimigo2()`, `desenhaTiroInimigo3()`:** Desenha os tiros dos inimigos.

- **`atiraInimigo1()`, `atiraInimigo2()`, `atiraInimigo3()`:** Lógica para os inimigos atirarem.

- **`timer(value)`:** Função de temporização para controlar a frequência de atualização do jogo.

## Controles do Jogo

- O jogador controla um canhão que pode girar em torno de sua base.
- Use as teclas para mover o canhão e atirar nos inimigos.
- Inimigos se movem pela tela e atiram periodicamente.
- O objetivo é sobreviver o máximo de tempo possível, evitando os tiros inimigos e eliminando os inimigos.

## Inimigos

O jogo possui três tipos de inimigos, cada um com padrões de movimento e comportamentos de tiro diferentes.

1. **Inimigo Tipo 1:** Movimento em padrões circulares.

2. **Inimigo Tipo 2:** Movimento linear com mudanças de direção.

3. **Inimigo Tipo 3:** Movimento errático com momentos de congelamento.

## Compilação e Execução


### PRE REQUISITOS:
OpenGL
Math.h
PARSE com: tinyxml.h

### ORIENTAÇÕES para correta execução:
O atributo "caminho" no arquivo mapa/config.xml deve conter o endereço local que consta o arquivo config.xml

### Compilando e Executando

Certifique-se de ter as bibliotecas GLUT e TinyXML instaladas. Compile o código e execute o jogo.

- Alternativa 1:

>> make

>> ./arenagame mapa/


- Alternativa 2:


```bash
g++ jogo.cpp -o jogo -lGL -lglut -lGLU -ltinyxml
./jogo




