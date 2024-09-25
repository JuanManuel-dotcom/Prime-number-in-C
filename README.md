# Prime-number-in-C
School assignment for a C language program where you enter a number and it tells you if it is a prime number or not.





#include <stdio.h>

int main() {
    int num, i, esPrimo = 1;
    // es numero Primo si inicia como 1

    printf("Ingresa un numero: ");
    scanf("%d", &num);

    if (num <= 1) {
        esPrimo = 0; // Números menores o iguales a 1 no son primos
    } else {
        for (i = 2; i * i <= num; i++) {

                // Solo comprobar hasta la raíz cuadrada de num

            if (num % i == 0) {
                esPrimo = 0; // Si es divisible por i, no es primo
                break;
        // Salimos del ciclo
            }
        }
    }

    if (esPrimo) {
        printf("%d es un numero primo.\n", num);
    } else {
        printf("%d no es un numero primo, maldito perro.\n", num);
    }

    return 0;
}
