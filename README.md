# Arrays(vetores) e Matrizes

PARTE 1 – CONCEITOS FUNDAMENTAIS

1. O que é um ARRAY?
2. Array é uma lista ordenada de elementos do mesmo tipo, guardados em posições consecutivas na memória.
Imagine um estacionamento de carros com vagas numeradas:
•	Cada vaga tem um número fixo (0, 1, 2, 3...)
•	Em cada vaga só cabe um carro por vez
•	Você não pode colocar um carro "entre" as vagas
•	Para acessar um carro, você diz: "me dê o carro da vaga 2"

4. Regras de ouro do Array
•	Tamanho fixo – quando você cria, decide quantas posições terá. Depois não pode aumentar nem diminuir.
•	Índice sempre começa em 0 (primeira posição é 0, segunda é 1, etc.)
•	Todos os elementos são do mesmo tipo (ex: só números, só textos, etc.)
•	Acesso direto: você vai direto na posição que quer – é muito rápido

Conceito 1: Indexação começa do ZERO
Isso pega muita gente. No mundo real, contamos 1, 2, 3... Na programação (arrays/matrizes), contamos 0, 1, 2...
Se um array tem 5 elementos, os índices vão de 0 a 4 (não de 1 a 5)


Como construir um array
tipo nome_do_array[tamanho];
O que você escolhe	Exemplo
Tipo (o que guardar)	int (números), float (decimais), char (letras)
Nome (como chamar)	idades, notas, numeros
Tamanho (quantas posições)	5, 10, 100


Índice é a "casa" do elemento. Começa no 0.
array[0] = primeira casa
array[1] = segunda casa
array[2] = terceira casa
E assim por diante.
#include <stdio.h>

int main() {
    // Array com números
    int numeros[5] = {10, 20, 30, 40, 50};
    
    // Mostrando cada número com sua posição (índice)
    printf("Posicao 0: %d\n", numeros[0]);
    printf("Posicao 1: %d\n", numeros[1]);
    printf("Posicao 2: %d\n", numeros[2]);
    printf("Posicao 3: %d\n", numeros[3]);
    printf("Posicao 4: %d\n", numeros[4]);
    
    return 0;
}
SAÍDA:
text
Posicao 0: 10
Posicao 1: 20
Posicao 2: 30
Posicao 3: 40
Posicao 4: 50
________________________________________
🔄 EXEMPLO 2: USANDO LOOP FOR (MAIS LIMPO)
c
#include <stdio.h>

int main() {
    int numeros[5] = {100, 200, 300, 400, 500};
    
    // Loop para mostrar todas as posições
    for(int i = 0; i < 5; i++) {
        printf("Posicao %d -> valor: %d\n", i, numeros[i]);
    }
    
    return 0;
}

________________________________________
🧱 PARTE 2 – O que é uma MATRIZ?

4. Matriz = array de arrays (ou tabela) 
Matriz é uma tabela com linhas e colunas – você precisa de DOIS números para achar um elemento: linha e coluna.
Imagine um prédio com andares e apartamentos:
•	Andar 0, apartamento 0
•	Andar 0, apartamento 1
•	Andar 1, apartamento 0

7. Regras da Matriz
•	Precisa de linha e coluna para acessar um elemento
•	Todas as linhas têm o mesmo número de colunas (matriz retangular)
•	Também tem tamanho fixo e tipo único

9. COMO CONSTRUIR UMA MATRIZ
10. Uma matriz é uma estrutura bidimensional - ou seja, ela tem ALTURA (linhas) e LARGURA (colunas)
    EX.:
          Coluna 0  Coluna 1  Coluna 2
Linha 0   [ ]      [ ]      [ ]
Linha 1   [ ]      [ ]      [ ]
Linha 2   [ ]      [ ]      [ ]

Cada [ ] é um espaço que guarda UM valor.

📚 CONCEITO 2: VOCÊ DECIDE O TAMANHO NA CONSTRUÇÃO
Quando você constrói uma matriz, você precisa decidir quantas linhas e quantas colunas ela terá.

Isso é FIXO para sempre. Depois que a matriz está construída, você não pode adicionar ou remover linhas/colunas.

text
Você decide: "Quero uma matriz 3x3"
Resultado: 9 espaços fixos, organizados em 3 linhas e 3 colunas

Você NÃO pode depois:
❌ Adicionar uma 4ª linha
❌ Remover a 2ª coluna

Att.: o array e matrizes dependem de cada linguagem de programação. ambos não podem ser acrescidos ou diminuidos em C, C++,C#
Mas podem ser acrescidos ou diminuidos em python, javascript,php, java.


#include <stdio.h>

int main() {
    // Matriz 2x2 (2 linhas, 2 colunas)
    int matriz[2][2] = {
        {1, 2},  // linha 0
        {3, 4}   // linha 1
    };
    
    // Mostrando cada número com sua posição (linha, coluna)
    printf("Posicao [0][0]: %d\n", matriz[0][0]);
    printf("Posicao [0][1]: %d\n", matriz[0][1]);
    printf("Posicao [1][0]: %d\n", matriz[1][0]);
    printf("Posicao [1][1]: %d\n", matriz[1][1]);
    
    return 0;
}
SAÍDA:
text
Posicao [0][0]: 1
Posicao [0][1]: 2
Posicao [1][0]: 3
Posicao [1][1]: 4
EXPLICAÇÃO VISUAL:
text
        coluna 0   coluna 1
linha 0 [   1    ][   2    ]
linha 1 [   3    ][   4    ]
________________________________________
🔄 EXEMPLO 2: USANDO LOOP FOR (MATRIZ 3x3)
c
#include <stdio.h>

int main() {
    int matriz[3][3] = {
        {1, 2, 3},
        {4, 5, 6},
        {7, 8, 9}
    };
    
    printf("MATRIZ 3x3 COMPLETA:\n\n");
    
    for(int linha = 0; linha < 3; linha++) {
        for(int coluna = 0; coluna < 3; coluna++) {
            printf("Posicao [%d][%d] = %d\n", linha, coluna, matriz[linha][coluna]);
        }
        printf("\n");  // pular uma linha entre as linhas da matriz
    }
    
    return 0;
}





