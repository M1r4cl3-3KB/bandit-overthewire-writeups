# Bandit Nivel 25 --> Nivel 26

## Objetivo 
Perfecto ! Una vez que pasemos de nivel nos dice que autenticarnos como bandit26 desde bandit25 deberia ser bastante facil, La shell para el usuario bandit26 no es /bin/bash pero es otra cosa. Encuentra cual es, como funciona y como romperlo.  

## Comandos usados 
ls 
ssh
cat
more
vi
id
pwd

## Explicaciòn
Para poder ganar acceso nos conectamos desde bandit25 a bandit26 :
ssh -i bandit26.sshkey bandit26@localhost 
Vemos que intenta ingresar pero se dectonecta al ultimo segundo osea que no nos permite conectarnos normalmente, como vimos que no usa /bin/bash verificamos en /etc/passwd que tipo de shell usa bandit26
bandit26:x:11026:11026:bandit level 26:/home/bandit26:/usr/bin/showtext
Utiliza una /bin/showtext --> Para este caso vamos a leer que es exactamente esto : 
cat /usr/bin/showtext
#!/bin/sh

export TERM=linux

exec more ~/text.txt
exit 0

Vemos que es un script en bash donde usa exporta TERM como linux y exce more, esto nos da una pista para poder intentar conectarnos por ssh y que el comando more nos ayude a poder ingresar a bandit26
por lo que tenemos que usar una terminal mas pequeña para que nos permita utilizarlo
Forma 1 : 

ssh -i bandit26.sshkey -p 2220 bandit26@localhost --> En esta parte deberan hacer pequeña la terminal que tengan o abrir mas terminales hasta tener una terminal pequeña. 

En caso que no les salga el MORE o un mensaje de Permission denied (publickey) pueden probar la segunda opciòn. 

Forma 2 : 
Copiaremos el archivo bandit26.sshkey a nuestra terminal, creamos un archivo desde nuestra terminal touch bandit26.sshkey, le damos permisos chmod 600 bandit26.sshkey e introducimos el texto dentro con nano 

Una vez hecho esto guardamos el archivo con Ctrl + o --> Enter --> Ctrl + x para salir, ahora nos conectamos desde nuestra terminal al bandit26 

ssh -t -i bandit26.sshkey -p 2220 bandit26@bandit.labs.overthewire.org 
Una vez tengan el MORE en pantalla deberan seguir estas instrucciones : 

Darle ESC y luego V para entrar al modo visual, escribir ":" dos puntos y seguido de set shell=/bin/bash, ENTER
Poner nuevamente ":" shell y les entregara una shell de bandit26 donde ya podremos leer la contraseña de este ejercicio. 
cat /etc/bandit_pass/bandit26


## Contraseña para el siguiente nivel 

s0773xxkk0MXfdqOfPRVr9L3jJBUOgCZ
