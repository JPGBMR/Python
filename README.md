# Python_Intro

Introducción a Python...

```javascript
# Made by Pablo
#   Variable: Contenedor para un valor de diferentes tipo

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


