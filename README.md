

## Welcome to CVMonline repository!

## Content table

- [:star: Entorno de configuración](#star-entorno-de-configuración)
    - [:globe_with_meridians: Instalación de la aplicación](#globe_with_meridians-instalación-de-la-aplicación)
        - [:globe_with_meridians: Composer steps](#globe_with_meridians-composer-steps)
        - [:globe_with_meridians: Node configuration steps](#globe_with_meridians-node-configuration-steps)
        - [:globe_with_meridians: Database configuration steps](#globe_with_meridians-database-configuration-steps)
        - [:globe_with_meridians: Last steps](#globe_with_meridians-last-steps)
- [:globe_with_meridians: Deploy](#globe_with_meridians-deploy)
    - [:globe_with_meridians: QA deploy](#globe_with_meridians-qa-deploy)
    - [:globe_with_meridians: Client deploy](#globe_with_meridians-client-deploy)
- [:four_leaf_clover: Extras](#four_leaf_clover-extras)
    - [:robot: Prototypes](#robot-prototypes)

## :star: Entorno de configuración

### :globe_with_meridians: Instalación de la aplicación
- Luego de instalar las dependencias de PHP, debes ejecutar los siguientes comandos para completar la instalación:
  ### :globe_with_meridians: Composer steps
- `make start`

- `make login-php`

- `php -d memory_limit=-1 /usr/local/bin/composer self-update 1.10.20`

- `php -d memory_limit=-1 /usr/local/bin/composer install`

- `exit`

### :globe_with_meridians: Node configuration steps
- `nvm install 6.17.1`

- `nvm use 6`

- `npm install`

- `npm run dev`

- `npm start`

### :globe_with_meridians: Database configuration steps

- `sudo chmod -R 777 storage/`
- `configure database connection`
- `user: root`
- `pass: cvmonline`
- `port: 33079`
- Por último copia y pega el contenido del archivo `mysql/cvmonline20211011.sq` en  la consola MySQL y ejecútalo.

### :globe_with_meridians: Last steps
- Asegúrate de tener instalada la versión 6 de Node. De tenerla, ejecuta el comando **nvm use 6**
- Por último, **npm run watch**

## :globe_with_meridians: Deploy

### :globe_with_meridians: QA deploy

- make deploy
- nvm use 6
- npm run dev

### :globe_with_meridians: Client deploy

- git pull fork master
- git pull origin master
- git push origin master
- php artisan migrate
- npm run dev

## :four_leaf_clover: Extras

### :robot: Prototypes

    In order to see the project prototypes you must follow the next step:


- Access `http://localhost/cvmonline/prototype/`
- Enter credentials:
  - admin: admin@gmail.com
  - password: 123456

