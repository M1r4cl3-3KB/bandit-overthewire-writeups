# Bandit Nivel 5 --> Nivel 6

## Objetivo
Para este nivel nos indican que hay un archivo dentro del directorio inhere y que tiene las siguientes propiedades:
- human readable
- 1033 bytes in size
- not executable

## Comandos usados
ls 
cd
find . -type f -readable -size 1033c ! -executable 

## Evidencia
![Nivel 05](./Imagenes/bandit05.png)


##Explicaciòn
Listamos dentro de la carpeta de bandit5 y vemos un directorio llamado inhere al cual accedemos usando cd, seguidamente filtramos 
por las pistas que nos da el ejercicio, utilizamos nuevamente el comando find pero esta vez usando el -size 1033c que indica el tamaño
de los archivos dentro de nuestro sistema ponemos c al costado de 1033 por que asi se definen los byes en el sistema ya que si ponemos solamente
1033 veremos que no nos arroja ninguna respuesta, y como nos indica que no es ejecutable tenemos que negar el comando -executable que lo hacemos con "! "
De esta manera el output de este comando completo nos da la ruta absoluta de donde se encuentra este archivo que es ./maybehere07/.file2
le hacemos cat directamente y nos da la contraseña para el siguiente nivel

## Contraseña para el siguiente nivel

HWasnPhtq9AVKe0dmk45nxy20cvUa6EG
