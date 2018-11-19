Vamos ahora a empezar utilizar el comando pupppet para empezar a configurar la máquina

## Ver todas las opciones del comando Puppet

Lo primero que se va a ver será los diferentes comandos que podemos lanzar con Puppet, para ello se va utilizar el comando --help del propio comando

`puppet help`{{execute}}

Ahora que se conoce los distintos comandos que podemos lanzar con Puppet vamos a empezar a trabajar con el comando inline que permite crear recursos directamente sin necesidad de crear un fichero pp (extensión de puppet)

`puppet apply  -e "user{'Eloy': ensure=>present}"`{{execute}}

Con este comando lo que se ha hecho es crear un usuario 'Eloy' en nuestro sistema. Ahora vamos a comprobar la capacidad idempotente de puppet lanzando de nuevo el mismo comando.

`puppet apply  -e "user{'Eloy': ensure=>present}"`{{execute}}

Como has podido commprobar no ha fallado al lanzar el comando, esto es porque ha comprobado que el usuario existe en la máquina y que todos sus atributos son correcto. En cambio, si modificamos algun atributo de este usuario como por ejemplo puede ser su contraseña la herramienta deberá sólo modificar este atributo y mantener el resto.

`puppet apply  -e "user{'Eloy': ensure=>present, password=>sTr0nG}"`{{execute}}

También se podría lanzar el comando puppet para que no compruebe todo el recurso y sólo verificar uno concreto. Con el siguiente comando cambiaremos el home del usuario y dejamos sin compmrobar el resto de atributos.

`puppet apply  -e "user{'Eloy': home=>/home/Eloy}"`{{execute}}

En este caso puppet no ha comprobado nada relativo a la contraseña, lo único que ha hecho es comprobar que su home es el correcto.

__¿Sabrías decir porque no ha cambiado nada?__
