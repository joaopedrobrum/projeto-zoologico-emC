#include <stdio.h>
#include <stdlib.h>

int main() {
    int qtd_animais;
    int escolha;
    float qtd_kg;
    float qtd_dia;
    float qtd_mes;
    float custo_kg;
    float custo_mes;

    printf("Zoológico\n");
    printf("\n-------------------------------------------------------\n");

    printf("ESCOLHA UM ANIMAL\n");
    printf("(1) Macaco\n");
    printf("(2) Gorila\n");
    printf("(3) Leão\n");
    printf("\n-------------------------------------------------------\n");
    
    printf("Escolha: ");
    scanf("%d", &escolha);

    switch (escolha) {
        case 1:
            printf("Você escolheu macaco.\n");
            printf("Digite a quantidade de macacos:\n");
            scanf("%d", &qtd_animais);
            qtd_kg = 5;
            break;
        case 2:
            printf("Você escolheu gorila.\n");
            printf("Digite a quantidade de gorilas:\n");
            scanf("%d", &qtd_animais);
            qtd_kg = 10;
            break;
        case 3:
            printf("Você escolheu o leão.\n");
            printf("Digite a quantidade de leões:\n");
            scanf("%d", &qtd_animais);
            qtd_kg = 30;
            break;
        default:
            printf("Opção inválida. Por favor, reinicie o programa e escolha uma opção válida.\n");
            return 1;
    }

    printf("Qual o custo por kilo de alimento?\n");
    scanf("%f", &custo_kg);

    qtd_dia = qtd_kg * qtd_animais;
    qtd_mes = qtd_dia * 30;
    custo_mes = qtd_mes * custo_kg;

    printf("A quantidade por kilo por animal é: %f\n", qtd_kg);
    printf("Quantidade por dia é: %f\n", qtd_dia);
    printf("A quantidade por mês é: %f\n", qtd_mes);
    printf("Custo estimado por mês é: %f\n", custo_mes);

    system("pause");
    return 0;
}
