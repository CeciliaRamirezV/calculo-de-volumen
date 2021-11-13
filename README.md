# calculo-de-volumen
#include <stdio.h>
#include <conio.h>
#include<math.h>
#include<cstdlib>

void volumen_cubo();
void volumen_cilindro();
void volumen_esfera();

// FUNCIONES
void volumen_cubo(){
   int lado;
   int volumen;
   printf("Dame el lado del cubo: \n");
   scanf("%d",&lado);
   volumen=pow(lado,3);
   printf("El volumen del cubo es %d \n",volumen);
}
void volumen_cilindro()
{
   int radio ,altura;
   float volumen;
   printf("Dame el radio del cilindro: \n");
   scanf("%d",&radio);
   printf("Dame la altura del cilindro: \n");
   scanf("%d",&altura);
   volumen=(3.1416*pow(radio,2))*altura;
   printf("El volumen del cilindro es: %2.2f unidades cubicas \n",volumen);
}
void volumen_esfera()
{
   int radio;
   float volumen;
   printf("Dame el radio de la esfera: \n");
   scanf("%d",&radio);
   volumen=4*(3.1416)*pow(radio,3)/3;
   printf("El volumen de la esfera es: %2.2f unidades cubicas \n",volumen);
}
// PRINCIPAL
int main()
{ 
int opcion;
do
 {
   int opc;
   printf("\t Que deseas calcular?\n\n");
   printf("\t 1.- Volumen de cubo\n");
   printf("\t 2.- Volumen de cilindro\n");
   printf("\t 3.- Volumen de esfera\n");
   scanf("%d",&opc);
   if (opc==1)
   volumen_cubo();
   if(opc==2)
   volumen_cilindro();
   if(opc==3)
   volumen_esfera();
   printf("\nDeseas repetir el programa: 1.- SI  2.- NO : ");
   scanf("%d",&opcion);
   system ("cls");
}
   while (opcion==1);
   return 0;
}
