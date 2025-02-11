# Reto_9
Elaborado por: Maria Fernanda Parra Osorio-1014980661 <br>
1.Desarrollar un algoritmo que calcule el promedio de un arreglo de reales. <br>
2.Desarrollar un algoritmo que calcule el producto punto de dos arreglos de números enteros (reales) de igual tamaño. <br>
3.Hacer un algoritmo que deje al final de un arreglo de números todos los ceros que aparezcan en dicho arreglo. <br>
4.Revisar que son los algoritmos de sorting, entender bubble-sort (enlace a implementación). <br>

---

### **¿Qué son los algoritmos de sorting (ordenamiento)?**
Los algoritmos de sorting son técnicas utilizadas para organizar los elementos de una lista en un orden específico, ya sea **ascendente** o **descendente**.  

## **Tipos de algoritmos de ordenamiento**
Los algoritmos de sorting se pueden clasificar en dos grandes grupos:

1- **Algoritmos de ordenamiento por comparación**  
Estos algoritmos comparan pares de elementos y los intercambian si es necesario.  
Ejemplos:  
- Bubble Sort → Simple, pero ineficiente (\(O(n^2)\))  
- Selection Sort → Selecciona el menor en cada iteración (\(O(n^2)\))  
- Insertion Sort → Inserta cada elemento en su posición correcta (\(O(n^2)\), pero bueno para listas pequeñas o casi ordenadas)  
- Merge Sort → Divide y conquista, más eficiente (\(O(n \log n)\))  
- Quick Sort → Usa un pivote para dividir la lista (\(O(n \log n)\) en promedio)  
- Heap Sort → Basado en estructuras de montículos (\(O(n \log n)\))  

2- **Algoritmos de ordenamiento no comparativos**  
No usan comparaciones entre elementos, sino que aprovechan otras estructuras como conteos o distribuciones.  
Ejemplos:  
- Counting Sort → Útil para valores enteros pequeños (\(O(n+k)\))  
- Radix Sort → Ordena por dígitos de menor a mayor (\(O(nk)\))  
- Bucket Sort → Divide los datos en grupos (\(O(n)\) en el mejor caso)  

---

## **¿Cuándo usar cada algoritmo?**
- Para listas pequeñas: `Bubble Sort`, `Insertion Sort`, `Selection Sort`  
- Para listas grandes: `Merge Sort`, `Quick Sort`, `Heap Sort`  
- Si los datos tienen un rango pequeño de valores enteros: `Counting Sort`, `Radix Sort`  
- Si necesitas mantener el orden de elementos iguales: `Merge Sort`, `Counting Sort`, `Radix Sort`  

---

## 🔹 **Bubble Sort (Ordenamiento de Burbuja)**
### 📌 **Concepto:**
Bubble Sort es un algoritmo de ordenamiento **simple pero ineficiente**, que compara pares de elementos adyacentes y los intercambia si están en el orden incorrecto. Este proceso se repite hasta que la lista esté completamente ordenada.

---

### 📌 **Funcionamiento:**
1. **Recorre la lista varias veces.**
2. **Compara cada par de elementos adyacentes.**
3. **Si están en el orden incorrecto, los intercambia.**
4. **Después de cada pasada, el número más grande "burbujea" hacia el final.**
5. **El proceso se repite hasta que no se realicen más intercambios.**

---

### 📌 **Ejemplo paso a paso:**
Supongamos que tenemos la lista:
```
[5, 3, 8, 4, 2]
```
🔹 **Primera pasada:** (los números se intercambian si están en el orden incorrecto)  
```
[3, 5, 4, 2, 8]  # El 8 "burbujea" al final
```
🔹 **Segunda pasada:**
```
[3, 4, 2, 5, 8]  
```
🔹 **Tercera pasada:**
```
[3, 2, 4, 5, 8]  
```
🔹 **Cuarta pasada:**  
```
[2, 3, 4, 5, 8]  # Lista ordenada
```

---

### 📌 **Código en Python:**
```python
def bubble_sort(arr):
    n = len(arr)
    for i in range(n - 1):
        for j in range(n - 1 - i):  # Últimos i elementos ya están ordenados
            if arr[j] > arr[j + 1]:  # Intercambiar si están en orden incorrecto
                arr[j], arr[j + 1] = arr[j + 1], arr[j]
    return arr

# Ejemplo de uso
lista = [5, 3, 8, 4, 2]
print("Lista ordenada:", bubble_sort(lista))
```

---

### 📌 **Complejidad Temporal:**
| Caso | Complejidad |
|------|------------|
| **Peor caso (lista invertida)** | \(O(n^2)\) |
| **Mejor caso (lista ya ordenada)** | \(O(n)\) |
| **Caso promedio** | \(O(n^2)\) |

🔹 **Nota:** Bubble Sort no es eficiente para listas grandes, ya que tiene una complejidad cuadrática \(O(n^2)\).  

---

### 📌 **¿Cuándo usar Bubble Sort?**
✅ Cuando la lista es **pequeña**.  
✅ Para **aprender algoritmos de ordenamiento**.  
✅ Cuando el código debe ser **fácil de entender**, aunque no sea el más eficiente.  

❌ **No es recomendable** para listas grandes debido a su **baja eficiencia**.  

---

### **Conclusión**  
Los algoritmos de sorting son fundamentales en la programación y cada uno tiene ventajas y desventajas según el caso de uso. Para listas grandes, los algoritmos eficientes como **Merge Sort** o **Quick Sort** son preferibles, mientras que para listas pequeñas o casi ordenadas, **Insertion Sort** puede ser más rápido.  

---

## **Referencias**
1- Algoritmos de ordenación explicados con ejemplos en JavaScript, Python, Java y C++. (2023, mayo 1). freeCodeCamp.org. https://www.freecodecamp.org/espanol/news/algoritmos-de-ordenacion-explicados-con-ejemplos-en-javascript-python-java-y-c/ <br>
2- Bubble sort algorithm. (2014, febrero 2). GeeksforGeeks. https://www.geeksforgeeks.org/bubble-sort-algorithm/ <br>

