# EJERCICIOS GIT, GITHUB Y MARKDOWN
Alejandro Diaz Galache

> La práctica completa esta realizada sobre un entorno virtual montado con sistema operativo Linux distribución Ubuntu 14.04.

## 2.1 REPOSITORIO CAMPUSCIFF
Creamos el repositorio de trabajo en GitHub. Aprovechamos la operación para generar el fichero README.md.

![Repositorio Github](https://github.com/adiazgalache/campusciff/blob/master/img/01.png)

Clonamos ahora en local.

```
# cd ~
# mkdir practica
# cd practica
# git init
# git remote add campusciff git@github.com:/adiazgalache/campusciff.git
# git remote -v
# git clone git@github.com:/adiazgalache/campusciff.git

```
## 2.2 README
Al crear el repositorio remoto campusciff, ya incluimos el fichero README.md, por tanto durante la clonación del mismo ya hemos disponibilizado el fichero en nuestro repositorio local de trabajo.

## 2.3 COMMIT Y PUSH INICIAL

```
# git add .
# git commit -m "commit inicial"
# git push origin master
```

![Primer Commit](https://github.com/adiazgalache/campusciff/blob/master/img/02.png)


![Primer Push](https://github.com/adiazgalache/campusciff/blob/master/img/03.png)

## 2.4 IGNORAR ARCHIVOS

Generamos el fichero y directorio a omitir. Posteriormente configuramos el fichero .gitignore

```
# touch privado.txt
# mkdir privada
# vim .gitignore
```

El contenido del fichero .gitignore:

![Fichero .gitignore](https://github.com/adiazgalache/campusciff/blob/master/img/04.png)

## 2.5 CREAR EL TAG V0.1

Creamos un fichero en 1.txt sin contenido y subimos los cambios al repositorio remoto.

```
# touch 1.txt
# git add .
# git commit -m "commit ejercicio 2.5"
# git tag -a v0.1 -m "etiqueta ejercicio 2.5"
# git push origin master
```

Empujamos tag v0.1 a repositorio remoto

```
# git tag
# git push origin v0.1
```

## 2.6 CREAR UNA RAMA REMOTA V0.2

Creamos y cambiamos de rama a v0.2

```
# git checkout -b v0.2
# git branch -v
```

Creamos fichero 2.txt y subimos cambios a la rama v0.2

```
# touch 2.txt
# git add .
# git commit -m "commit ejercicio 2.6"
# git push origin v0.2
```

## 2.7 MERGE DIRECTO

Posicionados en el branch master hacemos un merge de v0.2

```
# git checkout master
# git merge v0.2
```

![Merge directo](https://github.com/adiazgalache/campusciff/blob/master/img/06.png)

## 2.8 MERGE CON CONFLICTO

Realizamos una modificación sobre fichero 1.txt en rama master.

```
# echo "Hola" > 1.txt
# git commit -a -m "commit ejercicio 2.8 sobre master"
```

De la misma manera, realizamos una modificación sobre el fichero 1.txt pero esta vez desde la rama v0.2

```
# git checkout v0.2
# echo "Adios" > 1.txt
# git commit -a -m "commit ejercicio 2.8 sobre rama v0.2"
```

Nos posicionamos de nuevo en rama master y mergeamos provocando el conflicto.

```
# git checkout master
# git merge v0.2
```

![Merge con conflicto](https://github.com/adiazgalache/campusciff/blob/master/img/07.png)

Listamos las ramas con merge (--merged) y sin merge (--no-merged)

```
# git branch --merged
# git branch --no-merged
```

![merged y no merged](https://github.com/adiazgalache/campusciff/blob/master/img/08.png)

Solucionamos el conflicto

```
# echo -e "Hola\nAdios" > 1.txt
# git commit -a -m "commit ejercicio 2.8 sobre rama master arregla conflicto"
# git checkout v0.2
# echo -e "Hola\nAdios" > 1.txt
# git commit -a -m "commit ejercicio 2.8 sobre rama v0.2 arregla conflicto"
# git checkout master
```

## 2.9 BORRAR RAMA

```
# git tag v0.2
# git list
``` 

![salida git list](https://github.com/adiazgalache/campusciff/blob/master/img/09.png)

Borramos rama v0.2

```
# git branch -d v0.2
```

![salida git branch -d](https://github.com/adiazgalache/campusciff/blob/master/img/10.png)

## 2.10 CUENTA DE GITHUB

Procedemos a configurar la cuenta github:

![configuracion github profile](https://github.com/adiazgalache/campusciff/blob/master/img/11.png)

Configuración del doble factor de autentificación via SMS:

![configuracion github auth](https://github.com/adiazgalache/campusciff/blob/master/img/12.png)

Y por último añadimos la clave pública del pc desde el que conectamos:

![configuracion github ssh keys](https://github.com/adiazgalache/campusciff/blob/master/img/13.png)

## 2.11 USO SOCIAL DE GITHUB

## 2.12 CREAR TABLA

A continuación la tabla con 3 compañero de clase:

Nombre | Github
------- | -------
macarenagaranena | http://github.com/macarenagaranena 
Miriam-Asenjo | http://github.com/Miriam-Asenjo
Danielobit | http://github.com/Danielobit

## 2.13 COLABORADORES

Añadimos a asanzdiego como colaborador.

## 2.14 CREAR UNA ORGANIZACIÓN

Desde GitHub creo la orgcampusciff-adiazgalache.

## 2.15 CREAR EQUIPOS



## 2.16 CREAR UN INDEX.HTML

Hemos creado un repositorio para soportar la organización campusciff-adiazgalache. Posteriormente clonamos en nuestro directorio de trabajo en local para poder crear el index.html.

```
# echo "Organization campusciff-adiazgalache" > index.html
# git add .
# git commit -m "primer commit en organización"
# git push origin master
```

Este es el enlace resultante de la organización: [pincha aqui](http://campusciff-adiazgalache.github.io.)

## 2.17 CREAR PULL-REQUEST

Realizo un fork a los siguientes repositorios:

- Danielobit/campusciff-2015-1.github.io
- campusciff-Miriam-Asenjo/campusciff-Miriam-Asenjo.github.io

Creo los branch "cambioalex" asociados a las copias y realizo los cambios en los index.html antes de las operaciones pull request.

(IMAGEN 15)

Realizamos los pull request sobre los repositorios contribuidos de los compañeros.

## 2.18 GESTIONAR PULL REQUEST

Gestionados.
