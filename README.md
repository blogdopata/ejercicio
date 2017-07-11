[logo]: https://github.com/adam-p/markdown-here/raw/master/src/common/images/icon48.png "Logo Title Text 2" 
# SSH PASOS

### Crear repositorio en github
### Crear llave ssh

### CREAR llave SSH : 

' $ ssh-keygen -t rsa -b 4096 -C "poner aquí correo electrónico" '

### 3 Buscar la llave pública que se guardo en la dirección por defecto para ponerla en github, puedes verificar los directorios con:

### usar ls -la

### y verificar que existe la carpeta .ssh, entramos a .ssh y verificando sus archivos examinamos el archivo (llave pública) id_rsa.pub para extraer la llave pública y dársela a github con el comando:

### cat id_rsa.pub

### lo que sale (el número-te enorme) es la llave pública que colocaremos en github (Settings - SSH) para que github identifique que tenemos de alguna forma la llave privada (Guardada en el local).

# SUBIR A GITHUB

 - 'git remote add origin  tu git@github.com:tuUser/tuRepo.git'

# Cuando repo remoto este diferente del repo local :

- Tienes que actualizar el local con un fetch 
- Hacer git fetch origin 
- fusionar el contenido descargado en origin/master con tu rama principal  master  (en local)
- git merge origin/master (si no hay conflicto fue un fast forward exitoso)
- De haber conflicto estas en un manual merge y no queda otra que ver que archivos estan 
   en conflicto, arreglas esas lineas de código y grabar el commit.
   

### Agreguemos este SUPERLOG
## git config --global alias.superlog "log --graph --abbrev-commit --decorate --date=relative --format=format:'%C(bold blue)%h%C(reset) - %C(bold green)(%ar)%C(reset) %C(white)%s%C(reset) %C(dim white)- %an%C(reset)%C(bold yellow)%d%C(reset)' --all"
