/*
 * adventofcode.com - Day 1 / Part Two
 * Author: Droditto
 * 
 */


#include <stdio.h>
#define N 200

int main(int argc, char **argv)
{
	int v_num[N];
	FILE *pf;
	int ctrl, i, j, k;
	
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
				for(k = j + 1; k < N; k++){
					if(v_num[i] + v_num[j] + v_num[k] == 2020){
					// Mostrar el producto de dichos números
					printf("\n\n%d + %d + %d == %d", v_num[i], v_num[j ], v_num[k], v_num[i] + v_num[j] + v_num[k]);
					printf("\n%d * %d * %d == %d", v_num[i], v_num[j], v_num[k], v_num[i] * v_num[j] * v_num[k]);
					printf("\n\nPosiciones:");
					printf("\n(%3d) %d", i + 1, v_num[i]);
					printf("\n(%3d) %d", j + 1, v_num[j]);
					printf("\n(%3d) %d", k + 1, v_num[k]);
					}
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
