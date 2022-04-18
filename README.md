## Welcome to CVMonline repository!

## Content table

- [:star:Entorno de configuración](#star-entorno-de-configuración)
    - [:star2:Herramientas utilizadas](#star2-herramientas-utilizadas)
    - [:hammer_and_wrench:Configuración del entorno](#hammer_and_wrench-configuración-del-entorno)
    - [:globe_with_meridians:Instalación de la aplicación](#globe_with_meridians-instalación-de-la-aplicación)
        - [:globe_with_meridians:Composer steps](#globe_with_meridians-composer-steps)
        - [:globe_with_meridians:Node configuration steps](#globe_with_meridians-node-configuration-steps)
        - [:globe_with_meridians:Database configuration steps](#globe_with_meridians-database-configuration-steps)
        - [:globe_with_meridians:Last steps](#globe_with_meridians-last-steps)


## :star: Entorno de configuración

### :star2: Herramientas utilizadas

1. [Instalar Docker](https://www.docker.com/get-started) :whale:
2. :cyclone:Clonar este proyecto: `git clone git@github.com:fjmn2001/cvmonline.git`

### :hammer_and_wrench: Configuración del entorno

- Crear un archivo de entorno local si es necesario:  `cp .env .env.example`:page_facing_up:

### :globe_with_meridians: Instalación de la aplicación
- Luego de instalar las dependencias de PHP, debes ejecutar los siguientes comandos para completar la instalación:
  ### :globe_with_meridians: Composer steps
    - 	    make start  
    -       make login-php  
    -	    php -d memory_limit=-1 /usr/local/bin/composer self-update 1.10.20  
    -	    php -d memory_limit=-1 /usr/local/bin/composer install  
    -      exit  

  ### :globe_with_meridians: Node configuration steps
    -     nvm install 6.17.1 
    -     nvm use 6 
    -     npm install
    -     npm run dev

  ### :globe_with_meridians: Database configuration steps

    -     sudo chmod -R 777 storage/  
    -     configure database connection
      	- user: root
      	- pass: cvmonline
      	- port: 33079
      	- Por último copia y pega el contenido del archivo `mysql/cvmonline20211011.sq` en  la consola MySQL y ejecútalo.

  ### :globe_with_meridians: Last steps
    - Asegúrate de tener instalada la versión 6 de Node y de tenerla, ejecuta el comando **nvm use 6**
    - Por último, **npm run watch**
