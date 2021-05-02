# Python_Intro <img src="https://media.giphy.com/media/dxn6fRlTIShoeBr69N/giphy.gif" width="45">

Introducción a Python...

```javascript
# Made_by_Pablo
#   Variable : Contenedor para un valor de diferentes tipo

'''
Asi haces comentarios
En varias lineas
Pueden ser comillas singles o dobles
'''

"""
Reglas de variables en python:
  - Puede tener un numero pero no comenzar por uno. Tiene empezar con una letra o an underscore (_).
  - Cada abstracción del tipo de variable las condiciona a como usarlas.
  - Case Sensitive.
"""

# x = 10            # int
# y = 5             # float
# nombre = 'Juan'   # str
# is_cool = True    # bool

# Multiple assignment
x, y, name, is_cool = (1, 2.5, 'John', True)

# Casting
x = str(x)
y = int(y)
z = float(y)

print(type(z), z)

# Matematica
a = x + y
```

Strings...

```javascript
# Strings en python

nombre = 'Pablo'
edad = 25
altura = 1.69

# Concatenar
print('Hola, mi nombre es ' + nombre + ' y tengo ' + str(edad) +' años de edad  y mido ' + str(altura) + 'cm')

# String Format
# Argumentos por posición
print('Mi nombre es {nombre} y tengo {edad} mido {altura} cm'.format(nombre=nombre, edad=edad, altura=altura))
print(f'Hola, mi nombre es {nombre} tengo {edad} y mido {altura}')# F-Strings (3.6+)
s = 'holamundo.'                    # String Methods
print(s.capitalize())               # Capitalize string
print(s.upper())                    # Make all uppercase
print(s.lower())                    # Make all lower
print(s.swapcase())                 # Swap case
print(len(s))                       # Get length
print(s.replace('.', 'Hola Todos!'))# Replace
print(s.startswith('hola'))         # Starts with
print(s.endswith('.'))              # Ends with
print(s.split())                    # Split into a list
print(s.find('h'))                  # Find position
print(s.isalnum())                  # Is all alphanumeric
print(s.isalpha())                  # Is all alphabetic
print(s.isnumeric())                # Is all numeric
```

Listas...

```javascript
# Lista es una colección ordenada y mutable. Permite duplicados
# Crea lista al instanciarla ó usando un constructor
#   numeros = [1, 2, 3, 4, 5] es igual a -> num = lista((1, 2, 3, 4, 5)) 

cosasquehacer = ['Automatizar', 'Consultar', 'Big Datear', 'Digitalización', 'Empoderar']

print(cosasquehacer[1])   # Obtener un valor
print(cosasquehacer[-1])  # Obtener último valor
print(len(cosasquehacer)) # Obtener tamaño
cosasquehacer.append('Big Datear') # Append a lista
cosasquehacer.remove('Big Datear') # Remove from lista
cosasquehacer.insert(2, 'Hacerlo mejor de nuevo') # Insert into position
cosasquehacer[0] = 'Aplicar  A.I' # Change valor
cosasquehacer.pop(2) # Remover con pop
cosasquehacer.reverse() # Reverse lista
cosasquehacer.sort() # Sort lista
cosasquehacer.sort(reverse=True) # Reverse sort
print(cosasquehacer)

```

Tuples & Sets...

```javascript
# Tuple: colección ordenada inmutable. Permite duplicados
# Crea tuple al instanciarlo ó usando un constructor => mascotas = tuple(('Buho', 'Cascabel', 'Gato')) es igual a ->  mascotas = tuple(('Buho', 'Cascabel', 'Gato'))

mascotas = tuple(('Buho', 'Cascabel', 'Gato'))

print(mascotas[1])      # Obtener valor
mascotas[0] = 'Pears'   # No se puede cambiar un valor
del mascotas            # Borrar ó Delete tuple
print(len(mascotas))    # Get length

# Set: colección desordenada inmutable. NO Permite duplicadosis
# Crear set
mascotas_set = {'Buho', 'Cascabel', 'Gato'}

print('Buho' in mascotas_set)   # Check if in set
mascotas_set.add('Gata')        # Add to set
mascotas_set.remove('Gato')     # Remove from set
mascotas_set.add('Perros')      # Add duplicate
mascotas_set.clear()            # Clear set
del mascotas_set                # Delete
print(mascotas_set)

```

Diccionarios...

```javascript
# Un diccionario es una colección desordenada y mutable. NO Permite duplicadosis. Más info en https://docs.python.org/3/tutorial/datastructures.html#dictionaries
# Crear dict usando constructor contacto2 = dict(primer_nombre='Juan', segundo_nombre='Garcia','telefono': 6226961,'edad': 52, 'altura': 1,79)

contacto2 = dict(primer_nombre='Juan', segundo_nombre='Garcia', telefono= 6226961, edad= 52, altura= 1.79)

contacto = {
    'primer_nombre': 'Pablo',
    'segundo_nombre': 'Doe',
    'telefono': 6226969,
    'edad': 25,
    'altura': 1.69
}

print(contacto['primer_nombre'])      # Get value
print(contacto.get('segundo_nombre'))# Get value
contacto['region'] = 'AMER'          # Add key/value
print(contacto.keys())               # Get dict keys
print(contacto.items())              # Get dict items
contacto2 = contacto.copy()          # Copy dict
contacto2['city'] = 'Boston'
del(contacto['edad'])                # Remove item
contacto.pop('telefono')
contacto.clear()                     # Clear
print(len(contacto2))                # Get length
contactos = [
    {'nombre': 'Maria', 'edad': 30},
    {'nombre': 'Karen', 'edad': 25}
] # List of dict
print(contactos[1]['nombre'])
```

Loops (Bucles)...

```javascript




# Un loop es usado para iterar sobre una coleccion o sequencia de elemtos (list, a tuple, a dictionary, a set, or a string)
personas = ['Andres', 'Betty', 'Carlos', 'David']

# For loop simple 
for person in personas:
  print(f'Persona Actual: {person}')

for person in personas: # Break
  if person == 'Carlos':
    break
  print(f'Persona iterando actualmente: {person}')

for person in personas: # Continuar
  if person == 'Sara':
    continue
  print(f'Persona iterando actualmente: {person}')

for i in range(len(personas)): # range
  print(personas[i])

for i in range(0, 11):
  print(f'Number: {i}')

# While loops se ejecutan indefinitamente mientras una condicion sea verdadera
count = 0
while count < 10:
  print(f'Count: {count}')
  count += 1

```

Condicionales (Bucles)...

```javascript
# If/ Else son usados para condicionar el comportamiento, dependiendo de una variable en verdadora o falsa, true or false.

x = 101
y = 100

# Operador de comparasión (==, !=, >, <, >=, <=) - Usada para comparar valores

# Simple if
if x > y:
  print(f'{x} is greater than {y}')

# If/else
if x > y:
  print(f'{x} is greater than {y}')
else:
  print(f'{y} is greater than {x}')  

# elif
if x > y:
  print(f'{x} is greater than {y}')
elif x == y:
  print(f'{x} is equal to {y}')  
else:
  print(f'{y} is greater than {x}')  

# Nested if
if x > 2:
  if x <= 10:
    print(f'{x} is greater than 2 and less than or equal to 10')

# Logical operators (and, or, not) - Used to combine conditional statements

if x > 2 and x <= 10: # and
    print(f'{x} is greater than 2 and less than or equal to 10')

if x > 2 or x <= 10: # or
    print(f'{x} is greater than 2 or less than or equal to 10')

if not(x == y): # not
  print(f'{x} is not equal to {y}')

# Membership Operators (not, not in) - Membership operators are used to test if a sequence is presented in an object

numbers = [1,2,3,4,5]

if x in numbers: #  in
  print(x in numbers)

if x not in numbers: # not in
  print(x not in numbers)

# Identity Operators (is, is not) - Compare the objects, not if they are equal, but if they are actually the same object, with the same memory location:
if x is y: # is
  print(x is y)
  
if x is not y: # is not
  print(x is not y)
```

Funciones...

```javascript
# A bloque de codigo que se ejecuta cuando se invoca
# Crear función
def sayHello(name='Sam'):
    print(f'Hello {name}')
# Return values
def getSum(num1, num2):
    total = num1 + num2
    return total
# A lambda función is a small anonymous función.
# A lambda función can take any number of arguments, but can only have one expression. Very similar to JS arrow función
getSum = lambda num1, num2: num1 + num2
print(getSum(10, 3))
```

Clases...

```javascript
# Una clase es una plantilla para crear objetos. Objetos tienen propiedades & metodos asociados.

# Crear clase
class User:

  # Constructor
  def __init__(self, name, email, age):
    self.name = name
    self.email = email
    self.age = age
    
    # Adding Encapsulation of variables... Encapsulation is the concept of making the variables non-accessible or accessible upto some extent from the child classes
    self._private = 1000 # Encapsulated variables are declares with '_' in the constructor.

  def greeting(self):
      return f'My name is {self.name} and I am {self.age}'

  def has_birthday(self):
      self.age += 1
 
 #function para encap variable
  def print_encap(self):
      print(self._private)

# Extender class
class Customer(User):
  # Constructor
  def __init__(self, name, email, age):
      User.__init__(self, name, email, age) #Called proper parent class constructor to make this as proper child inehriting all methods.
      self.name = name
      self.email = email
      self.age = age
      self.balance = 0

  def set_balance(self, balance):
      self.balance = balance

  def greeting(self): # Creacion de un método
      return f'Mi nombre es{self.name} and I am {self.age} and my balance is {self.balance}'

#  Init user object
pablo = User('Pablo Barriuso', 'pabl0barrius00@gmail.com', 37)
# Init customer object
maria = Customer('maria garcia', 'maria@yahoo.com', 25)

maria.set_balance(500)
print(maria.greeting())

pablo.has_birthday()
print(pablo.greeting())

#Encapsulation -->
pablo.print_encap()
pablo._private = 800 #Changing for pablo
pablo.print_encap()

# Method inherited from parent
maria.print_encap() #Changing the variable for pablo doesn't affect marias variable --> Encapsulation
maria._private = 600
maria.print_encap()

#Similary changing maria's doesn't affect pablo's variable.
pablo.print_encap()

```

Modulos...

```javascript
# Modulo : Es un archivo que contiene un set de funciones a incluir en tu app. Hay core python modules, modules instalables usando pip package manager y tambien custom modules

# Core modules
import datetime
from datetime import date
import time
from time import time


# Import custom module
import validator_9_1
from validator_9_1 import validate_email
# Ejemplo de modulo por importar: crear otro archivo de python para exportarlo a este:

import re
def validate_email(email):
    if len(email) > 7:
        return bool(re.match("^.+@(\[?)[a-zA-Z0-9-.]+.([a-zA-Z]{2,3}|[0-9]{1,3})(]?)$", email))



today = date.today() # today = datetime.date.today()
timestamp = time()

email = 'test#test.com'
if validate_email(email):
  print('Email valido')
else:
  print('Email invalido')

```



