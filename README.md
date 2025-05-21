# Apuntes Tercer Corte - Sistemas Dinamicos


$$
Jose Manuel   Ortiz   Soler - 121769
$$


$$
Nicolas   Cortes    Triana - 120883
$$


$$
Carlos   Andres   Cante   Saavedra - 122248
$$


# 25 de abril 

# Sistema de tanques

En sistemas industrials de tanques es deseable mantener
flujo o nivel constante


![image](https://github.com/user-attachments/assets/bab05579-22f2-490e-ae46-6b9bb7bbad47)


Flujo de salida del tanque


$$
q_1 = \frac{h_1}{R_1}
$$


Intercambio de energía


$$
A_1 \frac{dh_1}{dt} = q_i - q_1
$$

Modelo de un tanque:

![image](https://github.com/user-attachments/assets/47466672-464d-407a-86ff-076afe7149fb)

Tomando \( q_i \) como entrada y \( q_1 \) como salida:

$$
q_1 = \frac{h_1}{R_1}
$$

$$
A_1 \frac{dh_1}{dt} = q_i - q_1
$$

Relación adicional:

$$
h_1 = q_1 \cdot R_1
$$

Sustituyendo en la ecuación diferencial:

$$
R_1 A_1 \frac{dq_1}{dt} = q_i - q_1
$$

# Ejemplo 1 

En el sistema de nivel de Iíquido de la Fig. 4-35 supóngase que la
razón de flujo de salida Q rn3/s a través de la válvula de salida está relacionada con
la altura H m por 


$$
Q = K \sqrt{H} = 0.01 \sqrt{H}
$$


Supóngase tambih que cuando la razón de flujo de entrada Qi es 0.015 m3/s, la altura
permanece constante. En t = O la válvula de entrada de flujo se cierra y, por lo tanto
no hay flujo de entrada para t 1 O. Encuéntrese el tiempo necesario para vaciar el
tanque a la mitad de su altura original. La capacitancia del tanque es de 2m^2

![image](https://github.com/user-attachments/assets/dbfd8bb1-6846-4cb2-81ba-5ed5dbedbe19)

Cuando la altura es estacionaria, la razón del flujo de entrada es igual a la
razón del flujo de salida. Así, la altura &, en t = O se obtiene de 

$$
0.015 = 0.01\sqrt{H_0}
$$


o bien


$$
H_0 = 2.25 \, \text{m}
$$

La ecuación del sistema para t > O es 

$$
-C \, dH = Q \, dt
$$


o bien

$$
\frac{dH}{dt} = -\frac{Q}{C} = \frac{-0.01\sqrt{H}}{2}
$$


En consecuencia,

$$
\frac{dH}{\sqrt{H}} = -0.005\,dt
$$

Supóngase que \( H = 1.125 \, \text{m} \) en \( t = t_1 \). Integrando ambos lados de esta última ecuación, tenemos

$$
\int_{2.25}^{1.125} \frac{dH}{\sqrt{H}} = \int_{0}^{t_1} (-0.005) dt = -0.005t_1
$$

Por lo tanto, se infiere que

$$
2\sqrt{H} \bigg|_{2.25}^{1.125} = 2\sqrt{1.125} - 2\sqrt{2.25} = -0.005t_1
$$

o bien

$$
t_1 = 176 \, \text{s}
$$

# Ejemplo 2 

En el sistema de nivel de líquido mostrado en la Fig. 4-38, la razbn de flujo en estado estable a través del tanque es Q y las alturas en estado estable
del tanque 1 y el tanque 2 son fi y 4, respectivamente. En 1 = O la razón de flujo de
entrada se cambia de Q a Q + q, donde q es un cambio pequefio en la razón de flujo
de entrada. Los cambios correspondientes en las alturas (hl y h2) y los cambios en la 

![image](https://github.com/user-attachments/assets/6fc0ab0d-7445-4fb6-bf3f-e273d251d0bf)


razón de flujo (q, y q2) se suponen pequefios. Las capacitancias del tanque I y el tanque 2 son Cl y C;, respectivamente. La resistencia de la válvula entre los tanques es
Rl y la correspondiente a la válvula de salida es R2.
Suponiendo que q es la entrada y q2 es la salida, obténgase el modelo maternatico (ecuación diferencial) del sistema. 

Solution. Para el tanque 1, tenemos

$$
C_1 \, dh_1 = (q - q_1) \, dt
$$

donde

$$
q_1 = \frac{h_1 - h_2}{R_1}
$$

Así pues

$$
C_1 \, \frac{dh_1}{dt} + \frac{h_1}{R_1} = q + \frac{h_2}{R_1} \quad (4-30)
$$

Para el tanque 2, tomamos

$$
C_2 \, dh_2 = (q_1 - q_2) \, dt
$$

donde

$$
q_2 = \frac{h_2}{R_2}
$$

Por lo tanto,

$$
C_2 \, \frac{dh_2}{dt} + \frac{h_2}{R_1} + \frac{h_2}{R_2} = \frac{h_1}{R_1} \quad (4-31)
$$

Al eliminar \( h_1 \) de las Ecs. (4-30) y (4-31), el resultado es

$$
R_1C_1R_2C_2 \frac{d^2h_2}{dt^2} + (R_1C_1 + R_2C_2 + R_2C_1) \frac{dh_2}{dt} + h_2 = R_2q
$$

Observando que \( h_2 = R_2q_2 \), obtenemos

$$
R_1C_1R_2C_2 \frac{d^2q_2}{dt^2} + (R_1C_1 + R_2C_2 + R_2C_1) \frac{dq_2}{dt} + q_2 = q
$$

Este es el modelo matemático deseado o ecuación diferencial que relaciona \( q_2 \) y \( q \).


# 28 de abril

# Fuuncion de transferencia

En el área de control se usa otro tipo de representación
matemática denominada función de transferencia.


Consiste en la transformada de Laplace de la ecuación
diferencial



Clasificación de las funciones de
transferencia:


- Una función de transferencia se puede expresar como:

$$
G(s) = \frac{N(s)}{D(s)}
$$

- Donde \( N(s) \) y \( D(s) \) son polinomios en la variable "s".
- Si denominamos \( n \) al grado del polinomio del numerador.
- Si denominamos \( m \) al grado del polinomio del denominador.
- Se tienen 3 casos posibles:
  - \( n > m \) (impropia)
  - \( m > n \) (estrictamente propia)
  - \( n = m \) (bipropia)
 

Zeros de una función de transferencia

• Si se iguala N(s) a 0 se obtienen los valores de “s” que
cumplen con la condición
• Si el numerador se hace 0 toda la función de
transferencia se vuelve cero de ahí el nombre para estos
valores de “s”
• Estos valores pueden ser reales o complejos por lo tanto
se pueden ubicar en un plano cartesiano


Hallar los zeros de una función de
transferencia


$$
G(s) = \frac{Y(s)}{U(s)} = \frac{3s-1}{s^2+3s+2} = \frac{N(s)}{D(s)}
$$

$$
N(s) = 0 \quad 3s-1=0
$$


# Ejemplo 1

Dada la función de transferencia:

$$
G(s) = \frac{s^2 + 4s + 13}{(s + 2)(s + 5)}
$$

Determinar los ceros.

**Solución:**

Ceros = raíces del numerador:

$$
s^2 + 4s + 13 = 0
$$

Aplicamos fórmula general:

$$
s = \frac{-4 \pm \sqrt{(4)^2 - 4(1)(13)}}{2(1)} = \frac{-4 \pm \sqrt{-36}}{2} = -2 \pm 3i
$$


# Ejemplo 2 

Dada la siguiente función de transferencia de un sistema dinámico de segundo orden:

$$
G(s) = \frac{s^2 + 6s + 25}{s^2 + 10s + 24}
$$

En este caso, el numerador es:

$$
s^2 + 6s + 25 = 0
$$

Aplicamos la fórmula cuadrática:

$$
s = \frac{-6 \pm \sqrt{6^2 - 4(1)(25)}}{2(1)} = \frac{-6 \pm \sqrt{36 - 100}}{2} = \frac{-6 \pm \sqrt{-64}}{2}
$$

$$
s = \frac{-6 \pm 8i}{2} = -3 \pm 4i
$$

La función de transferencia tiene dos ceros complejos conjugados en:

$$
s = -3 + 4i \quad y \quad s = -3 - 4i
$$

# Polos de una función de transferencia

Si se iguala D(s) a 0 se obtienen los valores de “s” que
cumplen con la condición
• Si el denominador se hace 0 toda la función de
transferencia se vuelve infinito de ahí el nombre para
estos valores de “s”
• Estos valores pueden ser reales o complejos por lo tanto
se pueden ubicar en un plano cartesiano

# Ejemplo 1 

Dada la función de transferencia:

$$
G(s) = \frac{s + 3}{(s + 1)(s + 4)}
$$

Los polos son las raíces del denominador:

$$
(s+1)(s+4) = 0
$$

$$
\Rightarrow s+1 = 0 \Rightarrow s = -1
$$

$$
\Rightarrow s+4 = 0 \Rightarrow s = -4
$$

# 2 de mayo


# 5 de mayo

# Maquina de vapor

# 9 de mayo

# Diagrama de flujo de señal

# 12 de mayo




# 16 de mayo


# 19 de mayo

# Sistema de segundo orden
