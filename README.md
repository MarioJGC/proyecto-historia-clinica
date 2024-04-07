# Proyecto Historia Clinica UC

Este es un proyecto que utiliza Angular para el frontend, Nest.js para el backend y MySQL como base de datos. El objetivo principal de este proyecto es proporcionar una plataforma integral para la gestión de historias clínicas de pacientes en el ámbito de la odontología. La aplicación permitirá a los profesionales de la odontología registrar y acceder de manera eficiente a la información relevante de los pacientes, incluyendo historiales médicos, tratamientos realizados, radiografías, notas de consulta, entre otros datos pertinentes.

## Instalación

### Requisitos Previos

Asegúrate de tener instalado lo siguiente antes de comenzar:

- Node.js y npm: [Descargar e Instalar](https://nodejs.org/)
- Angular CLI: `npm i @angular/cli@16.2.10`
- Nest CLI: `npm i @nestjs/core@10.2.8`
- MySQL Server: `https://dev.mysql.com/downloads/mysql/8.0.html`

### Pasos de Instalación

1. Clona este repositorio en tu máquina local:

    ```bash
    git clone https://github.com/MarioJGC/proyecto-historia-clinica.git
    ```

2. Instala las dependencias del frontend y backend:

    ```bash
    cd proyecto-historia-clinica/frontend
    npm install

    cd ../backend
    npm install
    ```

3. Configura la base de datos MySQL:

    - Crea una base de datos MySQL llamada `db_historia_clinica`.
    - En el archivo `backend/src/config/database.config.ts`, configura los detalles de tu base de datos:

    ```typescript
    export default {
        type: 'mysql',
        host: 'localhost',
        port: 3306,
        username: 'tu_usuario',
        password: 'tu_contraseña',
        database: 'nombre_base_de_datos',
        entities: [__dirname + '/../**/*.entity{.ts,.js}'],
        synchronize: true,
    };
    ```

    Asegúrate de cambiar `tu_usuario`, `tu_contraseña` y `nombre_base_de_datos` con los detalles correctos.

4. Inicia el servidor Nest.js:

    ```bash
    cd ../backend
    npm run start:dev
    ```

5. Inicia la aplicación Angular:

    ```bash
    cd ../frontend
    ng serve
    ```

Ahora puedes acceder a la aplicación en tu navegador visitando `http://localhost:4200`.

## Estructura del Proyecto

- **frontend/**: Contiene el código fuente del frontend Angular.
- **backend/**: Contiene el código fuente del backend Nest.js.
- **database/**: Puedes colocar aquí scripts SQL para inicializar la base de datos.

## Contribución

Si quieres contribuir a este proyecto, sigue estos pasos:

1. Haz un fork del repositorio.
2. Crea una nueva rama (`git checkout -b feature/nueva-funcionalidad`).
3. Haz tus cambios y haz commit (`git commit -am 'Agrega nueva funcionalidad'`).
4. Sube tus cambios a tu rama (`git push origin feature/nueva-funcionalidad`).
5. Crea un Pull Request.

## Licencia

Este proyecto está bajo la licencia MIT. Para más detalles, consulta el archivo LICENSE.
