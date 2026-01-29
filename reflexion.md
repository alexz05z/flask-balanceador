## Reflexión sobre la práctica

### ¿Qué has aprendido sobre balanceo?
He aprendido cómo funciona un balanceador de carga y cómo distribuye las peticiones entre varias instancias para mejorar la disponibilidad del sistema.

### ¿Cómo has identificado qué instancia respondía?
Cada instancia devuelve su hostname usando la función `socket.gethostname()`, lo que permite identificar claramente el contenedor que responde a cada petición.

### ¿Qué pasaría si NGINX falla?
NGINX es un punto único de fallo. Si se detiene, el sistema deja de ser accesible. En entornos reales se usaría redundancia o un balanceador externo.

### ¿Qué mejorarías en este sistema?
Añadiría HTTPS, escalado automático, monitorización y múltiples balanceadores para evitar puntos únicos de fallo.

### ¿Qué ventajas ves al usar GitHub?
GitHub permite control de versiones, organización del código, trabajo colaborativo y facilidad para compartir y documentar proyectos.