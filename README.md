# TUTORIAL DE GIT

Este es un resumen básico de todos los coceptos de git.

Git es un programa para versionar código

Git es un sistema de control distribuido a diferencia de SVN que era centralizado

### Git es distribuido

Cada desarrollador tiene una copia del código y el historial de las versiones en su maquina.

### Configuración de Git

```console
git config --global user.name "Rafael Ortiz"
git config --global user.email "infoman.rafael@gmail.com"
```

## Nota: Para cambiar de usarios de Git en Windows 10 se debe ir al Administrador de Contraseñas

Para ver como se tiene configurado, se escribe:

```console
git config --list
```
### Archivo .gitignore

Si se desea que algun alrchivo no se encuentre en el repositorio, se crea un archivo **gitignore**

Si queremos que el repositorio no incluya un archivo especifico
```
prueba.php
```
Si queremos que todos los archivo jpg no esten incluido en el repositorio
```
*.jpg
```
Si queremos que todo un directorio no este en el repositorio
```
imagenes/*
```
### Editor vim

Podemos editar un documento desde la linea de comandos, con el editor **vim**
```console
vim .gitignore
```
- **:q** -> Para salir
- **:w** -> Para Guardar
- **:q!** -> Para salir sin guardar
- **Esc** -> Para cambiar de modo

Para crear un archivo se puede hacer de la siguiente forma:
```console
touch documento.txt
```
 ### Etapas de Git

Un proyecto puede estar en tres etapas:

1. **Working directory** Que es el directorio donde se encuentra trabajando el desarrollador.
2. **Staging**
3. **Repositorio** El lugar donde esta subido el código, historial.

Para agregar los archivos que están "untracked" en el **stagging area**, escribimos el siguiente comando:

```console
git add -A
```

Si queremos quitar un archivo del stagging area, digitamos el siguiente comando:

```console
git rm --cached .gitignore
```
Ahora si solo queremos agregar ese archivo digitamos el siguiente comando

```console
git add .gitignore
```
Pasamos los archivos al repositorio:

```console
git commit -m "Estos son mis primero archivos"
```
Ahora si se quiere ver el historial de todos los "commits" que se realizarón:

```console
git log
```

## Branches

La ramas o branches permiten que el usuario crear un rama alterna a la rama principal **master** en la cual cada desarrollador puede trabajar en sus propias modificaciones.

Para crear una branch se escribe el siguiente comando

```console
git branch miNuevaRama
```
Para ver todas las branch, se escribe el siguiente comando

```
git branch
```

Para subir el cambio a una nueva branch, se escribe el siguiente comando:

```console
git push -u origin mNuevaRama
```

Para ver todas las branch locales y remotas

```console
git branch -a
```

Para cambiar de branch

```console
git checkout master
```

Para obtener la **ultima versión**:

## Unir los branches al master

Primeramente si se encuentra en cualquier otra rama, debe irse a la rama **master**

```console
git checkout master
```
Bajarse la última version de la rama master con:

```console
git pull origin master
```
Para ver las branch que hemos mergeado hasta ahora, ejecutamos el siguiente comando:

```
git branch --merged
```
Ahora hacemos la union con la branche **master**

```
git merge miNuevaRama
```
Ahora subimos al servidor

```console
git push origin master
```
Para eliminar la branch , se ejecuta el siguiente comando:

```console
git push origin --delete miNuevaRama
```

Para eliminar la branch de mi local ejecutamos:

```console
git branch -d miNuevaRama
```

Para copiarnos el cambio de master a la otra rama seguimos los siguientes pasos:

1. Con el comando **git log** copiamos el id de la modificación que llevaremos a la otra rama
2. ingresamos a la rama correspondiente con **git checkout**
3. Luego ingresamos el siguiente comando con el id de la modificación:

```console
git cherry-pick 4f0fa46a721b9eb1da6 
```
4. Finalmente con el comando **git log** verificamos que id de la modificación este dentro de la rama.















