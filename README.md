
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


#### Ejercicio de ejemplo sistema mecanico   
![Ecuación](https://latex.codecogs.com/svg.latex?\color{white}m_1\ddot{x}_1=(k_2(x_1-x_2))+(m_1g)-(k_1(x_1))+(b\dot{x_1}))   
![Ecuación](https://latex.codecogs.com/svg.latex?\color{white}m_2\ddot{x}_2=u(t)+(m_2g)-(k_2(x_2-x_1)))  
![Ecuación](https://latex.codecogs.com/svg.latex?\color{white}0.1X_1(s)-0.3X_2(s)+98-0.1sX(s)=10s^2X(s))  
![Ecuación](https://latex.codecogs.com/svg.latex?\color{white}549-0.3X_1(s)+0.3X_2(s)=5s^2X(s))

#### **Despejamos** \(X_1(s)\) y luego Sustituir \(X_2(s)\) en \(X_1(s)\): 
![Ecuación](https://latex.codecogs.com/svg.latex?\color{white}X_1(s)=\frac{10s^2X(s)+0.1sX(s)-98+0.3X_2(s)}{0.1})  
![Ecuación](https://latex.codecogs.com/svg.latex?\color{white}X_1(s)=100s^2X(s)+sX(s)-980+3X_2(s))
![Ecuación](https://latex.codecogs.com/svg.latex?\color{white}X_1(s)=100s^2X(s)+sX(s)-980+3\left(\frac{-25s^2X(s)}{3}-\frac{sX(s)}{2}+1405\right))  
![Ecuación](https://latex.codecogs.com/svg.latex?\color{white}X_1(s)=-75s^2X(s)-0.5sX(s)+3235)

#### Resultados finales
![Ecuación](https://latex.codecogs.com/svg.latex?\color{white}X_2(s)=-\frac{25s^2X(s)}{3}-\frac{sX(s)}{2}+1405)

```matlab
function sistema_dos_masas
    % Parámetros dados
    m1 = 10;         % masa 1 (kg)
    m2 = 5;          % masa 2 (kg)
    k1 = 0.2;        % constante de resorte 1 (N/m)
    k2 = 0.3;        % constante de resorte 2 (N/m)
    b = 0.1;         % coeficiente de amortiguamiento (N·s/m)
    g = 9.81;        % gravedad (m/s^2)

    % Tiempo de simulación
    tspan = [0 20];  % segundos

    % Condiciones iniciales: [x1 x1_dot x2 x2_dot]
    x0 = [0.1 0 0.2 0];  % puedes ajustar esto si lo deseas

    % Resolver con ode45
    [t, X] = ode45(@(t, x) modelo(t, x, m1, m2, k1, k2, b, g), tspan, x0);

    % Graficar resultados
    figure;
    plot(t, X(:,1), 'r', t, X(:,3), 'b', 'LineWidth', 1.5);
    legend('x1(t)', 'x2(t)');
    xlabel('Tiempo (s)');
    ylabel('Posición (m)');
    title('Sistema masa-resorte-amortiguador');
    grid on;
end

function dxdt = modelo(t, x, m1, m2, k1, k2, b, g)
    % Variables de estado
    x1 = x(1);
    x1_dot = x(2);
    x2 = x(3);
    x2_dot = x(4);

    % Fuerza externa sobre m2
    u = sin(t);  % Puedes reemplazar esto por otra función

    % Ecuaciones diferenciales
    x1_ddot = (k2*(x1 - x2) + m1*g - k1*x1 + b*x1_dot) / m1;
    x2_ddot = (u + m2*g - k2*(x2 - x1)) / m2;

    dxdt = [x1_dot; x1_ddot; x2_dot; x2_ddot];
end

```

