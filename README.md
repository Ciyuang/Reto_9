# RETO 9 🤓

## Ejercicio 1
- Desarrollar un algoritmo que calcule el promedio de un arreglo de reales.
```python
# lista de flotantes
reales = [2.0, 3.5, 6.7, 10.1]
suma = 0
# numero de elementos de la lista
numero_elementos = len(reales)
# blucle for encargado de sumar los elementos de la lista
for n in reales:
    suma = suma+n
# calculo del promedio e impresion del resultado
promedio = suma/numero_elementos
print(f" El promedio de {reales} es: {promedio}")
```

## Ejercicio 2
- Desarrollar un algoritmo que calcule el producto punto de dos arreglos de números enteros (reales) de igual tamaño.
```python
# listas con la misma cantidad de elemento
lista1 = [1, 2, 3, 4, 5]
lista2 = [6, 7, 8, 9, 10]
# lista vacio para agregar el resultado de la multiplicacion como una nueva lista
multi = []
# bucle for que que recorre y multiplica en parejas ambas listas al mismo tiempo, gracias a que tienen la misma cantidad de elementos
for i in range(len(lista1)):
    producto = lista1[i] * lista2[i]
    multi.append(producto)

print(f"Multiplicacion en parejas de los arrays: {multi}")
# suma e impresion del producto punto entre ambos arrays
suma = 0
for n in multi:
    suma = suma+n

print(f"El producto punto de ambos arrays es: {suma}")
```

## Ejercicio 3
- Hacer un algoritmo que deje al final de un arreglo de números todos los ceros que aparezcan en dicho arreglo.
```python
arreglo = [3, 0, 5, 1.1, 0, 0.0, 4, 7, 8.5]
arreglo.sort(reverse = True) 
print(arreglo)
```

## Ejercicio 4
- Revisar que son los algoritmos de sorting, entender bubble-sort.

    - ### bubble-sort
       es el algoritmo mas sencillo para ordenar listas de tamaño relativamente pequeño, pues este es muy ineficiente conforme mas grande sea la lista. Sin embargo comprender su estructura y logica es interesante para entender bien como ordenar una lista sin sorted() o .sort que son mas eficientes.

        **Implementación**
        ```python
        def bubble_sort(lista):
            n = len(lista)  # Obtener la longitud de la lista
            for i in range(n):  # Repetir el proceso n veces
                for j in range(0, n - i - 1):  # Recorrer desde el inicio hasta el final "útil"
                    if lista[j] > lista[j + 1]:  # Comparar elemento actual con el siguiente
                        # Si están en orden incorrecto, intercambiarlos
                        lista[j], lista[j + 1] = lista[j + 1], lista[j]
            return lista  # Devolver la lista ya ordenada

        # Lista de ejemplo
        numeros = [5, 3, 8, 4, 2]
        print("lisa original:", numeros)

        # Aplicar bubble_sort
        ordenada = bubble_sort(numeros)

        # Mostrar el resultado
        print("Lista ordenada:", ordenada)

        ```

    - ### Sorting
       Los modulos o funciones que funcionan con otro algoritmo distinto a bubble-sort son .sort y sorted(), estos utilizando otro mucho mas eficiente "Timsort" (Tim + sort, por Tim Peters, quien lo diseñó para Python) ademas de que ahorra el tener que crear una funcion especifica para una lista.
       
        **Implementación .sort y sroted()**
        ```python
        # Ordenar lista en el lugar (modifica la original)
        lista = [5, 2, 9, 1]
        lista.sort()

        # Ordenar sin modificar la original (devuelve una nueva lista)
        nueva_lista = sorted([5, 2, 9, 1])
        ```

# Autor 🤖
- [Juan Carlos Polania Bolivar](https://github.com/Ciyuang)
