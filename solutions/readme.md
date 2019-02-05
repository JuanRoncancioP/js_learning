# solutions

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