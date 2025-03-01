---
title: Modificar su llave SSH en caso de pérdida
excerpt: Modificar su llave SSH en caso de pérdida
slug: modificar_su_llave_ssh_en_caso_de_perdida
legacy_guide_number: g2069
section: Seguridad
---

> [!primary]
> Esta traducción ha sido generada de forma automática por nuestro partner SYSTRAN. En algunos casos puede contener términos imprecisos, como en las etiquetas de los botones o los detalles técnicos. En caso de duda, le recomendamos que consulte la versión inglesa o francesa de la guía. Si quiere ayudarnos a mejorar esta traducción, por favor, utilice el botón «Contribuir» de esta página.
>

**Última actualización: 27 de septiembre de 2018**

## Objetivo

En caso de pérdida de llave SSH, ya sea como consecuencia de una reinstalación de correos o de otro tipo, es posible que no pueda conectarse a su instancia si no ha configurado ninguna forma alternativa de conectarse a su instancia.

Para recuperar el acceso, hemos puesto a su disposición un [modo de rescate](https://docs.ovh.com/us/es/public-cloud/poner_una_instancia_en_modo_de_rescate/) que le permite conectarse con una contraseña y modificar sus archivos.

**Esta guía explica cómo configurar el archivo *authorized_keys* del usuario *admin* para poder añadir una nueva llave SSH para recuperar el acceso a la instancia.**

## Requisitos

- Crear una llave SSH
- Pasar una instancia a modo de rescate

## Procedimiento

> [!primary]
>
Si quiere registrar una llave SSH en el área de cliente de OVHcloud, le recomendamos que utilice el cifrado RSA o ECDSA. ED25519 no está soportado actualmente.
>

Una vez que haya montado el disco de su instancia en [modo de rescate](https://docs.ovh.com/us/es/public-cloud/poner_una_instancia_en_modo_de_rescate/), podrá acceder a todos sus archivos.

El archivo que contiene las llaves SSH es el siguiente:

```sh
/home/USER_NAME/.ssh/authorized_keys
```

Si quiere añadir su nueva llave SSH, solo tiene que editar el archivo y añadir la nueva clave:

```sh
sudo vim /mnt/home/USER_NAME/.ssh/authorized_keys
ssh-rsa 111111111222222222223333333333334444444555555 5555566666677777777778888888888899999999999900000 00000000000000000000= old@sshkey
ssh-rsa AAAAAAAAAAAAAAABBBBBBBBBBBCCCCCCCCCCCCCCCCCCCCCCCCCCCCCCCCCCCCDDDDDDDDDDDDDDDDDDDDDDDDDDDDDDDDDDDEEEEFFFFFFFFFFFFFFFFFFFFGGGGGGGGGGGGGGGGGGGGGGGGGGGGGGGGGGGGGGGGGGGGGGGGGGGGGGGGGGGGGGGGGGGGGGGGGGGGGGGGGGGGGHhhhhhhhhhhhhhhhhhhhhhhhhhhhhhhhhhhhhhhhhhhhhhhhhhhhhhhhhhhhhhhhhhh= new@sshkey
```

### Cambiar la llave SSH de usuario por defecto

Para modificar la llave SSH del usuario por defecto, acceda a la carpeta personal del usuario. Por ejemplo, para el usuario admin, el archivo que se va a encontrar se encuentra en la siguiente carpeta:

```sh
/home/admin/.ssh/authorized_keys
```

Para una instancia en Ubuntu 15.10, el usuario por defecto será ubuntu , por lo que el archivo estará en la siguiente carpeta:

```sh
/home/ubuntu/.ssh/authorized_keys
```

### Cambiar la contraseña de usuario predeterminada

También puede cambiar la contraseña de su usuario predeterminado utilizando el modo de rescate y los siguientes comandos (en caso de que el usuario sea admin):

Se cambia el directorio raíz para situarse directamente en el disco de la instancia:

> [!primary]
>
En el ejemplo a continuación, utilizamos vdb1 como nombre del disco del servidor y mnt como punto de montaje.
>

```sh
/home/admin# mount /dev/vdb1 /mnt/
/home/admin# chroot /mnt/
```

Se cambia la contraseña de administrador:

```sh
passwd admin
```

Una vez realizada la modificación y guardada, solo tiene que reiniciar su instancia en su disco para poder conectarse a su instancia con su nueva llave SSH.

## Más información

[Pasar una instancia a modo de rescate](https://docs.ovh.com/us/es/public-cloud/poner_una_instancia_en_modo_de_rescate/)

Interactúe con nuestra comunidad de usuarios en <https://community.ovh.com/en/>.
