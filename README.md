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

```
# touch privado.txt
# mkdir privada
# vim .gitignore
(INCLUIR IMAGEN 04)
```

## 2.5 CREAR EL TAG V0.1

```
# touch 1.txt
# git add .
# git commit -m "commit ejercicio 2.5"
# git tag -a v0.1 -m "etiqueta ejercicio 2.5"
# git push origin master
```

## 2.6 CREAR UNA RAMA REMOTA V0.2
