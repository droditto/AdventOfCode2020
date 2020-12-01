/*
 * adventofcode.com - Day 1
 * Author: Droditto
 * 
 */


#include <stdio.h>
#define N 200

int main(int argc, char **argv)
{
	int v_num[N];
	FILE *pf;
	int ctrl, i, j;
	
	pf = fopen("numeros.txt", "r");
	if(pf == NULL){
		printf("\nError al abrir el archivo");
	}else{
		i = 0;
		// Grabar archivo en el vector
		do{
			ctrl = fscanf(pf, "%d", &v_num[i]);
			if(ctrl == 1){
				printf("\n(%3d) %d", i + 1, v_num[i]);
				i++;
			}
		}while(ctrl == 1);
		
		// Comprobar qué números suman 2020 entre si
		for(i = 0; i < N; i++){
			for(j = i + 1; j < N; j++){
				if(v_num[i] + v_num[j] == 2020){
					// Mostrar el producto de dichos números
					printf("\n\n%d + %d == %d", v_num[i], v_num[j], v_num[i] + v_num[j]);
					printf("\n%d * %d == %d", v_num[i], v_num[j], v_num[i] * v_num[j]);
					printf("\n\nPosiciones:");
					printf("\n(%3d) %d", i + 1, v_num[i]);
					printf("\n(%3d) %d", j + 1, v_num[j]);
				}
			}
		}
		if(fclose(pf) != 0){
			printf("\nError al cerrar el archivo de numeros");
		}
	}
	printf("\n\n");
	return 0;
}
