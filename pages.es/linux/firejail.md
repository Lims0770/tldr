# firejail

> Aísla de forma segura los procesos en contenedores utilizando capacidades integradas de Linux.
> Más información: <https://manned.org/firejail>.

- Integra firejail con tu ambiente de escritorio:

`sudo firecfg`

- Abre un Mozilla Firefox restringido:

`firejail {{firefox}}`

- Inicia un servividor de Apache restringido en una interfaz y dirección conocida:

`firejail --net={{eth0}} --ip={{192.168.1.244}} {{/etc/init.d/apache2}} {{start}}`

- Lista contenedores activos:

`firejail --list`

- Lista actividad de red de los contenedores activos:

`firejail --netstats`

- Apaga un contenedor activa:

`firejail --shutdown={{7777}}`

- Inicia una sesión de Firefox restringida para navegar en internet:

`firejail --seccomp --private --private-dev --private-tmp --protocol=inet firefox --new-instance --no-remote --safe-mode --private-window`

- Usa archivos host personalizados (sobrescribe el archivo `/etc/hosts`):

`firejail --hosts-file={{~/myhosts}} {{curl http://mysite.arpa}}`
