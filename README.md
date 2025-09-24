# Tutorial para la conexión SSH a nuestro repositorio

```bash
pwd
ls ~/.ssh   # para ver si tenemos una conexión
ssh-keygen -t ed25519 -C "adombar413@g.educaand.es"   # generar la clave publica y privada ssh
eval "$(ssh-agent -s)"   # levantar el servidor ssh
ssh-add ~/.ssh/id_ed25519   # añadir la clave privada al sistema, la publica es la que acaba en .pub

cat ~/.ssh/id_ed25519.pub   # ver la clave publica para copiarla y llevarla a github

mkdir carpeta
cd carpeta
git init   # inicializar el seguimiento de carpeta
git config --global --list   # ver nuestra identificacion
git config --global user.name "AngeliusDB06"   # identificarnos con nuestro usuario de github
git config --global user.email "adombar413@g.educaand.es"   # identificarnos con nuestro email
echo "# Configurando SSH" > README.md   # crear archivo vía ssh

git status -s   # ver los ficheros que se ha hecho seguimiento
git add .   # añadir al área stage todo lo que hay en el directorio
git add nombredelfichero

git commit -m "Created: README.md"   # hacer un commit con un mensaje
git log --oneline   # información sobre los últimos commits
git log   # más información sobre los commits

git remote add origin git@github.com:AngelDB06/Optativa-GS.git   # añadir nuestro repositorio (origin es un alias de la ruta)
git remote -v   # comprobar si estamos conectados remotamente al repositorio
git pull   # traer al directorio lo que hay en el repositorio
git push   # subirlo
```
