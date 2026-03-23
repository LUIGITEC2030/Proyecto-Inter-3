# Informe Proyecto No. 1 Intermedia 3
**Universidad:** Universidad de San Carlos de Guatemala  <br>
**Facultad:** Facultad de Ingeniería  <br>
**Carrera:** Ingeniería en Ciencias y Sistemas  <br>

**Curso:** Matemática Intermedia 3  <br>

**Proyecto No.1** <br>


**Fecha:** 27/03/2026<br>
## Integrantes del equipo

| No | Nombre | Carné | Rol |
|---|---|---|---|
| 1 | Carlos Rolando Barrios Estrada | 202500432 | Coordinador |
| 2 | Nombre integrante | 2025XXXXX | Investigador |
| 3 | Nombre integrante | 2025XXXXX | Diseñador de material |


---
# Introducción
---
# Objetivos
## General:
>Colocar texto<br>

## Específicos:
> 1. Introducción
> 2. Objetivos
> 3. Descripción del tema


---
# Resolución de los problemas

## Problema No. 3
Problema: Con objeto de regular la pesca en los océanos, se han establecido
comisiones internacionales para implementar los controles. Para entender el
efecto de tales controles se han construido modelos matemáticos de poblaciones
de peces. Una etapa en este esfuerzo por crear nuevos modelos incluye la
predicción del crecimiento de un tipo de pez. El modelo de crecimiento de von
Bertalanffy se refleja en la ecuación de Bernoulli.
Dada la ecuación: 
$$\frac{dw}{dt}=\alpha W^{\frac{2}{3}}-\beta W $$
Convertimos esta ecuación diferencial en ecuación diferencial estándar de bernoulli la cual nos queda 
$$\frac{dw}{dt}+\beta W=\alpha W^{\frac{2}{3}} $$
1. Sustitucion
$x=W^{1-\frac{2}{3}} = W^{\frac{1}{3}}$
2. Derivamos 
$\frac{dx}{dt}=\frac{1}{3}W^{\frac{-2}{3}}\frac{dw}{dt}$
3. Despejamos $\frac{dw}{dt}$
$\frac{\frac{dx}{dt}}{\frac{1}{3}W^{\frac{-2}{3}}}=\frac{dw}{dt}$
4. Sustituimos
$\frac{\frac{dx}{dt}}{\frac{1}{3}W^{\frac{-2}{3}}}+\beta W=\alpha W^{\frac{2}{3}}$
5. Multiplicamos por $\frac{1}{3}W^{\frac{-2}{3}}$
6. Obtenemos la nueva ecuación
$\frac{dx}{dt}+\frac{\beta}{3} W^\frac{1}{3}=\frac{\alpha}{3}$
*Sabemos que $X=W^{\frac{1}{3}}$
7. Encontramos el factor de integración
$e^{\int \frac{\beta}{3}\,dt} = e^{\frac{\beta}{3}t}$
8. Multiplicamos por el factor de integracion
$d(e^{\frac{\beta}{3}t}X)=e^{\frac{\beta}{3}t}\frac{\alpha}{3}$
9. Integramos a ambos lados 
$\int d(e^{\frac{\beta}{3}t}X)\,dt$ $=$ $\int e^{\frac{\beta}{3}t}\frac{\alpha}{3}\,dt$
10. Obtenemos los resultados
$e^{\frac{\beta}{3}t}X = \frac{\alpha}{\beta} e^{\frac{\beta}{3}t} + C   $
11. Volvemos a nuestra variable principal
$e^{\frac{\beta}{3}t}W^{\frac{1}{3}} = \frac{\alpha}{\beta} e^{\frac{\beta}{3}t} + C   $

### Cuando $\lim_{t \to \infty} W(t)$
1. Depejamos W y obtenemos
$ W^{\frac{1}{3}} $ $=$  $\frac{\alpha}{\beta} + \frac{C}{e^{\frac{\beta}{3}t}}$
* Sabemos que $\frac{C}{\infty}=0$ por lo que tenemos que: 
$\lim_{t \to \infty} W(t)= (\frac{\alpha}{\beta})^3$
 ### Valores iniciales $W(0)=0$
1. Sabiendo que cualquier numero elevado a la 0 es 1, obtenemos 
$0=\frac{\alpha}{\beta} +C$
Al despejar obtenemos
$C=-\frac{\alpha}{\beta} $
### Depeje de la ecuación a graficar
1. Obtenemos la nueva ecuación
$W =$ $(\frac{\alpha}{\beta} -\frac{\alpha}{\beta} e^{-\frac{\beta}{3}t})^3$
Al graficar obtendremos lo siguiente
![alt text](Imagenes\Graficaproblema3.png)
---

## Problema 4
Problema: Dos sustancias químicas A y B se combinan para formar la sustancia química C.  
La razón de reacción es proporcional al producto de las cantidades instantáneas 
de A y B que no se han convertido en C.  Al principio hay 40 gramos de A y 50 
gramos de B y por cada gramo de B se consumen 2 de A.  Se observa que a los 
cinco minutos se han formado 10 gramos de C.   

### **Teoria Necesaria para resolver este problema**

$ a - \frac{M}{M + N}(x)$ , $ b - \frac{N}{M + N} (x)$ 

**Ley de acción de masas**
$ \frac{dx}{dt}\alpha (a - \frac{M}{M +N}x)(b - \frac{N}{M +N}x)$

### Datos

- $a = 40$ gramos  
- $b = 50$ gramos  
- Relación: $a = 2b$  
- $x(0) = 0$  
- $x(5) = 10$  

---

### Sistema de ecuaciones

$$
\begin{cases}
a + b = 1 \\
a = 2b
\end{cases}
$$

Sustituyendo:

$$
b = 1 - 2b
$$

$$
3b = 1 \Rightarrow b = \frac{1}{3}
$$

$$
a = 2b = \frac{2}{3}
$$

---

### Modelo diferencial

$$
\frac{dx}{dt} \propto \left(40 - \frac{2}{3}x \right)\left(50 - \frac{1}{3}x \right)
$$

Factorizando:

$$
\frac{dx}{dt} = k(60 - x)(150 - x)
$$

---

### Separación de variables

$$
\frac{dx}{(60 - x)(150 - x)} = k \, dt
$$

---

### Fracciones parciales

$$
\frac{1}{(60 - x)(150 - x)} =
\frac{A}{60 - x} + \frac{B}{150 - x}
$$

Resolviendo:

$$
A = \frac{1}{90}, \quad B = -\frac{1}{90}
$$

---

### Integración

$$
\int \left( \frac{1}{90(60 - x)} - \frac{1}{90(150 - x)} \right) dx = \int k \, dt
$$

$$
\frac{1}{90} \ln \left| \frac{150 - x}{60 - x} \right| = kt + C
$$

---

### Condición inicial

$$
x(0) = 0
$$

$$
\frac{1}{90} \ln \left(\frac{150}{60}\right) = C
$$

$$
C = \frac{1}{90} \ln \left(\frac{5}{2}\right)
$$

---

### Ecuación final

$$
\ln \left( \frac{150 - x}{60 - x} \right)
= 90kt + \ln \left(\frac{5}{2}\right)
$$

---

### Encontrando $k$

Usando $x(5) = 10$:

$$
k = \frac{\ln(140/50) - \ln(5/2)}{450}
$$

$$
k \approx 0.000251842
$$

---

### Límite

$$
40 - \frac{2}{3}x = 0 \Rightarrow x = 60
$$

$$
50 - \frac{1}{3}x = 0 \Rightarrow x = 150
$$

$$
x_{\text{máx}} = 60
$$

---

### Comportamiento a largo plazo

$$
A = 0
$$

$$
B = 50 - \frac{1}{3}(60) = 30
$$

---

## b)

Si $A = 100$ gramos:

$$
C_{\max} = 150
$$

La mitad:

$$
x = 75
$$

---

### Nuevo modelo

$$
\frac{dx}{dt} = k(150 - x)^2
$$

Separando:

$$
\frac{dx}{(150 - x)^2} = k \, dt
$$

---

### Integración

$$
\frac{1}{150 - x} = kt + C
$$

Con $x(0)=0$:

$$
C = \frac{1}{150}
$$

---

### Encontrando $k$

$$
x(5) = 10
$$

$$
k \approx 0.000095138
$$

---

### Tiempo cuando $x = 75$

$$
\frac{1}{150 - 75} = kt + \frac{1}{150}
$$

$$
t \approx 70 \text{ minutos}
$$

--
