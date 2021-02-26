
#include <string.h>
#include <stdio.h>
#include <stdlib.h>
#include <conio.h>
#include <locale.h>

#define MAX 20
typedef struct{
    char nome[20];
    int cpf;
}cadastro;


    int main(void){
        setlocale(LC_ALL,"portuguese");

        cadastro vetor [MAX];

        void empresa(void);
        int menu(void);
        int opc, i, encontrou;
        char busca[20];

        empresa();
        menu();
        opc = menu();
    
        while (opc != 0){
        switch(opc){
            system("cls");
            case 1:
            printf("Digite seu cpf: \n");
            
            break;
            case 2:

            for(i=0; i<MAX; i++){
            printf("Digite seu nome completo: \n");
            fgets(vetor[i].nome, 20, stdin);
            fflush(stdin);
            printf("Digite seu cpf: \n");
            scanf("%d%*c", &vetor[i].cpf);
            }
        break;
            case 3:
            printf("Digite o nome desejado: \n");
            fgets(busca, 20, stdin);
            fflush(stdin);
            encontrou = 0;
                 for(i=0; i < MAX; i++){
                        if(strcmp(busca, vetor[i].nome)==0) {
                            printf("O funcionário digitado é ¨%s\n", vetor[i].nome);
                            encontrou++;
                }
                 }
                 if(encontrou == 0){
                     puts("Nome digitado nao foi encontrado!");
                 }
            break;
        }
        }

        return 0;
    }
    void empresa(void){
        printf("**********\t");
        printf("C O M P O S E   P L A N E J A D O S");
        printf("\t**********");
    }
    int menu(void){
        int opcao;

        printf("\nDigite a opção desejada: \n");
        printf("\n1- Assinatura eletrônica");
        printf("\n2- Cadastrar funcionário");
        printf("\n3- Listar funcionários");
        printf("\n4- Ver horários\n");
        scanf("%d%*c", &opcao);

    return opcao;
    }