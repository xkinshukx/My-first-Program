# My-first-Progra
# just a simple calculator in C language

#include<stdio.h>
#include<math.h>

void multiply(float a,float b);
void divide(float a,float b);
void addition(float a,float b);
void subtract(float a,float b);

int main(){

    float a,b;
    char calculate;

    printf("enter first numbewr : ");
    scanf("%f",&a);

    printf("enter second number : ");
    scanf("%f",&b);

    printf("enter M for multiply\nenter D for divide\nenter A for addition\nenter S for subtraction\n");
    scanf(" %c",&calculate);

    if(calculate == 'M' || calculate == 'm'){
        multiply(a,b);
    }
    else if(calculate == 'D' || calculate == 'd'){
        divide (a,b);
    }
    else if ( calculate == 'A' || calculate == 'a'){
        addition(a,b);
    }
    else if (calculate == 'S' || calculate == 's'){
        subtract(a,b);
    }
    else{
        printf("padh le bkl upar enter M,D,A,S\n");
    }
    return 0;    
}

void multiply(float a, float b){
    float sum = a * b;
    printf("Answer :%f\n",sum);
}
void divide(float a,float b){
if (b != 0) {
        float sum = a / b;
        printf("Answer: %f\n", sum);
    } else {
        printf("Error: Division by zero!\n");
    }
}
void addition(float a,float b){
    float sum = a + b;
    printf("Answer :%f\n",sum);
}
void subtract(float a,float b){
    float sum = a - b;
    printf("Answer :%f\n",sum);
}
