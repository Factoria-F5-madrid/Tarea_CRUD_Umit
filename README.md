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
*Modelos: Son el capa de datos de la aplicación. Definen la estructura de la base de datos y gestionan la lógica relacionada con el almacenamiento, consulta y manipulación de los datos.

*Vistas: Encargadas de la lógica de negocio y el procesamiento de las solicitudes del usuario. Recogen datos de los modelos, realizan operaciones necesarias y pasan la información a los templates para su presentación.

*Templates: Son la capa de presentación. Se ocupan de mostrar los datos al usuario, utilizando HTML y el lenguaje de plantillas de Django para renderizar la información de manera dinámica.

*URLs: Definen las rutas que conectan las solicitudes del usuario con las vistas correspondientes, permitiendo que cada dirección web lleve a la función o clase adecuada dentro de la aplicación.

🔹¿Para qué se usa el signo “%%” en los templates?
🔶El signo {% %} en los templates de Django se usa para escribir etiquetas de plantilla (template tags), que permiten ejecutar lógica como bucles, condicionales o incluir otras plantillas dentro del HTML. Por ejemplo, {% for item in lista %} para iterar sobre una lista o {% if condicion %} para evaluar una condición.

4)🔹¿Cuál es el flujo de datos entre un formulario HTML y la base de datos en Django?

-El flujo de datos entre un formulario HTML y la base de datos en Django sigue estos pasos:

-El usuario llena y envía el formulario HTML en la página web.

-La solicitud (POST) llega a la vista de Django, que recibe los datos enviados por el usuario.

-La vista crea una instancia del formulario con los datos recibidos y valida la información usando métodos como is_valid().

-Si los datos son válidos, la vista guarda la información en la base de datos usando el método save() del formulario o del modelo.

-La vista puede redirigir al usuario a otra página (por ejemplo, una página de confirmación o lista de registros).

-Si hay errores de validación, la vista vuelve a mostrar el formulario con los mensajes de error correspondientes para que el usuario corrija los datos.

-Django facilita este proceso gestionando la validación, el guardado y la visualización de mensajes de error, lo que simplifica la interacción entre el formulario HTML y la base de datos.

5)🔹 ¿Qué herramientas o comandos ofrece Django para facilitar el desarrollo de un
CRUD, para qué es cada una? (Por ejemplo: startapp, makemigrations, migrate,
runserver, ModelForm, admin, etc.)

💎startapp: Crea una nueva aplicación dentro del proyecto Django, generando la estructura básica de archivos para modelos, vistas, templates, etc.

💎makemigrations: Detecta los cambios en los modelos y crea archivos de migración para actualizar la estructura de la base de datos.

💎migrate: Aplica las migraciones pendientes a la base de datos, creando o modificando tablas según los modelos definidos.

💎runserver: Inicia un servidor de desarrollo local para probar la aplicación en el navegador.

💎ModelForm: Clase que permite crear formularios basados automáticamente en modelos, facilitando la validación y el guardado de datos desde formularios HTML.

💎admin: Interfaz administrativa generada automáticamente por Django para gestionar modelos y realizar operaciones CRUD de manera rápida y visual.

💎shell: Permite acceder a una consola interactiva de Python con el entorno de Django cargado, útil para probar consultas y manipular datos manualmente.

💎createsuperuser: Crea un usuario administrador para acceder al panel de administración de Django.

💎collectstatic: Reúne archivos estáticos (CSS, JS, imágenes) para su despliegue en producción.

Estas herramientas y comandos automatizan tareas repetitivas y estructuran el desarrollo, permitiendo crear, leer, actualizar y eliminar datos de forma eficiente en aplicaciones Django.

6)🔹 ¿Cómo funciona el Admin de Django?
El Admin de Django es una interfaz web automática y configurable que permite a los administradores del sitio gestionar fácilmente los modelos y realizar operaciones CRUD (crear, leer, actualizar, eliminar) sobre los datos de la base de datos sin necesidad de programar vistas o formularios personalizados.

Funcionamiento básico:

Para usarlo, primero debes registrar tus modelos en el archivo admin.py de cada aplicación usando admin.site.register(TuModelo).

Luego, accedes al panel en http://127.0.0.1:8000/admin/ tras crear un superusuario con el comando createsuperuser y ejecutar el servidor con runserver.

El panel te muestra formularios y listados generados automáticamente para cada modelo registrado, permitiendo agregar, editar, eliminar y buscar registros de manera visual.

Puedes personalizar qué campos se muestran, cómo se filtran, y agregar acciones personalizadas editando las clases en admin.py.

Internamente, el admin usa el sistema de plantillas de Django para renderizar dinámicamente las páginas de administración, y automatiza rutas, formularios y validaciones para cada modelo registrado.

En resumen, el Admin de Django es una herramienta poderosa para la administración de datos y modelos, ideal para tareas administrativas y gestión interna de aplicaciones web.



