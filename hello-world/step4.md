En el paso anterior hemos usado un recurso que se llama user, este recurso está definido dentro de los recursos que puede gestionar puppet. Si quieres conocer todos los recursos y los parámetros que se puede usar puppet, tómate unos minutos para visitar la siguiente web:

https://puppet.com/docs/puppet/6.0/type.html

Vamos ahora a empezar a trabajar con los ficheros de puppet (pp), para ello vamos a crear un fichero y vamos a introducir los comandos que hemos visto anteriormente

## Crea un fichero create_user_epi.pp con el siguiente contenido (puedes usar vi)

```
user {'Epi':
  ensure => present
}
```

Para aplicar el fichero creado sólo tienes que volver a lanzar el comando puppet apply pero esta vez sin la opción de ejecutar (-e)

`puppet apply create_user_epi.pp`{{execute}}
