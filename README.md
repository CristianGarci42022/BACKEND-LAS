
# Tus Cuentas en Orden

"Tus Cuentas en Orden" es un proyecto que se enfoca en simplificar la gestión de gastos. Proporciona una API con diversos endpoints para ver, crear, actualizar y eliminar registros de gastos. ¡Controla tus finanzas de manera eficiente con nuestra plataforma!

## Pre-requisitos 📋

Para la correcta ejecución de este proyecto, necesitas tener las siguientes tecnologías instaladas en tu ordenador.
* PHP ^8.1
* Composer 2
* Xampp Base de datos MySql


## Instalación 🔧

1. Clona este proyecto.

        git clone https://github.com/CristianGarci42022/Crud-LAS


2. Instala las dependencias de PHP con composer.

        composer install


3. Crea una nueva base de datos con tu gestor de base de datos preferido. Como sugerencia podrías crear una base de datos llamada `Accounts-in-Order`..
   # IMPORTANTE:
   - Es indispensable tener clonado y en ejecución el proyecto [Crud-LAS](https://github.com/CristianGarci42022/Crud-LAS)
   - Es indispensable estar ejecutando Xampp para la administracion de la base de datos llamada `Accounts-in-Order`.

5. Crea una copia del archivo env.example, renombralo como .env y configura las variables de entorno correspondientes, preferiblemente las variables para la conexión a la base de datos.
```json
APP_NAME=BudgetBuddy
APP_ENV=local
APP_KEY=
APP_DEBUG=true
APP_URL=http://localhost

LOG_CHANNEL=stack
LOG_DEPRECATIONS_CHANNEL=null
LOG_LEVEL=debug

DB_CONNECTION=mysql
DB_HOST=127.0.0.1
DB_PORT=3306
DB_DATABASE=tu_base_de_datos
DB_USERNAME=tu_username
DB_PASSWORD=tu_password

BROADCAST_DRIVER=log
CACHE_DRIVER=file
FILESYSTEM_DISK=local
QUEUE_CONNECTION=sync
SESSION_DRIVER=file
SESSION_LIFETIME=120

MEMCACHED_HOST=127.0.0.1

REDIS_HOST=127.0.0.1
REDIS_PASSWORD=null
REDIS_PORT=6379

MAIL_MAILER=smtp
MAIL_HOST=mailpit
MAIL_PORT=1025
MAIL_USERNAME=null
MAIL_PASSWORD=null
MAIL_ENCRYPTION=null
MAIL_FROM_ADDRESS="hello@example.com"
MAIL_FROM_NAME="${APP_NAME}"

AWS_ACCESS_KEY_ID=
AWS_SECRET_ACCESS_KEY=
AWS_DEFAULT_REGION=us-east-1
AWS_BUCKET=
AWS_USE_PATH_STYLE_ENDPOINT=false

PUSHER_APP_ID=
PUSHER_APP_KEY=
PUSHER_APP_SECRET=
PUSHER_HOST=
PUSHER_PORT=443
PUSHER_SCHEME=https
PUSHER_APP_CLUSTER=mt1

VITE_APP_NAME="${APP_NAME}"
VITE_PUSHER_APP_KEY="${PUSHER_APP_KEY}"
VITE_PUSHER_HOST="${PUSHER_HOST}"
VITE_PUSHER_PORT="${PUSHER_PORT}"
VITE_PUSHER_SCHEME="${PUSHER_SCHEME}"
VITE_PUSHER_APP_CLUSTER="${PUSHER_APP_CLUSTER}"
```

5. Genera una APP_KEY.
```bash
php artisan key:generate
```

6. Ejecuta las migraciones y los seeders.
```bash
php artisan migrate:fresh --seed
```

7. Ejecuta el proyecto laravel.
```bash
php artisan serve
```

## Construido con 🛠️

- [PHP 8.1](https://www.php.net/releases/8.1/es.php)
- [Laravel](https://laravel.com/docs/10.x)
- [Composer 2.6.5](https://getcomposer.org/)
- [MySQL ](https://dev.mysql.com/downloads/mysql/)


## Endpoints 🔗

A continuación se detallan los endpoints disponibles en la API:

| Método  | Ruta                        | Descripción                                                                                  |
|---------|-----------------------------|----------------------------------------------------------------------------------------------|
| GET     | /api/expenses               | Devuelve un array de gastos.                                                                 |
| POST    | /api/expenses               | Crea un gasto utilizando la información enviada dentro del `body` de la solicitud.           |
| GET     | /api/expenses/`{expense}`   | Devuelve el objeto de gasto con el `id` especificado.                                        |
| PUT     | /api/expenses/`{expense}`   | Actualiza el gasto con el `id` especificado utilizando los datos del `body` de la solicitud. |
| DELETE  | /api/expenses/`{expense}`   | Elimina el gasto con el `id` especificado.                                                   |


## Autor 🖋️

- [@CristianGarcia](https://github.com/CristianGarci42022)
