# solutions JS

## homework 1 
```js 
console.log('Hello World');
```

## Homework 2
```js 

var nX1, nX2;
nX1 = prompt('HW2 Digite el primer valor: ');
nX2 = prompt('HW2 Digite el segundo valor valor: ');

if(nX1 > nX2){ nX2 = nX1;}
console.log('larger: ' + nX2);
```
## Homework 3
```js 
var nX1, nX2, nX3;
nX1 = prompt('HW3 Digite el primer valor: ');
nX2 = prompt('HW3 Digite el segundo valor valor: ');
nX3 = prompt('HW3 Digite el tercer valor valor: ');

nX1 = nX1 * nX2 * nX3;

if(nX1 < 0)
{   
    alert ('Signo -');	
}
else{
    alert ('Signo +');	

}
```
## Homework 4
```js 
var nX1, nX2, nX3, nR = '';
nX1 = parseInt(prompt('HW4 Digite el primer valor: ') );
nX2 = parseInt(prompt('HW4 Digite el segundo valor valor: ') );
nX3 = parseInt(prompt('HW4 Digite el tercer valor valor: ') );



if(nX1 >= nX2 && nX1 >= nX3)
{   
    nR += nX1+', ';
    
    if(nX2 >= nX3)
    {
        nR += nX2+', '+nX3+'.';
    } else {
        nR += nX3+', '+nX2+'.';
    }
    
}
else if(nX2 > nX1 && nX2 >= nX3)
{
    nR += nX2+', ';
    
    if(nX1 >= nX3)
    {
        nR += nX1+', '+nX3+'.';
    } else {
        nR += nX3+', '+nX1+'.';
    }
    
}
else if(nX3 > nX1 && nX3 > nX2)
{
    nR += nX3+', ';
    
    if(nX1 >= nX2)
    {
        nR += nX1+', '+nX2+'.';
    } else 
    {
        nR += nX2+', '+nX1+'.';
    }
    
}    
    
    alert ('Ordenados: '+nR);	
```
## Homework 5
```js 
var i = 1, nX, nR; 
nR = parseInt(prompt('HW5 Digite el '+ i +' valor: ') );
while ( i < 5 ){
    i++;
    nX = parseInt(prompt('HW5 Digite el '+ i +' valor: ') );
    if(nX > nR) 
    {
            nR = nX;
    }
}
alert ('Mayor: '+nR);	

```
## Homework 6
```js 
var i = 0;
console.log('WH6 is even or odd. ');
while ( i < 16 ){
    if(i%2 == 0) 
    {
        console.log(i+' is even. ');
    }
    else 
    {
        console.log(i+' is odd. ');
    }  
    i++;  
}

```

# solutions PY
## Homework 1
```py
You just need to create a basic hello world and choose your dev tools.

print('Hello world')
```
##Homework 2
```py
Write a JavaScript program that accept two integers and display the larger.Go to the editor

lnNumbers = []
print('Digite el primer valor: ')
lnNumbers.append(input())
print('Digite el segundo valor: ')
lnNumbers.append(input())
lnNumbers.sort()
print('el numero mayor es ' + lnNumbers.pop())
```
##Homework 3
```py

lista = [int(input(f'Digite el {x+1} numero: ')) for x in range(3)]
res = 1
for x in range(3):
    res = res * lista[x]
if res > 0:
    print(' + ')
elif res < 0:
    print(' - ')
else:
    print('Cero')
resultado = ' + ' if res > 0 else ' - '
print(resultado)
print(' + ' if res > 0 else ' - ')
```
##Homework 4
``` py
Write a JavaScript conditional statement to sort three numbers. Display an alert box to show the result. Go to the editor Sample numbers: 0, -1, 4 Output: 4, 0, -1

lista = [int(input(f'Digite el {x+1} numero: ')) for x in range(3)]
print(lista.sort(reverse = True))
```

##Homework 5
```
Write a JavaScript conditional statement to find the largest of five numbers. Display an alert box to show the result. Go to the editor Sample numbers: -5, -2, -6, 0, -1 Output: 0

lista = [int(input(f'Digite el {x+1} numero: ')) for x in range(5)]
lista.sort(reverse = True)
print('largest: {}',lista[0])
```
##Homework 6
```
Write a JavaScript for loop that will iterate from 0 to 15. For each iteration, it will check if the current number is odd or even, and display a message to the screen. Go to the editor Sample Output : "0 is even" "1 is odd" "2 is even"


lista = [ str(x) +' even' if x%2 == 0 else str(x) + ' odd' for x in range(15)]
print(lista)

```