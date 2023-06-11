# Vetores
//1)

#include <stdio.h>

int main() 
{
    
    int vetor[10];
    int i, maior;
    
    printf("Digite 10 números:\n");
    for (i = 0; i < 10; i++) {
        scanf("%d", &vetor[i]);
    }
    
    maior = vetor[0]; // Assumimos o primeiro elemento como o maior inicialmente

    for (i = 1; i < 10; i++) {
        if (vetor[i] > maior) {
            maior = vetor[i];
        }
    }
    
    printf("O maior número é: %d\n", maior);

    return 0;
}

//2)

#include <stdio.h>
int main() 
{
    
    int vetor[10];
    int i;
    int maior, menor, diferenca;
    
    
    printf("Digite 10 números:\n");
    for (i = 0; i < 10; i++) {
        printf("Número %d: ", i + 1);
        scanf("%d", &vetor[i]);
    }
    
    maior = vetor[0];
    menor = vetor[0];
    // Encontrar o maior e o menor número
    for (i = 1; i < 10; i++) {
        if (vetor[i] > maior) {
            maior = vetor[i];
        }
        if (vetor[i] < menor) {
            menor = vetor[i];
        }
    }
    
    diferenca = maior - menor;

    printf("Maior número: %d\n", maior);
    printf("Menor número: %d\n", menor);
    printf("Diferença: %d\n", diferenca);

    return 0;
}

//3)

#include <stdio.h>

int main() 
{
    
    int vetor[10];
    int i;

    
    printf("Digite 10 números:\n");
    for (i = 0; i < 10; i++) {
        printf("Número %d: ", i + 1);
        scanf("%d", &vetor[i]);
    }

    printf("Números ímpares no vetor:\n");

    
    for (i = 0; i < 10; i++) {
        if (vetor[i] % 2 != 0) {
            printf("%d\n", vetor[i]);
        }
    }

    return 0;
}

//4)

#include <stdio.h>

int Primo(int num) 
{
    
    if (num <= 1) {
        return 0;
    }

    for (int i = 2; i * i <= num; i++) {
        if (num % i == 0) {
            return 0;
        }
    }
    return 1;
}
int main() 
{
    
    int vetor[10];
    int i;
    
    printf("Digite 10 números:\n");
    for (i = 0; i < 10; i++) {
        printf("Número %d: ", i + 1);
        scanf("%d", &vetor[i]);
    }
    printf("Números primos no vetor:\n");
    
    for (i = 0; i < 10; i++) {
        if (Primo(vetor[i])) {
            printf("%d\n", vetor[i]);
        }
    }
    return 0;
}

//5)

#include <stdio.h>
int main() 
{
    
    int vetor[8];
    int i, numero, posicao = -1;

    printf("Digite 8 números inteiros:\n");
    for (i = 0; i < 8; i++) {
        printf("Número %d: ", i + 1);
        scanf("%d", &vetor[i]);
    }
    printf("Digite um número para pesquisar: ");
    scanf("%d", &numero);

    for (i = 0; i < 8; i++) {
        if (vetor[i] == numero) {
            posicao = i;
            break;
        }
    }
    if (posicao != -1) {
        printf("O número %d está na posição %d do vetor.\n", numero, posicao);
    } else {
        printf("O número %d não existe no vetor.\n", numero);
    }
    return 0;
}
