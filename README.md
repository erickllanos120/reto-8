# reto-8
punto 1
# Área de un círculo
Fórmula:

𝐴=𝜋𝑟2

Función en lambda:

    import math
    area_circulo = lambda r: math.pi * r**2
    print("Área del círculo con radio 5:", area_circulo(5))




# Área de un triángulo
Fórmula:

  Área = (base * altura) / 2

    area_triangulo = lambda b, h: (b * h) / 2
    print("Área del triángulo (base 10, altura 6):", area_triangulo(10, 6))


# valor compuesto

C: capital inicial

i: interés mensual (en decimal)

n: número de meses

    interes_compuesto = lambda C, i, n: C * (1 + i) ** n
    print("Valor del préstamo: ", interes_compuesto(100000, 0.015, 12))



# punto 2
De los retos anteriores selecione 3 funciones y escribalas con argumentos no definidos (*args).

#area del circulo
    
    import math
    
    def area_circulo_args(*args):
        r = args[0]
        return math.pi * r**2
    print("Área del círculo con radio 5:", area_circulo_args(5))


#area del triangulo
  
    def area_triangulo_args(*args):
        b = args[0]
        h = args[1]
        return (b * h) / 2
    print("Área del triángulo (base 10, altura 6):", area_triangulo_args(10, 6))


#valor interes compuesto

    def interes_compuesto_args(*args):
        C = args[0]
        i = args[1]
        n = args[2]
        return C * (1 + i) ** n
    print("Valor del préstamo (C=100000, i=0.015, n=12):", interes_compuesto_args(100000, 0.015, 12))

# punto 3
Escriba una función recursiva para calcular la operación de la potencia.


    def potencia(base, exponente):
        if exponente == 0:
            return 1
        return base * potencia(base, exponente - 1)
    
    print("2 elevado a la 5 es:", potencia(2, 5))  # Resultado esperado: 32

# punto 4
Utilice la siguiente plantilla de code para contar el tiempo:
  
    import time

    start_time = time.time()
    # instrucciones sobre las cuales se quiere medir tiempo de ejecución
    end_time = time.time()
    
    timer = end_time - start_time
    print(timer)

codigo 
    
    import time
    
    def potencia(base, exponente):
        if exponente == 0:
            return 1
        return base * potencia(base, exponente - 1)
    
    # Medir tiempo usando la plantilla
    start_time = time.time()
    
    resultado = potencia(2, 20)
    
    end_time = time.time()
    timer = end_time - start_time
    
    print("Resultado:", resultado)
    print("Tiempo de ejecución:", timer)

# punto 5

    import time
    
    def fibonacci_recursivo(num):
        if num <= 1:
            return num
        else:
            return fibonacci_recursivo(num - 1) + fibonacci_recursivo(num - 2)
    
    def fibonacci_iterativo(num):
        a, b = 0, 1
        for _ in range(num):
            a, b = b, a + b
        return a
    
    print("n\tTiempo Recursivo (s)\tTiempo Iterativo (s)")
    
    for n in range(10, 41, 5):  # de 10 a 40 con saltos de 5
        # Tiempo del método recursivo
        start_time = time.time()
        fibonacci_recursivo(n)
        end_time = time.time()
        tiempo_rec = end_time - start_time
    
        # Tiempo del método iterativo
        start_time = time.time()
        fibonacci_iterativo(n)
        end_time = time.time()
        tiempo_iter = end_time - start_time
    
        print(f"{n}\t{tiempo_rec:.5f}\t\t\t{tiempo_iter:.5f}")

        
# conclusion
La comparación entre las implementaciones recursiva e iterativa de la función de Fibonacci muestra una diferencia significativa en eficiencia a medida que aumenta el valor de n.

Para valores pequeños (por ejemplo, n = 10 o n = 15), ambas versiones tienen tiempos de ejecución muy bajos y casi imperceptibles.

A partir de n ≈ 30, el tiempo de ejecución de la versión recursiva comienza a crecer exponencialmente debido a la gran cantidad de llamadas repetidas que realiza, lo que la vuelve ineficiente para valores grandes.

En contraste, la versión iterativa mantiene un tiempo de ejecución constante y muy bajo incluso para n = 40 o mayores, ya que su complejidad es lineal 𝑂(𝑛), mientras que la versión recursiva tiene complejidad exponencial 𝑂(2𝑛).

 # punto 6
 ![image](https://github.com/user-attachments/assets/208130ad-d7b7-49b9-b4e0-f41669df25ad)


 # punto 7
 www.linkedin.com/in/erick-llanos-espinel-091845372
