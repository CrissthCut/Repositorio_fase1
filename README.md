# Repositorio_fase1
Tercer semestre evidencia 1
# Aplicar  las  estructuras  nativas  del  lenguaje  Python  tales  como  Listas,Tuplas,  Conjuntos  y  Diccionarios para almacenar en memoria principal el estado de una aplicación a desarrollar y emplearlas para codificar pilas y colas que permitan el proceso delosconjuntos de datos.

# Ejercicio Math
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


# Ejercicio Random
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


# Ejercicio Time
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


# Ejercicio Datetime
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


# Ejercicio SYSOS
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
     
 
 
# Ejercicios semana 2

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



