# Conexión de React con MySql Local

Para un proyecto web que sera mucho más que un sitio estático es fundamental agregar la **manipulación de datos**, esto provoca más dinamismo a un sitio web. Este es el **paso** a **paso** de como **conectar tu base de datos de MySql con React**.

### El ejemplo que utilizaremos sera un CRUD de tareas.

## 1. Crear base de datos

En mi caso utilizare **DBeaver** como cliente de SQL para administrar mi base de datos.

[Descarga DBeaver - Sitio Oficial](https://dbeaver.io/download/)

```sql
/* Create DB */
CREATE DATABASE tasks_db;
use tasks;

/* Create table */
CREATE TABLE tasks (
    id INT PRIMARY KEY AUTO_INCREMENT,
    todo TEXT NOT NULL,
    creation_date DATE NOT NULL,
    creation_time TIME NOT NULL
);
```

## 2. Cofigurar Servidor con NodeJS

Como primer paso es necesario inicializar un nuevo paquete npm para instalar las librerias necesarias, ***se requiere tener instalado de NodeJS***.

Dentro del proyecto incluí una carpeta destinada al servidor:

![Server Dir](./assets/2_1.png "Server Dir")

Con la terminal ingresamos a la carpeta creada e inicializamos nuestro **package.json** con **npm** para poder instalar las librerias requeridas.

```bash
cd server
npm init -y
```

### Instalar y configurar Express

Para desarrollar nuestra **API** instalaremos **express**:

```bash
npm i express
```



---
> configurar express

> instalar mysql2

