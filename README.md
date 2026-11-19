# lab8
#include <stdio.h>

typedef struct {
   int id;
   char name[100];
   float salary;
   int dept;
   }employee;  
   
void record(employee s[], int n){
   printf("employee records");
   printf("ID    Name      Salary  Dept .");
   for(int i=0;i<n;i++){
      printf("%d    %s      %.2f  %d\n", s[i].id, s[i].name,  s[i].salary,  s[i].dept);
      }
 
void high_paid(employee s[], int n){
    int high=0;
    for(int i=0;i<n;i++){
       if(s[i].salary>s[high].salary){
           high=i;
       }
     }
     printf("Highest - paid employee :\n");
     printf("%d    %s      %.2f  %d\n", s[high].id, s[high].name,  s[high].salary,  s[high].dept);
     }

void search(employee s[], int find, int n){
    for(int i=0;i<n;i++){
       if(s[i].id==find){
         printf("Employee found :\n");
         printf("%d    %s       %.2f  %d", s[i].id, s[i].name,  s[i].salary,  s[i].dept);
         }
         else{
         printf("Employee not found");
         }
       }

void number(employee s[], int dep, int n){
     int c=0;
     for(int i=0;i<n;i++){
        if(s[i].dept==dep){
          c++;
          }
        }
     printf("Employees in department %d: %d", find, c);
     }

int main(){
   int n;
   scanf("%d", &n);
   employee s[n];
   for(int i=0;i<n;i++){
      scanf("%d    %s      %.2f  %d\n", &s[i].id, s[i].name,  &s[i].salary,  &s[i].dept);
   }
   record(s[n], n);
   high_paid(s[], n);
   
   int find;
   printf("Enter ID to search :");
   scanf("%d", &find);
   search(s, find, n);
   
   int dep;
   printf("Enter department code :");
   scanf("%d", &dep);
   number(s[], dep, n);
   
   return 0;
   }
   
