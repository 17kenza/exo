# exo 1
#include<stdio.h>
#include<math.h>
int n=10;
void sélection (int T[10]){
int max,i,posmax;
max=T[0];
posmax=0;
for(i=0;i<10;i++){
if(max<T[i]){
max=T[i];
posmax =i;
}
}
for(i=posmax;i<10;i++){
T[i]=T[i+1];
}
T[n-1]=max;
n--;
printf("le tri par sélection est :\n");
for(i=0;i<10;i++)
printf("T[%d]=%d",n-1,max);
}
void insertion (int T[10]){
int i,j,tmp;
for(i=0;i<=9;i++){
tmp=T[i];
j=i-1;
while(j>=1 && T[j]>tmp){
T[j+1]=T[j];
j=j-1;
}
T[i+1]=tmp;
}
printf("le tri par insertion est:");
for(i=0;i<=9;i++)
printf("T[%d]=%d",i+1,tmp);
}
void bulles(int T[10]){
int x,i,j;
for(i=0;i<=9;i++){
for(j=0;j<=9;j++){
if(T[j]<T[j+1]){
x=T[j];
T[j]=T[j+1];
T[j+1]=x;
}
}
}
printf("le tri par insertion est:");
for(i=0;i<=9;i++)
for(j=0;j<=9;j++)
printf("T[%d]=%d \n",i,T[j]);
}
void Tableau(int T[10]){
int i,j,Tpe;
for(i=0;i<=9;i++){
for(j=0;j<=9;j++){
if(T[i]<T[j])
Tpe=T[i];
T[i]=T[j];
T[j]=Tpe;
}
}
for(i=0;i<=9;i++)
for(j=i+1;j<=9;j++)
printf("%d \n",T[j]);
}


int main(){
int T[10];
int i;
printf("saiser les valeurs :");
for(i=0;i<=9;i++){
printf("T[%d]= ",i);
scanf("%d",&T[i]);
}
sélection (T);

int main(){
int T[10];
int i;
printf("saiser les valeurs :");
for(i=0;i<=9;i++){
printf("T[%d]= ",i);
scanf("%d",&T[i]);
}
insertion (T);

int main(){
int T[10];
int i;
printf("saiser les valeurs :");
for(i=0;i<=9;i++){
printf("T[%d]= ",i);
scanf("%d",&T[i]);
}
bulles (T);
int main(){
int T[10];
int i;
printf("saiser les valeurs :");
for(i=0;i<=9;i++){
printf("T[%d]= ",i);
scanf("%d",&T[i]);
}
tableau (T);
    return 0;
}}}}

