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

```

```




