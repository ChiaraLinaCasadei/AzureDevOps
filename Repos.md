# Repos

## Files

Es un explorador de repositorios y tambien permite listar todas las ramas asociadas a ese repositorio.
Tiene opciones desde la interfaz para crear nuevas ramas, o crear nuevos repositorios.
El botón de "Clone" nos permite clonar el repo.
Cuando hagamos el comando de Git Clone, y nos pidan credenciales, las podemos generar antes desde la interfaz. 

Se puede, por ser una herrramienta de Microsoft, realizar todo esto desde VS.

## Commits

Tiene la misma capacidad de exploracion que Files, pero orientada al historial de commits de la rama. 
Se pueden crear ramas a partir de commits en específicos.
Se pueden crear tags y agregarlos a los commits.

## Pushes

Veremos todos los push realizados. Recordemos que un solo push puede tener varios commits, así que no es lo mismo. 
Al hacer click en el commit, se pueden ver detalles sobre el push, y explorar. 

## Branches

Da una lista de todas las ramas disponibles en un repositorio. 
A destacar las etiquetas que tienen las ramas. 
Default quiere decir que se va a colocar como destino por defecto (se puede cambiar) para los merges.
Compare significa que todas las otras ramas van a compararse con ella.

*Behind | Ahead*
*Hicieron cambios aparte de la version que tenes en local | Hiciste cambios a partir de la versión que está en remoto*

Tenemos un menú de opciones disponible para cada rama, con ciertas opciones que cabe destacar:
* Branch Policies: se definen reglas que ayudan a prevenir incorporar cambios que no hayan sido revisados.
* Set As Compare Branch: para comparar estas ramas con las otras. 

## Tags
Es para fijar puntos importantes en el historial de un repositorio. Tiene una herramienta gráfica para poder etiquetar tanto rama, como commit, como un mismo tag. 

## Pull Request
Es un proceso automatizado para incorporar cambios a una rama principal. Su ventaja es que pueden involucran varios participantes para que revisen los cambios a incorporar. 
Tienen funciones para ayudar a la comunicación y trazabilidad de los cambios que se van realizando.
