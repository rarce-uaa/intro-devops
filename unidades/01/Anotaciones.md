# Notas

## Primeros pasos con los repositorios

```
git clone git@github.com:rarce-uaa/intro-devops.git
git config [--global] user.email "rarce@..."
git config [--global] user.name "Rodolfo D. Arce S."
git checkout -b dev
git checkout -b unidad-1
```

## Cuál es el contexto, dónde estoy?

```
git branch
git branch -a
git checkout [rama]
git status
git log
```

## Agregar archivos, guardar información y enviarla al repositorio

```
git add [*|archivo]
git commit [-a|archivo] -m "Comentario sobre los cambios, esto es importante que sea completo porque sino nos vamos a la B en la documentación después"
git push origin dev
GIT_SSH_COMMAND='ssh -i ~/.ssh/id_rsa.rarce_.. -o IdentitiesOnly=yes' git push origin dev
```

## Si meto la pata, guardo y lo llevo a donde se debe

```
git stash
git apply
```
