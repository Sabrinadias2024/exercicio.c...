#include <stdio.h>

int main()
{
        int mes,
            dias=31;

        printf("Digite o mes [1-12]: ");
        scanf("%d", &mes);

        if(mes>12 || mes<1)
            printf("Mes invalido");
        else
            switch( mes )
                {
                    // fevereiro: subtraímos 2 dias aqui e 1 dia no próximo case
                    case 2:
                        dias -=2;

                    //meses que possuem 30 dias: só subtraímos 1 dia
                    case 4: case 6: case 9: case 11:
                        dias--;

                }

        printf("O mes %d possui %d dias", mes, dias);

}

