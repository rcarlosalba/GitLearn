# Git & GitHub
Aprendiendo Git enserio!


## Espacios de trabajo en Git
- Working - Area de Trabajo.
- Staging - Area de Preparación - podemos escoger cuales suben al Repository.
- Repository - Area donde se almacenan los commit y todos ven como se arma la historia.

## Comandos comunes de inicio
- git --version / verifica instalación y muestra versión.
- git config --global user.name "tu nombre" / define el nombre del usario. 
- git config --global user.email "correo registrado en git" /Correo registrado en Git (sirve para enlazar con github más adelante).
- git config --global --list / muestra la configuración global.

## Comandos para iniciar repositorios
- git init / inicia el rastreo de los archivos.
- git status / status del rastreo y/o funcionamiento en la carpeta.
- git add folder/nombreArchivo.extensión.
- git add -A (todos los archivos) / pasa los archivos al staging area.
- git commit -m "texto" --amend / corregir el ultimo commit se vale solo en el ultimo.
- git log / el log de Git permite saber donde se ejecutaron cambios.
- git log --oneline /todo en una linea.
- git log --decorate /donde esta el head // Con OhMyZSH no es necesario.
- git log --stat /detalles de las inserciones.
- git log --p /descripcción grafica de que fue borrado y/o agregado.
- git log -- graph / asteriscos del rumbo.
- git log -# / muestra los commits por cantidad.
- git log -S "code" / muestra donde se uso la palabra "code".

## Creando Logs personalizados: 
git config --global alias.superlog "log --graph --abbrev-commit --decorate --date=relative --format=format:'%C(bold blue)%h%C(reset) - %C(bold green)(%ar)%C(reset) %C(white)%s%C(reset) %C(dim white)- %an%C(reset)%C(bold yellow)%d%C(reset)' --all" /Crea el superlog

git config --global alias.nicelog "log --oneline --graph --all"

## Git Reset 
- git reset --hard  / alinea el workin el stage y el repository, edita el codigo.
- git reset --mixed  / no toca el working - alinea stage y repository osea que si tenemos modificado el codigo tenemos que repetir la iteración basica.
- git reset --soft   / alinea stage y repository aqui no tenemos que iterar, esta listo para el siguiente cambio.

## Ramas en Git
La rama (branch) por default en Git es master
- git checkout -b nombre de la rama /  crea una rama
- git checkout "nombre de rama" / cambia de rama

## Rebase & Merge
Rebase / sirve para colocar los commits de la rama alterna adelante en un espacio especifico del time line 
- git rebase master /por que nos ubicamos en la rama que queremos empujar luego nos pasamos a master y hacemos merge
- git merge "nombre de la rama rebase" y hace un fast foward
- git merge / para mezclar ramas ubicado en la rama que va a absorber pide poner nombre.
- git branch -d nombre de la rama / borrado y no se borra si no esta fusionada

**desde la terminal rm -rf .git - borra directorio git y reinicia todo todo!!!! se pierde el rastreo**

## Clonar 
- git clone y la direccion de SSH (debemos estar unicados en donde queremos que coloque el clon).

## Crear una llave SSH
- ssh-keygen -t rsa -b 4096 -C "email de github" // entro a la raiz de ahí coloco "ls -la" sin comillas
- cat id_rsa.pub - para editar la llave publica 
Para conectarse con un repositorio remoto (personal)
- Crear el repositorio en github 
- Crear la carpeta local 
- Iniciar git 
- Crear archivos
- git remote add origin (direccion remota ssh) 
- git push origin master 
- git push -u origin master
