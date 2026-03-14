import math

# --- 1. Área del Círculo (El que ya tenías) ---
def area_circulo(radio):
    return math.pi * (radio ** 2)

# --- 2. Función es_primo ---
def es_primo(n):
    if n < 2: return False
    for i in range(2, int(n**0.5) + 1):
        if n % i == 0: return False
    return True

# --- 3. Función factorial ---
def factorial(n):
    res = 1
    for i in range(1, n + 1): res *= i
    return res

# --- 4. Función fibonacci ---
def fibonacci(n):
    if n <= 0: return []
    seq = [0, 1] if n > 1 else [0]
    while len(seq) < n:
        seq.append(seq[-1] + seq[-2])
    return seq

# --- 5. Celsius a Fahrenheit ---
def celsius_a_fahrenheit(c):
    return (c * 9/5) + 32

# --- 6. Función máximo ---
def maximo(lista):
    if not lista: return None
    mayor = lista[0]
    for x in lista:
        if x > mayor: mayor = x
    return mayor

# ======================================================
# BLOQUE DE IMPRESIÓN (Lo que verás en la terminal)
# ======================================================
print("--- RESULTADOS DE MI TAREA ---")

# Ejercicio 1
print(f"1. El área de un círculo con radio 5 es: {area_circulo(5):.2f}")

# Ejercicio 2
print(f"2. ¿Es el número 7 primo?: {es_primo(7)}")

# Ejercicio 3
print(f"3. El factorial de 5 es: {factorial(5)}")

# Ejercicio 4
print(f"4. Los primeros 8 números de Fibonacci: {fibonacci(8)}")

# Ejercicio 5
print(f"5. 25°C a Fahrenheit: {celsius_a_fahrenheit(25)}°F")

# Ejercicio 6
lista_ejemplo = [10, 45, 2, 80, 33]
print(f"6. El número mayor en {lista_ejemplo} es: {maximo(lista_ejemplo)}")
