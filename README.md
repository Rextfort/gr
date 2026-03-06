Taller matseb347 - Sitio Web en Django
Descripción del Proyecto
Este es un sitio web desarrollado con Django para mi emprendimiento de mantenimiento y reparación de computadoras en Santo Domingo ,Ecuador. Incluye páginas para inicio, servicios (limpieza, formateo, armado), galería de trabajos (antes/después) y contacto con formulario que envía emails a mi Gmail. El estilo es cyberpunk/neon con glow y glitch.
El proyecto sigue la "Guía Práctica para el Desarrollo de un Sitio Web con Django" de la Universidad Japón, adaptado a mi tema: modelos para servicios y fotos, admin para editar, vistas para renderizar HTML, plantillas con herencia, static/media para CSS e imágenes, y URLs configuradas.
Requisitos

Python 3.10+ (recomendado 3.12 como en la guía)
Django 5.x
Pillow (para manejo de imágenes)
Visual Studio Code con extensiones: Django Template, Python (como en página 2 del PDF)

Instalación y Ejecución

Descomprime el ZIP en una carpeta (ej: taller-mateo).
Abre CMD/Terminal y ve a la carpeta:textcd taller-mateo
Crea y activa entorno virtual (páginas 3-4 del PDF):textpython -m venv venv
Windows: venv\Scripts\activate
Linux/Mac: source venv/bin/activate

Instala dependencias (página 4):textpip install django pillow
Aplica migraciones (páginas 11-12):textpython manage.py migrate
Crea superusuario para el admin (páginas 12-13):textpython manage.py createsuperuser(Usa un usuario, email y contraseña segura)
Ejecuta el servidor (páginas 25-26):textpython manage.py runserver
Accede al sitio:
http://127.0.0.1:8000/ (inicio)
http://127.0.0.1:8000/servicios/ (servicios)
http://127.0.0.1:8000/galeria/ (galería)
http://127.0.0.1:8000/contacto/ (contacto)
http://127.0.0.1:8000/admin/ (panel para editar servicios y fotos)


Funcionalidades

Inicio: Bienvenida con estilo neon y servicios destacados.
Servicios: Lista de servicios con precios y descripciones (modelo Servicio).
Galería: Fotos de trabajos (modelo FotoTrabajo, antes/después).
Contacto: Formulario que envía consultas a mateolucero365@gmail.com (usando FormSubmit, adaptado de formulario en página 17-18).
Admin: Edita servicios y fotos (páginas 12-14).
Estilo cyberpunk: Neon glow, glitch animación, responsive.

Notas

Las imágenes en las plantillas son externas; necesitan internet para cargar.
El formulario no usa backend email completo (adaptado a FormSubmit para simplicidad; para producción, configura settings.EMAIL en página 18).
Si agregas modelos o cambias, corre makemigrations y migrate (p11-12).
Para producción: DEBUG = False, usa PostgreSQL (p27).
