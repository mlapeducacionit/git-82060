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