# EVALUACION_MODULO_6

M6_Evaluación del módulo[Actividad Evaluada]

Evaluación del módulo
Contexto de la actividad

En la actualidad, las aplicaciones empresariales necesitan comunicarse entre sí a través de servicios estandarizados y eficientes. El uso de servicios RESTful ha tomado gran relevancia por su ligereza, escalabilidad y facilidad de integración. El Spring Framework, mediante su módulo Spring Web, facilita la construcción de APIs REST robustas que permiten la interoperabilidad entre distintos sistemas. Esta actividad busca que los estudiantes diseñen e implementen un servicio REST con Spring para resolver un problema concreto que implique la integración entre sistemas.


Objetivo general

Desarrollar una API REST utilizando Spring Framework que permita la gestión de recursos compartidos entre distintas aplicaciones, aplicando buenas prácticas de diseño y principios de interoperabilidad.


Descripción del reto

Tu tarea es construir una API REST con Spring Boot que funcione como sistema de catálogo de productos para un conjunto de tiendas. Este servicio será consumido por diversas aplicaciones cliente (aplicaciones móviles, dashboards web, u otros servicios) y debe cumplir con los siguientes requerimientos:

Permitir operaciones CRUD sobre el recurso Producto.

Cada producto debe tener: id, nombre, descripción, precio, y stockDisponible.

Exponer endpoints REST que sigan convenciones (GET, POST, PUT, DELETE).

Utilizar anotaciones de Spring para definir los controladores, servicios y repositorios.

Serializar y deserializar datos en formato JSON.

Manejar errores mediante respuestas estandarizadas.

Incorporar control de versiones en los endpoints (/api/v1/productos).

Implementar CORS para permitir el acceso desde otros dominios.


Fases de desarrollo
Fase 1: Diseño del modelo y arquitectura del servicio

Define la clase Producto y su representación como recurso REST.

Crea un esquema de arquitectura con capas: Controlador, Servicio y Repositorio.

Diseña los endpoints siguiendo buenas prácticas REST y estilo plural (/productos, /productos/{id}).

Fase 2: Implementación del servicio con Spring Boot

Inicializa un proyecto Spring Boot con dependencias necesarias: spring-boot-starter-web, spring-boot-devtools, spring-boot-starter-data-jpa, H2 o MySQL.

Crea el controlador REST (ProductoController) con todos los métodos necesarios.

Implementa la lógica en la capa de servicio (ProductoService).

Configura un repositorio que interactúe con la base de datos (ProductoRepository).

Usa anotaciones como @RestController, @Service, @Repository, @RequestMapping, @PathVariable, @RequestBody.

Fase 3: Interoperabilidad y buenas prácticas

Configura CORS para aceptar solicitudes desde cualquier cliente (@CrossOrigin o configuración global).

Asegura que las respuestas tengan el formato y códigos HTTP adecuados (201 al crear, 404 si no existe, etc.).

Documenta los endpoints usando Swagger u OpenAPI (opcional, recomendado).

Agrega control de versiones con la convención /api/v1.

Fase 4: Pruebas y verificación

Verifica el funcionamiento de cada endpoint usando Postman o curl.

Realiza pruebas de integración con otra aplicación (puede ser mock).

Asegúrate de que el servicio permita ser consumido correctamente desde distintas aplicaciones.


Entregables

Proyecto Spring Boot con estructura organizada (controller, service, repository, model).

Script SQL de la base de datos o archivo .sql con datos de prueba.

Documento README.md que incluya:

Descripción del servicio y casos de uso.

Instrucciones de compilación, ejecución y prueba.

Capturas de pantalla o ejemplos de peticiones/respuestas.
