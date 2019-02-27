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
##Py agenda
```
import re
import os
import json
import Utilidades

#import Utilidades
#import Menu
#import Contactos


class Utilidades:

    def validaTelefono(self, telefono):
        patron = r"[^0-9] -"
        return(not re.search(patron, telefono))

    def validaCorreo(self, correo):
        patron = r"([\w\.\-]+)@([\w\.-]+)\.([\w\.-]+)"
        return(re.search(patron, correo))

    def confirmacion(self, label, opciones):
        op = opciones[0].lower()
        opciones = [x[0].upper() for x in opciones]
        while op[0] not in opciones:
            op = input(label + ' (' + '/'.join(opciones) + '): ')
            op = [x[0].upper() for x in op]
        return(op)

    def capturaDatos(self, label, contenedor, validacion):
        respuesta = ['S']
        print('Digite su ' + label)
        while respuesta[0] == 'S':
            contenedor.append(input(label + ': '))
            if not validacion(contenedor[len(contenedor) - 1]):
                contenedor.pop()
                print(label + ' no valido')
                print('pos val ', contenedor)
            if len(contenedor):
                respuesta = self.confirmacion('Desea ingresar otro ' +
                label, ['S', 'N'])
        return(contenedor)


class Menu:

    def __init__(self, opciones):
            self.opciones = opciones
            self.salir = max(opciones)
            #self.objeto = objeto
            self.listaOpciones = list(x for x in self.opciones)
            self.opmin = str(int(min(self.listaOpciones)) - 1)

    def imprimirMenu(self, titulo = 'GUIA TELEFONICA\n'):
        print(titulo)
        print('\n'.join(self.opciones[x] for x in self.opciones))

    def leerOpcion(self):
        op = self.opmin
        while op not in self.listaOpciones:
            op = input('Digite su opcion: ')
            if(op not in (self.listaOpciones)):
                print('\tLos números del menú... Hijo!!!')
        return(op)

class Contactos:

    def __init__(self):
        self.util = Utilidades()

    def leerDir(self):
        statinfo = os.stat('directorio.txt')
        if not statinfo:
            self.datos = {}
            self.llave = '1'
        else:
            with open("directorio.txt", "r") as File:
                if bool(File):
                    self.datos = json.loads(File.read())
                    self.llave = str(int(max(self.datos)) + 1)
                    #print(self.datos, type(self.datos))
                else:
                    print('El directorio no pudo ser abierto')

    def crearContacto(self):
        nombre = input('Nombre del contacto: ')
        telefonos = self.util.capturaDatos('Teléfono', [],
        self.util.validaTelefono)
        correos = self.util.capturaDatos('Correo', [], self.util.validaCorreo)
        self.datos = {self.llave: [nombre, telefonos, correos]}
        self.llave = str(int(self.llave) + 1)

    def guardaDir(self):
        with open("directorio.txt", "w") as File:
            if bool(File):
                File.write(json.dumps(self.datos))
            else:
                print('El directorio no pudo ser abierto para guardar')

    def correMenuP(self):

        menup = {
            '3': '9. Salir',
            '2': '2. Listar contactos',
            '1': '1. Crear contacto'
        }
        m = Menu(menup)
        m.imprimirMenu()
        op = m.leerOpcion()
        #print('\n\n', menup[op][0])
        if(op == '1'):
            pass
        elif(op == '2'):
            self.listarContactos()
        elif(op == '3'):
            print('\n\n', menup[op][0], '\n')

    def listarContactos(self):
        #for x in self.datos:
        #    print('\t', x.ljust(10, '.'), self.datos[x][0])
        #print('\t', self.llave.ljust(10, '.'), 'Menu Principal')
        menuContactos = {x:'\t'+ x.ljust(10, '.') + self.datos[x][0] for x in self.datos}
        menuContactos[self.llave] = '\t'+ self.llave.ljust(10, '.') + 'Menu Principal'
        conmenu = Menu(menuContactos)
        conmenu.imprimirMenu('\n\n\tContactos')
        op = conmenu.leerOpcion()

        if(op != self.llave):
            print('\n\n\t\tDatos ',self.datos[op][0],'\n')
            print('\t\tTelefonos\n')
            for x in self.datos[op][1]:
                print('\t\t\t',x)
            print('\t\tCorreos\n')
            for x in self.datos[op][2]:
                print('\t\t\t',x)





contactos = Contactos()
contactos.leerDir()
contactos.correMenuP()


```
