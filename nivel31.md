# Bandit Nivel 31 --> Nivel 32

## Objetivo 
Aprendiendo bastante con git veremos el siguiente ejercicio para aprender mas a utilizar estas herramientas ya que nos ayudaran a lo largo de nuestras vidas. 
Nos dice que hay un repositorio ssh://bandit31-git@bandit.labs.overthewire.org:2220/home/bandit31-git/repo. 
La contraseña para bandit31-git es la misma que la del usuario bandit31

## Comandos usados 
git clone 

## Evidencia 
![Nivel 31](./Imagen/bandit31.png)

## Explicaciòn
Creamos nuestro directorio "mktemp -d" y nos movemos a esa ruta. 

Clonamos el repositorio --> git clone ssh://bandit31-git@bandit.labs.overthewire.org:2220/home/bandit31-git/repo

Y al leer README.md nos dice lo siguiente: 

1 │ This time your task is to push a file to the remote repository.
   2 │ 
   3 │ Details:
   4 │     File name: key.txt
   5 │     Content: 'May I come in?'
   6 │     Branch: master

Nos dice que ahora nuestra tarea es empujar un archivo al repositorio remoto. Usando lo siguiente. 

Un arhivo llamado key.txt que contenga el mensaje May I come in? y usar herramientas de git para enviarlo para esto es necesario tener el archivo listo con touch o nano y escribir dentro el texto solicitado.

A continuaciòn usamos los siguientes comando para añadir archivos y enviarlos al repositorio. 

1-. git add -f key.txt --> Para añadir un nuevo archivo 
2-. git commit -m "Insertamos un nuevo archivo" --> Para añadir un commit diciendo que es lo que estas haciendo con esa accion
3-. git push -u origin master --> Para poder empujar el archivo dentro del repositorio, le damos ENTER y le brindamos la contraseña y nos sale el siguiente mensaje: 

remote: ### Attempting to validate files... ####
remote: 
remote: .oOo.oOo.oOo.oOo.oOo.oOo.oOo.oOo.oOo.oOo.
remote: 
remote: Well done! Here is the password for the next level:
remote: 3O9RfhqyAlVBEZpVb6LYStshZoqoSx5K 
remote: 
remote: .oOo.oOo.oOo.oOo.oOo.oOo.oOo.oOo.oOo.oOo.

Por lo que tendriamos la contraseña para el siguiente nivel 

## Contraseña para el siguiente nivel 

3O9RfhqyAlVBEZpVb6LYStshZoqoSx5K
