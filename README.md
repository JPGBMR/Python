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


