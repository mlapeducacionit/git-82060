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