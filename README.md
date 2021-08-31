# Repositorio_fase1
Tercer semestre evidencia 1
# Aplicar  las  estructuras  nativas  del  lenguaje  Python  tales  como  Listas,Tuplas,  Conjuntos  y  Diccionarios para almacenar en memoria principal el estado de una aplicación a desarrollar y emplearlas para codificar pilas y colas que permitan el proceso delosconjuntos de datos.

# Ejercicios semana_1 (17)
# 1.- #2 elevado a a 5ta potencia
import math
print(math.pow(2,5))


# 2._Raiz cuadrada de 2
import math
print(math.sqrt(2)) 


# 3._Longitud euclídea entre 3 y . Equivale a la longitud de la hipotenusa de un triangulo rectangulo de lados con longitud igual a 3 y 4
import math
print(math.hypo(3,4))


# 4._Coseno del angulo de 2*pi radianes (180°)
import math
print(math.cos(2*math.pi))


# 5._Imprime una letra de una lista de letras
import random
print(random.choice(['A','B','C','D','E','F']))


# 6._Repite 14 veces una lista de frutas generada
import random
mylist=["apple","banana","cherry"]
print(random.choices(mylist, weights[10,1,1], k=14))


# 7._De una lista de frutas imprime la misma lista en orden diferente
import random
mylist=["apple","banana","cherry"]
print(random.shuffle(mylist))
print(mylist)


# 8._De una lista de frutas regresa un ejemplo de 2 frutas de la lista
import random
mylist=["apple","banana","cherry"]
print(random.sample(mylist))


# 9._Imprime un numero aleatorio que este entre el 0 y 1
import random
print(random.random())


# 10._Imprime el directorio actual
import os
mi_ubi=os.getcwd()
print(mi_ubi)


# 11._Imprime lista de directorios de la direccion actual
import os
print(os.listdir(os.getcwd()))


# 12._Mostrar aviso de si existe un directorio
import os
print(os.path.exists("/Users/mediacenter"))


# 13._Crea una carpeta llamada sistemas
import os
os.makerirs("Sistemas")


#14._Mostrar la fecha y hora actual
import datetime
x= datetime.datetime.now()
print(x)


#15._Mostrar año y día
import datetime
x=datetime.datetime.now()
print(x.year)
print(x.strftime("%A"))
 
 
# 16._Dada una fecha imprimirla en formato de fecha y hora
import datatime
x=datetime.datetime(2020,5,17)
print(x)


# 17._Dada una fecha imprime el nombre del mes
import datetime
x= datetime.datetime(2018,6,1)
print(x.strftime("%B"))

_---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------_

# Ejercios semana 1 (5)
# 1. Ejercicio Math
import math
SEPARADOR = ("*" * 20) + "\n"

'''
Ejemplo para ilustrar la importación de la librería math en Python 3
Demuestra el uso de: floor(x),trunc(x),ceil(x),round(x),factorial(x),pow(x,y),sqrt(x) y pi
'''
valorFlotante = float(input("Introduce un valor con fracción decimal:\n"))
print(f"El siguiente entero hacia arriba de {valorFlotante} es {math.ceil(valorFlotante)}")
print(SEPARADOR)
print(f"El siguiente entero hacia abajo de {valorFlotante} es {math.floor(valorFlotante)}")
print(SEPARADOR)
print(f"La parte entera truncada de {valorFlotante} es {math.trunc(valorFlotante)}") #Equivalent e a floor() para positivos, y a ceil() para negativos porque se mueve hacia el 0
print(SEPARADOR * 2)
pass

valorNumerico = int(input("Dame un valor entero:\n"))
print(f"La raiz cuadrada de {valorNumerico} es igual a {math.sqrt(valorNumerico)}")
print(SEPARADOR)
print(f"El factorial de {valorNumerico} es igual a {math.factorial(valorNumerico)}")
potencia = int(input("Dame un valor entero:\n"))
print(f"El resultado de elevar {valorNumerico} a la {potencia} potencia es igual a {math.pow(valorNumerico,potencia)}")
print(SEPARADOR * 2)
pass
print(f"El valor de Pi es {math.pi}")


# 2.Ejercicio Random
import random
SEPARADOR = ("*" * 20) + "\n"
print(f"Obteniendo un numero entero aleatorio que puede ir del 0 al 19: {random.randrange(20)}")
print(SEPARADOR)
print(f"Obteniendo un numero entero aleatorio par que puede ir del 2 al 20: {random.randrange(2,21, 2)}")
print(SEPARADOR)
print(f"Obteniendo un valor numérico entre 0.0 y 1.0: {random.random()}")
print(SEPARADOR * 2)
listaDePrueba = [10, 20, 30, 40, 15, 25, 35, 45]
print(f"La lista de prueba es {listaDePrueba}")
print(f"El valor seleeccionado aleatoriamente de la lista anterior es {random.choice(listaDePrueba)}")
print(SEPARADOR)
random.shuffle(listaDePrueba)
print(f"La lista ya 'perturbada/barajada' es {listaDePrueba}")


# 3.Ejercicio Time
import time
SEPARADOR = ("*" * 20) + "\n"
segundos = int(input("Cantidad de segundos a esperar:\n"))
time.sleep(segundos) #Espera por lo menos la cantidad de segundos especificada
print(f"Han transcurrido, por lo menos, {segundos} segundos")
print(SEPARADOR * 2)
print("Iniciaremos la medición de un proceso simulado")
horaInicial = time.time()
for termino in range(10):
 time.sleep(segundos)
print("proceso simulado concluído!")
duracion = time.time() - horaInicial #Puede verse afectado si se cambia la hora del sistema
print(f"La duración del proceso simulado fue de {duracion} segundos")


# 4.Ejercicio Datetime
import datetime
import time
SEPARADOR = ("*" * 20) + "\n"
#Creación de una hora específica
hora = datetime.time(10, 20, 30)
print(f"El tipo de objeto de la hora es {type(hora)}")
print(f"La hora es {hora}")
print(f"La hora de {hora} es {hora.hour}") #Limitado 0..23
print(f"El minuto de {hora} es {hora.minute}") #limitado 0..59
print(f"El segundo de {hora} es {hora.second}") #limitado 0..59
print(f"El microsegundo de {hora} es {hora.microsecond}") #limitado 0..999
print(SEPARADOR * 2)
#Determinar la fecha del sistema
fecha_actual = datetime.date.today()
print(f"El tipo de objeto de la fecha es {type(fecha_actual)}")
print(f"La fecha actual es {fecha_actual}")
print(f"El año actual es {fecha_actual.year}")
print(f"El mes actual es {fecha_actual.month}")
print(f"El día actual es {fecha_actual.day}")
print(SEPARADOR * 2)
#Convertir un string a fecha
fecha_capturada = input("Dime una fecha (dd/mm/aaaa): \n")
fecha_procesada = datetime.datetime.strptime(fecha_capturada, "%d/%m/%Y").date()
print(type(fecha_capturada))
print(type(fecha_procesada))
print(f"La fecha capturada se transformó a {fecha_procesada}")
#Aritmética de fechas básica
cant_dias = int(input("Dime la cantidad de días a adelantar:\n"))
nueva_fecha = fecha_procesada + datetime.timedelta(days=+cant_dias)
print(f"La nueva fecha es {nueva_fecha}")
print(SEPARADOR)


# 5.Ejercicio SYSOS
import sys
import os
SEPARADOR = ("*" * 20) + "\n"
#uso del módulo sys
lista = list()
for numero in range(1, 1001):
 lista.append(numero)
print(f"La lista tiene {len(lista)} elementos, y tiene un tamaño de {sys.getsizeof(lista)} bytes")
print(SEPARADOR)
tupla = tuple(lista)
print(f"La tupla tiene {len(tupla)} elementos, y tiene un tamaño de {sys.getsizeof(tupla)} bytes")
print(SEPARADOR)
#uso del módulo os
print(f"El directorio actual de trabajo es {os.getcwd()}")
for raiz, dirs, archivos in os.walk(".", topdown=False): #Demostración de unpacking
 for nombre in archivos:
     print(os.path.join(raiz, nombre))
 for nombre in dirs:
     print(os.path.join(raiz, nombre))
     
 
_---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------_

# Ejercicios semana 2 (22)

# Ejercicio_1
factura = ['pan','huevos',100,1234]
print(factura)


# Ejercicio_2 
factura = ['pan','huevos',100,1234]
print(factura[0])


# Ejercicio_3
factura = ['pan','huevos',100,1234]
print(factura[3])


# Ejercicio_4
factura = ['pan','huevos',100,1234]
print(len(factura))


# Ejercicio_5
factura = ['pan','huevos',100,1234]
print(len(factura)-1)


# Ejercicio_6 
factura = ['pan','huevos',100,1234]
print(factura[-1])


# Ejercicio_7
'Escribir un programa que almacene las asignaturas de un curso (por ejemplo mates, fisica,quimica, historia y lengua) en una lista y la muetsre en la pantalla'
materias = ["Matematicas", "Fisica", "Quimica","Historia", "Lengua"]
print(materias)


# Ejercicio_8
print("5->", valores.count(5))


# Ejercicio_9
valores =("Python",True,"Zope",5)
print(valores.index(True))
print(valores.index(5))


# Ejercicio_10
tecnologias =('Zope','Plone','Pyramid')
for i in range(0,len(tecnologias)):
    print(i,tecnologias[i])


# Ejercicio_11
text = 'Python Programing'
#get slice object to slice Python
sliced_text = slice(6)
print(text[sliced_text]) 


# Ejercicio_12
a = ("a","b","c","d","e","f","g","h")
x = slice(0,8,3)
print(a[x])


# Ejercicio_13
a = ("a","b","c","d","e","f","g","h")
x = slice(3,5)
print(a[x])


# Ejercicio_14
py_list = ["P","y","h","o","n"]
py_tuple = ("P","y","h","o","n")

#contains indices 0, 1 and 2
slice_object = slice(3)
print(py_list[slice_object])#['p','y','t']

#contains indices 1 and 3
slice_object = slice(1,5,2)
print(py_tuple[slice_object])#('y','h')


# Ejercicio_15 
# contains indices 0, 1 and 2}
py_string = 'Python'
print = (py_string[0:3]) #Pyt

#contins indices 1 and 3
print(py_string[1:5:2])#yh


# Ejercicio_16
py_string = 'Python'

thisdict = {
    "brand": "Ford",
    "model": "Mustang",
    "year": 1964
}
print(thisdict)


# Ejercicio_17 
#imprima el valor de marca 

thisdict = {
    "brand": "Ford",
    "model": "Mustang",
    "year": 1964
}
print(thisdict["brand"])


# Ejercicio_18
thisdict = {
    "brand": "Ford",
    "model": "Mustang",
    "year": 1964,
    "year": 2020
}
print(thisdict)


# Ejercicio_19
thisdict = {
    "brand": "Ford",
    "model": "Mustang",
    "year": 1964,
    "year": 2020,
    "color": "Black"
}
print(len(thisdict))


# Ejercicio_20 
thisset = {"apple","banana","cherry"}
print(thisset)


# Ejercicio_21
thisset = {"apple","banana","cherry","apple"}
print(thisset)


# Ejercicio_22
thisset = {"apple","banana","cherry","apple"}
print(len(thisset))


_---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------_

# Ejercicios semana 2 (4)

# 1.EJERCICIOS DE LISTAS
SEPARADOR = ("*" * 20) + "\n"
#Creación de listas
#Lista vacía
lista_vacia = list()
otra_lista_vacia = []
#Lista con elementos iniciales
lista_uno = [1, 2, 3, 4]
print(lista_uno)
print(SEPARADOR)
pass
#Agregar elementos a listas existentes
lista_uno.append(5)
print(lista_uno)
lista_uno.append((6, 7)) #Una lista puede ser un elemento de otra lista
print(lista_uno)
print(SEPARADOR)
pass
#Remover elementos de una lista
lista_uno.remove((6, 7)) #Se le pasa el valor del elemento a remover
print(lista_uno)
print(SEPARADOR)
pass
#Ordenar elementos de una lista
#sort()
lista_original1 = [3, 4, 2]
print(lista_original1)
lista_original1.sort()
print(lista_original1)
pass
#sorted()
lista_original2 = [23, 10, 30, 5]
lista_ordenada = sorted(lista_original2)
print(f"lista original = {lista_original2}, y la version ordenada es {lista_ordenada}")
print(SEPARADOR)
pass
#Comprension de listas
print(f"lista original = {lista_uno}")
#SIN comprensión de listas
lista_uno_al_doble = []
for valor in lista_uno:
 lista_uno_al_doble.append(valor * 2)
print(f"Lista resultante, cada elemento al doble = {lista_uno_al_doble}")
pass
#CON comprensión de listas
lista_uno_al_doble = [valor * 2 for valor in lista_uno]
print(f"Mismo resultado, pero con comprensión de listas = {lista_uno_al_doble}")
pass
#Comprensión de listas con condición
lista_valores_pares = [valor for valor in lista_uno if (valor % 2 == 0)]
print(f"Solamente se agregaron los elementos con valor par: {lista_valores_pares}")


# 2.EJERCICIO DE COLAS
SEPARADOR = ("*" * 20) + "\n"
cola = list() #Cola utilizando una lista
for cantidad in range(5):
 nuevo = input("Nombre del recién llegado: ")
 cola.append(nuevo)
print(f"Se agregaron {len(cola)}, elementos:")
for elemento in cola:
 print(elemento)
print(SEPARADOR)
pass #Hacer notar que los elementos permanecen en la cola
print("Procedemos a retirarlos de la cola")
while cola:
 print(cola.pop(0))
pass #Verificar que la estructura se encuentra vacia


# 3.Eliminar elementos de un diccionario
print("*" * 20)
del diccionario_citas["AMLO"]
print(diccionario_citas)
pass
#Opciones para obtener el volcado de un diccionario,
#en cada una, la respuesta DEBE convertirse a una lista primero
#para un más fácil manejo
#Opción 1 : Todas las claves, solamente las claves
print(list(diccionario_citas.keys()))
pass
#Opción 2 : Todos los valores, solamente los valores
print(list(diccionario_citas.values()))
pass
#Opción 3 : Todos los elementos, elemento por elemento
print(list(diccionario_citas.items()))


# 4.EJEMPLO LISTAS ALEATORIAS ANIDADAS
import random
SEPARADOR = ("*" * 20) + "\n"
#Creación de una lista con diez valores aleatorios entre 1 y 100
lista = [random.randrange(1,101) for valor in range(10)]
print(type(lista))
print(f"El primer elemento es {lista[0]} y el último es {lista[9]}")
print(type(lista))
print(SEPARADOR)
#Creación de una lista de cinco listas con diez elementos cada una
lista_de_listas = [[random.randrange(1,101) for valor in range(10)] for valor in range(5)]
print(lista_de_listas)
print(f"El primer elemento es {lista_de_listas[0][0]} y el último es {lista_de_listas[4][9]}")
#print(lista_de_listas[0][:])
print(lista_de_listas[0])
for lista_interna in lista_de_listas:
 print(lista_interna[0])
print(type(lista_de_listas))
print("[")
for lista_primer_nivel in lista_de_listas:
 #print(f"lista interna: {lista_primer_nivel}")
 print("[", end="")
 for elemento in lista_primer_nivel:
     print(f"{elemento}", end="\t")
 print("]", end="")
 print("")
print("]")
print(SEPARADOR)
print(f"El elemento 0,2 es {lista_de_listas[0][2]}")
print(f"El elemento 2,7 es {lista_de_listas[2][7]}")
#print(lista_de_listas[0,4])#ESTO ES UN ERROR


_---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------_

# Ejercicios semana 3 (8)
# Ejercicio_1
from multiprocessing import Queue
import queue
import random 

queue_time = Queue

print("Almacenamiento en queue..")
for i in range(5):
    random_time=random.randint(1,100)
    queue_time.put(random_time)
    print("%d added at queue" % random_time)
print("leyendo de queue...")
while not queue_time.empty():
    time_read = queue_time.get()
    print("%d read from queue" % time_read)
    
    

# Ejercicio_2 
class Cola:
    def __init__(self):
        self.items =[]
    
    def estaVacia(self):
        return self.items == []
    
    def agregar(self, item):
        self.items.insert(0,item)
        
    def avanzar(self):
        return self.items.pop()
    
    def tamano(self):
        return len(self.items)
    
c = Cola() 

c.agregar(4)
c.agregar('perro')
c.agregar(True) 
print(c.tamano())

print (c.estaVacia())
c.agregar(8.4)
print(c.avanzar())
print(c.avanzar())
print(c.avanzar())



# Ejercicio_3 
#Crer un menu para colas
#creamos un alista vacia 

cola = []
#Creamos un menú con 4 colas
def main():
    print("1 Insertar cola")
    print("2 Borra en cola")
    print("3 Listar cola")
    print("4 Salir")

option = input("Elija una opcion: ")

#Esta opción permite encolar el numero en la lista 
if str(option)=="1":
    elemento = input("Introduzca el número a encolar")
    cola.append(elemento)
    print("número encolado con exito")
    main()
    
#Esta opcion saca de la lista el número en orden de ingreso 
elif str(option) == "2":
    if len(cola)>0:
        print("El número: ",cola.pop(0),"fue desencolado")
        main()
    else:
        print("Cola vacia")
        main()
    
 #Esta opción imprime en pantalla la cola
elif str(option) == "3":
     for i in cola:
         print("Cola vacia")
         main=()
         
#Esta opcion permite salir de la ejecucion del codigo
elif str(option)=="4":
    exit()
    
else:
    print("Selecciones una opcion valida.")
    main()
    
main()



# Ejercicio_4 
#Crear colección de cola y mostrar contenido.
from collections import deque cola = deque()
print(cola)



# Ejercicio_5
#Crear cola con elementos e imprimirla
from collections import deque cola = deque()
print(cola)

cola = deque(['Hector','Juan','Miguel']) print(cola)



# Ejercicio_6
#Crear una cola y después agregarle elementos
from collections import deque cola = deque()
print(cola)

cola = deque(['Hector','Juan','Miguel']) print(cola)

cola.append('Maria') cola.append('Arnaldo') print(cola)



# Ejercicio_7
Crear una cola, imprimirla, después extraer el primer elemento de la izquierda y volver a imprimir la cola
from collections import deque 
cola = deque()
cola = deque(['Hector','Juan','Miguel','Maria','Arnaldo']) 
print(cola)
print(cola.popleft()) 
print(cola)



# Ejercicio_8
Crear una clase para representar la estructura de datos cola (queue) usando una lista
class Cola:
    def init (self): 
        self.datos = []

    def cantidad(self): 
        return len(self.datos)

    def insertar(self, dato): 
        self.datos.insert(0, dato)

    def extraer(self):
        if self.cantidad():
            return self.datos.pop() 
        else:
            return None

    def primer_dato(self): 
        if self.cantidad():
            return self.datos[-1] 
    
    def ultimo_dato(self):
        if self.cantidad():
            return self.datos[0]

numeros = Cola() 
numeros.insertar(2) 
numeros.insertar(3) 
numeros.insertar(5) 
numeros.insertar(7)

print(numeros.primer_dato())   # 2
print(numeros.ultimo_dato())   # 7
print(numeros.cantidad()) # 4
 
print()

dato = numeros.extraer() 
print(dato) # 2
print(numeros.cantidad()) # 3 

print()

numeros.extraer() 
numeros.extraer() 
numeros.extraer() 
print(numeros.cantidad()) # 0

print()

dato = numeros.extraer() 
print(dato) # None

   
_---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------_
   
# Ejercicios semana 4 (12)
# Ejercicio 1
class Stack: # Creamos la clase Stack def     init (self):
self.items = []

def is_empty(self): # Metodo para verificar si la pila esta vacia return self.items == []

def push(self, item): # Metodo para insertar elementos a la pila self.items.insert(0, item)

def pop(self): # Metodo para eliminar el ultimo elemento apilado return self.items.pop(0)

def print_stack(self): # Metodo para mostrar los elementos de la pila print(self.items)


pila = Stack() # Creamos una instancia de la pila
#ingresamos algunos elementos a la pila pila.push('a')
pila.push('b')
pila.push('c')
pila.print_stack() # Mostramos los elementos de la pila pila.pop() # Utilizamos el metodo pop
pila.print_stack() # Mostramos nuevamente los elementos de la pila


# Ejercicio 2
pila = [3,4,5] 
pila.append(6) 
pila.append(7) 
print(pila)


# Ejercicio 3
pila = [3,4,5] 
pila.append(6) 
pila.append(7) 
print(pila)

print(pila.pop()) 
print(pila)


# Ejercicio 4
pila = [3,4,5] 
pila.append(6) 
pila.append(7)
print(pila)

numero = pila.pop() 
print(numero)


# Ejercicio 5
class Pila:
    def     init (self): self.items = []

def estaVacia(self):
    return self.items == []

def incluir(self, item): 
    self.items.insert(0,item)

def extraer(self):
    return self.items.pop(0)

def inspeccionar(self):
    return self.items[0]

def tamano(self):
    return len(self.items)

s = Pila() 
s.incluir('hola') 
s.incluir('verdadero')

print(s.extraer())


# Ejercicio 6
'''
Demostración de implementación de pilas utilizando listas '''

import collections 
SEPARADOR = ("*" * 20) + "\n"

pila_con_lista = list() 
for i in range(5):
    pila_con_lista.append(input("Dime el nombre a agregar: "))

#Sacar elementos de la pila 
while pila_con_lista:
      print(pila_con_lista.pop()) 
 
print(SEPARADOR)


# Ejercicio 7
'''
Demostración de implementación de pilas utilizando deques
'''

import collections 
SEPARADOR = ("*" * 20) + "\n"

pila_deque = collections.deque() 
for i in range(5):
    pila_deque.append(input("Dime el nombre a agregar: "))

#Sacar elementos de la pila 
while pila_deque:
      print(pila_deque.pop()) 
pass


# Ejercicio 8
#Creamos una lista vacia stack = []

#Creamos un Menu con 4 opciones 
def main():
    print("1 Aplilar elemento (entero)") 
    print("2 Desapilar elemento") 
    print("3 Mostrar pila")
    print("4 Salir")
    option = input("Elija una opcion: ")

   #Esta opcion permite apilar el numero en la lista 
   if str(option)=="1":
         elemento = input(" Introduzca el numero a apilar: ") 
         stack.append(elemento)
         print(" Elemento apilado ") 
         main()

   #Esta opcion saca desapila a partir del ultimo numero ingresado 
   elif str(option)=="2":
        if len(stack) == 0:
           print(" No hay elementos para desapilar ")
           main()
        else:
           print("El numero: ",stack.pop()," fue desapilado") 
           main()

   #Esta opcion imprime en pantalla la pila 
   elif str(option)=="3":
         for i in reversed(range(len(stack))): 
             print("Pila: ",stack[i])
         main()

   #Esta opcion permite salir de la ejecucion del codigo 
   elif str(option)=="4":
        exit() 
   else:
    print("\nOpcion incorrecta.\n") 
    main()

main()


# Ejercicio 9
letters = []
#agregar listas 
letters.append('c') 
letters.append('a') 
letters.append('t') 
letters.append('g')

#Extraer 'g'
last_item = letters.pop() 
print(last_item)

#Extraer 't'
last_item = letters.pop() 
print(last_item)

#imprimir pila 
print(letters) #['c', 'a']


# Ejercicio Pila (nombre:Pila_imp.py
class Pila:
    """ Representa una pila con operaciones de apilar, desapilar y verificar si está vacía. """

def __init__ (self):
    """ Crea una pila vacía. """
#La pila vacía se representa con una lista vacía self.items=[]

def apilar(self, x):
    """ Agrega el elemento x a la pila. """ 
#Apilar es agregar al final de la lista. self.items.append(x)

def desapilar(self):
    """ Devuelve el elemento tope y lo elimina de la pila. Si la pila está vacía levanta una excepción. """
    try:
        return self.items.pop() 
    except IndexError:
        raise ValueError("La pila está vacía")

def es_vacia(self):
    """ Devuelve True si la lista está vacía, False si no. """ 
    return self.items == []

def mostrarelementos(self):
    print ("Los elementos de la pila son: ")
 
    print (self.items)
    
   
# Ejercicio Pila 1
from Pila_imp import Pila

p = Pila()
print (p.es_vacia()) 
p.apilar(1) 
p.es_vacia() 
p.apilar(5) 
p.apilar("+") 
p.apilar(22)
print(p.mostrarelementos()) 
print(p.desapilar()) 
print(p.mostrarelementos())


# Ejercicio Pila 2
from Pila_imp import Pila 
p=Pila()
print(p.es_vacia()) 
p.apilar(4) 
p.apilar('perro') 
print(p.inspeccionar()) 
p.apilar(True) 
print(p.tamano()) 
print(p.es_vacia()) 
p.apilar(8.4)
print(p.mostrarelementos()) 
print(p.desapilar()) 
print(p.desapilar()) 
print(p.tamano()) 
print(p.mostrarelementos())


# Ejercicio Pila 3
from Pila_imp import Pila

pila = Pila() # Creamos una instancia de la pila

#ingresamos algunos elementos a la pila pila.apilar('a')
pila.apilar('b')
pila.apilar('c')
print(pila.mostrarelementos()) # Mostramos los elementos de la pila 
pila.desapilar() # Utilizamos el metodo pop
print(pila.mostrarelementos()) # Mostramos nuevamente los elementos de la pila

_---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------_

# En total 68 problemas 
# Ana Cristina Cavazos Oyervidez







