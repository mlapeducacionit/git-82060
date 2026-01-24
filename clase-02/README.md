# Clase 02 - Git desarrollo colaborativo

## Repaso comando vistos.

> Muestro el estado y área en la que están los archivos

```sh
git status
```

> Marcamos archivos que están en el working directory para posteriormente hacer un commit

```sh
git add class-01/_ref/* # Marco todos los archivos que están dentro de la carpeta _ref
git add . # Este comando me sirve para marcar todos los archivos para luego hacer un commit
```

> Hacemos un commit (Snapshot, instantanea)

```sh
git commit -m "Mensaje descriptivo" # 80 caracteres
```

> Listo timeline de commits (Listado de commits)

```sh
git log --oneline
```

# .gitignore
Es un archivo que me permite indicarle a GIT que no quiero que la carpeta o el archivo sea controlado por GIT

# .gitkeep
Es un archivo que me permite darle seguimiento a una carpeta que quiero sea parte del repo pero que este vacía. 

**Se hace de esta manera porque GIT no versiona carpetas vacías.**

<https://www.campusmvp.es/recursos/post/que-son-los-archivos-gitkeep-en-git.aspx?srsltid=AfmBOopAgwXq8qolbnQNfPXDO2-9Wj7q7SqVgDspc0HQpq1GJJw2MUZz>

# Ver la diferencia entre WD y SA o LR

```sh
git diff
``` 

# Ver más información de un commit 

```sh
git show <HASH>
git show cb20a1a
```

## Recuperar archivos desde el LOCAL REPO

```sh
git restore <nombre-archivo1> <nombre-archivo2>
git restore clase-02/README.md
git restore . # Recupera todos los archivos a la versión actual del LR
```

## Comando para hacer add y commits en un solo paso

**IMPORTANTE**: Solo funciona con archivo que ya estén siendo seguidos por GIT. Si tengo archivos untracked esos archivos cuando haga el comando no se van agregar al Staging Area

```sh
git commit -am "mensaje descriptivo" # -a <---- ADD | -m <----- MENSAJE
``` 