#Ejemplo de pila y arreglo
Este ejemplo demuestra dos estructuras de datos fundamentales y sus aplicaciones en la vida diaria:

- Pila (Stack): Se utiliza para implementar un historial de navegación web simplificado. Esto simula cómo los navegadores web manejan el historial de páginas visitadas, permitiendo al usuario retroceder a páginas anteriores28.

- Arreglo (Array): Se implementa usando NumPy para manejar un conjunto de calificaciones. Esto representa cómo se podrían almacenar y procesar datos numéricos, como calificaciones escolares
```
import numpy as np

# Implementación de una pila
class Pila:
    def __init__(self):
        self.items = []

    def esta_vacia(self):
        return len(self.items) == 0

    def apilar(self, item):
        self.items.append(item)

    def desapilar(self):
        if not self.esta_vacia():
            return self.items.pop()
        else:
            return None

    def ver_tope(self):
        if not self.esta_vacia():
            return self.items[-1]
        else:
            return None

# Ejemplo de uso: Historial de navegación web
historial = Pila()

# Simulación de navegación
paginas_visitadas = ["www.inicio.com", "www.noticias.com", "www.deportes.com", "www.tecnologia.com"]

print("Navegando...")
for pagina in paginas_visitadas:
    historial.apilar(pagina)
    print(f"Visitando: {pagina}")

print("\nRetrocediendo en el historial:")
for _ in range(3):
    pagina_anterior = historial.desapilar()
    if pagina_anterior:
        print(f"Volviendo a: {pagina_anterior}")

# Implementación de un arreglo usando NumPy
print("\nCreando un arreglo de calificaciones:")
calificaciones = np.array([85, 90, 78, 92, 88])
print("Calificaciones:", calificaciones)

# Calculando el promedio
promedio = np.mean(calificaciones)
print(f"Promedio de calificaciones: {promedio:.2f}")

# Encontrando la calificación más alta
maxima = np.max(calificaciones)
print(f"Calificación más alta: {maxima}")
```

