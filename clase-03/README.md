# Clase 03 - Git desarrollo colaborativo

## RAMAS (Branches)

### Crear ramas

```sh
git branch <nueva-rama>
git branch feature/branches
```

### Listar ramas

```sh
git branch
```

### Crear rama y moverme a la rama creada

```sh
git switch -c <nombre-rama>
git switch -c feature/navbar
```

### Movernos entre las últimas 2 ramas ciclicamente

```sh
git switch -
```

### Eliminar una rama que no haya tenido cambios

```sh
git branch -d <nombre-rama>
git branch -d feature/navbar
```

### Eliminar una rama que tenga cambios que no estén en el resto del proyecto
Borro una rama de manera forzada

```sh
git branch -D <nombre-rama>
git branch -D feature/navbar
```

### Subir una rama al remoto

```sh
git push <remoto> <nombre-rama>
git push origin features/branches
```

### Descargar toda la metadata del remoto (Actualizar la carpeta .git local)

```sh
git fetch
```

### Listar ramas locales y remotas

```sh
git branch -a
```

### Listar ramas locales y remotas con detalle

```sh
git branch -av
```

# Alias en GIT

```sh
git config --global alias.ll "log --oneline --all --decorate --graph"
git config --global alias.l "log --oneline"
git config --global alias.s "status"
git config --global alias.ss "status --short"
```

## Listar configuraciones y alias

```sh
git config --global --list
``` 

## Borrar alias

```sh
git config --global --unset alias.sc
```

# Empezando con fusiones (juntar 2 ramas)
Voy a poder funsionar 2 o más ramas entre si para llevar los cambios de una rama origen a la destino.

## Trabajando con fusiones
IMPORTANTE: Es que para hacer una fusión. Tengo que estar en la rama destino. O sea si me quiero traer los cambios de la rama feature/branches a la rama main, tengo que estar parado en la rama main y traerme los cambios de la otra rama

```sh
git switch main
git merge feature/branches
``` 

### Pueden suceder 3 cosas

* Fast-forward -> Fusión automatica -> Git se encarga de resolver la fusión
* Tercer Vía -> Diferentes algoritmos para resolver la fusión -> Automatico
* Conflicto -> El proceso de fusión es manual. Voy a tener que solventar el conflicto y avisarle a git que lo hice para terminar el proceso de fusión.
