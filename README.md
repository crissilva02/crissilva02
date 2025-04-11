
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

-----
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

------
#### 💡 Ejercicio de ejemplo sistema mecanico   
![WhatsApp Image 2025-04-07 at 3 56 09 AM](https://github.com/user-attachments/assets/b2114af7-f808-443e-b819-8b28515ada19)   
   
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
    x0 = [0.1 0 0.2 0];  

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
    % Variables 
    x1 = x(1);
    x1_dot = x(2);
    x2 = x(3);
    x2_dot = x(4);

    % Fuerza externa sobre m2
    u = sin(t);  

    % Ecuaciones diferenciales
    x1_ddot = (k2*(x1 - x2) + m1*g - k1*x1 + b*x1_dot) / m1;
    x2_ddot = (u + m2*g - k2*(x2 - x1)) / m2;

    dxdt = [x1_dot; x1_ddot; x2_dot; x2_ddot];
end

```
![image](https://github.com/user-attachments/assets/df63d732-7419-4264-9065-ffd27b87272d)    

------

### ⚡ SIETEMAS DINAMICOS ELECTRICOS

![Eq1](https://latex.codecogs.com/svg.latex?\color{white}-U%20+%20V_c'%20+%20V_c%20+%20V_c%20=%200)   
![Eq2](https://latex.codecogs.com/svg.latex?\color{white}-U%20+%20\left(\frac{R_2}{R_1}\right)%20+%20V_c%20=%200)    
![Eq3](https://latex.codecogs.com/svg.latex?\color{white}V_c%20=%20-\left(-U%20+%20\frac{R_2}{R_1}\right))   
![Eq4](https://latex.codecogs.com/svg.latex?\color{white}-\frac{V_c}{R_2}%20=%20\frac{U}{R_1}%20-%20Y\left(\frac{1}{R_1}%20+%20\frac{1}{R_2}\right))   
![Eq5](https://latex.codecogs.com/svg.latex?\color{white}-\frac{V_c}{R_2}%20=%20\frac{UR_2%20-%20Y(R_1%20+%20R_2)}{R_1R_2})   
![Eq6](https://latex.codecogs.com/svg.latex?\color{white}V_c%20=%20Y\left(\frac{R_1%20+%20R_2}{R_1}\right)%20-%20U\frac{R_2}{R_1})   
![Eq7](https://latex.codecogs.com/svg.latex?\color{white}V_c'%20=%20Y'\left(\frac{R_1%20+%20R_2}{R_1}\right)%20-%20U'\frac{R_2}{R_1})   

   
### ⚡
 
![Eq1](https://latex.codecogs.com/svg.latex?\color{white}I_1%20-%20I_2%20-%20I_3%20=%200)   
![Eq2](https://latex.codecogs.com/svg.latex?\color{white}e_i%20-%20V_x%20-%20C_1\frac{dV_x}{dt}%20-%20C_2\frac{dV_{e0}}{dt}%20=%200)    
![Eq3](https://latex.codecogs.com/svg.latex?\color{white}V_x%20=%20V_{R_2}%20+%20V_{e0})   
![Eq4](https://latex.codecogs.com/svg.latex?\color{white}V_x%20=%20I_3R_2%20+%20V_{e0})   
![Eq5](https://latex.codecogs.com/svg.latex?\color{white}V_x%20=%20C_2R_2\frac{dV_{e0}}{dt}%20+%20V_{e0})   
![Eq6](https://latex.codecogs.com/svg.latex?\color{white}e_i%20=%20-V_x%20-%20R_1C_1\frac{dV_x}{dt}%20-%20R_1C_2\frac{dV_{e0}}{dt})   
![Eq7](https://latex.codecogs.com/svg.latex?\color{white}e_i%20=%20-C_2R_2\frac{dV_{e0}}{dt}%20-%20V_{e0}%20-%20R_1C_1\left(C_2R_2\frac{d^2V_{e0}}{dt^2}%20+%20\frac{dV_{e0}}{dt}\right)%20-%20R_1C_2\frac{dV_{e0}}{dt}%20=%200)

### ⚡
![Eq1](https://latex.codecogs.com/svg.image?\color{white}e_i%20=%20V_x%20-%20I_1%20R_1%20-%20C_1%20\frac{dV_x}{dt}%20-%20C_2%20\frac{dV_{e0}}{dt})    
![Eq2](https://latex.codecogs.com/svg.image?\color{white}V_x%20=%20V_{R2}%20+%20V_{e0})   
![Eq3](https://latex.codecogs.com/svg.image?\color{white}V_x%20=%20I_3%20R_2%20+%20V_{e0})   
![Eq4](https://latex.codecogs.com/svg.image?\color{white}V_x%20=%20C_2%20R_2%20\frac{dV_{e0}}{dt}%20+%20V_{e0})   
![Eq5](https://latex.codecogs.com/svg.image?\color{white}e_i%20=%20-V_x%20-%20R_1%20C_1%20\frac{dV_x}{dt}%20-%20R_1%20C_2%20\frac{dV_{e0}}{dt})   
![Eq6](https://latex.codecogs.com/svg.image?\color{white}e_i%20=%20-C_2%20R_2%20\frac{dV_{e0}}{dt}%20-%20V_{e0}%20-%20R_1%20C_1%20\left(C_2%20R_2%20\frac{d^2V_{e0}}{dt^2}%20+%20\frac{dV_{e0}}{dt}\right)%20-%20R_1%20C_2%20\frac{dV_{e0}}{dt})   

### ⚡ Amplificadores 

![Eq1](https://latex.codecogs.com/svg.image?\color{white}I_1%20=%20I_2%20)   
![Eq1](https://latex.codecogs.com/svg.image?\color{white}\frac{e_o%20-%20V_x}{R_2}%20-%20\frac{V_x}{R_1}%20=%200)   
![Eq2](https://latex.codecogs.com/svg.image?\color{white}V_x%20=%20e_i)   
![Eq3](https://latex.codecogs.com/svg.image?\color{white}\frac{e_o}{R_2}%20-%20\frac{e_i}{R_2}%20-%20\frac{e_i}{R_1}%20=%200)   
![Eq4](https://latex.codecogs.com/svg.image?\color{white}\frac{e_o}{R_2}%20=%20e_i%20\left(\frac{1}{R_2}%20+%20\frac{1}{R_1}\right))   
![Eq5](https://latex.codecogs.com/svg.image?\color{white}e_o%20=%20e_i%20\left(1%20+%20\frac{R_2}{R_1}\right))   

---
### ⚡ Ejerccio con valorres numericos    
![image](https://github.com/user-attachments/assets/768faac5-7c44-47ed-8ba5-fbc65342caae)
   
![Eq1](https://latex.codecogs.com/svg.image?\color{white}-u%20+%20v\cdot%20R_1%20+%20v\cdot%20R_2%20+%20v_C%20=%200)   
![Eq2](https://latex.codecogs.com/svg.image?\color{white}-u(t)%20+%20\left(C\cdot\frac{dv(t)}{dt}\cdot%20R_1\right)%20+%20\left(C\cdot\frac{dv(t)}{dt}\cdot%20R_2\right)%20+%20C\cdot\frac{dv(t)}{dt}%20=%200)   
![Eq3](https://latex.codecogs.com/svg.image?\color{white}\frac{u%20-%20y}{R_1}%20=%20\frac{y%20-%20v_C}{R_2})   
![Eq4](https://latex.codecogs.com/svg.image?\color{white}-\frac{v_C}{R_2}%20=%20\frac{u%20-%20y}{R_1}%20-%20\frac{y}{R_2})   
![Eq5](https://latex.codecogs.com/svg.image?\color{white}-\frac{v_C}{R_2}%20=%20\frac{u}{R_1}%20-%20y\left(\frac{1}{R_1}%20+%20\frac{1}{R_2}\right))   

#### u = 5v
#### R1 = 50
#### R1 = 50
#### C = 100mF   

![Eq1](https://latex.codecogs.com/svg.image?\color{white}-\frac{v_C}{20}%20=%20\frac{5}{50}%20-%20y\left(\frac{1}{50}%20+%20\frac{1}{20}\right))   
![Eq2](https://latex.codecogs.com/svg.image?\color{white}-\frac{v_C}{20}%20=%200.1%20-%20y\left(0.02%20+%200.05\right))   
![Eq3](https://latex.codecogs.com/svg.image?\color{white}-\frac{v_C}{20}%20=%200.1%20-%200.07y)   
```matlab
% Parámetros
R1 = 50;
R2 = 20;
C = 100e-3;  % 100 mF = 0.1 F
u = 5;       % Voltaje de entrada

% Función que define la EDO para vC(t)
f = @(t, vC) (1/C) * ((u / R1) - ((1 / R1 + 1 / R2) * ((u / R1 + vC / R2) / (1 / R1 + 1 / R2))) + vC / R2);

% Simulación con ode45
tspan = [0 5];
vC0 = 0;  % Condición inicial
[t, vC] = ode45(f, tspan, vC0);

% Calcular y(t) para cada vC(t)
y = (u / R1 + vC / R2) / (1 / R1 + 1 / R2);

vR2 = y - vC;


figure;
plot(t, vR2, 'LineWidth', 2);
xlabel('Tiempo (s)');
ylabel('Voltaje en R_2 (V)');
title('Voltaje en la resistencia R_2 usando ODE45');
grid on;
```
![image](https://github.com/user-attachments/assets/2075cbb1-5d70-4937-957a-118df65a813e)   
![image](https://github.com/user-attachments/assets/1368f36f-ad67-48eb-b760-c346fd732365)

