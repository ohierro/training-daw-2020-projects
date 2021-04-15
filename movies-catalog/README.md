# Movies catalog

El objetivo del proyecto es crear un catálogo de películas al estilo Netflix, pero por supuesto sin la parte de streaming.
Dicho catálogo permitirá listar un conjunto de películas del catálogo, marcarlas como visto/no visto, me gusta/no me gusta y añadir a lista de películas a ver más tarde.

## Funcionalidad

### Listado de películas
Pantalla principal de la aplicación.

![main page](img/Main.png "Main page")

Se mostrará un listado de películas, con su título y descripción breve, además de dos iconos para indicar si se ha visto o no y si me gusta o no. Estos iconos a su vez actuarán como botón y permitirán cambiar el estado.

Desde el catálogo se accederá también a listado de películas para ver más tarde, podrá ser un botón, un enlace o si se prefiere también es válido hacer un menú para la aplicación con dos opciones (catalogo y películas para ver):
`EXTRA: En principio tanto visto o me gusta tendrán solo dos posibles valores, pero para el caso de me gusta/no me gusta lo ideal sería implementar también sin valor, es decir, ni me gusta ni no me gusta`

### Visualizar detalle de una película
Al pulsar sobre "Ver", nos llevará a la página de detalle de la película.

![details](img/Details.png "Details of product")

Dicha pantalla mostrará la descripción larga de la película, así como el reparto y la clasificación por edades de esta. Incluirá también los dos iconos para indicar si se ha visto o no y si me gusta o no, con el mismo funcionamiento descrito para el listado. Y adicionalmente se deberá añadir un botón para añadir la película a la lista de películas a ver más tarde.

### Marcar visto/no visto

Al pulsar sobre el icono de visto en cada una de las películas, la aplicación alternará el valor (tanto en servidor como en cliente). Si al hacer clic está como no visto se cambiará a visto y viceversa.

### Marcar me gusta/no me gusta

Al pulsar sobre el icono de me gusta/no me gusta en cada una de las películas, la aplicación alternará el valor (tanto en servidor como en cliente). Si al hacer clic está como no me gusta se cambiará a me gusta y viceversa.

### Añadir a ver más tarde
Al pulsar sobre el botón "Ver más tarde", deberá agregar la película en una lista de películas pendientes para ver (en servidor) mostrando un mensaje de confirmación al usuario "Película agregada correctamente para ver más tarde"

### Visualizar el lista de películas a ver más tarde

Al pulsar sobre la opción de "Películas a ver más tarde", nos llevará a la página listado de películas para ver más tarde

![checkout](img/Checkout.png "Checkout")

En dicha pantalla, podremos realizar las siguientes acciones:

* Eliminar de la lista


## Requisitos técnicos

Aplicación web formada por el front-end con la capa de presentación y el back-end con la capa de procesado de datos.

### Front-End
* Utilización de vue 2 para el proyecto
* Utilización de vue-router para la navegación en las páginas
* Utilización correcta de componentes


### Back-End
* API REST desarrollada .Net Core 3.1
* Publicación de la API en un App Service de Azure desde donde se expondrá la API al front-end
* Documentación de la API bajo es estándar OpenApi mediante Swagger. Deberá permitir poder importar la API como colección en Postman para ser testeada, así como exponer un interfaz que permita interactuar con la API directamente desde el navegador Web.
* Utilización de SQLite como gestor de BD y estrategia "Code First" mediante el uso de migraciones para la creación del modelo en BD.
* Validaciones de los datos en servidor, respuestas de la API estableciendo los códigos especificos de estado del protocolo HTTP y control de errores

## Bonus

* Realizar los puntos indicados como `EXTRA``
* Diseñar todo el UI mediante vue-bootstrap
* Implementar el carrito mediante Vuex
* Implementar el patron de diseño UnitOfWork y Repository para el acceso a datos.

## Puntuación
El ejercicio se valorará dividendo la parte de Front-End y Back-End con 10 puntos cada una y sacando la nota final mediante la media aritmética entre Front-End y Back-End.

### Front-End (10 puntos)

Son 130 puntos, que se trasladarán a 10 mediante la aplicación de la regla: `nota * 10 / 150`.

Ejemplos: 130 ptos sería un 10, 90 ptos sería un 6,9 y 70 ptos un 5,3.

* FUNCIONALIDAD (90 ptos)
    * 40 ptos - Listado correcto de productos
        * Listado de los datos
        * Enlaces de view, añadir y checkout funcionando correctamente
        * Actualización del componente de carrito correctamente al añadir un producto
        * Diseño basado en componentes, utilizando adecuadamente los eventos y propiedades
    * 30 ptos - Visualización de producto
        * Visualización de los datos completos del producto
        * Visualización de las distintas imágenes del producto
        * Funcionamiento de los botones de la pantalla
    * 20 ptos - Carrito de la compra
        * Eliminación de un producto
        * Modificar la cantidad de elementos (y los calculos implicados de totales...)
* GENERALES (40 ptos)
    * 20 ptos - Limpieza de código (sin comentarios, indentación correcta, nombrado consistente...)
    * 20 ptos - Aplicación correcta de conceptos (propiedades, eventos, componentes...)

* EXTRAS (70 ptos SI (FUNCIONALIDAD + GENERALES) > 70):
    * 20 ptos - Implementar mecanismos de paginación
    * 10 ptos - Utilizar algún componente de carrusel
    * 10 ptos - Utilización de vue-bootstrap
    * 30 ptos - Utilización de Vuex

### Back-End (9 puntos + 1 puntos de bonus)
* 1 pt - Entrega respetando formatos
* 1 pt - Publicación correcta sobre Azure App Service.
* 1 pt - Revisión de código. Correcto uso de [convenciones de nomenclatura](https://docs.microsoft.com/es-es/dotnet/standard/design-guidelines/naming-guidelines), al menos en nombres de clases, interface, variables, metodos y parametros, y uso de [buenas practicas](https://docs.microsoft.com/es-es/dotnet/csharp/programming-guide/inside-a-program/coding-conventions)
* 6 pt - Implementación de Swagger y correcto funcionamiento de todos los métodos expuestos desde swaggwer. En caso de **no estar publicada la API en Azure y no compilar el código** o **no implementar swagger**, y por lo tanto no poder probar, este punto no se evaluará y serán **0 puntos**.
* 1 pt - Bonus implementar el patrón de diseño UnitOfWork y Repository para el acceso a datos.
