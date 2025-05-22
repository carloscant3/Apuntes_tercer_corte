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








# 12 de mayo




# 16 de mayo


# 19 de mayo

# Sistema de segundo orden
