# Bandit Nivel 9 --> Nivel 10

## Objetivo
El siguiente ejercicio nos indica que hay un archivo llamado data.txt el cual no esta en texto plano pero que si podemos obtener el archivo en texto plano 
podemos filtrar la contraseña que esta junta a caracteres especiales "--" 


## Comandos usados
strings
grep 

##Explicaciòn
Verificamos que efectivamente hay un archivo llamado data.txt y al hacerle cat data.txt nos muestra informacion no legible ya que parece que esta encriptada, 
para poder transformarla a texto plano podemos usar strings sobre el mismo archivo "strings data.txt" por lo que ahora vemos texto plano pero mucha informacion, 
seguidamente podemos filtrar con el comando grep los caracteres especiales por lo que solo nos queda las lineas que contengan == 
De esa manera se forma un mensaje donde nos indica que la contraseña es : 
========== the
========== password
========== is
========== FGUW5ilLVJrxX9kMYMmlN4MgbpfMiqey



## Contraseña para el siguiente nivel

FGUW5ilLVJrxX9kMYMmlN4MgbpfMiqey
