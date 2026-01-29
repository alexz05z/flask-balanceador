## Comprobación técnica del sistema

### ¿Qué hace el bloque upstream?
El bloque upstream define un grupo de servidores backend a los que NGINX reparte las peticiones entrantes.

### ¿Cómo se configuran los healthchecks?
Docker Compose utiliza el endpoint `/status` para comprobar que cada instancia Flask está funcionando correctamente.

### ¿Cómo se pasa el tráfico de NGINX a Flask?
NGINX actúa como proxy inverso utilizando la directiva `proxy_pass` para redirigir las peticiones hacia los servicios Flask.

### ¿Qué puertos se usan?
- 8080: acceso del cliente
- 80: NGINX interno
- 8000: Flask con Gunicorn

### ¿Qué función tiene Gunicorn?
Gunicorn es el servidor WSGI encargado de ejecutar la aplicación Flask de forma eficiente y preparada para producción.
