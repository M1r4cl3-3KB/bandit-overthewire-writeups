# Bandit Nivel 28 --> Nivel 29

## Objetivo 
Para el siguiente nivel tenemos otro repositorio de git, ssh://bandit28-git@bandit.labs.overthewire.org/home/bandit28-git/repo por el puerto 2220. 


## Comandos usados 
git clone
git log
git show


## Evidencia 
![Nivel 28](./Imagen/bandit28.png)

## Explicaciòn
De igual manera nos clonamos el repositorio en el mktemp -d creado y le brindamos la contraseña de bandit28 lo que se nos descargara un archivo llamado repo entramos y leemos README.md el cual dice lo siguiente: 
git clone ssh://bandit28-git@bandit.labs.overthewire.org:2220/home/bandit28-git/repo

# Bandit Notes
   2 │ Some notes for level29 of bandit.
   3 │ 
   4 │ ## credentials
   5 │ 
   6 │ - username: bandit29
   7 │ - password: xxxxxxxxxx

Nos dan credenciales donde nos dan usuario pero no contraseñas, averiguando vemos que github crea commits, por lo que podemos ver los cambios que se hacen internamente en git hub. 
Usamos git log para ver los commits realizados --> En caso de que te de error el git log es por la herramienta less por lo que en arch linux lo instalamos de la siguiente manera : 
sudo pacman -S less --> en caso de que nos de error de nuevo por falta de paqueter u otro motivo, podemos utilizar el siguiente comando para ver los commits --> git --no-pager log

commit adc7f885a129baee883058b8a870739489f80194 (HEAD -> master, origin/master, origin/HEAD)
Author: Morla Porla <morla@overthewire.org>
Date:   Fri Apr 3 15:17:54 2026 +0000

    fix info leak

Vemos que en este commit dice fix info leak, que significa arreglando fuga de informaciòn. 

Para ver que paso con ese commit filtramos por el identificador y usamos git show adc7f885a129baee883058b8a870739489f80194

- username: bandit29
-- password: 4pT1t5DENaYuqnqvadYs1oE4QLCdjmJ7
+- password: xxxxxxxxxx

Verificamos que dentro se quito una contraseña el "hash" y se añadio password : XXXXXXX por lo que ya tendriamos la contraseña para bandit29

## Contraseña para el siguiente nivel 

4pT1t5DENaYuqnqvadYs1oE4QLCdjmJ7
