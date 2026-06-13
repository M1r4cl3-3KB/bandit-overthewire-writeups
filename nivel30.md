# Bandit Nivel 30 --> Nivel 31

## Objetivo 
Como es de esperarse este nivel nos dice que hay un repositorio ssh://bandit30-git@bandit.labs.overthewire.org:2220/home/bandit30-git/repo
La contraseña para el usuario bandit30-git es la misma que la del usuario bnadit30

## Comandos usados 
git clone
git tag
git show

## Evidencia 
![Nivel 31](./Imagen/bandit31.png)

## Explicaciòn
Iniciamos creando un directorio con "mktemp -d" creado y nos movemos a esa ruta 

Clonamos --> git clone ssh://bandit30-git@bandit.labs.overthewire.org:2220/home/bandit30-git/repo

Al usar el comando "git branch -a" o "git log" vemos que no hay mucha informaciòn 

Si buscamos en internet podemos ver que github trabaja con "tags" que dice que sirve como una rama firma que no permuta que es inaltarable, es un nombre que puedes usar para marcar un punto especifico en la historia de un repositorio.

Por lo que viendo el manual de como utilizar comandos dentro de linux vemos --> "git tag" para ver que tags tienen y al ponerlo vemos que nos sale como una especie de archivo secret.

Pero ten mucho cuidado, por que no es un archivo que podamos trabajarlo con cd o cat para ver lo que hay dentro de secret debemos usar la herramienta de git --> "git show secret" o "git --no-pager secret"

Lo que nos dara la contraseña para el siguiente nivel --> fb5S2xb7bRyFmAvQYQGEqsbhVyJqhnDy


## Contraseña para el siguiente nivel 

fb5S2xb7bRyFmAvQYQGEqsbhVyJqhnDy
