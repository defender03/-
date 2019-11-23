# -
#include <stdio.h>
int main()
{
    
    
int a,k=0,i,j,b;
FILE *f;
f=fopen("data.txt","rt");

fscanf(f,"%d",&a);
fclose(f);
if(a<3 || a>32000)
printf("Incorrect number\n");

else{
while(k!=2){
for(i=1;i<32003;i++){
for(j=1;j<=32003;j++){
if((a+i)%j==0) k+=1;
}
if(k==2){b=a+i;break;}
k=0;
}
}
printf(" The nearest Prime number on the right");

f=fopen("data1.txt","w");

fprintf(f," %d \n",b);
fclose(f);
k=0;
while(k!=2){
for(i=1;i<32003;i++){
for(j=1;j<=32003;j++){
if((a-i)%j==0) k+=1;
}
if(k==2){b=a-i;break;}
k=0;
}
}
printf("\n The nearest Prime number on the left");

f=fopen("data2.txt","w");

fprintf(f," %d \n",b);
fclose(f);
}
return 0;
}


