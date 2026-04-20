# Mini Core MVC - Sistema de Gestión de Ventas y Comisiones

## Descripción

Este proyecto consiste en una aplicación web desarrollada con Django REST Framework en el backend y React + Vite en el frontend.
El sistema permite registrar ventas, consultar vendedores, aplicar reglas de comisión y calcular comisiones por rango de fechas. La aplicación sigue una estructura basada en la separación de responsabilidades propia del patrón MVC/MVT, donde el backend administra los datos y la lógica de negocio, y el frontend se encarga de la presentación e interacción con el usuario.

## Objetivo

Implementar el ejercicio MVC de semestres pasados mediante una aplicación funcional con backend, frontend, repositorio en GitHub y despliegue en la nube.

## Tecnologías utilizadas

* Python
* Django
* Django REST Framework
* React
* Vite
* Axios
* SQLite
* Render

## Funcionalidades principales

* Listado de ventas registradas
* Registro de nuevas ventas
* Eliminación de ventas
* Consulta de vendedores
* Gestión de reglas de comisión
* Cálculo de comisiones por rango de fechas
* Resumen de comisiones por vendedor
* Visualización de detalle individual de comisiones

## Estructura del proyecto

```text
mini-core-mvc-django/
├── backend/
│   ├── commission_app/
│   ├── commission_project/
│   ├── requirements.txt
│   └── manage.py
└── frontend/
    ├── src/
    ├── public/
    ├── package.json
    └── vite.config.js
```

## Ejecución local

### Backend

1. Ingresar a la carpeta `backend`.

2. Crear el entorno virtual:

   `python -m venv env`

3. Activar el entorno virtual en Windows PowerShell:

   `.\env\Scripts\Activate.ps1`

4. Instalar dependencias:

   `pip install -r requirements.txt`

5. Aplicar migraciones:

   `python manage.py migrate`

6. Cargar datos iniciales:

   `python manage.py loaddata commission_app/fixtures/initial_data.json`

7. Ejecutar el servidor:

   `python manage.py runserver`

Backend disponible en: `http://127.0.0.1:8000/api/`

### Frontend

Crear un archivo `.env` dentro de la carpeta `frontend` con el siguiente contenido:

`VITE_API_URL=http://127.0.0.1:8000`

Luego:

1. Ingresar a la carpeta `frontend`.

2. Instalar dependencias:

   `npm install`

3. Ejecutar el servidor de desarrollo:

   `npm run dev`

Frontend disponible en: `http://localhost:3000/`

## Endpoints principales

- `GET /api/vendedores/`
- `GET /api/reglas/`
- `GET /api/ventas/`
- `POST /api/ventas/`
- `DELETE /api/ventas/{id}/`
- `POST /api/comisiones/calcular/`

## Estado del proyecto

Proyecto funcional en entorno local con backend y frontend conectados correctamente.

## Autor

Roberto Zamora