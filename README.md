# Jogo de xadrez

![Java](https://img.shields.io/badge/java-%23ED8B00.svg?style=for-the-badge&logo=openjdk&logoColor=white)

## Descrição

Programa que simula uma partida de xadrez realizada por duas pessoas. 
O jogo segue as regras tradicionais do xadrez, com a possibilidade de movimentação das peças, 
captura de peças adversárias e execução de xeque e xeque-mate, além de incluir jogadas especiais como:

- **Roque ou Castling:** quando é permitido o rei mover 2 casas, junto com a torre, em caso de:
  - O rei e uma das torres ainda não se moveram.
  - As casas entre o rei e a torre estiverem vagas.
  - O rei não estiver sob xeque.
    
![image](https://github.com/user-attachments/assets/1e947cbe-7e4e-4325-a9d4-12b08a63ea5e)

- **En passant:** o movimento de um peão na diagonal que, por sua vez, captura o peão do adversário ao lado quando este somente moveu duas casas.
A imagem abaixo ilustra um peão preto, que apenas moveu duas casas, sendo capturada pela peça branca ao lado.

![Image](https://github.com/user-attachments/assets/28cb9178-0d01-4a28-a43e-0ceffbded63e)

- **Promoção:** quando o peão chega até a última casa, é concedido ao jogador trocar esta peça por uma torre, rei, rainha ou bispo.

![Image](https://github.com/user-attachments/assets/92bfc90d-8841-4959-81d9-b0694ae314ae)

## Instrução de instalação
### Pré-requisitos

- Instalação da JDK 21.
- Instalação do Git.
- Conhecimento prévio das regras do xadrez.

### Como instalar o jogo

- Acesse o link https://github.com/PedroCarv21/chess-system-java -> clique no botão verde `<> Code` -> clique em HTTPS -> Copie o link.
  
![image](https://github.com/user-attachments/assets/e8bff929-a338-4c23-a24f-5b917556cdaa)

- Abra o Git e digite o comando `pwd` para saber em qual diretório você se encontra. Se deseja mudar de diretório, digite `cd` mais
o caminho do diretório em que será armazenado o programa.
  
![image](https://github.com/user-attachments/assets/59ee962a-6d70-48a2-a833-51131b1f4518)

- Digite `git clone` e cole o link copiado do site do GitHub.

![image](https://github.com/user-attachments/assets/3a24346f-ffa5-4233-95a1-d257473bb17c)

- Digite `cd chess-system-java` para entrar na pasta do projeto.
  
- Compile o código com os seguintes comandos:
  - `find src -name "*.java" > sources.txt`
  - `javac -d bin @sources.txt`

![image](https://github.com/user-attachments/assets/cb5d0ffc-b706-4172-b0e1-6677c53ac608)

- Acesse a pasta bin através do comando `cd bin` e digite `java application/Program` para executar o programa. O resultado deverá ser
a exposição do tabuleiro.

![image](https://github.com/user-attachments/assets/2135bd2b-fa8e-4bc8-acdb-24e59d3007f9)

## Instrução de uso

### Peças do jogo

As peças são representadas pelas seguintes letras:

- **Peão (P)**
- **Torre (R)**
- **Bispo (B)**
- **Cavalo (N)**
- **Rainha (Q)**
- **Rei (K)**

## Comandos

Para movimentar uma peça, é necessário informar a coluna (representada por uma letra) e a linha (representada por um número) em que a peça se encontra (a sua posição de origem).
Por exemplo, se você deseja mover o peão presente na coluna `a` e na linha `2` então digite `a2` para indicar a peça que será movida.

![Image](https://github.com/user-attachments/assets/c1d070d1-7878-4c2f-95ab-31cb04daed21)

Ao fazer isso, serão destacadas em azul as casas em que a peça poderá se mover. Mais uma vez, descreva para onde a peça deve ir indicando a letra da coluna e o número da linha.

![image](https://github.com/user-attachments/assets/bb4ddc09-7b54-4a9b-9f0b-321493adc158)

O resultado será então o movimento da peça.

![image](https://github.com/user-attachments/assets/68cd221f-fe20-4810-be53-aaa84aa3b9c6)

### Possíveis mensagens de erros

Em caso de ocorrência de qualquer um dos erros listados abaixo, pressione a tecla `Enter` para prosseguir o jogo.

- Ao informar uma posição inexistente de uma casa, será exibida a mensagem: `Error reading ChessPosition. Valid values are from a1 to h8`.
- Se for informado como posição de origem uma casa sem peça, será apresentada a seguinte mensagem: `There is no piece on source position`.
- Se tentar mover a peça do adverário, será apresentada a mensagem: `The chosen piece is not yours`.
- Caso tente movimentar a peça para uma lugar inválido, aparecerá a mensagem: `The chosen piece can't move to target position`.
- Ao tentar deslocar uma peça em que não há possibilidade de movimento naquele momento: `There is no possible moves for the chosen piece`.
