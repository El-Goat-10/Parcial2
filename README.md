# Sistema de Gestión de Proyectos y Tareas

## Descripción
Este proyecto fue desarrollado con Django y permite administrar proyectos y las tareas relacionadas con cada uno mediante el panel de administración.

## Tecnologías utilizadas
- Python
- Django
- SQLite
- HTML del administrador de Django

## Modelos
### Proyecto
Permite registrar proyectos con los siguientes campos:
- Nombre
- Descripción
- Fecha de creación

### Tarea
Permite registrar tareas relacionadas con un proyecto:
- Título
- Descripción
- Proyecto asociado

Cada tarea está relacionada con un proyecto mediante una clave foránea (`ForeignKey`).

## Instalación y ejecución

1. Instalar Django:

   ```bash
   pip install django
   ```

2. (Opcional) Definir una clave secreta propia en producción mediante la variable
   de entorno `DJANGO_SECRET_KEY`. El valor predeterminado es solo para desarrollo.

3. Aplicar las migraciones:

   ```bash
   python manage.py makemigrations
   python manage.py migrate
   ```

4. Crear un superusuario para acceder al administrador:

   ```bash
   python manage.py createsuperuser
   ```

5. Ejecutar el servidor:

   ```bash
   python manage.py runserver
   ```

6. Ingresar al administrador de Django:

   http://127.0.0.1:8000/admin/

## Base de datos
El proyecto utiliza SQLite. La base local (`db.sqlite3`) no se incluye en el
repositorio porque puede contener cuentas, sesiones y otros datos locales.
Al aplicar las migraciones se crea una base nueva.

## Autor
Estudiante: Jose Miguel Rodriguez Escobar
