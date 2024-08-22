# Atividade-19

#include<stdio.h>
#include<stdlib.h>

int verificarNumeroPerfeito(int numero) {
    if (numero <= 0) {
        return 0; // Números não positivos não são perfeitos
    }
    int soma = 0;
    // Calcula a soma dos divisores próprios
    for (int i = 1; i <= numero / 2; i++){ 
        if (numero % i == 0){ // Se i é divisor de numero
            soma += i;
        }
    }
    return soma == numero;
}
int main() {
    int numero;
    printf("Digite um numero: ");
    scanf("%d", &numero);
    if (verificarNumeroPerfeito(numero)) {
        printf("%d e um numero perfeito.\n", numero);
    } else {
        printf("%d nao e um numero perfeito.\n", numero);
    }
    return 0;
}
