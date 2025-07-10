Tarea: Investigación y Desarrollo de un CRUD con Django
1)🔹¿Qué es un CRUD;

🔵Crear (Create): Añadir nuevos datos o registros al sistema, como registrar un nuevo usuario o agregar un producto a una tienda en línea.

🔴Leer (Read): Consultar o visualizar los datos existentes, por ejemplo, mostrar la lista de usuarios o buscar información específica en la base de datos.

🟣Actualizar (Update): Modificar datos ya existentes, como editar el perfil de un usuario o cambiar el precio de un producto.

🟢Borrar (Delete): Eliminar datos del sistema, como borrar una cuenta o quitar un producto del inventario.

🔷Cuál es su propósito en el desarrollo de aplicaciones web?;
CRUD es el conjunto de las cuatro operaciones básicas para gestionar datos en aplicaciones web: Crear, Leer, Actualizar y Eliminar. Su propósito es facilitar la administración de la información almacenada, permitiendo a usuarios y desarrolladores agregar, consultar, modificar y borrar registros de manera eficiente. En el desarrollo web, CRUD es fundamental porque constituye la base para construir funcionalidades dinámicas y manejar bases de datos, agilizando el proceso de desarrollo y mejorando la experiencia del usuario. Además, muchas herramientas y frameworks modernos facilitan la creación rápida de aplicaciones CRUD, optimizando tiempo y recursos en proyectos de software.

🔶Un ejemplo claro de aplicación web que utiliza una estructura CRUD es un sistema de gestión de contenidos (CMS), como WordPress. En este tipo de plataforma, los usuarios pueden:
-Crear nuevas entradas o páginas.
-Leer el contenido existente en el sitio.
-Actualizar o editar publicaciones y páginas.
-Eliminar contenido obsoleto o irrelevante.
Estas operaciones; permiten gestionar de forma sencilla y eficiente toda la información del sitio web, y son posibles gracias a la implementación de una estructura CRUD en el backend del sistema.
Otros ejemplos comunes; incluyen tiendas online, donde se pueden gestionar productos, clientes y pedidos, y redes sociales, donde los usuarios crean, consultan, modifican y eliminan publicaciones y perfiles.

2)🔹¿Qué son los patrones de arquitectura en desarrollo de software?;
Los patrones de arquitectura en desarrollo de software son soluciones reutilizables para organizar y estructurar sistemas, facilitando el diseño eficiente y la toma de decisiones técnicas. Ayudan a mejorar la calidad, mantenibilidad y escalabilidad de las aplicaciones.

🔶¿Qué es el patrón MVC (Modelo–Vista–Controlador)?; El patrón MVC es una forma de organizar aplicaciones dividiéndolas en tres partes: Modelo (gestiona los datos), Vista (muestra la información) y Controlador (coordina la interacción entre ambos). Esto facilita el desarrollo, mantenimiento y escalabilidad del software.

🔶El patrón MVT, usado en Django, organiza las aplicaciones en tres partes: Modelo (gestiona los datos), Vista (contiene la lógica de negocio) y Template (define la presentación). Esta estructura separa claramente los datos, la lógica y la interfaz, facilitando el desarrollo y mantenimiento.

🟧Diferencias entre MVC y MVT.En resumen: MVC utiliza un controlador explícito para coordinar la lógica y la presentación, mientras que MVT delega esa responsabilidad a la vista y separa la presentación en plantillas, haciendo el flujo más automatizado y el código más desacoplado, especialmente en frameworks como Django

🔶¿Cuál de estos dos patrones se usa en Django?: En Django se utiliza el patrón MVT (Modelo–Vista–Template), que es una variante del patrón MVC adaptada a la filosofía y estructura de este framework

3)🔹 ¿Cómo se estructura un proyecto en Django? 
🔶Un proyecto en Django se estructura siguiendo el patrón MVT (Modelo–Vista–Template) y se organiza en varios archivos y directorios clave:
-manage.py: Herramienta de línea de comandos para gestionar el proyecto (ejecutar el servidor, migraciones, etc.).

🔶Directorio principal del proyecto: Contiene archivos de configuración global:

__init__.py: Indica que el directorio es un paquete de Python.

-settings.py: Configuración general (base de datos, apps instaladas, seguridad, etc.).

-urls.py: Definición de rutas URL y enrutamiento de solicitudes.

-asgi.py y wsgi.py: Configuración para servidores ASGI/WSGI.

🔶Dentro de cada aplicación creada en el proyecto, la estructura básica incluye:

-models.py: Define los modelos (estructura y acceso a los datos).

-views.py: Contiene las vistas (lógica de negocio y procesamiento de solicitudes).

-templates/: Carpeta donde se guardan las plantillas (archivos HTML para la presentación).

-urls.py: (Opcional en cada app) Define rutas específicas de la aplicación.

🔶El flujo típico es:

*El usuario hace una solicitud a una URL.

*Django usa urls.py para dirigir la solicitud a la vista correspondiente.

*La vista (views.py) procesa la lógica, interactúa con los modelos si es necesario, y prepara los datos.

*La vista renderiza una plantilla (templates/) con esos datos.

*Se devuelve la respuesta al usuario.

*Esta estructura fomenta una separación clara entre la lógica de negocio, la manipulación de datos y la presentación, facilitando el mantenimiento y la escalabilidad del proyecto.

🔍 En resumen; Un proyecto en Django se organiza en un directorio principal con archivos de configuración (settings.py, urls.py, etc.) y uno o más apps. Cada app contiene archivos para modelos (datos), vistas (lógica) y plantillas (presentación). Las URLs dirigen las solicitudes a las vistas, que interactúan con los modelos y renderizan las plantillas para mostrar la información al usuario. Esta estructura sigue el patrón MVT y facilita el desarrollo ordenado y mantenible.

🔹Explicar brevemente el rol de los modelos, vistas, templates y URLs.






