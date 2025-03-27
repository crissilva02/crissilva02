
### SEGUNDO CORTE
apuntes segundo corte

### SISTEMA DINAMICO
Muchos sistemas dinámicos, independientemente de que sean mecánicos, eléctricos, térmicos, hidráulicos, neumáticos, químicos, económicos, biológicos, etc. se pueden caracterizar por ecuaciones diferenciales las cuales se obtienen con base en leyes físicas, como por ejemplo las leyes de Kirchhoff, las leyes de Newton, etc.

#### Derivadas de transformadas de Laplace:
![Ecuación](https://latex.codecogs.com/svg.latex?\color{white}f'(t)%20=%20sf(s)%20-%20f(0))  
![Ecuación](https://latex.codecogs.com/svg.latex?\color{white}f''(t)%20=%20s^2f(s)%20-%20f(0)%20-%20f'(0))  
![Ecuación](https://latex.codecogs.com/svg.latex?\color{white}f'''(t)%20=%20s^3f(s)%20-%20s^2f(0)%20-%20sf'(0)%20-%20f''(0))

#### Ecuación diferencial:
![Ecuación](https://latex.codecogs.com/svg.latex?\color{white}x''%20+%202x'%20+%205x%20=%203)  
![Ecuación](https://latex.codecogs.com/svg.latex?\color{white}x(0)%20=%200;%20x'(0)%20=%200)  

#### Transformada de Laplace aplicada:
![Ecuación](https://latex.codecogs.com/svg.latex?\color{white}(s^2x(s))%20+%202(5x(s))%20+%205x(s)%20=%203)  
![Ecuación](https://latex.codecogs.com/svg.latex?\color{white}xs(s^2%20+%202s%20+%205)%20=%203)  
![Ecuación](https://latex.codecogs.com/svg.latex?\color{white}xs%20=%20\frac{3}{s(s^2%20+%202s%20+%205)})

#### Ley de Hooke y amortiguadores:
![Ecuación](https://latex.codecogs.com/svg.latex?\color{white}f%20=%20kx%20=%20k(x_1%20-%20x_2))  
![Ecuación](https://latex.codecogs.com/svg.latex?\color{white}ff%20=%20k_1%20\cdot%20y')  
![Ecuación](https://latex.codecogs.com/svg.latex?\color{white}f%20=%20bx'%20=%20b(x_1'%20-%20x_2'))  
![Ecuación](https://latex.codecogs.com/svg.latex?\color{white}f_r%20=%20k_2%20\cdot%20x)  
![Ecuación](https://latex.codecogs.com/svg.latex?\color{white}ff%20=%20k_2%20\cdot%20v_m)  
![Ecuación](https://latex.codecogs.com/svg.latex?\color{white}f%20=%20m%20\cdot%20a)

#### Fuerzas resultantes y movimiento:
![Ecuación](https://latex.codecogs.com/svg.latex?\color{white}u%20-%20f_r%20-%20ff%20=%20m%20\cdot%20a)  
![Ecuación](https://latex.codecogs.com/svg.latex?\color{white}f_r%20=%20k_2%20\cdot%20y(t))  
![Ecuación](https://latex.codecogs.com/svg.latex?\color{white}ff%20=%20k_1%20\cdot%20y'(t))  
![Ecuación](https://latex.codecogs.com/svg.latex?\color{white}a%20=%20y''(t))  
![Ecuación](https://latex.codecogs.com/svg.latex?\color{white}u(t)%20-%20(k_2%20\cdot%20y(t))%20-%20(k_1%20\cdot%20y'(t))%20+%20fg%20=%20m%20\cdot%20a)  
![Ecuación](https://latex.codecogs.com/svg.latex?\color{white}u(t)%20+%20(m%20\cdot%20g)%20-%20(k_2%20\cdot%20y(t))%20-%20(k_1%20\cdot%20y'(t))%20=%20m%20\cdot%20a)  
![Ecuación](https://latex.codecogs.com/svg.latex?\color{white}u(t)%20+%20(m%20\cdot%20g)%20-%20(k_2%20\cdot%20y(t))%20-%20(k_1%20\cdot%20y'(t))%20=%20m%20\cdot%20y''(t))


# Solución de la Ecuación Diferencial

Este documento explica paso a paso la solución del sistema de ecuaciones diferenciales en el dominio de Laplace.

## **Paso 1: Escribir las ecuaciones en el dominio de Laplace**

Las ecuaciones dadas son:

![Ecuación 1](https://latex.codecogs.com/png.latex?0.1X_1(s)-0.3X_2(s)%2B98-0.1sX(s)=10s^2X(s))

![Ecuación 2](https://latex.codecogs.com/png.latex?549-0.3X_1(s)%2B0.3X_2(s)=5s^2X(s))

Nuestro objetivo es despejar ![X_1(s)](https://latex.codecogs.com/png.latex?X_1(s)) y ![X_2(s)](https://latex.codecogs.com/png.latex?X_2(s)).

---

## **Paso 2: Resolver el sistema**

### **Despejamos** ![X_1(s)](https://latex.codecogs.com/png.latex?X_1(s)) **de la primera ecuación**

![Paso 1](https://latex.codecogs.com/png.latex?0.1X_1(s)-0.3X_2(s)=10s^2X(s)%2B0.1sX(s)-98)

Despejamos ![X_1(s)](https://latex.codecogs.com/png.latex?X_1(s)):

![Paso 2](https://latex.codecogs.com/png.latex?X_1(s)=\frac{10s^2X(s)%2B0.1sX(s)-98%2B0.3X_2(s)}{0.1})

![Paso 3](https://latex.codecogs.com/png.latex?X_1(s)=100s^2X(s)%2BsX(s)-980%2B3X_2(s))

---

### **Sustituyéndolo en la segunda ecuación**

Sustituyamos ![X_1(s)](https://latex.codecogs.com/png.latex?X_1(s)) en la segunda ecuación:

![Paso 4](https://latex.codecogs.com/png.latex?549-0.3(100s^2X(s)%2BsX(s)-980%2B3X_2(s))%2B0.3X_2(s)=5s^2X(s))

Distribuyendo ![-0.3](https://latex.codecogs.com/png.latex?-0.3):

![Paso 5](https://latex.codecogs.com/png.latex?549-30s^2X(s)-0.3sX(s)%2B294-0.9X_2(s)%2B0.3X_2(s)=5s^2X(s))

Simplificamos:

![Paso 6](https://latex.codecogs.com/png.latex?843-30s^2X(s)-0.3sX(s)-0.6X_2(s)=5s^2X(s))

Despejamos ![X_2(s)](https://latex.codecogs.com/png.latex?X_2(s)):

![Paso 7](https://latex.codecogs.com/png.latex?-0.6X_2(s)=-5s^2X(s)%2B30s^2X(s)%2B0.3sX(s)-843)

---

### **Conclusión**
El sistema se ha transformado en una ecuación en términos de ![X(s)](https://latex.codecogs.com/png.latex?X(s)), y se puede resolver para obtener la respuesta final en el dominio de Laplace.
