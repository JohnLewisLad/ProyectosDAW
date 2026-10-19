# Proyectos DAW 2024-2025

Aplicación web desarrollada con **Laravel** que reúne diferentes propuestas, ejercicios y funcionalidades trabajadas por alumnos del ciclo formativo de **Desarrollo de Aplicaciones Web (DAW)** durante el curso académico 2024-2025.

El proyecto sirve como espacio de experimentación y aprendizaje, integrando distintos ejemplos de desarrollo web en una misma aplicación.

## 🎯 Objetivo del proyecto

El objetivo es reunir y poner en práctica los conocimientos adquiridos durante el curso mediante el desarrollo de diferentes funcionalidades web.

La aplicación permite experimentar con aspectos habituales del desarrollo web, como la gestión de datos, las operaciones CRUD, la autenticación de usuarios, el enrutamiento y la integración de interfaces dinámicas.

## ✨ Funcionalidades

Entre los módulos y funcionalidades presentes en el proyecto se encuentran:

- **Dibujos:** listado paginado y operaciones para crear, consultar, modificar y eliminar dibujos.
- **Piedra, papel o tijera:** módulo de juego accesible desde la sección correspondiente de la aplicación.
- **Gestión de gastos:** sección para trabajar con registros de gastos.
- **Publicaciones (*Chirps*):** módulo de publicaciones con operaciones de gestión.
- **Autenticación de usuarios:** registro, inicio de sesión y funcionalidades relacionadas con la cuenta.
- **Perfil de usuario:** gestión de la información del perfil.

La disponibilidad de algunas secciones depende de la autenticación y de las rutas definidas en la aplicación.

## 🛠️ Tecnologías utilizadas

- **[Laravel 11](https://laravel.com/):** framework PHP para el desarrollo de la aplicación.
- **[PHP](https://www.php.net/):** lenguaje de programación del servidor (versión 8.2 o superior).
- **[SQLite](https://www.sqlite.org/):** base de datos configurada por defecto en el archivo de entorno de ejemplo.
- **[Tailwind CSS](https://tailwindcss.com/):** utilidades para la construcción de interfaces.
- **[Alpine.js](https://alpinejs.dev/):** interactividad en el cliente.
- **[Vite](https://vite.dev/):** herramientas para el desarrollo y la compilación de recursos frontend.
- **[Composer](https://getcomposer.org/):** gestión de dependencias PHP.
- **[Node.js y npm](https://nodejs.org/):** gestión de dependencias y herramientas frontend.

## 📋 Requisitos previos

Antes de instalar el proyecto, asegúrate de disponer de:

- PHP 8.2 o superior.
- Composer.
- Node.js y npm.
- Las extensiones de PHP necesarias para Laravel y SQLite.

También puedes utilizar el entorno Docker configurado mediante Laravel Sail, siempre que dispongas de Docker y sigas los requisitos de dicho entorno.

## 🚀 Instalación y puesta en marcha

### 1. Clonar el repositorio

```bash
git clone https://github.com/JohnLewisLad/ProyectosDAW.git
cd ProyectosDAW
```

### 2. Instalar las dependencias

Instala las dependencias de PHP y JavaScript:

```bash
composer install
npm install
```

### 3. Configurar el entorno

Crea el archivo de configuración local a partir del ejemplo:

```bash
cp .env.example .env
```

Genera la clave de la aplicación:

```bash
php artisan key:generate
```

### 4. Preparar la base de datos

La configuración de ejemplo utiliza SQLite. Crea el archivo de base de datos si todavía no existe:

```bash
touch database/database.sqlite
```

Comprueba que el archivo `.env` contiene la siguiente configuración:

```dotenv
DB_CONNECTION=sqlite
```

Ejecuta las migraciones para crear las tablas:

```bash
php artisan migrate
```

Si deseas utilizar otro sistema de base de datos, tendrás que adaptar la configuración del entorno y disponer del servidor correspondiente.

### 5. Compilar los recursos frontend

Para generar los recursos de la aplicación:

```bash
npm run build
```

Durante el desarrollo puedes utilizar el modo de actualización automática:

```bash
npm run dev
```

### 6. Iniciar el servidor

En una terminal, ejecuta:

```bash
php artisan serve
```

Abre en el navegador la dirección que indique Artisan, normalmente:

[http://127.0.0.1:8000](http://127.0.0.1:8000)

> **Nota:** la ruta principal de la aplicación redirige actualmente al inicio de sesión. Para acceder a las secciones protegidas, necesitarás una cuenta válida y completar la configuración que corresponda.

## 📁 Estructura del proyecto

El proyecto sigue la estructura habitual de una aplicación Laravel:

| Directorio | Descripción |
|---|---|
| `app/` | Controladores, modelos y lógica de la aplicación. |
| `bootstrap/` | Inicialización del framework. |
| `config/` | Configuración de los servicios y componentes. |
| `database/` | Migraciones, factorías y seeders. |
| `public/` | Punto de entrada y recursos públicos. |
| `resources/` | Vistas y recursos frontend. |
| `routes/` | Definición de las rutas de la aplicación. |
| `storage/` | Archivos generados, registros y otros datos de almacenamiento. |
| `tests/` | Pruebas automatizadas. |

## 🎓 Contexto académico

Este repositorio está vinculado al aprendizaje y la práctica del desarrollo de aplicaciones web durante el curso 2024-2025.

Los módulos incluidos permiten trabajar con diferentes conceptos y técnicas de programación web, así como servir de referencia para explorar distintas soluciones dentro de una aplicación basada en Laravel.

## 📄 Licencia

Este proyecto se distribuye bajo la **licencia MIT**, una licencia de código abierto que permite utilizar, copiar, modificar, fusionar, publicar, distribuir, sublicenciar y comercializar el software, siempre que se respeten sus condiciones, incluida la conservación del aviso de copyright y del texto de la licencia.

Consulta el archivo [`LICENSE`](LICENSE) para conocer los términos completos de la licencia.

ESte código esta disponible públicamente para fomentar el aprendizaje, la colaboración y el intercambio de conocimientos
