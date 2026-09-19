# Tarea - API REST de Gestión de Biblioteca

## Descripción del proyecto
Este proyecto es una API REST desarrollada para administrar el catálogo de libros de una biblioteca. Permite realizar las operaciones CRUD (Crear, Leer, Actualizar y Eliminar) sobre los libros. 

Destaca por implementar el patrón de **Arquitectura en Capas** para separar responsabilidades:
- **Models:** Representación de los datos (Libro).
- **Controllers:** Gestión de peticiones y respuestas HTTP.
- **Services:** Capa de lógica de negocio.
- **Repositories:** Gestión de persistencia de datos.

En este ejercicio, la persistencia de datos se realiza de forma temporal utilizando una colección en memoria `List(Of Libro)`, configurada mediante Inyección de Dependencias (Singleton).

## Tecnologías utilizadas
- Visual Basic .NET
- ASP.NET Core Web API
- Almacenamiento en memoria (List)

## Descripción de los endpoints
La API expone los siguientes endpoints bajo la ruta principal `/api/libros`:

* **`GET /api/libros`** : Devuelve la lista completa de libros registrados.
* **`GET /api/libros/{id}`** : Obtiene los detalles de un libro específico buscando por su ID.
* **`POST /api/libros`** : Registra un nuevo libro. Requiere un objeto JSON en el cuerpo de la petición con las propiedades: `Titulo`, `Autor` y `AnioPublicacion`.
* **`PUT /api/libros/{id}`** : Modifica los datos de un libro existente. Requiere enviar el ID en la URL y el objeto actualizado en el cuerpo de la petición.
* **`DELETE /api/libros/{id}`** : Elimina un libro del registro utilizando su ID.

## Instrucciones necesarias para ejecutar el proyecto
1. **Descargar el proyecto:** Clona este repositorio o descárgalo como archivo ZIP y extráelo en tu computadora.
2. **Abrir la solución:** Haz doble clic en el archivo `.sln` para abrir el proyecto en Visual Studio 2022.
3. **Ejecutar la API:** Presiona la tecla `F5` (o el botón verde "Iniciar depuración") en Visual Studio. Se abrirá una ventana de consola o el navegador indicando que el servidor local está corriendo (ej. `https://localhost:<puerto>`).
4. **Probar los endpoints:** Puedes usar tu navegador web para probar la ruta GET `https://localhost:<puerto>/api/libros`. Para probar el flujo completo (POST, PUT, DELETE), utiliza herramientas como **Postman**. 

*Nota: Al usar una colección en memoria, los datos agregados mediante POST se perderán al detener la ejecución del servidor en Visual Studio.*
