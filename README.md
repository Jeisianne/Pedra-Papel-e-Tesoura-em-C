#include<stdio.h>
#include<stdlib.h>
#include<time.h>

int main() {
    int escolha, computador;
    
    srand(time(NULL));
    computador = (rand() %3) +1;
    
    printf("*******************\n");
    printf("Qual a sua escolha??\n");
    printf("*******************\n");
    printf("1- Pedra, 2- Papel, 3- Tesoura\n");
    scanf("%d",&escolha);
    
    printf("Computador escolheu: %d\n", computador);
   
    if(escolha == computador) {
    printf("Empate!!\n");
    } 
    else {
        switch(escolha) {
            case 1:
            if(computador == 3) printf("Você venceu!! (Pedra quebra Tesoura)\n");
            else printf("Você perdeu!! (Papel embrulha Pedra)\n");
            break;
            
            case 2:
            if(computador == 1) printf("Você venceu!! (Papel embrulha Pedra)\n");
            else printf("VocÊ perdeu!! (Tesoura corta Papel)\n");
            break;
            
            case 3:
            if(computador == 2) printf("Vovê venceu!! (Tesoura corta Papel)\n");
            else printf("Você perdeu!! (Pedra esmaga Tesoura)\n");
            break;
            
            default:
            printf("Opção inválida!!\n");
        } 
    }
    return 0;
}
