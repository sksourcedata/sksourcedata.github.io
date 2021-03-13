---
layout: page
title: Prácticas con Python
menu: fractal-geometry
comments: true
mathjax: true
---

## Introducción

Problema 1: Cambio de base
: Define una función que tenga como entrada un número real entre 0 y 1 y devuelva una lista (o un array de `numpy` o similar) con las primeras 20 coordenadas de la representación del número en la base indicada.
{: .prob}

~~~python
def convert(x, base, length = 20):
    """Devuelve un número decimal entre 0 y 1 en la base especificada."""
    output=[]
    remainder=x
    a=0
    for i in range(length):
        b = int(remainder * base)
        output.append(b)
        a = b
        remainder = remainder * base - a
    return output
~~~

## Dimmensión box-counting

Los objetivos básicos a perseguir en esta práctica son los siguientes:
- Calcular la dimensión box-counting de un conjunto de puntos.
- Calcular la dimensión box-counting de una imagen.

Para abrir un archivo se usa el comando `open` y para cerrarlo (lo cual es aconsejable una vez que hayamos finalizado las operaciones necesarias con él) `close`.

Pongamos en práctica estos comandos utilizando [este archivo](sierpinski.txt), llamado `sierpinski.txt`. Observemos que este archivo texto contiene una gran lista de puntos en el plano.

Vamos a almacenar todas las líneas que contiene dicho archivo en una variable como lista. Para ello, usaremos el siguiente código:
~~~python
f = open('sierpinski.txt')
lines = f.readlines()
f.close()
~~~

Ya que tenemos los datos de este archivo, sigamos trabajando con él. Si usamos el comando `lines[:5]`, nos mostrará las primeras cinco líneas.

Pongamos como objetivo extraer los puntos de cada línea. Comencemos con la primera línea. Si escribimos

