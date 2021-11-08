# Manipulación Avanzada en Git
## Indice
- **[Ejercicio 1](#ejercicio-1)**
- **[Ejercicio 2](#ejercicio-2)**
- **[Ejercicio 3](#ejercicio-3)**
- **[Ejercicio 4](#ejercicio-4)**
- **[Ejercicio 5](#ejercicio-5)**
- **[Ejercicio 6](#ejercicio-6)**
- **[Ejercicio 7](#ejercicio-7)**
- **[Ejercicio 8](#ejercicio-8)**
- **[Ejercicio 9](#ejercicio-9)**
## Ejercicio 1
Para el primer ejercicio lo primero que realizaremos es mostrar el historial de los cambios realizados en el repositorio con el comando **“git log”**.

<img src="img/1.png">

Luego crearemos una carpeta , la cual llamaremos capítulos con el comando **“mkdir capitulos”**, y dentro de esta carpeta creamos el fichero capítulo1.txt con el comando **“cat > capitulo1.txt”**.

<img src="img/2.png">

Tras esto añadiremos los cambios a la zona de intercambio con el siguiente comando: **“git add .”**.

<img src="img/3.png">

Después de esto hacemos un commit de los cambios realizados con un mensaje con el comando **“git commit -m "Añadido capítulo 1."”**.

<img src="img/4.png">

Cuando hayamos hecho todo volveremos a revisar el historial con el comando **“git log”**.

<img src="img/5.png">

## Ejercicio 2
En este ejercicio creamos un nuevo fichero que llamaremos capitulo2.txt, para ello usaremos **“cat > capitulos/capitulo2.txt”**.

<img src="img/6.png">

Lo añadimos a la zona de intercambio temporal con el comando **“git add .”**.

<img src="img/7.png">

A continuación, realizaremos un commit de los cambios realizados recientemente con el comando **“git commit -m "Añadido capítulo 2."”**.

<img src="img/8.png">

Finalmente mostraremos la diferenciencia entre al últimas versión y las dos versiones anteriores a esta con el comando **“git diff HEAD~2..HEAD”**.

<img src="img/9.png">

## Ejercicio 3
Como en los anteriores ejercicios, crearemos un nuevo fichero llamado capitulo3.txt con el comando **“cat > capitulos/capitulo3.txt”**.

<img src="img/10.png">

Ahora realizaremos un **“git add”** para añadir los cambios a la zona de intercambio temporal.

<img src="img/7.png">

Volvemos a hacer un commit, como en ejercicios anteriores, con el comando **“git commit -m "Añadido capítulo 3."”**.

<img src="img/11.png">

Para finalizar, mostraremos los cambios realizados entre el primer y el último repositorio. Primeramente usaremos el comando **“git log”** para poder copiar el código hash de la primera versión, el cual nos servirá para el siguiente comando, **“git diff <código hash de la primera versión>..HEAD”**.

<img src="img/12.png">

<img src="img/13.png">

## Ejercicio 4
Creamos, primeramente, un nuevo txt que se llame indice.txt con el comando **“cat > indice.txt”**.

<img src="img/14.png">

Lo añadimos a la zona de intercambio temporal tras su creación **“git add .”**.

<img src="img/7.png">

Haremos un commit de la creación del fichero con el comando **“git commit -m "Se crea el índice."”**.

<img src="img/15.png">

A continuación, añadiremos un texto al fichero indice.txt de la siguiente manera: **“echo "Indice de los capítulos, con conceptos avanzados de git" >> indice.txt”**.

<img src="img/16.png">

Añadimos esto último a la zona de intercambio temporal con **“git add .”**.

<img src="img/7.png">

Ahora haremos un commit en el que se añade el cambio en el fichero de índice **“git commit -m "Añadido el índice."”**.

<img src="img/17.png">

Finalmente, mostraremos quien ha hecho los cambios y el cambio que se ha realizado con el comando **“git annotate indice.txt”**.

<img src="img/18.png">

## Ejercicio 5
En este ejercicio crearemos una nueva rama llamada bibliografía para ello usaremos el comando **“git branch bibliografia”**.

<img src="img/19.png">

Finalmente para comprobar las ramas que tenemos actualmente usaremos el comando **“git branch -av”**.

<img src="img/20.png">

## Ejercicio 6
Crearemos un nuevo fichero llamado capitulo4.txt con el comando **“cat > capitulos/capitulo4.txt”**.

<img src="img/21.png">

Añadimos los cambios a la zona de intercambio temporal con **“git add .”**.

<img src="img/7.png">

Haremos un commit con el comando **“git commit -m "Añadido capítulo 4."”**.

<img src="img/22.png">

Finalmente mostraremos la historia del repositorio en el que se incluyen todas las ramas con el comando **“git log --graph --all --oneline”**.

<img src="img/23.png">

## Ejercicio 7
Ahora nos cambiamos a la rama de bibliografía con el comando **“git checkout bibliografia”**.

<img src="img/24.png">

A continuación, creamos el fichero bibliografia.txt con el comando **“cat > bibliografia.txt”**.

<img src="img/25.png">

Luego lo añadimos a la zona de intercambio temporal con **“git add .”**.

<img src="img/7.png">

Lo siguiente que haremos es un commit con el siguiente comando **“git commit -m "Añadida primera referencia bibliográfica."”**.

<img src="img/26.png">

Finalmente, mostraremos la historia del repositorio en todas las ramas con el comando **“git log --graph --all --oneline”**.

<img src="img/27.png">

## Ejercicio 8
En el siguiente ejercicio vamos a fusionar la rama bibliografía, creada anteriormente, con la rama master, todo esto con el comando **“git checkout master”** y **“git merge bibliografia”**.

<img src="img/28.png">

<img src="img/29.png">

Luego de esto  mostramos la historia del repositorio en todas las ramas mediante **“git log --graph --all --oneline”**.

<img src="img/30.png">

Después eliminamos la rama de bibliografía con el comando **“git branch -d bibliografia”**.

<img src="img/31.png">

Tras eliminar bibliografía volveremos a comprobar la historia del repositorio con **“git log --graph --all --oneline”**.

<img src="img/32.png">

## Ejercicio 9
Para este último ejercicio comenzaremos creando la rama bibliografía, otra vez, esto con el comando **“git branch bibliografia”**.

<img src="img/33.png">

Nos colocamos en la rama bibliografía con el comando **“git checkout bibliografia”**.

<img src="img/34.png">

Luego, estando ya en la rama bibliografía, creamos el fichero bibliografia.txt mediante la siguiente sentencia **“cat > bibliografia.txt”**.

<img src="img/35.png">

A continuación, realizaremos el primer commit del ejercicio con el comando  **“git commit -a -m "Añadida nueva referencia bibliográfica."”**.

<img src="img/36.png">

Ahora nos cambiamos de rama y nos moveremos a la rama master de la siguiente forma **“git checkout master”**.

<img src="img/37.png">

En esta rama creamos un fichero igual que el anterior bibliografia.txt pero le cambiaremos su contenido.

<img src="img/38.png">

Realizamos un commit de los cambios recientes con **“git commit -a -m "Añadida nueva referencia bibliográfica."”**.

<img src="img/39.png">

Luego fusionamos la rama master con la rama bibliografía con el comando **“git merge bibliografia”**.

<img src="img/40.png">

Nos sale que hay conflicto con el fichero de bibliografia.txt, para solucionar editaremos su contenido con **“sudo nano bibliografia.txt”** y pondremos el mismo contenido en ambos.

<img src="img/41.png">

Haremos un commit al solucionarlo **“git commit -a -m "Solucionado conflicto bibliografía."”**.

<img src="img/42.png">

Para finalizar mostraremos la historia del repositorio en todas las ramas **“git log --graph --all --oneline”**.

<img src="img/43.png">
