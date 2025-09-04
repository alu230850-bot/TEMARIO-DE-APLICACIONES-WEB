# TEMARIO-DE-APLICACIONES-WEB
# 1. Introducción al Desarrollo Web
<img width="300" height="172" alt="image" src="https://github.com/user-attachments/assets/4bbe593f-5d24-4263-8dc0-a869903ecaeb" />

## Historia y evolución del desarrollo web

El desarrollo web comenzó en la década de los 90 con la creación de la World Wide Web por Tim Berners-Lee. Inicialmente, las páginas web eran simples documentos HTML estáticos. A medida que la web evolucionó, se añadieron tecnologías como CSS para el diseño visual y JavaScript para la interactividad en el navegador. Posteriormente, surgieron lenguajes de servidor como PHP y bases de datos como MySQL, permitiendo crear aplicaciones web dinámicas.

La web continuó evolucionando con la aparición de frameworks y bibliotecas como jQuery, React, Angular y Vue para el frontend, y Node.js, Django, y Ruby on Rails para el backend. Hoy en día, las aplicaciones web pueden ser tan sofisticadas como cualquier aplicación de escritorio, incorporando tecnologías modernas como SPA y PWA.

## Tipos de aplicaciones web

- **Aplicaciones estáticas:** Son páginas cuyo contenido no cambia y se presenta igual para cada usuario. Ejemplo: portafolios simples o landing pages.
- **Aplicaciones dinámicas:** El contenido cambia en función de la interacción del usuario y datos provenientes de bases de datos. Ejemplo: foros, blogs, tiendas online.
- **SPA (Single Page Applications):** Aplicaciones que funcionan en una sola página HTML y actualizan el contenido dinámicamente sin recargar la página completa. Ejemplo: Gmail, Trello.
- **PWA (Progressive Web Applications):** Aplicaciones web que ofrecen experiencia similar a una app nativa, incluyendo acceso offline, notificaciones push y posibilidad de instalarse en dispositivos.

---

# 2. Arquitectura de aplicaciones web
<img width="317" height="165" alt="image" src="https://github.com/user-attachments/assets/02872b7f-123e-47ea-ad97-e7bd75aac2fd" />

## Cliente-Servidor

La arquitectura cliente-servidor implica que el usuario (cliente) realiza peticiones a un servidor, que procesa la información y responde con los datos solicitados. El cliente suele ser el navegador web, mientras que el servidor ejecuta la lógica y gestiona el acceso a la base de datos.

## Arquitectura de tres capas

- **Presentación:** Interfaz que interactúa con el usuario (frontend).
- **Lógica de negocio:** Procesa la información y aplica reglas (backend).
- **Datos:** Maneja el almacenamiento y recuperación de datos (base de datos).

Esta separación facilita la organización, mantenimiento y escalabilidad de las aplicaciones web.

## REST y API-first design

- **REST (Representational State Transfer):** Es un estilo arquitectónico para el diseño de servicios web, basado en el uso de recursos y operaciones HTTP (GET, POST, PUT, DELETE). Permite que aplicaciones diferentes se comuniquen fácilmente.
- **API-first design:** Enfoque donde la API se diseña antes que la implementación de la aplicación, asegurando que el frontend y el backend puedan desarrollarse de manera independiente y comunicarse correctamente.

---

# 3. Lenguajes y tecnologías fundamentales
<img width="326" height="154" alt="image" src="https://github.com/user-attachments/assets/4c38363f-53e8-4243-81ff-f5bf1fbdc9af" />

- **HTML (HyperText Markup Language):** Lenguaje de marcado que define la estructura básica de las páginas web.
- **CSS (Cascading Style Sheets):** Lenguaje de estilos para definir la apariencia visual de las páginas.
- **JavaScript:** Lenguaje de programación que permite la interactividad y lógica en el navegador.
- **PHP:** Lenguaje de programación del lado del servidor, ampliamente usado para aplicaciones dinámicas.
- **MySQL:** Sistema de gestión de bases de datos relacional, utilizado para almacenar y acceder a datos.

---

# 4. Control de versiones
<img width="268" height="164" alt="image" src="https://github.com/user-attachments/assets/730d2e22-fe2f-4bda-a875-04adc6b2efc3" />

## Git y GitHub

- **Git:** Sistema de control de versiones distribuido que permite gestionar los cambios en el código fuente de manera eficiente, facilitando la colaboración entre varios desarrolladores.
- **GitHub:** Plataforma basada en Git que permite alojar repositorios, colaborar, revisar código y gestionar proyectos de desarrollo.

## Flujo de trabajo con ramas

- **Branching (ramas):** Permite trabajar en nuevas funcionalidades o correcciones de errores sin afectar la rama principal (main/master).
- **Merge:** Integración de los cambios realizados en diferentes ramas.
- **Pull Requests:** Solicitud para que los cambios de una rama sean revisados y fusionados en la rama principal, facilitando la colaboración y la revisión de código.
Propósito de Aprendizaje 2: Desarrollar componentes y funcionalidades de una aplicación web
# 1. Diseño e implementación del frontend
<img width="266" height="171" alt="image" src="https://github.com/user-attachments/assets/0d4ccd8d-de53-4800-af03-64bd794acb93" />

## Maquetación, Wireframe y Mockup

- **Maquetación:** Es la organización visual de los elementos en una página web. Se realiza usando HTML para la estructura y CSS para posicionar y estilizar los componentes.
- **Wireframe:** Esquema básico (boceto) que representa la distribución de los elementos principales de una interfaz, sin detalles visuales. Ayuda a definir la experiencia de usuario (UX).
- **Mockup:** Es una versión más detallada, casi definitiva, del diseño de la interfaz. Incluye colores, tipografía, imágenes y otros detalles visuales.

Estos pasos son fundamentales antes de empezar a programar el frontend para asegurar que el diseño cumple con los requisitos y es fácil de usar.

## API

El frontend normalmente se comunica con el backend mediante APIs (Interfaz de Programación de Aplicaciones). Una API define cómo el frontend puede enviar y recibir datos del servidor, generalmente usando el formato JSON y el protocolo HTTP (a través de métodos como GET, POST, PUT, DELETE).

Ejemplo de llamada a una API con JavaScript (fetch):

```js
fetch('https://miapp.com/api/usuarios')
  .then(response => response.json())
  .then(data => console.log(data));
```

---

# 2. Diseño e implementación del backend
<img width="279" height="152" alt="image" src="https://github.com/user-attachments/assets/90df00ad-38d6-4cc3-a1d4-adb6938c275f" />

## Servidor

El servidor es el programa que recibe las peticiones del cliente (navegador), procesa la lógica de negocio y envía respuestas adecuadas. Se puede implementar en lenguajes como PHP, JavaScript (Node.js), Python, etc.

Ejemplo de servidor con Node.js y Express:
```js
const express = require('express');
const app = express();

app.get('/api/usuarios', (req, res) => {
  res.json([{ nombre: "Juan" }, { nombre: "Ana" }]);
});

app.listen(3000, () => console.log('Servidor funcionando en puerto 3000'));
```

## Manejo de peticiones y respuestas HTTP

El backend recibe peticiones HTTP (GET, POST, PUT, DELETE) y responde con datos o mensajes. Cada método se usa para diferentes operaciones:
- **GET:** Obtener datos.
- **POST:** Crear nuevos datos.
- **PUT/PATCH:** Actualizar datos existentes.
- **DELETE:** Eliminar datos.

## Conexión a bases de datos (MySQL, PostgreSQL, MongoDB)

El backend se conecta a bases de datos para guardar y recuperar información. Ejemplo de conexión a MySQL con Node.js:

```js
const mysql = require('mysql');
const conexion = mysql.createConnection({
  host: 'localhost',
  user: 'usuario',
  password: 'contraseña',
  database: 'mi_base_de_datos'
});
conexion.connect();
```

---

# 3. Bases de datos
<img width="274" height="177" alt="image" src="https://github.com/user-attachments/assets/6ec69a84-284a-484b-b1de-fc0730ad0b3d" />

## Modelado de datos y relaciones

Consiste en diseñar cómo se almacenará la información: qué tablas habrá, qué campos tendrán y cómo se relacionan (uno a uno, uno a muchos, muchos a muchos).

Ejemplo: Usuarios y Publicaciones (un usuario puede tener muchas publicaciones).

## ORM (Object Relational Mapping)

Un ORM permite interactuar con la base de datos usando objetos y métodos en lugar de escribir directamente consultas SQL. Facilita el desarrollo y mantenimiento.

Ejemplo de ORM en Node.js con Sequelize:
```js
const User = sequelize.define('User', {
  nombre: Sequelize.STRING,
  email: Sequelize.STRING
});
User.findAll().then(users => console.log(users));
```

## CRUD desde el backend

Las operaciones CRUD (Create, Read, Update, Delete) son fundamentales en cualquier aplicación web. El backend debe implementar endpoints para que el frontend pueda crear, leer, actualizar y eliminar recursos.

---

# 4. Seguridad básica en aplicaciones web
<img width="333" height="148" alt="image" src="https://github.com/user-attachments/assets/477b466c-794c-44b0-96aa-0100d6973119" />

## Validación de formularios

Es imprescindible validar los datos que los usuarios envían para evitar errores y ataques. La validación puede hacerse tanto en el frontend (JavaScript) como en el backend.

Ejemplo en HTML:
```html
<input type="email" required>
```

## Autenticación y autorización

- **Autenticación:** Verifica la identidad del usuario, por ejemplo, mediante inicio de sesión con usuario y contraseña.
- **Autorización:** Controla qué acciones puede realizar cada usuario según sus permisos (roles).

Ejemplo de autenticación con JWT en Node.js:

```js
const jwt = require('jsonwebtoken');
const token = jwt.sign({ userId: 1 }, 'secreto');

Propósito de Aprendizaje 3: Implementar y desplegar una aplicación web funcional
# 1. Integración de frontend y backend

## Interfaz de usuario Frontend

La interfaz de usuario (UI) es la parte visible de la aplicación web con la que interactúan los usuarios. Se construye con HTML para la estructura, CSS para el estilo y JavaScript para la interactividad. Es fundamental que la UI sea intuitiva, accesible y responsiva, adaptándose a distintos dispositivos.

Ejemplo de interfaz:
```html
<form id="loginForm">
  <input type="text" placeholder="Usuario" required>
  <input type="password" placeholder="Contraseña" required>
  <button type="submit">Ingresar</button>
</form>
```

## Manejo de API

El frontend se comunica con el backend a través de APIs (usualmente REST). Utiliza peticiones HTTP para enviar y recibir datos. El intercambio suele hacerse en formato JSON.

Ejemplo de consumo de API con JavaScript:
```js
fetch('https://miapp.com/api/usuarios')
  .then(response => response.json())
  .then(data => mostrarUsuarios(data));
```

## Proceso de Solicitud y Respuesta de Backend

El flujo típico es:
1. El usuario interactúa con la interfaz (ejemplo: envía un formulario).
2. El frontend envía una solicitud HTTP a la API del backend.
3. El backend recibe la solicitud, procesa la lógica, accede a la base de datos si es necesario y genera una respuesta.
4. El backend envía la respuesta al frontend.
5. El frontend muestra la información al usuario.

---

# 2. Almacenamiento en Servidor
<img width="310" height="163" alt="image" src="https://github.com/user-attachments/assets/d9f602d3-7898-45bc-946b-340d25ae159b" />

## Tipos de servidores

- **Servidor compartido:** Varios sitios web comparten los recursos de un mismo servidor físico. Económico pero menos flexible.
- **Servidor dedicado:** Un servidor físico exclusivo para un solo cliente. Mayor control y rendimiento.
- **VPS (Servidor Privado Virtual):** Un servidor físico dividido en varios entornos virtuales independientes.
- **Cloud:** Servicios en la nube que ofrecen escalabilidad y alta disponibilidad (ejemplo: AWS, Azure, Google Cloud).

## Servidores y servicios de hosting

El hosting es el servicio que permite publicar sitios y aplicaciones web en Internet. Entre los tipos más comunes están:
- **Hosting tradicional:** Espacio en servidores compartidos o dedicados.
- **Hosting en la nube:** Infraestructura escalable y flexible, paga por uso.
- **Plataformas especializadas:** GitHub Pages (para sitios estáticos), Netlify, Vercel, Heroku (para apps dinámicas).

## Proveedores de Servicios de Almacenamiento

Dependiendo de las necesidades de la aplicación, se puede usar almacenamiento local (en el servidor) o servicios externos para guardar archivos, imágenes o bases de datos:
- **Amazon S3:** Almacenamiento de objetos en la nube.
- **Google Cloud Storage:** Almacenamiento escalable de archivos.
- **Azure Blob Storage:** Servicio para guardar grandes volúmenes de datos no estructurados.
- **Firebase Storage:** Rápido y fácil de integrar con apps móviles y web.
---

# 3. Optimización y rendimiento
<img width="293" height="165" alt="image" src="https://github.com/user-attachments/assets/9bcd1059-0ee0-4db9-8a9b-caa8f02975a0" />

## Optimización de recursos (imágenes, scripts)

- **Minificación:** Reducir el tamaño de archivos CSS y JavaScript eliminando espacios y comentarios.
- **Compresión de imágenes:** Usar formatos modernos (WebP) y reducir la resolución para acelerar la carga.
- **Carga diferida (lazy loading):** Cargar imágenes y scripts solo cuando se necesitan.
- **Uso de CDN:** Distribuir contenido estático desde servidores cercanos al usuario.

## Despliegue de aplicaciones web

- **Despliegue manual:** Subir archivos por FTP o SSH al servidor.
- **Despliegue automático:** Usar plataformas como Netlify, Vercel o Heroku que detectan cambios en el repositorio y despliegan automáticamente.
- **Contenedores:** Usar Docker para empaquetar y desplegar aplicaciones de manera consistente.

## CI/CD básico (Integración y entrega continua)

- **CI (Integración Continua):** Automatiza la integración de cambios de código, ejecutando pruebas automáticamente en cada commit.
- **CD (Entrega/Despliegue Continua):** Automatiza la publicación de la aplicación tras aprobar los cambios.
- **Herramientas comunes:** GitHub Actions, GitLab CI, Jenkins.

## Documentación del proyecto

- **README:** Archivo esencial que describe el objetivo del proyecto, instalación, uso y contribución.
- **Comentarios en código:** Facilitan el mantenimiento y comprensión.
- **Wiki y documentación técnica:** Explicaciones detalladas sobre la arquitectura, API y procesos importantes para desarrolladores y usuarios.
