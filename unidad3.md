# 3️⃣UNIDAD 3📚

---

---

## 🧬 MODULARIDAD 📦 ##
### 📥 Pase de parámetros por valor 🛡️ ###

El paso de parámetros por valor es una forma de enviar información a una función en programación. Su característica principal es que se crea una copia de los datos.

#### 💡Ejemplo: ####
##### Código Fuente en C

```
#include <stdio.h>

void aumentarEnergia(int nivel) {
    nivel = nivel + 50; 
    printf("Dentro de la funcion: %d \n", nivel);
}

int main() {
    int miEnergia = 10;

    printf("Antes de la funcion: %d\n", miEnergia);

    aumentarEnergia(miEnergia);

    printf("Despues de la funcion: %d\n", miEnergia);
    printf("(El 10 no cambio porque solo enviamos una copia)\n");

    return 0;
}

```
> Cuadro de código 1: Aumentar Energia

##### 📝 Pruebas de ecritorio 

<div align="center">
  <img src="https://cdn.discordapp.com/attachments/1347778788964040717/1466300331800395969/image.png?ex=697c3e19&is=697aec99&hm=72ee2ca10874120aa00fe77e1f267b7d6de20f424fd3ffd7ab912b48884d4375&" width="350">
</div>

> Fig. 1 Pruebas de escritorio en la terminal de C

##### 📢 Explicación Del Código

El códigp presenta  datos basados en una escala de energía utilizando una funcion void para "aumentar" el nivel de energia, mientras que en el main, el nivel de energia ya fue establecido y se lo imprime primeramente, mientras que despues de invocar la función solo nos imprime una copia de el valor que fue otorgado al comienzo en la función void.

---

### 🔑 Pase de parámetros por referencia 🔗 ###

A diferencia del paso por valor (donde mandas una copia), en el paso por referencia le das a la función el acceso directo a la variable original. En lugar de pasarle el contenido, le pasas la dirección de memoria.

#### 💡Ejemplo: ####
##### Código Fuente en C

```
#include <stdio.h>

void aumentarEnergia(int *nivel) {
    *nivel = *nivel + 50;
    printf(" Modificado a: %d \n", *nivel);
}

int main() {
    int miEnergia = 10;

    printf("1. Antes de la funcion: %d\n", miEnergia);

    aumentarEnergia(&miEnergia);

    printf("2. Despues de la funcion: %d\n", miEnergia);
    printf("   (El valor original SI cambio)\n");

    return 0;
}


```
> Cuadro de código 2: Aumentar Energia - Pase de valores por referencia

##### 📝 Pruebas de ecritorio 

<div align="center">
  <img src="https://cdn.discordapp.com/attachments/1347778788964040717/1466305295704658173/image.png?ex=697c42b9&is=697af139&hm=35bc71a608325a77efb84a0f0fac6d8203899743ea0df87fa42dc1de63854256&" width="250">
</div>

> Fig. 2 Pruebas de escritorio en la terminal de C

##### 📢 Explicación Del Código

El código presenta una función que  permite aumentar el nivel de energia y se nota que usamos paso de valores por referencia cuando usamos punteros para acceder a la direccion de la variable. Por lo que primero imprimimos el valor dado primeramente en el main, y luego accedemos a la variable para que la modifique.

---

## 🗓️ ARREGLOS 🔢 ##
### 🧱 Arreglos Unidimensionales -- Vectores ###

Comúnmente llamados Vectores (o arrays), son una estructura de datos que permite almacenar un conjunto de elementos del mismo tipo bajo un solo nombre. Poseen una sola fila y varias columnas; para contabilizar sus posiciones se empieza siempre desde el número 0.

#### 💡Ejemplo: ####
##### Código Fuente en C

```
#include <stdio.h>

int main() {
    float voltajes[4] = {4.2, 3.8, 4.0, 3.5};

    printf("El primer voltaje es: %.1f V \n", voltajes[0]);

    voltajes[2] = 4.1; 
    
    printf("Voltaje 3 actualizado: %.1f V \n", voltajes[2]);

    return 0;
}
```
> Cuadro de código 3: Variabilidad de Valores de voltaje, mediante arreglo Unidimensional

##### 📝 Pruebas de ecritorio 

<div align="center">
  <img src="https://cdn.discordapp.com/attachments/1347778788964040717/1466308334855655465/image.png?ex=697c458d&is=697af40d&hm=8cee54b4ca233ea74734899e41cee0aca3e85a641031884f55419b5fb5cd0015&" width="200">
</div>

> Fig. 3 Pruebas de escritorio en la terminal de C

##### 📢 Explicación Del Código

El código presente muestra un arreglo con 4 valores de voltaje, y primero imprimimos el primer valor del arreglo, teniendo en cuanta que para invocar ese valor, usamos el conteo por posicion el cual se inicializa en 0, luego modificamos el tercer valor del arreglo y lo imprimimos.

---

### 🧱 + 🧱 Arreglos Bidimensionales -- Matrices ###

Los Arreglos Bidimensionales (conocidos como Matrices) son una cuadrícula o tabla organizada en filas y columnas, las cuales presentan cualquier numero de filas y columnas; para contabilizar sus posiciones se empieza siempre desde el número 0.

#### 💡Ejemplo: ####
##### Código Fuente en C

```
#include <stdio.h>

int main() {

    int matriz[2][3] = {
        {10, 20, 30}, 
        {40, 50, 60}  
    };

    printf("Valor en la posicion [1][1]: %d \n", matriz[1][1]);

    
    matriz[0][2] = 100; 

    printf("Valor en la posicion [0][2]: %d \n", matriz[0][2]);

    return 0;
}

```
> Cuadro de código 4: Cambio de valores en matrices

##### 📝 Pruebas de ecritorio 

<div align="center">
  <img src="https://cdn.discordapp.com/attachments/1347778788964040717/1466310812506521651/image.png?ex=697c47dc&is=697af65c&hm=79ae2bad6a9062620638d5f9e60e10d3d26354550c58597dda7e59b9c55c03e7&" width="200">
</div>

> Fig. 4 Pruebas de escritorio en la terminal de C

##### 📢 Explicación Del Código

El código establece una matriz en la cual accedemos a la ubicacion [1][1] la cual en terminos de la matriz seria la segunda fila y segunda columna; asi mismo intercambiamos el numero en otra posicion de la matriz y lo imprimimos.

---

### 🧱 + 🧱 + 🧱 Arreglos Tridimensionales  ###

Imagina una pila de matrices, una encima de otra. Para encontrar un valor, ahora necesitas tres coordenadas: profundidad (capa o página), fila y columna. Tal y como un cubo de datos; ; para contabilizar sus posiciones se empieza siempre desde el número 0.

#### 💡Ejemplo: ####
##### Código Fuente en C

```
#include <stdio.h>

int main() {

    int edificio[2][3][2] = {
        { 
            {20, 21}, 
            {22, 23}, 
            {24, 25}  
        },
        { 
            {18, 19}, 
            {17, 16}, 
            {15, 14}  
        }
    };

    printf("Temperatura: %d grados centigrados \n", edificio[1][2][0]); 

    return 0;
}

```
> Cuadro de código 5: Temperatura en un edificio

##### 📝 Pruebas de ecritorio 

<div align="center">
  <img src="https://cdn.discordapp.com/attachments/1347778788964040717/1466313231940325591/image.png?ex=697c4a1d&is=697af89d&hm=ef7b0bed2cf67dd1967986c8c724a2ce8e63e2fbcf2ab70b3077e7f781eb63ae&" width="300">
</div>

> Fig. 5 Pruebas de escritorio en la terminal de C

##### 📢 Explicación Del Código

El código nos muestra el arreglo con 2 capas, 3 filas y 2 columnas de las cuales se les asigno valores tal y como si fueran edificios, cada posicion seria un lugar distinto donde una temperatura distinta se ejecuta, para luego imprimir la temperatura de un lugar ben especifico.

---

## ⚠️ PRINCIPALES DIFICULTADES EN LA APLICACIÓN DE LOS CONTENIDOS ##

La principal dificultad que me he dado cuenta en esta unidad es como se manejan los punteros en el pase de parametros por referencia, ya que al principo no sabia cuando y donde eran necesarios ejecutarlos, para una mayor eficiencia en el código.

---

## 🧠 REFLEXIÓN CRÍTICA DE LOS APRENDIZAJES DE LA UNIDAD ##

Los aprendizajes de esta unidad fueron verdaderamente utiles ya que nos ayudan a ser mas eficientes en cuanto a la creacion de codigo, siendo mas ordenados y pudiendo analizar el codigo por estructuras para  facilitar el trabajo y ademas los arreglos que nos ayudan a mantener una estructura ordenada en la cual se puede acceder de manera util.

---

## 📎 Anexos 📚 ## 

📌 [Ejercicios Unidad 3](https://drive.google.com/drive/folders/1qMWMG3ggJEW1uPXbbFtdflxKgM89s9MG?usp=sharing)

---

<p align="right">
  <a href="index.md">Volver a la página principal</a>
</p>
