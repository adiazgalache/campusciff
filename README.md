# EJERCICIOS GIT, GITHUB Y MARKDOWN
Alejandro Diaz Galache

## 2.1 REPOSITORIO CAMPUSCIFF
Creamos el repositorio de trabajo en GitHub. Aprovechamos la operación para generar el fichero README.md.
(INCLUIR IMAGEN)

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
(INCLUIR IMAGEN 02)
# git push origin master
```

## 2.4 IGNORAR ARCHIVOS

Generamos el fichero y directorio a omitir. Posteriormente configuramos el fichero .gitignore

```
# touch privado.txt
# mkdir privada
# vim .gitignore
```

## 2.5 CREAR EL TAG V0.1

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

Creamos una rama remota v0.2 en Github
(IMAGEN 05)

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
(IMAGEN 06)

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

(IMAGEN 07)

Listamos las ramas con merge (--merged) y sin merge (--no-merged)

```
# git branch --merged
# git branch --no-merged
```

(IMAGEN 08)

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

(IMAGEN 09)

Borramos rama v0.2

```
# git branch -d v0.2
```

(IMAGEN 10)

## 2.10 CUENTA DE GITHUB

Procedemos a configurar la cuenta github:

(IMAGEN 11)

Configuración del doble factor de autentificación via SMS:

(IMAGEN 12)

Y por último añadimos la clave pública del pc desde el que conectamos:

(IMAGEN 13)

## 2.11 USO SOCIAL DE GITHUB

## 2.12 CREAR TABLA

A continuación la tabla con 3 compañero de clase:

Nombre | Github
------- | -------
macarenagaranena | http://github.com/macarenagarena 
Miriam-Asenjo | http://github.com/Miriam-Asenjo
Danielobit | http://github.com/Danielobit

## 2.13 COLABORADORES

Añadimos a asanzdiego como colaborador.

## 2.14 CREAR UNA ORGANIZACIÓN

campusciff-adiazgalache

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

 
