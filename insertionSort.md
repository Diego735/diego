#include <stdio.h>
#include <time.h>
#include <stdlib.h>

 (Insertion Sort)
void insertionSort(int array[], int tamanho) {
    for (int i = 1; i < tamanho; i++) {
        int chave = array[i];
        int j = i - 1;

        
        while (j >= 0 && array[j] > chave) {
            array[j + 1] = array[j];
            j = j - 1;
        }

        
        array[j + 1] = chave;
    }
}


void imprimirArray(const int array[], int tamanho) {
    for (int i = 0; i < tamanho; i++) {
        printf("%d ", array[i]);
    }
    printf("\n");
}

int main() {
    const int tamanhoArray = 6;
    int meuArray[] = {64, 25, 12, 22, 11, 1};

    
    printf("Array antes da ordenação por inserção:\n");
    imprimirArray(meuArray, tamanhoArray);

    
    insertionSort(meuArray, tamanhoArray);

    
    printf("Array após a ordenação por inserção:\n");
    imprimirArray(meuArray, tamanhoArray);

    return 0;
}



------------------------------------------------------------------------------------------------------------------------------------------

Explicação:
Função insertionSort: Implementa o algoritmo Insertion Sort.
Função printArray: Imprime os elementos de um array, para fins de verificação antes e após a ordenação (no exemplo, imprime apenas os 10 primeiros elementos).
Medindo o tempo:
A função clock() da biblioteca time.h é usada para medir o tempo de execução do algoritmo.
O tempo de execução é calculado como a diferença entre o tempo antes e depois da execução do algoritmo, convertida para segundos.
Geração de números aleatórios: O array é inicializado com números aleatórios para simular uma entrada típica.
Tamanho do array: O exemplo usa um array de tamanho n = 10000, mas você pode ajustar conforme necessário.





/*
Ordenação por Inserção: O algoritmo de ordenação por inserção constrói uma sequência ordenada de elementos um de cada vez. Ele é eficiente para pequenos conjuntos de dados ou quando os dados estão quase ordenados.

Chave e Deslocamento: A chave é o elemento atual sendo comparado e movido para a posição correta. O deslocamento ocorre quando elementos maiores que a chave são movidos para a direita.

Implementação Genérica: O código é projetado para trabalhar com arrays de inteiros, mas pode ser adaptado para outros tipos de dados.

Complexidade: O Insertion Sort possui complexidade de tempo O(n^2) no pior caso, mas pode ser mais eficiente que outros algoritmos de ordenação para conjuntos de dados pequenos.
*/
