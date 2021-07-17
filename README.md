---
TITULO: "TAREA 02 PROGRAMACIÓN"
ALUMNO: "LIMAS CERNA ANTONIO JESUS"
CODIGO: 19160180
FECHA: "16/07/2021"
---

## PROBLEMAS/EJERCICIOS

### PARTE 1

**1. Calcula los valores numéricos aproximados de:**

- a. $\frac{0.3*0.15}{0.3*0.15+0.2*0.8+0.5*0.12}$
```{vector}
a <- (0.3*0.15)/(0.3*0.15+0.2*0.8+0.5*0.12) 
round(a,2)
ceiling(a)
```

- b. $\frac{5^{6}}{6!}e^{-5}$
```{vector}
b <- 5^6/factorial(6) * exp(-5)
round(b,2)
ceiling(b)
```

- c. $\binom{20}{7}0.4^{7}0.6^{13}$
```{vector}
c <- factorial(20)/factorial(7)*factorial(13) * 0.4^7 * 0.6^13
ceiling(c)
```

**2. Realizar la siguiente suma**

- a. 1+2+3+...+1000
```{divisibilidad}
d <- 1:1000
sum(d)
```

- b. 1+2+4+8+16...+1024
```{divisibilidad}
e <- (1:1024)^2
f <- 1 + sum(e)
```

**3. El vector _grupo_ representa el grupo al que pertenece una serie de alumnos**

```{vector}
grupo <- c("CUBEN","CARLOS","CATY","ALEJANDRO","ALISA","DOGELIO","ANDREA","CAROLA","ARIA","BERNARDO","CUASIMODO","CHICHO","ANDALIO","ESTEFANO","ERMES","BRILLIT","ANA", "CIRIAM","ALEXIA","ANGELICA","ANASTASIA", "ERLINDA", "ANTONIO", "BESEUS", "CRISTIAN", "EOLO", "AGUSTIN", "BETTO","BIMBO", "DAVID","ELEANOR","DARWIN","COSEFINA","DELIA","ALEXIS", "ATORNALIO","ELMER", "EINNIE", "DORA", "CUIGUI", "BICENZO", "AMON","ELANY","BETTY","AARON","ABIGAIL","ALAMIS","ALBERTO","DEYSI","DANIEL","DIANA", "DENNIS", "DIEGO", "EDUARDO", "ALAIN", "EMILIA", "ELVIS", "ERICK", "ESTEPANHY")
```

- a. ¿Cuántos elementos tiene?
```{divisibilidad}
length(grupo)
```

- b. ¿En qué posiciones del vector está la letra “A”?
```{divisibilidad}
grep("A", grupo)
```

**4. El vector nota representa la nota de un examen de los alumnos que están en los grupos del vector grupo.**

```{vector}
nota <-  c( 10, 4.9, 11, 13.5, 4.7, 3.6,15.2, 13.6, 19.4, 11.6, 20, 12.9,10.4, 12, 13.7, 14.4, 5.8, 1.9, 2,12.7, 11.3, 12.8, 16.2, 15.3, 17.1, 17, 16, 13, 15.6, 3.1, 19.2, 19, 18.4, 18.5, 18, 18.3, 17.9, 11.1, 9.8, 9.2, 8.3, 7.6, 6.5, 5.8, 6.7, 7.5, 1.2, 3.2, 0, 9.2, 11.5, 12, 17.2, 18.6, 16.4, 15.3, 10.1, 10.5, 14.3)
```
 
  - a. ¿Cuanto suman todas las notas?
```{vector}
sum(nota)
```

  - b. ¿Cual es la media aritmética de todas las notas?
```{vector}
media_aritmetica <- sum(nota)/length(nota) mean(nota)
```

  - c. ¿En qué posiciones están las notas mayores de 7.0?
```{vector}
which(nota<7)
```

  - d. Visualiza las notas ordenadas de mayor a meno
```{vector}
nota[order(nota, decreasing = TRUE)]
```

  - e. ¿En qué posición está la nota máxima?
```{vector}
which(nota==max(nota))
```

**5. A partir de los vectores grupo y nota definidos..**

```{vector}
grupo_general <- cbind(grupo, nota)

grupo_A <- c("ALEJANDRO","ALISA","ANDREA","ARIA","ANDALIO","ANA","ALEXIA","ANGELICA","ANASTASIA","ANTONIO","AGUSTIN","ALEXIS","ATORNALIO","AMON","AARON","ABIGAIL","ALAMIS","ALBERTO","ALAIN")
grupo_B <- c("BERNARDO","BRILLIT","BESEUS","BETTO", "BIMBO","BICENZO","BETTY")
grupo_C <- c("CUBEN","CARLOS","cATY","CAROLA","CUASIMODO","CHICHO","CIRIAM","CRISTIAN","COSEFINA","CUIGUI")
grupo_D <- c("DOGELIO","DAVID","DARWIN","DELIA","DORA","DEYSI","DANIEL","DIANA", "DENNIS", "DIEGO")
grupo_E <- c("ESTEFANO","ERMES","ERLINDA","EOLO","ELEANOR","ELMER", "EINNIE","ELANY","EDUARDO",
             "EMILIA","ELVIS","ERICK","ESTEPANHY")

nota_A <- c(13.5,15.2,19.4,10.4,5.8,2,12.7,11.3,16.2,16,18, 18.3,7.6,6.7,7.5,1.2,3.2,16.4,15.3)
nota_B <- c(11.6,14.4,15.3, 13, 15.6,8.3,5.8)
nota_C <- c(10,4.9,11,13.6,20,12.9,1.9,17.1,18.4,9.2)
nota_D <- c(3.6,3.1,19,18.5,9.8,0, 9.2, 11.5, 12, 17.2)
nota_E <- c(12,13.7,12.8,17,19.2,17.9, 11.1, 6.5,18.6,15.3,10.1, 10.5,14.3)
```

 - a. Suma las notas de los 10 primeros alumnos del vector
```{df}
g <- grupo_general[1:10,2]
sum(g)
```

  - b. ¿Cuántos alumnos hay del grupo C?
```{df}
length(grupo_C)
```

  - c. ¿Cuántos alumnos han aprobado?
```{df}
h <- nota[nota>10.5]
length(h)
```

  - d. ¿Cuántos alumnos del grupo B han aprobado?
```{df}
i <- nota_B[nota_B>10.5]
length(i)
```

  - e. ¿Qué porcentaje de alumnos del grupo C han aprobado?
```{df}
nota_aprob_C <- nota_C[nota_C>10.5]
grupo_aprob_C <- c("cATY","CAROLA","CUASIMODO","CHICHO","CRISTIAN","COSEFINA")

df_C <- data.frame(grupo_aprob_C, nota_aprob_C)

df$prob <- prop.table(df_C$nota_aprob_C)

df$porcentaje <- round(prop.table(df_C$nota_aprob_C), 6)*100
```

 - f. ¿De qué grupos son la máxima y mínima notas de toda la muestra?
```{df}
max(nota)
min(nota)
```

**6. Calcula el percentil 66 de:r**

 - a. Las notas de todos los alumnos
```{vector}
quantile(nota, 0.66)
```

 - b. De los alumnos del grupo C
```{vector}
quantile(nota_C, 0.66)
```

**7. Un alumno tiene una nota de 4.9**

 - a. ¿Qué porcentaje, del total de alumnos, tiene una nota menor o igual que la suya?
```{vector}
nota_menor <- nota[nota<=4.9]
grupo_menor <- c("CARLOS","ALISA","DOGELIO","CIRIAM","ALEXIA","DAVID","ALAMIS","ALBERTO","DEYSI")

df_menor <- data.frame(grupo_menor, nota_menor)

df$prob <- prop.table(df_menor$nota_menor)

df$porcentaje <- round(prop.table(df_menor$nota_menor), 9)*100
```
 
 - b. ¿Y qué porcentaje tiene una nota mayor o igual que la suya?
```{vector}
nota_mayor <- nota[nota>=4.9]
grupo_mayor <- c("CUBEN","CARLOS","cATY","ALEJANDRO","ANDREA","CAROLA","ARIA","BERNARDO","CUASIMODO","CHICHO","ANDALIO","ESTEFANO","ERMES","BRILLIT","ANA","ANGELICA","ANASTASIA","ERLINDA","ANTONIO","BESEUS","CRISTIAN","EOLO","AGUSTIN","BETTO","BIMBO","ELEANOR","DARWIN","COSEFINA","DELIA","ALEXIS","ATORNALIO","ELMER","EINNIE","DORA","CUIGUI","BICENZO","AMON","ELANY","BETTY","AARON","ABIGAIL","DANIEL","DIANA","DENNIS","DIEGO","EDUARDO","ALAIN","EMILIA","ELVIS","ERICK","ESTEPANHY")

df_mayor <- data.frame(grupo_mayor, nota_mayor)

df$prob <- prop.table(df_mayor$nota_mayor)

df$porcentaje <- round(prop.table(df_mayor$nota_mayor), 51)*100
```

**8.Realiza el gráfico de diagramas de caja de las notas de cada grupo, para poder comparar el nivel de cada uno de ellos.**

```{df}
df <- data.frame(grupo, nota)
boxplot(x = nota)
```


### PARTE 2

**1. Graficar los puntos (1,1), (2,4), (3,6), (4,8), (5,25), (6,36), (7,49), (8,64), (9,81), (10,100) en un plano utilizando RStudio**

```{plot}
x <- seq(1:10)
y <- x^2

plot (x, y, "l")
```

**2.  Ingresar la matriz A en RStudio**
```{matrix}
k <- (1:4)
l <- 2*k
m <- 3*k

matriz_A <- cbind(k,l,m)
```

**3. Ingresar la matriz identidad de tamaño 3.**

```{matrix}
matriz_I <- diag(3)
```

**4. Crea una función que cree una matriz nula ingresando las dimensiones**

```{matrix}
n <- rep(0,16)
o <- matrix(n, ncol = 4)
```

**5. Modificar la matriz diag(4), para que se parezca a la matriz B.**

```{matrix}
matriz_B <- diag(4)
matriz_B[1,1]=0
matriz_B[2,2]=2
matriz_B[3,3]=3
matriz_B[4,4]=4
```

**6. Obtener la matriz transpuesta de A (ejercicio 2)**

```{matrix}
t(matriz_A)
```

**7. Realizar las siguientes operaciones:**

 - a. A+B
```{matrix}
A+B <- (matriz_A+matriz_B)
```
 
 - b. A-B
```{matrix}
A-B <- (matriz_A-matriz_B)
```

 - c. 3B
```{matrix}
"3B" <- 3*matriz_B
```

 - d. AB
```{matrix}
AB <- matriz_A*matriz_B
```

**8.Crea una función para calcular $P^{6}$**

```{matrix}
p <-function(M,n){S=M;
for(i in 2:n){S=S%*%M};
print(S)}
P<-matrix(c(1,-2,1,2,4,0,3,-2,1), ncol=3, nrow=3)
p (P,6)
```

**9. Resolver el sistema de ecuaciones:**
**3x - y + z = -1**
**9x - 2y + z = -9**
**3x + y - 2z = -9**
```{matrix}
q <- matrix(c(3,9,3,-1,-2,1,1,1,-2), ncol=3,nrow=3)
r <-c(-1,-9,-9)
solve(q,r)
```

**10. Utilizando la ayuda de R, investigue para qué sirven las funciones eigen() y det()**

```{conceptos}
eigen(): Calcula autovalores y autovectores de matrices 
         numéricas (dobles, enteras, lógicas) o complejas.
det(): Viene a ser el determinante de una matriz.

```
