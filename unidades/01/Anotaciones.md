# Notas

## Primeros pasos con los repositorios

git clone git@github.com:rarce-uaa/intro-devops.git
git config --global user.email "rarce@..."
git config --global user.name "Rodolfo D. Arce S."
git checkout -b dev
git checkout -b unidad-1
git commit [archivo|-a] -m "Comentario sobre los cambios, esto es importante que sea completo porque sino nos vamos a la B en la documentación después"
git push origin dev
GIT_SSH_COMMAND='ssh -i ~/.ssh/id_rsa.rarce_.. -o IdentitiesOnly=yes' git push origin dev