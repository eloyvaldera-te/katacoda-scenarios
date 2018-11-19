Ahora vamos a empezar a jugar con los primeros comandos de Puppet, para ello lo primero que se va a hacer es comprobar la versión instalada de Puppet

## Comprobar versión instalada de Puppet

`puppet -V`{{execute}}

Junto con Puppet también se instala en la máquina una herramienta llamada _facter_, esta herramienta permite obtener en tiempo real información relevante sobre la máquina con la que estamos trabajando. ¡Prueba a lanzar este comando!

## Facter

`facter`{{execute}}

Como has podido ver la salida de este comando devuelve una lista de elementos con toda la información de la máquina, si quisieramos obtener el dato concreto de un elemento sólo tendríamos que indicar el nombre de ese elemento

## Facter obtener información concreta

`facter memoryfree`{{execute}}

También podríamos acceder información mucho más concreta concatenando otros valores:

`facter os.family`{{execute}}
