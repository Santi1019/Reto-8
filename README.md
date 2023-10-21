# Reto-8
Imprimir un listado con los números del 1 al 100 cada uno con su respectivo cuadrado.
```
for i in range(1,101): #Teniendo en cuenta que tomna el intervalo abierto
    print(i, i**2)
```
Imprimir un listado con los números impares desde 1 hasta 999 y seguidamente otro listado con los números pares desde 2 hasta 1000.
```
for i in range(1,1000,2) :
    print(i)
    

for a in range(2,1001,2):
    print(a)


print(i,a)
```
Imprimir los números pares en forma descendente hasta 2 que son menores o iguales a un número natural n ≥ 2 dado
```
n= int(input("Ingrese un numero entero: "))

if n%2==0:
    lista_mk = [i for i in range(2,n+1,2)] 

    lista_mk = sorted(lista_mk, reverse=True)
    for a in lista_mk:
        print(a)
    
else:
    listaa_ = [i for i in range(2,n,2)]
    listaa_ = sorted(listaa_,reverse=True)
    print(listaa_)
```

Imprimir los números de 1 hasta un número natural n dado, cada uno con su respectivo factorial
```
x = int(input("Ingrese numero: "))

def numero_factorial(n : int ):
  i : int = 1
  factorial : int = 1
  while(i <= n):
    factorial *= i
    i += 1
  return factorial

for n in range(1,x+1):
  print(n, numero_factorial(n) )
```

Calcular el valor de 2 elevado a la potencia n usando ciclos for.
```
n = int(input("Ingrese un numero entero: "))
for i in range(1,n+1):
    a= 2**i
    print(a)
```
Leer un número natural n, leer otro dato de tipo real x y calcular x^n usando ciclos for. Disclaimer: Trate de no utilizar el operador de potencia (**).
```
x = float(input("Ingrese un numero natural: "))
n = int(input("Ingrese un numero real: "))
import math
a = math.pow(x,n)

for i in range(1,n+1):
    a
    
print(a)
```

Diseñe un programa que muestre las tablas de multiplicar del 1 al 9.
```
m:int=1
for i in range(1,10):
    for m  in range(1,11):
        a= i*m
    
        print(a)
```
Diseñar una función que permita calcular una aproximación de la función exponencial alrededor de 0 para cualquier valor x (real), utilizando los primeros n términos de la serie de Maclaurin. Nota: use math para traer la función exponencial y mostrar la diferencia entre el valor real y la aproximación.
```
x = int(input("Ingrese numero: "))  #Defino la funcion que me da e factorial de un numero

def numero_factorial(x): #En el desarrollo de esta, inicializo 2 variables
  i : int = 1
  factorial : int = 1
  while(i <= x):  #Esto para tener el listado de numeros por los que multiplicaré
    factorial *= i
    i += 1 #De esta manera, le doy continuidad 
  return factorial

a= int(input("Ingrese un numero entero: "))  
n = int(input("Ingrese un numero entero: "))

def aproximacion_exp(a,n): #Funciona bien para valores grandes, entre más pequeños, más aumenta el error
  suma : float =0
  for x in range(0,n+1):
      q = (a**x)/numero_factorial(x)
      suma+= q
  return suma  
print (aproximacion_exp(a,n))  


import math
w = math.exp (a)
print(w)
```

 
Diseñar una función que permita calcular una aproximación de la función seno alrededor de 0 para cualquier valor x (real), utilizando los primeros n términos de la serie de Maclaurin. Nota: use math para traer la función seno y mostrar la diferencia entre el valor real y la aproximación.
x = float(input("Ingrese numero real: "))
```
def numero_factorial(x):
  i : int = 1
  factorial : int = 1
  while(i <= x):
    factorial *= i
    i += 1
  return factorial

a = float(input("Ingrese un numero real: "))
n = int(input("Ingrese un numero entero: "))

def funcion_9_punto (a,n): #Funciona bien para valores pequeños, entre más aumenta el valor de a y de n, más aumenta el error
  suma: int = 0
  for x in range(0,n+1):
    q= ((-1)**x)*((a**(2*x+1))/ numero_factorial((2*x)+1)) 
    suma+=q
  return suma

print (funcion_9_punto(a,n))    

import math
w= math.sin(a)
print(w)
```
 
Diseñar una función que permita calcular una aproximación de la función arcotangente alrededor de 0 para cualquier valor x en el rango [-1, 1], utilizando los primeros n términos de la serie de Maclaurin. Nota: use math para traer la función arctan y mostrar la diferencia entre el valor real y la aproximación.
```
x = float(input("Ingrese numero real: "))

def numero_factorial(x): #Se aproxima más entre más pequeño sea el numero 
  i : int = 1
  factorial : int = 1
  while(i <= x):
    factorial *= i
    i += 1
  return factorial

n = int(input("Ingrese un numero entero: "))
a = float(input("Ingrese un numero real: "))
def funcion_arctan(n,a):
    suma: int = 0
    for x in range(0,n+1):
       q=((-1)**x)*(a**(2*x+1))/(2*x+1)
       suma+=q
       return suma
print(funcion_arctan(n,a))   

import math
q= math.atan(a)
print(q)
```               
