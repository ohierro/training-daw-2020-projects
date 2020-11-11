# PassSaver

El objetivo del proyecto es crear un gestor de contraseñas.
Dicho gestor de contraseñas nos permitirá almacenar URLs para distintos sitios.
Así mismo, nos permitirá organizar las contraseñas por categorías.

## Funcionalidad

* Añadir una nueva categoría
* Eliminar una categoría
* Visualizar los sites de una categoría
* Añadir un nuevo site a una categoría
* Editar un site
* Eliminar un site

A la hora de añadir una categoría, serán obligatorios los siguientes campos:
* Nombre

A la hora de añadir un site, serán obligatorios los siguientes campos:
* Nombre
* User
* Password


## Mockups
A continuación se muestran unos diseñor orientativos sobre el diseño de la aplicación

Pantalla principal de la aplicación.
![main page](img/Main_page.png "Main page")

Al añadir una nueva categoría, simplemente preguntaremos el nombre
![main page](img/Main_page_new_category.png "Main page -new category")


Pantalla para añadir/editar una nueva entrada:
![main page](img/Edit_add.png "Edit page")

Cada uno de las pantallas será una página distinta, sin necesidad de tener que recargar datos ni modificar el DOM.
