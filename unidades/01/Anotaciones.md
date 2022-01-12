# Notas

## Primeros pasos con los repositorios

Clonar un repositorio de software desde Github
```
git clone git@github.com:rarce-uaa/intro-devops.git
```

Setear la información adicional en el repositorio o en todo el sistema, esto es pertinente porque se guarda en cada commit

```
git config [--global] user.email "rarce@..."
git config [--global] user.name "Rodolfo D. Arce S."
```

Crear una nueva rama y mudarse a la misma para empreza a trabajar en los cambios

```
git checkout -b dev
git checkout -b unidad-1
```

Moverse entre las ramas

```
git checkout main
git checkout unidad-1
```


## Cuál es el contexto, dónde estoy?

Para saber en que rama estoy de las ramas que hay en el repositorio local
```
git branch
```

Ver todas las ramas locales y remotas

```
git branch -a
```

Ver los cambios pendientes, o el estado de la rama/repositorio

```
git status
git log
```

## Agregar archivos, guardar información y enviarla al repositorio

Cuando se crea una nuevo archivo, el mismo no se agrega manualmente al repositorio o tampoco se verifica sus cambios, recién al agregarlo es que se observa (**track, tracking**), se puede usar _*_ para todos los archivos.

```
git add [*|archivo]
```

Cuando hay un cambio hecho en algun archivo, para "formalizar" esos cambios se hace un commit de los cambios en uno o mas archivos, el _*_ es un wildcard para todos los archivos o se puede especificar el/los archivo/s que se van a guardar.

```
git commit [-a|archivo] -m "Comentario sobre los cambios, esto es importante que sea completo porque sino nos vamos a la B en la documentación después"
```

Cuando estan guardados en el repositorio, en la rama correspondiente, esta misma rama/commit se puede empujar al repositorio remoto. Este paso es opcional si no trabajamos con un repositorio remoto

```
git push origin dev


# Si se trabajan con varias llaves privadas, esta forma permite usar una en particular

GIT_SSH_COMMAND='ssh -i ~/.ssh/id_rsa.rarce_.. -o IdentitiesOnly=yes' git push origin dev
```

## Si meto la pata, guardo y lo llevo a donde se debe

Los cambios que se dén en los archivos, se pueden guardar para usarlos despues, y con eso volver al estado original del commit

```
git stash
```

Ver todos los cambios que fueron guardados y a partir de que commit salieron

```
git stash list
```


```
# Con esto se aplican los cambios y se borran
git stash pop

# Con esto se aplican los cambios y se guardan para usar
git stash apply
```
