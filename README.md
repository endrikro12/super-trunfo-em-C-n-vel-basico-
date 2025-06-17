

*Super Trunfo: Jogo de Cartas*

O Super Trunfo é um jogo de cartas onde dois jogadores comparam suas cartas com base em propriedades específicas. O jogador com a carta que tiver o valor mais alto na propriedade escolhida vence.

*Código:*
#include <stdio.h>
#include <stdlib.h>
#include <time.h>

// Estrutura para representar uma carta de país
typedef struct {
    char nome[50]; // Nome do país
    int populacao; // População do país
    double pib; // PIB do país
    int pontos_turisticos; // Número de pontos turísticos do país
} Carta;

// Função para ler os dados de uma carta
void lerCarta(Carta *carta) {
    printf("Digite o nome do país: ");
    scanf("%49s", carta->nome);
    printf("Digite a população do país: ");
    scanf("%d", &carta->populacao);
    printf("Digite o PIB do país: ");
    scanf("%lf", &carta->pib);
    printf("Digite o número de pontos turísticos do país: ");
    scanf("%d", &carta->pontos_turisticos);
}

// Função para imprimir os dados de uma carta
void imprimirCarta(Carta carta) {
    printf("Nome: %s\n", carta.nome);
    printf("População: %d\n", carta.populacao);
    printf("PIB: %.2lf\n", carta.pib);
    printf("Pontos turísticos: %d\n", carta.pontos_turisticos);
}

// Função para comparar as cartas e determinar o vencedor
void compararCartas(Carta carta1, Carta carta2, int escolha) {
    switch (escolha) {
        case 1:
            if (carta1.populacao > carta2.populacao) {
                printf("A carta 1 venceu!\n");
            } else if (carta2.populacao > carta1.populacao) {
                printf("A carta 2 venceu!\n");
            } else {
                printf("Empate!\n");
            }
            break;
        case 2:
            if (carta1.pib > carta2.pib) {
                printf("A carta 1 venceu!\n");
            } else if (carta2.pib > carta1.pib) {
                printf("A carta 2 venceu!\n");
            } else {
                printf("Empate!\n");
            }
            break;
        case 3:
            if (carta1.pontos_turisticos > carta2.pontos_turisticos) {
                printf("A carta 1 venceu!\n");
            } else if (carta2.pontos_turisticos > carta1.pontos_turisticos) {
                printf("A carta 2 venceu!\n");
            } else {
                printf("Empate!\n");
            }
            break;
        default:
            printf("Escolha inválida!\n");
    }
}

int main() {
    Carta carta1, carta2;

    printf("Digite os dados da carta 1:\n");
    lerCarta(&carta1);

    printf("\nDigite os dados da carta 2:\n");
    lerCarta(&carta2);

    printf("\nCarta 1:\n");
    imprimirCarta(carta1);

    printf("\nCarta 2:\n");
    imprimirCarta(carta2);

    printf("\nEscolha uma propriedade para comparar:\n");
    printf("1. População\n");
    printf("2. PIB\n");
    printf("3. Pontos turísticos\n");
    int escolha;
    scanf("%d", &escolha);

    compararCartas(carta1, carta2, escolha);

    return 0;
}
*Estrutura do Código:*

- A estrutura `Carta` representa uma carta de país com propriedades como nome, população, PIB e pontos turísticos.
- A função `lerCarta` lê os dados de uma carta.
- A função `imprimirCarta` imprime os dados de uma carta.
- A função `compararCartas` compara as cartas e determina o vencedor com base na propriedade escolhida.
- O `main` é a função principal que controla o fluxo do jogo.

*Documentação:*

- Cada função tem uma descrição clara de sua finalidade e parâmetros.
- O código é comentado para explicar a lógica e as decisões tomadas.

Essa estrutura e documentação devem facilitar a compreensão e manutenção do código.