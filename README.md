#include "pch.h" 
#include <iostream> 
#include <math.h> 
using namespace std; 
int main() 
{ 
const int n = 3; 
float x[n], y[n]; 
setlocale(0, "Rus"); 

int i; 
cout « "Введите x\n"; 
for (i = 0; i < n; i++) 
cin » x[i]; 

cout « "Введите y\n"; 
for (i = 0; i < n; i++) 
cin » y[i]; 

float s1 = 0; 
for (i = 0; i < n; i++) 
s1 += x[i]; 

float s2 = 0; 
for (i = 0; i < n; i++) 
s2 += y[i]; 

float z[n]; 
for (i = 0; i < n; i++) 
{ 
z[i] = 0; 
z[i] = x[i] * y[i]; 
} 
float s3 = 0; 
for (i = 0; i < n; i++) 
s3 += z[i]; 

float w[n]; 
for (i = 0; i < n; i++) 
{ 
w[i] = 0; 
w[i] = x[i] * x[i];  
} 

float s4 = 0; 
for (i = 0; i < n; i++) 
s4 += w[i]; 

float a, b; 
a = (n*s3 - s1 * s2) / (n*s4 - pow(s1, 2)); 
cout « "a = " « a « endl; 
b = (s2 – (a * s1)) / n; 
cout « "b = " « b « endl; 
system("pause"); 
return 0; 
} 


