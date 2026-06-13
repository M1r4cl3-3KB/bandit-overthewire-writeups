# Bandit Nivel 26 --> Nivel 27

## Objetivo 
Excelente, para el siguiente nivel me dice que muy buen trabajo en conseguir esa shell, que ahora me apure en atrapar la contraseña de bandit27!  

## Comandos usados 
ls

## Explicaciòn
Al hacerle un ls -l al home, vemos que hay un binarios con SETUID, por lo que podemos ejecutar este binario siendo bandit26 pero con permisos de bandit27 por que haremos lo siguiente: 
bandit26@bandit:~$ ./bandit27-do cat /etc/bandit_pass/bandit27
upsNCc7vzaRDx6oZC6GiR6ERwe1MowGB

Por lo que obtenemos la contraseña de bandit27


## Contraseña para el siguiente nivel 

upsNCc7vzaRDx6oZC6GiR6ERwe1MowGB
