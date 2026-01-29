# Práctica 11 – Balanceo de Carga Escalable con Flask, Gunicorn, NGINX y Docker

##  Descripción del sistema
En esta práctica se ha desarrollado un sistema web escalable basado en contenedores Docker.  
El sistema utiliza un balanceador de carga NGINX que distribuye las peticiones HTTP entre varias instancias de una aplicación Flask ejecutada con Gunicorn.

La arquitectura permite mejorar la disponibilidad, escalabilidad y tolerancia a fallos.

### Arquitectura
Cliente → NGINX (8080) → web1 | web2 | web3 (Flask + Gunicorn)

El reparto de peticiones se realiza mediante el algoritmo **round-robin**.

---

##  Tecnologías utilizadas
- Python
- Flask
- Gunicorn
- NGINX
- Docker
- Docker Compose
- GitHub

---

##  Estructura del proyecto

app/
├── application.py
├── wsgi.py
docker/
└── nginx_balanceador.conf
scripts/
└── test_balanceo.sh
capturas/
docker-compose.yml
requirements.txt
README.md
reflexion.md
comprobacion.md
entrega.json


---

## 🚀 Despliegue del sistema
Desde la raíz del proyecto ejecutar:

```bash
docker compose up --build


Una vez levantado, acceder desde el navegador a:

http://localhost:8080

🧪 Pruebas realizadas
Prueba de balanceo

Ejecutar el script:

bash scripts/test_balanceo.sh


Se observa que las respuestas provienen de diferentes instancias.

Simulación de caída
docker stop web2


El sistema sigue funcionando correctamente gracias al balanceo.
