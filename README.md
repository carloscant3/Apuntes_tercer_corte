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

# Funcion de transferencia

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


# Ejemplo 2 

Sea la siguiente función de transferencia:

$$
G(s) = \frac{10}{s^2 + 6s + 13}
$$

El denominador es:

$$
s^2 + 6s + 13 = 0
$$

Aplicamos fórmula cuadrática:

$$
s = \frac{-6 \pm \sqrt{6^2 - 4(1)(13)}}{2(1)} = \frac{-6 \pm \sqrt{36 - 52}}{2} = \frac{-6 \pm \sqrt{-16}}{2} = -3 \pm 2i
$$

Los polos del sistema son: 

$$
s = -3 \pm 2i
$$

# Teorema del valor final

•El error en estado estacionario corresponde al error
medido en 𝑡 = ∞

Es posible aprovechar el teorema del valor final para
saber el valor final del error

$$
G(s) = \frac{Y(s)}{U(s)} = \frac{4}{5s+1}
$$

$$
Y(s) = \frac{4 \cdot U(s)}{5s+1}
$$

- Si la entrada es un escalón:

$$
Y(s) = \frac{\frac{4}{s}}{5s+1}
$$

El valor final de \( Y(s) \) se puede calcular aplicando el teorema del valor final:

$$
\lim_{s \to 0} sY(s) = \lim_{s \to 0} s \cdot \frac{\frac{4}{s}}{5s + 1} = \lim_{s \to 0} \frac{4}{5s + 1} = 4
$$

# Ejemplo 1

Dada la función de transferencia:

$$
G(s) = \frac{5s + 10}{s^2 + 4s + 5}
$$

Calcular el valor final de la salida \( y(t) \), si la entrada es un escalón unitario.

Sabemos que:

$$
\lim_{t \to \infty} y(t) = \lim_{s \to 0} s \cdot G(s) \cdot \frac{1}{s} = \lim_{s \to 0} \frac{5s + 10}{s^2 + 4s + 5}
$$

Sustituímos \( s = 0 \):

$$
= \frac{5(0) + 10}{0 + 0 + 5} = \frac{10}{5} = 2
$$


# Ejemplo 2 

Dada la función de transferencia:

$$
G(s) = \frac{10}{s(s + 2)}
$$

Calcular el valor final de la salida \( y(t) \), si la entrada es un escalón unitario.

Aplicando el teorema del valor final:

$$
\lim_{t \to \infty} y(t) = \lim_{s \to 0} s \cdot G(s) \cdot \frac{1}{s} = \lim_{s \to 0} \frac{10}{s + 2}
$$

Sustituyendo \( s = 0 \):

$$
\frac{10}{2} = 5
$$






# 2 de mayo

# Entrada de prueba de un sistema

Cuando se quiere analizar un sistema dinámico, no se usan señales reales directamente porque:

- Hay ruido
- Son difíciles de controlar
- Hay muchas variaciones

Por eso usamos funciones conocidas para probar el sistema.

**Ejemplo:** 
Sistema con un agitador, donde:

- T_i(t) = temperatura de entrada
- T(t) = temperatura en el tanque
- f = flujo de entrada (m³/s)
- n = velocidad del agitador

La idea es ver cómo responde T(t) frente a cambios en T_i(t) usando funciones estándar.

**Entradas comunes usadas para probar un sistema:**
- Escalón
- Impulso
- Rampa
- Señal senoidal

# Entrada Escalón

Es una entrada que representa un **cambio repentino de nivel**. Muy usada para analizar cómo responde un sistema ante un cambio brusco.

- Se define como:

$$
u(t) =
\begin{cases}
0 & \text{para } t < t_0 \\
A & \text{para } t \geq t_0
\end{cases}
$$

- Transformada de Laplace:

$$
\mathcal{L}\{u(t)\} = \frac{A}{s}
$$

A menudo se usa con t_0 = 0, es decir, el cambio ocurre justo al iniciar la prueba.

![image](https://github.com/user-attachments/assets/4ca3c2fc-ac06-4f52-b5e2-1eb8446e80c3)

# Entrada Rampa

Es una entrada que **varía linealmente con el tiempo**, comenzando en un punto t_0.

- Se define como:

$$
x(t) =
\begin{cases}
0 & \text{para } t < t_0 \\
At & \text{para } t \geq t_0
\end{cases}
$$

- Transformada de Laplace:

$$
\mathcal{L}\{x(t)\} = \frac{A}{s^2}
$$

**Interpretación**: representa un **aumento progresivo constante**, como el llenado de un tanque a caudal constante, o un motor acelerando linealmente.

![image](https://github.com/user-attachments/assets/288273ab-11b8-4ec4-b81b-644cb7ce4559)

# Entrada Parábola

Es una entrada que considera una **variación no lineal en el tiempo**, permitiendo evaluar diferentes condiciones de inicio y final.

- Se define como:

$$
r(t) =
\begin{cases}
0 & \text{para } t < t_0 \\
At^2 & \text{para } t \geq t_0
\end{cases}
$$

- Transformada de Laplace:

$$
\mathcal{L}\{r(t)\} = \frac{A}{s^3}
$$

**Interpretación**: este tipo de entrada representa una **aceleración creciente**. Es útil para simular movimientos con aceleración variable o sistemas con condiciones de cambio progresivo no lineal.

![image](https://github.com/user-attachments/assets/11e23f4e-f061-488c-aa4d-9b19fee8e0d8)

# Ejemplo No. 1

# Cálculo del valor final para las entradas de prueba

Aplicamos el **Teorema del Valor Final**:

$$
\lim_{t \to \infty} y(t) = \lim_{s \to 0} sY(s)
$$

donde 

$$
\( Y(s) = G(s)X(s) \) 
$$

con 

$$
\( G(s) \) 
$$

la función de transferencia del sistema y 


$$
\( X(s) \) la transformada de la entrada.
$$


**Entrada Escalón**

- Entrada:

$$
x(t) = A u(t) 
$$

Transformada: 

$$ 
X(s) = \frac{A}{s} 
$$

Suponiendo 

$$ 
G(s) = \frac{1}{s+2} 
$$

**Cálculo**:

$$
\lim_{s \to 0} s \cdot \frac{1}{s+2} \cdot \frac{A}{s}
= \lim_{s \to 0} \frac{A}{s+2} = \frac{A}{2}
$$

**Valor final: 

$$
\( \frac{A}{2} \)**
$$

# Entrada Rampa

- Entrada:

$$ 
x(t) = At \cdot u(t) 
$$

- Transformada:

$$
X(s) = \frac{A}{s^2} 
$$

- Suponiendo

$$ 
G(s) = \frac{1}{s+2} 
$$

**Cálculo**:

$$
\lim_{s \to 0} s \cdot \frac{1}{s+2} \cdot \frac{A}{s^2}
= \lim_{s \to 0} \frac{A}{s(s+2)} = \infty
$$

**Valor final: ∞ (el sistema no alcanza estado estacionario)**

# Entrada Parábola

- Entrada:

$$ 
x(t) = At^2 \cdot u(t) 
$$

- Transformada:
$$
X(s) = \frac{A}{s^3}
$$

- Suponiendo

$$
G(s) = \frac{1}{s+2} 
$$

**Cálculo**:

$$
\lim_{s \to 0} s \cdot \frac{1}{s+2} \cdot \frac{A}{s^3}
= \lim_{s \to 0} \frac{A}{s^2(s+2)} = \infty
$$

**Valor final: ∞ (diverge aún más rápido que la rampa)**

**Conclusión**: solo la entrada escalón permite un valor final finito en este sistema. Las otras dos (rampa y parábola) generan salidas crecientes indefinidamente si el sistema es tipo 0.

# Ejemplo No. 2

# Análisis de sistema con ecuación diferencial

Considere la siguiente **ecuación diferencial** del sistema:

$$
\ddot{y} + 4\dot{y} + 6y = 2\dot{u} + 3u
$$

Obtenga:

- Función de transferencia
- Zeros y polos
- Valor final frente a un **escalón unitario**
- Valor final frente a una **rampa de pendiente 3**

# 1. Función de transferencia

Aplicamos transformada de Laplace con condiciones iniciales nulas:

$$
\mathcal{L}\{\ddot{y}\} = s^2 Y(s) 
$$

$$
\mathcal{L}\{\dot{y}\} = s Y(s) 
$$

$$
\mathcal{L}\{\dot{u}\} = s U(s) 
$$

Entonces:

$$
s^2 Y(s) + 4s Y(s) + 6Y(s) = 2s U(s) + 3U(s)
$$

Factorizamos:

$$
Y(s) \left( s^2 + 4s + 6 \right) = U(s) \left( 2s + 3 \right)
$$

Función de transferencia:

$$
G(s) = \frac{Y(s)}{U(s)} = \frac{2s + 3}{s^2 + 4s + 6}
$$

### 🔹 2. Zeros y Polos

- **Zero**: raíz del numerador:

$$ 
2s + 3 = 0 \Rightarrow s = -\frac{3}{2} 
$$

- **Polos**: raíces del denominador:

$$
s^2 + 4s + 6 = 0 \Rightarrow s = -2 \pm j
$$

Zeros: \( s = -1.5 \)  
Polos: \( s = -2 \pm j \)

# 3. Valor final frente a escalón unitario

Entrada: 

$$
u(t) = 1 \cdot u(t) \Rightarrow U(s) = \frac{1}{s} 
$$

Aplicamos teorema del valor final:

$$
\lim_{t \to \infty} y(t) = \lim_{s \to 0} sY(s) = \lim_{s \to 0} s \cdot G(s) \cdot U(s)
= \lim_{s \to 0} s \cdot \frac{2s + 3}{s^2 + 4s + 6} \cdot \frac{1}{s}
= \lim_{s \to 0} \frac{2s + 3}{s^2 + 4s + 6}
= \frac{3}{6} = 0.5
$$

**Valor final: 0.5**

# 4. Valor final frente a rampa de pendiente 3

Entrada: 

$$
u(t) = 3t \Rightarrow U(s) = \frac{3}{s^2}
$$

$$
\lim_{t \to \infty} y(t) = \lim_{s \to 0} s \cdot G(s) \cdot U(s)
= \lim_{s \to 0} s \cdot \frac{2s + 3}{s^2 + 4s + 6} \cdot \frac{3}{s^2}
= \lim_{s \to 0} \frac{3(2s + 3)}{s(s^2 + 4s + 6)}
= \infty
$$

**Valor final: ∞ (el sistema no sigue una rampa sin error en estado estacionario)**

**Resultados**:

$$
G(s): \( \frac{2s + 3}{s^2 + 4s + 6} \)
$$

- Zero:

$$
\( s = -1.5 \)
$$

- Polos:

$$
\( s = -2 \pm j \)
$$

- Valor final para escalón: **0.5**
- Valor final para rampa de pendiente 3: **Infinito**

# 5 de mayo

# Álgebra de Bloques

Una herramienta que puede ayudar a entender un poco
la interacción entre varios sistemas son los diagramas de
bloques 

Primer sistema de control J. Watt

Para explicar su sistema empezó adesarrollar los diagramas de bloques


# Maquina de vapor

Una herramienta que ayuda a entender un poco como funcionan los diagramas de bloques

![image](https://github.com/user-attachments/assets/02d0636f-6e40-4b05-8d11-24dd0ebb13f8)


Las flechas: Representan señales dentro del proceso:

![image](https://github.com/user-attachments/assets/0a2d0e2d-6238-4de9-af45-61a48fa69144)


Punto suma: Representa la suma algebraica de dos o más señales

![image](https://github.com/user-attachments/assets/f0d7b3b4-609d-4f78-ae30-107336eb724d)


Ramificacion: ocurre cuando una señal se divide y se envía a varios bloques al mismo tiempo.

![image](https://github.com/user-attachments/assets/e19e7c10-3065-469e-ba8c-386499591da6)


Interpretación del diagrama
La salida de un bloque funcional corresponde a la señal
de entrada (Dominio s) multiplicada por por la función de
transferencia del bloque. 


![image](https://github.com/user-attachments/assets/825996a4-b1c3-46f9-8b15-45361d1dfcbe)


Si se tienen 2 sistemas interconectados


![image](https://github.com/user-attachments/assets/16f16e3f-bfd5-4300-bb13-46cbca39cb47)


$$
Y_1(s) = U_1(s)G_1(s)
$$
$$
Y_2(s) = Y_1(s)G_2(s)
$$
$$
Y_2(s) = U_2(s)G_2(s)
$$
$$
Y_2(s) = U_1(s)G_1(s)G_2(s)
$$

![image](https://github.com/user-attachments/assets/e8acf0fc-6785-4340-8540-b3e88e9099ca)


Lazo de realimentación positivo


![image](https://github.com/user-attachments/assets/5db7d737-aad7-44f3-bb38-b92b02262f94)

$$
E(s) = X(s) + Y_1(s)
$$

$$
Y(s) = E(s)G_1(s)
$$

$$
Y_1(s) = Y(s)G_2(s)
$$

$$
Y(s) = (X(s) + Y_1(s))G_1(s)
$$

$$
Y(s) = (X(s) + Y(s)G_2(s))G_1(s)
$$

$$
Y(s) = X(s)G_1(s) + Y(s)G_2(s)G_1(s)
$$

$$
Y(s) - Y(s)G_2(s)G_1(s) = X(s)G_1(s)
$$

$$
Y(s)(1 - G_2(s)G_1(s)) = X(s)G_1(s)
$$

$$
\frac{Y(s)}{X(s)} = \frac{G_1(s)}{1 - G_2(s)G_1(s)}
$$

# Ejemplo 1 

Del diagrama de bloques mostrado en la imagen, obtenga la
función de transferencia que relaciona

![image](https://github.com/user-attachments/assets/28cee82a-78ba-4780-8231-826a25e3856e)

La señal \( X(s) \) es la suma de las dos señales \( G_1 \Theta_i(s) \) y \( \Theta_j(s) \). Por lo tanto,


$$
X(s) = G_1 \Theta_i(s) + \Theta_j(s)
$$

$$
La señal \( X(s) \) es la suma de las dos señales \( G_1 \Theta_i(s) \) y \( \Theta_j(s) \). Por lo tanto,
$$


$$
\Theta_o(s) = G_2 X(s) + \Theta_i(s) = G_2 [G_1 \Theta_i(s) + \Theta_j(s)] + \Theta_i(s)
$$

Y, por lo tanto, tenemos

$$
\frac{\Theta_o(s)}{\Theta_i(s)} = G_1 G_2 + G_2 + 1
$$


$$
X(s) = G_1 \Theta_i(s) + \Theta_j(s)
$$

La señal de salida \( \Theta_o(s) \) es la suma de \( G_2 X(s) \) y \( \Theta_i(s) \). De donde,

$$
\Theta_o(s) = G_2 X(s) + \Theta_i(s) = G_2 [G_1 \Theta_i(s) + \Theta_j(s)] + \Theta_i(s)
$$

Y, por lo tanto, tenemos

$$
\frac{\Theta_o(s)}{\Theta_i(s)} = G_1 G_2 + G_2 + 1
$$

# Ejemplo 2 

Simplifiquese el diagrama de bloques mostrado

![image](https://github.com/user-attachments/assets/607f14a7-0c17-4b0b-8ab4-70ca963ea6e7)

Primero nos vamos al punto de bifurcación de la trayectoria que incluye a
H, por fuera de la trayectoria que incluye a H2 como se muestra en la primera imagen.
Luego elimínense las dos trayectorias y resulta la segunda imaegn. La combinación de
dos bloques en uno da la ultima imagen

![image](https://github.com/user-attachments/assets/15ad152f-f7a4-4449-b4f8-2a9ad1fec7b3)


![image](https://github.com/user-attachments/assets/82777497-b87f-4cea-bb95-2f31aeed1d16)


![image](https://github.com/user-attachments/assets/81d80f54-5e33-4d77-8cc8-918bb9c87325)


# 9 de mayo

# Diagrama de flujo de señal

Este tipo de diagramas permite otra forma de
representación de los sistemas más complejos
Se utilizan para obtener de una manera más sencilla la
función de transferencia total del Sistema
La formula de Mason permite calcular la función de
trasferencia de sistemas muy complejos

Elementos de los diagramas de flujo de
señal

Nodo: Representan las señales de entrada o salida del
Sistema
• Se representa por medio de un círculo con una
etiqueta que indique el nombre de la señal

![image](https://github.com/user-attachments/assets/6332d045-77b5-473f-9077-b36166929aeb)

Elementos de los diagramas de flujo de
señal

Flecha: Representa la relación entre las variables del
sistema
• Se representa por medio de flechas que indicando el
sentido de la relación
• La fleche sale de la señal (Nodo) de entrada y llega a
la señal de salida (Nodo)
• Se agrega una etiqueta a la flecha para indicar la
función de transferencia que relaciona la entrada y la
salida

![image](https://github.com/user-attachments/assets/b16a0dc1-624a-4547-94ae-8f7a08d50207)


Interpretación de los diagramas de flujo
de señales

![image](https://github.com/user-attachments/assets/c1aed0a9-985c-43e2-ab2e-230b92cce677)


Comparación diagramas de bloques y
flujo de señales

![image](https://github.com/user-attachments/assets/47e63824-8590-463c-a67c-97c311235baa)


Fórmula de Mason

$$
P = \frac{1}{\Delta} \sum_k P_k \Delta_k
$$

𝑃𝑘Ganancia de los caminos directos
• Δ = 1 − (suma ganancias de los lazos) + (suma producto de 2
lazos que no se tocan) – (suma producto de 3 lazos que no se
tocan)+…
• Δ𝑘 = 1 −(suma ganancias lazos que no toquen la trayectoria
𝑃𝑘)+(suma ganancias 2 lazos que no toquen la trayectoria 𝑃𝑘 y
no se toquen entre sí)-(suma ganancias 3 lazos que no toquen
la trayectoria 𝑃𝑘 y no se toquen entre sí)+…

# Ejemplo 1

![image](https://github.com/user-attachments/assets/11427175-35b5-4001-b68c-2e9a28e265ac)

**Trayectoria directa:**
$$
P_1 = 1 \cdot 1 \cdot G_1 \cdot G_2 \cdot G_3 \cdot 1 = G_1 G_2 G_3
$$

**Lazos cerrados:**
$$
L_1 = G_1 G_2 H_1
$$

$$
L_2 = -G_2 G_3 H_2
$$

$$
L_3 = -G_1 G_2 G_3
$$

### Determinante del sistema:
$$
\Delta = 1 - (L_1 + L_2 + L_3) \quad \text{(Determinante del sistema)}
$$

### Cofactores:
$$
\Delta_1 = 1 \quad \text{(Cofactor para la trayectoria directa)}
$$

### Función de transferencia resultante:
$$
\frac{C(s)}{R(s)} = \frac{P_1 \Delta_1}{\Delta} = \frac{G_1 G_2 G_3}{1 - G_1 G_2 H_1 + G_2 G_3 H_2 + G_1 G_2 G_3}
$$

# Ejemplo 2

![image](https://github.com/user-attachments/assets/be8509aa-a513-41f8-af1b-43d93ffb468d)


### Trayectorias Directas:
$$
P_1 = G_1 G_2 G_3 G_4 G_5
$$

$$
P_2 = G_1 G_6 G_4 G_5
$$

$$
P_3 = G_1 G_2 G_7
$$

### Lazos de Retroalimentación:
$$
L_1 = -G_4 H_1
$$

$$
L_2 = -G_2 G_7 H_2
$$

$$
L_3 = -G_6 G_4 G_5 H_2
$$

$$
L_4 = -G_2 G_3 G_4 G_5 H_2
$$

### Determinante del Sistema:
$$
\Delta = 1 - (L_1 + L_2 + L_3 + L_4) + L_1 L_2
$$


Cofactores

$$
\Delta_1 = 1 \\
\Delta_2 = 1 \\
\Delta_3 = 1 - L_1
$$

$$
L_1 \text{ no toca la trayectoria }
$$

$$
\frac{C(s)}{R(s)} = \frac{1}{\Delta} (P_1 \Delta_1 + P_2 \Delta_2 + P_3 \Delta_3)
$$

$$
= \frac{G_1 G_2 G_3 G_4 G_5 + G_1 G_6 G_4 G_5 + G_1 G_2 G_7 (1 + G_4 H_1)}{1 + G_4 H_1 + G_3 G_7 H_2 + G_6 G_4 G_5 H_2 + G_3 G_3 G_4 G_5 H_2 + G_4 H_1 G_3 G_7 H_2}
$$



# 12 de mayo
# FORMULA DE MASON

# ¿Qué es la Fórmula de Mason?

La **Fórmula de Mason**, también conocida como **Regla de Mason para gráficos de flujo de señal**, permite calcular de manera **directa** la **función de transferencia** de un sistema representado con un **diagrama de bloques o de flujo**.

Se expresa como:

$$
T(s) = \frac{C(s)}{R(s)} = \frac{1}{\Delta} \sum_k P_k \Delta_k
$$

Donde:

$$
\( C(s) \): salida del sistema.
$$

$$
\( R(s) \): entrada del sistema.
$$

$$
\( P_k \): cada camino directo desde la entrada hasta la salida.
$$

$$
\( \Delta \): determinante del sistema (considera todos los lazos).  
$$

$$
\( \Delta_k \): determinante considerando solo los lazos que **no tocan** el camino \( P_k \).  
$$

**¿Por qué es importante?**

- Evita simplificaciones complejas: en lugar de aplicar reducciones de bloques, Mason trabaja con el grafo completo.  
- Ideal para sistemas con múltiples lazos de realimentación.  
- Aplica a sistemas LTI (lineales e invariantes en el tiempo).  
- Base de herramientas como MATLAB, Simulink y Scilab.  

**¿Cuándo usarla?**

- Cuando hay varios caminos de entrada a salida.  
- Cuando hay muchos lazos y sus combinaciones.  
- Cuando se busca automatizar el análisis del sistema.

**¿Qué debes dominar para usarla bien?**

1. Identificar caminos directos \( P_k \).  
2. Detectar lazos individuales y sus ganancias.  
3. Encontrar lazos que no se tocan.  
4. Construir \( \Delta \) y \( \Delta_k \).  
5. Entender álgebra de bloques y sistemas lineales.  

# Ejemplo No. 1

![image](https://github.com/user-attachments/assets/a2ab525c-4bb2-4e54-9704-0b4bdfcac6ad)

# Solución del Ejemplo - Fórmula de Mason

**Objetivo:**
Calcular la función de transferencia \( \frac{Y(s)}{X(s)} \) usando la fórmula de Mason.

**Camino directo**

Solo hay **un camino directo** de entrada a salida:

$$
P_1 = G_1 \cdot G_2 \cdot G_3 \cdot G_4 \cdot G_5
$$

# Lazos

Los lazos identificados son:

$$
\begin{aligned}
B_1 &= G_2 \cdot H_1 \\
B_2 &= G_4 \cdot H_2 \\
B_3 &= G_6 \cdot H_3 \\
B_4 &= G_2 \cdot G_3 \cdot G_4 \cdot G_5 \cdot H_4 \cdot G_6 \cdot H_5
\end{aligned}
$$

**Determinante total \( \Delta \)**

Usamos la fórmula de Mason:

$$
\Delta = 1 - (B_1 + B_2 + B_3 + B_4) + (B_1 B_2 + B_1 B_3 + B_2 B_3) - (B_1 B_2 B_3)
$$

**Lazos que tocan el camino**

Todos los lazos tocan el camino directo, por tanto:

$$
\Delta_1 = 1
$$

**Función de transferencia final**

Aplicando la fórmula de Mason:

$$
\frac{Y(s)}{X(s)} = \frac{P_1 \cdot \Delta_1}{\Delta}
$$

Sustituyendo:

$$
\frac{Y(s)}{X(s)} = \frac{G_1 \cdot G_2 \cdot G_3 \cdot G_4 \cdot G_5}{1 - (B_1 + B_2 + B_3 + B_4) + (B_1 B_2 + B_1 B_3 + B_2 B_3) - (B_1 B_2 B_3)}
$$

Donde:

$$
\begin{aligned}
B_1 &= G_2 H_1 \\
B_2 &= G_4 H_2 \\
B_3 &= G_6 H_3 \\
B_4 &= G_2 G_3 G_4 G_5 H_4 G_6 H_5
\end{aligned}
$$

Esta es la forma simbólica general de la función de transferencia usando la fórmula de Mason.


# 16 de mayo
# SISTEMAS DE PRIMER ORDEN

Las funciones de transferencia de primer orden salen de una ecuación diferencial también de primer orden. Estas funciones se escriben así:

$$
\frac{Y(s)}{U(s)} = \frac{c}{as + b}
$$

Donde:
- \( Y(s) \) es la salida del sistema.
- \( U(s) \) es la entrada.
- \( a \), \( b \) y \( c \) son constantes que vienen del sistema físico.

Los mismos parámetros que están en la ecuación diferencial también aparecen en la función de transferencia. Estos parámetros son los que definen cómo se comporta el sistema.

# Ejemplo visto en clase

![image](https://github.com/user-attachments/assets/876a0544-b2db-4053-88ed-1565b03463bc)

Este es un sistema hidráulico simple donde entra un caudal \( q_i \), se almacena agua en un tanque con área transversal \( A_1 \), y sale por una resistencia \( R_1 \). La altura del agua es \( h_1 \).

La ecuación diferencial que describe este sistema es:

$$
R_1 A_1 \frac{dh_1}{dt} = R_1 q_i - h_1
$$

Esta ecuación se puede escribir en la forma estándar:

$$
a \dot{y}(t) + b y(t) = c u(t)
$$

Donde:
- \( a = R_1 A_1 \)
- \( b = 1 \)
- \( c = R_1 \)

La función de transferencia se obtiene tomando transformada de Laplace y es:

$$
\frac{Y(s)}{U(s)} = \frac{c}{as + b}
$$

En este caso, usando los valores del sistema:

$$
\frac{H_1(s)}{Q_i(s)} = \frac{R_1}{R_1 A_1 s + 1}
$$

Esto representa un sistema de primer orden, donde la entrada es el caudal \( Q_i(s) \) y la salida es la altura del líquido \( H_1(s) \).

# Forma canónica de los sistemas de primer orden

$$
\frac{Y(s)}{U(s)} = \frac{c}{as + b} = \frac{\frac{c}{b}}{\frac{a}{b}s + 1}
$$

La forma canónica considera:

$$
(\tau = \frac{a}{b}\): 
$$

Constante de tiempo  

$$
(K = \frac{c}{b}\): 
$$

Ganancia Estática

Por lo tanto:

$$
\frac{Y(s)}{U(s)} = \frac{K}{\tau s + 1}
$$

# Respuesta de un sistema de primer orden ante una entrada escalón

Cuando a un sistema de primer orden se le aplica una entrada escalón (una señal que sube de 0 a 1 de forma repentina), se puede hallar la salida multiplicando la función de transferencia \( G(s) \) por la entrada \( U(s) \).

Sabemos que para una entrada escalón la ecuación es:

$$
( U(s) = \frac{A}{s} \)
$$

Y si la función de transferencia del sistema es:

$$
G(s) = \frac{K}{\tau s + 1}
$$

Entonces la salida \( Y(s) \) es:

$$
Y(s) = U(s) \cdot G(s) = \frac{A}{s} \cdot \frac{K}{\tau s + 1} = \frac{AK}{s(\tau s + 1)}
$$

Esto es lo que se obtiene en el dominio de Laplace. Después, para pasar al tiempo real (dominio del tiempo), se aplica la transformada inversa.

# Ejemplo No. 1

**Sistema de primer orden**

**Problema:**  
Identificar \( \tau \) y \( K \) para el siguiente sistema de primer orden:

$$
\frac{Y(s)}{U(s)} = \frac{2}{s + 10}
$$

**Paso 1: Expresar en forma canónica**

Recordemos que la forma canónica de un sistema de primer orden es:

$$
\frac{Y(s)}{U(s)} = \frac{K}{\tau s + 1}
$$

Reescribimos la función de transferencia dada:

$$
\frac{2}{s + 10} = \frac{2}{10 \left( \frac{s}{10} + 1 \right)} = \frac{0.2}{\frac{s}{10} + 1} = \frac{0.2}{0.1 s + 1}
$$

**Paso 2: Identificar parámetros**

Comparando:

$$
\( K = 0.2 \)
$$

$$
\( \tau = 0.1 \) segundos
$$

**Interpretación**

Este sistema responde lentamente a una entrada escalón, alcanzando su valor final (0.2) de forma exponencial con una constante de tiempo de \( \tau = 0.1 \) s.

**Conclusión**

- Este es un **sistema de primer orden estable**.
- Se encuentra amortiguado y no presenta oscilaciones.
- La salida se estabiliza aproximadamente en \( 4\tau = 0.4 \) s.

# Ejemplo No. 2 – Problema práctico con sistema de primer orden

**Problema:**  
Un sistema de calefacción automática ajusta la temperatura de una habitación. Cuando se enciende el calentador, la temperatura sube hasta un valor estable, pero no instantáneamente. Se observa que el comportamiento de la temperatura puede modelarse como un sistema de primer orden con la siguiente función de transferencia:

$$
\frac{T(s)}{Q(s)} = \frac{5}{s + 20}
$$

Donde:
- \( T(s) \): Temperatura en Laplace
- \( Q(s) \): Calor entregado (entrada al sistema)
- El sistema parte desde una temperatura ambiente y responde a un incremento constante de calor.

Se pide:
1. Determinar los parámetros \( \tau \) (constante de tiempo) y \( K \) (ganancia estática) del sistema.
2. Interpretar el comportamiento de la temperatura en función del tiempo.

**Paso 1: Forma canónica**

Recordemos la forma canónica de un sistema de primer orden:

$$
\frac{Y(s)}{U(s)} = \frac{K}{\tau s + 1}
$$

Partimos de:

$$
\frac{5}{s + 20} = \frac{5}{20 \left( \frac{s}{20} + 1 \right)} = \frac{0.25}{0.05 s + 1}
$$

**Paso 2: Identificación de parámetros**

Comparando con la forma canónica:

$$
\( K = 0.25 \)
$$

$$
\( \tau = 0.05 \) segundos
$$

**Interpretación**

- La ganancia \( K = 0.25 \) indica que por cada unidad de calor constante que se entrega, la temperatura se estabiliza en 0.25 unidades más.
- La constante de tiempo \( \tau = 0.05 \) indica que el sistema alcanza el 63.2% de su valor final en 0.05 s, y se estabiliza completamente en aproximadamente \( 4\tau = 0.2 \) s.

**Conclusión**

- El sistema es rápido: responde en décimas de segundo.
- Representa adecuadamente un modelo térmico simple, como el control de temperatura en un horno pequeño o una incubadora.

# 19 de mayo

# Sistema de segundo orden

# Ecuaciones diferenciales de segundo orden

En este tema, una ecuación diferencial de segundo orden se ve así:

$$
\ddot{y}(t) + a_1 \dot{y}(t) + a_0 y(t) = b_0 u(t)
$$

Esto representa un sistema donde la salida \( y(t) \) depende de su derivada, su segunda derivada, y de la entrada \( u(t) \).

# Función de transferencia

Para obtener la función de transferencia, usamos la Transformada de Laplace (sin condiciones iniciales):

$$
s^2Y(s) + a_1sY(s) + a_0Y(s) = b_0U(s)
$$

Factorizando \( Y(s) \):

$$
Y(s)\left(s^2 + a_1s + a_0\right) = b_0U(s)
$$

Despejando la relación entre salida y entrada (Función de Transferencia):

$$
\frac{Y(s)}{U(s)} = \frac{b_0}{s^2 + a_1s + a_0}
$$

Esta es la forma estándar de un sistema de segundo orden. Sirve para analizar cómo responde un sistema cuando se le da una entrada \( u(t) \).

# Forma canónica de los sistemas de segundo orden

La función de transferencia general de un sistema de segundo orden es:

$$
G(s) = \frac{Y(s)}{U(s)} = \frac{b_0}{s^2 + a_1s + a_0}
$$

Donde:
- \( Y(s) \) es la salida en el dominio de Laplace,
- \( U(s) \) es la entrada,
- \( a_1 \) y \( a_0 \) son constantes que afectan el comportamiento del sistema.

- Esta forma **no permite identificar fácilmente** los parámetros temporales del sistema, como el tiempo de subida, amortiguamiento, o frecuencia natural.
- Por eso, en control se prefiere usar una **forma canónica** que los muestre claramente.

En la siguiente sección se explica cómo transformar esta ecuación a una forma canónica que sea más útil para análisis y diseño de controladores.

# Parámetros de los sistemas de segundo orden

Cuando usamos la forma canónica, la función de transferencia se escribe así:

$$
G(s) = \frac{Y(s)}{U(s)} = \frac{K \cdot \omega_n^2}{s^2 + 2\zeta \omega_n s + \omega_n^2}
$$

Donde:

- \( K \) es la **ganancia estática** del sistema.
- \( \omega_n \) es la **frecuencia natural** del sistema (rad/s).
- \( \zeta \) (zeta) es el **factor de amortiguamiento** del sistema.

# ¿Por qué esta forma es útil?

Esta forma **sí permite identificar directamente** los parámetros que afectan cómo responde el sistema:
- Si es rápido o lento (\( \omega_n \)).
- Si vibra mucho o poco (\( \zeta \)).
- Cuánto amplifica la salida en estado estable (\( K \)).

Esto hace que sea más práctica para análisis y diseño en ingeniería de control.

# Respuesta de un Sistema de Segundo Orden a una Entrada Escalón

Cuando se aplica una señal escalón a un sistema de segundo orden, su comportamiento depende del factor de amortiguamiento \( \zeta \) y la frecuencia natural \( \omega_n \).

# Función de transferencia en forma canónica:

$$
G(s) = \frac{K \cdot \omega_n^2}{s^2 + 2\zeta \omega_n s + \omega_n^2}
$$

# Aplicando una entrada escalón de amplitud \( A \):

$$
Y(s) = \frac{K \cdot \omega_n^2 \cdot A}{(s + \zeta \omega_n + \omega_n \sqrt{\zeta^2 - 1})(s + \zeta \omega_n - \omega_n \sqrt{\zeta^2 - 1})s}
$$

# Caso Subamortiguado (\( \zeta < 1 \)):

Cuando el sistema es subamortiguado, presenta oscilaciones que se atenúan con el tiempo. Su respuesta temporal es:

$$
\mathcal{L}^{-1}\{Y(s)\} = K \cdot A \cdot \left(1 - e^{-\zeta \omega_n t} \left[\cos(\omega_n \sqrt{1 - \zeta^2} \cdot t) + \frac{\zeta}{\sqrt{1 - \zeta^2}} \sin(\omega_n \sqrt{1 - \zeta^2} \cdot t)\right] \right)
$$

- Esta respuesta representa un comportamiento **oscilatorio amortiguado** típico en muchos sistemas físicos.
- Es útil para analizar tiempo de subida, sobrepaso y tiempo de establecimiento.

# Aplicación: 

![image](https://github.com/user-attachments/assets/9ccd0ae6-4d73-434c-a34c-9d15744d3882)

# Ejemplo No. 1

**Modelo sobreamortiguado:**

$$
G(s) = \frac{10}{s^2 + 10s + 20}
$$

Forma estándar:

$$
G(s) = \frac{\omega_n^2}{s^2 + 2\zeta\omega_n s + \omega_n^2}
$$

Identificando coeficientes:

$$
\( 2\zeta\omega_n = 10 \)
$$

$$
\( \omega_n^2 = 20 \Rightarrow \omega_n = \sqrt{20} \approx 4.472 \)
$$

Entonces:

$$
\zeta = \frac{10}{2 \cdot 4.472} \approx 1.118
$$

**Conclusión**: Como \( \zeta > 1 \), el sistema es **sobreamortiguado**, tiene dos raíces reales distintas y no oscila.

**Modelo críticamente amortiguado:**

$$
G(s) = \frac{25}{s^2 + 10s + 25}
$$

Forma estándar:

$$
G(s) = \frac{\omega_n^2}{s^2 + 2\zeta\omega_n s + \omega_n^2}
$$

Identificando coeficientes:

$$
\( 2\zeta\omega_n = 10 \)
$$

$$
\( \omega_n^2 = 25 \Rightarrow \omega_n = 5 \)
$$

Entonces:

$$
\zeta = \frac{10}{2 \cdot 5} = 1
$$

**Conclusión**: Como \( \zeta = 1 \), el sistema es **críticamente amortiguado**, tiene una raíz real doble y no oscila.

**Modelo subamortiguado:**

$$
G(s) = \frac{30}{s^2 + 6s + 30}
$$

Forma estándar:

$$
G(s) = \frac{\omega_n^2}{s^2 + 2\zeta\omega_n s + \omega_n^2}
$$

**Identificando coeficientes:

$$
\( 2\zeta\omega_n = 6 \)
$$

$$
\( \omega_n^2 = 30 \Rightarrow \omega_n = \sqrt{30} \approx 5.477 \)
$$

Entonces:

$$
\zeta = \frac{6}{2 \cdot 5.477} \approx 0.548
$$

**Conclusión**: Como \( 0 < \zeta < 1 \), el sistema es **subamortiguado**, tiene raíces complejas conjugadas y su respuesta es oscilatoria.

# Ejemplo No. 2

# Problema propuesto

Un sistema mecánico masa-resorte-amortiguador tiene como función de transferencia:

$$
G(s) = \frac{36}{s^2 + 6s + 36}
$$

Tomando una entrada tipo escalón unitario, responde lo siguiente:

1. ¿Qué tipo de sistema es según su amortiguamiento?
2. ¿Qué tipo de respuesta se espera observar?
3. ¿Cuál es la frecuencia natural y el factor de amortiguamiento?


## Solución

La forma general de un sistema de segundo orden es:

$$
G(s) = \frac{\omega_n^2}{s^2 + 2\zeta\omega_n s + \omega_n^2}
$$

Comparando con:

$$
G(s) = \frac{36}{s^2 + 6s + 36}
$$

Identificamos:

$$
\( \omega_n^2 = 36 \Rightarrow \omega_n = 6 \)
$$

$$
\( 2\zeta\omega_n = 6 \Rightarrow \zeta = \frac{6}{2 \cdot 6} = 0.5 \)
$$


# Parámetros del sistema

- Frecuencia natural: \( \omega_n = 6 \)
- Razón de amortiguamiento: \( \zeta = 0.5 \)

# Tipo de sistema

Dado que \( 0 < \zeta < 1 \), se trata de un sistema **subamortiguado**.

# Tipo de respuesta esperada

- La respuesta al escalón presentará **oscilaciones amortiguadas**.
- Estas oscilaciones disminuirán hasta llegar a un estado estable.
- Existirá un sobreimpulso y un tiempo de establecimiento definidos.

# Interpretación física

Este sistema representa, por ejemplo:

- Una masa conectada a un resorte con un amortiguador.
- Si se aplica un esfuerzo repentino, el sistema oscila y luego se estabiliza.


