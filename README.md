# OpenBooks

## Integrantes

- Romero Palacios Randy Rodrigo
- Villanueva García Emanuel

## Nombre del proyecto

**OpenBooks**

## Descripción del proyecto

OpenBooks es una aplicación iOS que permitirá buscar libros mediante Open Library, consultar la información básica de cada libro y administrar una colección personal de libros guardados.

La aplicación se desarrollará principalmente con SwiftUI.

## Objetivo

Permitir que el usuario explore y busque libros, consulte sus datos principales y pueda guardar o eliminar libros de una colección personal.

## Funcionalidades del MVP

La aplicación incluirá:

- Una pantalla principal con una lista de libros.
- Búsqueda de libros mediante Open Library.
- Visualización de resultados de búsqueda.
- Visualización del detalle de cada libro.
- Portada del libro cuando esté disponible.
- Título del libro.
- Autor o autores.
- Año de publicación cuando esté disponible.
- Opción para guardar libros.
- Opción para eliminar libros guardados.
- Una sección llamada **Mis libros**.
- Persistencia local de los libros guardados.
- Manejo de estados de carga.
- Manejo de errores.
- Manejo de búsquedas sin resultados.
- Manejo de libros sin portada.
- Manejo del estado de lista de libros guardados vacía.

## Flujo de usuario

La aplicación tendrá dos secciones principales:

- **Inicio**
- **Mis libros**

Desde la pantalla principal, el usuario podrá seleccionar directamente un libro de la lista para consultar su detalle o realizar una búsqueda.

Al realizar una búsqueda, la aplicación mostrará un estado de carga mientras obtiene la información de Open Library.

Si se obtienen resultados, el usuario podrá seleccionar un libro para acceder a su detalle.

Si la búsqueda no devuelve coincidencias, se mostrará un estado sin resultados y el usuario podrá modificar la búsqueda para intentarlo nuevamente.

Si ocurre un problema durante la consulta a Open Library, se mostrará un estado de error con la opción de volver a intentarlo.

Desde la pantalla de detalle, la aplicación comprobará si el libro ya se encuentra guardado.

- Si el libro no está guardado, se mostrará la opción **Guardar libro**.
- Si el libro ya está guardado, se mostrará la opción **Eliminar de Mis libros**.

La sección **Mis libros** mostrará los libros almacenados localmente. Desde esta sección el usuario también podrá seleccionar un libro para consultar su detalle.

Si todavía no existen libros guardados, se mostrará un estado de lista vacía que permitirá al usuario regresar a la búsqueda de libros.

Cuando un libro no tenga una portada disponible en Open Library, se mostrará un elemento visual sustituto en lugar de la imagen.

De esta manera, los diferentes flujos utilizan una misma pantalla de detalle y se conectan mediante el estado del libro y la navegación entre **Inicio** y **Mis libros**.

### Flujo general

<img width="1448" height="1086" alt="07-flujo-usuario" src="https://github.com/user-attachments/assets/d6456849-b7ba-4dac-8c73-b5c1177e884b" />

**Detalle del libro** y **Mis libros** se repiten en el diagrama para mostrar con mayor claridad los distintos recorridos, pero corresponden a las mismas pantallas de la aplicación.

El diagrama representa los recorridos principales de navegación. Los estados de carga, error, búsqueda sin resultados, libro sin portada y lista de libros guardados vacía se muestran por separado en los wireframes.

## Wireframes

Los siguientes wireframes representan la estructura inicial de las principales pantallas de la aplicación y los estados necesarios para cubrir el MVP.

### Pantalla principal

La pantalla principal contiene el buscador, una lista inicial de libros y el acceso a la sección **Mis libros**.

<img width="941" height="1672" alt="01-pantalla-principal" src="https://github.com/user-attachments/assets/536c273b-de4d-4cc2-8f0a-5ef315f4abfd" />

### Resultados de búsqueda

Muestra los libros encontrados después de realizar una búsqueda en Open Library.

<img width="941" height="1672" alt="02-resultados" src="https://github.com/user-attachments/assets/91fe1e23-cbea-4254-8e65-86122ed6ca93" />

### Detalle de un libro no guardado

Muestra la información del libro y permite guardarlo en la colección personal.

<img width="941" height="1672" alt="03-detalle-no-guardado" src="https://github.com/user-attachments/assets/57942af2-83cc-40ad-83f1-9de0f8728d8f" />

### Mis libros

Muestra los libros que el usuario ha guardado localmente.

<img width="941" height="1672" alt="04-mis-libros" src="https://github.com/user-attachments/assets/b2c8d236-f487-42f9-9fdf-1faa598ccec3" />

### Detalle de un libro guardado

Muestra la información de un libro que ya pertenece a la colección del usuario y permite eliminarlo de **Mis libros**.

<img width="941" height="1672" alt="05-detalle-guardado" src="https://github.com/user-attachments/assets/bddef89b-d801-4247-acc2-a69e8ac65ec2" />

### Mis libros vacío

Este estado se mostrará cuando el usuario todavía no tenga libros guardados.

<img width="941" height="1672" alt="06-mis-libros-vacio" src="https://github.com/user-attachments/assets/2cb30994-951e-4096-98ff-82daf107e87d" />

### Estados adicionales del MVP

Además de las pantallas principales, la aplicación contempla diferentes estados necesarios para manejar correctamente las respuestas de Open Library.

#### Búsqueda sin resultados

Se mostrará cuando Open Library no devuelva libros que coincidan con la búsqueda realizada. El usuario podrá modificar su búsqueda para intentarlo nuevamente.

#### Carga de resultados

Se mostrará mientras la aplicación obtiene los resultados de una búsqueda desde Open Library.

#### Error en la búsqueda

Se mostrará cuando ocurra un problema al obtener los resultados desde Open Library. El usuario tendrá la opción de intentar nuevamente la consulta.

#### Libro sin portada

Cuando Open Library no tenga una portada disponible para un libro, se mostrará un elemento visual sustituto en lugar de dejar el espacio de la imagen vacío.

<img width="1536" height="1024" alt="08-estados-adicionales" src="https://github.com/user-attachments/assets/c7f0de68-d058-4422-84f5-db4d024ac983" />

## Tecnologías previstas

- Swift
- SwiftUI
- Open Library API
- Navegación con SwiftUI
- Programación asíncrona con async/await
- Persistencia local
- Git y GitHub

## Estado actual del proyecto

Actualmente se encuentran definidos:

- El objetivo del proyecto.
- El MVP.
- El flujo principal de usuario.
- Los wireframes de las principales pantallas.
- Los estados adicionales necesarios para el MVP.
- La estructura inicial del repositorio.

La implementación de las pantallas y la integración con Open Library se desarrollarán progresivamente durante el proyecto.
