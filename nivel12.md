# Bandit Nivel 12 --> Nivel 13

## Objetivo
Para este nivel nos da un archivo data.txt que esta hexdump y que ademas a sido comprimido varias veces por que lo que si queremos leerlo no veremos nada mas que caracteres raros 
de igual manera si queremos usar strings no nos dejara leer nada ya que esta convertido a hexadecimal, nos da como tip crear una carpeta temporal en /tmp tal vez usando mktemp -d 
Copiar lo que hay dentro de este archivo y poder manejarlo desde ahi.

## Comandos usados
grep -A
tail -n 1
awk 'NF{print $NF}'
xxd -r
7z l / 7z x

## Evidencia
![Nivel 12](./Imagenes/bandit12.png)

##Explicaciòn
Comprobamos que el archivo esta dumpeado en hexadecimal por lo que dejare los pasos que deberiamos seguir para poder tenerlo hasta al menos en texto plano para poder trabajarlo : 
1- Hacemos cat al archivo data.txt y copiamos todo lo que hay en su interior. 
2- Salimos del SSH para poder crear un archivo dentro de nuestra terminal de trabajo llamado data.hex donde pondremos todo lo que estaba en el archivo data.txt, esto unicamente para poder trabajar desde nuetra terminal, puesto a que por alguna razon trabajar desde la terminal del bandit12 nos da problemas
3- Como sabemos que esta en hexadecimal tenemos que convertirlo a como estaba anteriormente con el comando xxd -r esto revierte el dumpeo de hexadecimal en este caso utilizamos el comando entero xxd -r data.hex > data.gzip
4- Ahora que redirigimos la data transformada tenemos un archivo que es un comprimido el data.gzip, si le hacemos file data.gzip confirmamos que es un gzip valga la redundancia por lo que desde aqui ya podremos trabajar.
5- Nosotros usaremos la herramienta 7z l y 7z x para saber si el archivo tiene un comprimido y tambien para obtener ese comprimido.
6- Si hacemos 7z x al archivo data.gzip nos dara un archivo nuevo al cual le tendremos que hacer de igual manera un 7z x a ese nuevo archivo y asi sucesivamente hasta que ya no nos quede nada comprimido, y al ultimo archivo recien leerlo con cat para que nos de la respuesta
Para efectos mas practicos, ejecute un script que me permite automatizar el flujo de trabajo y descomprime todos los archivos necesarios puedes reutilizar el codigo asumiento que ya creaste el archivo data.gzip como mencione anteriormente. 

#!/bin/bash

name_compressed=$(7z l data.gzip | grep "Name" -A 2 | tail -n 1 | awk 'NF{print $NF}'
7z x data.gzip > /dev/null 2>&1

while true;do
	7z l $name_compressed > /dev/null 2>&1
	
	if ["$(echo $?)" == "0" ]; then
		decompressed_next = $(7z l $name_compressed | grep "Name" -A 2 | tail -n 1 | awk 'NF{print $NF}'
		7z x $name_compressed > /dev/null 2>&1 && name_compressed = $decompressed_next
	else
		cat $name_compressed; rm -r data* 2>/dev/null
		exit 1
	fi

done



## Contraseña para el siguiente nivel
The password is FO5dwFsc0cbaliH0h8J2eUks2vdTDwAn
