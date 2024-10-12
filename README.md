# Proyecto Pruebas TSDC Ghost

## Aspectos generales

## Listado de funcionalidades

1. **Crear una publicación:** Se puede crear una publicación, esta es la unidad mínima de Ghost, en esta se puede escribir texto en formato markdown, agregar imágenes, etiquetas, etc.
2. **Editar una publicación:** Se puede editar todos los detalles de una publicación ya creada.
3. **Publicar una publicación:** Se puede publicar una publicación, haciendola accesible al resto de usuarios.
4. **Agendar una publicación:** Se puede agendar una publicación creada para que se publique en un tiempo específico.
5. **Eliminar una publicación:** Se puede eliminar una publicación ya creada.
6. **Previsualizar una publicación:** Al momento de la creación puede previsualizar como se vería la publicación.
7. **Crear Miembros:** Se permite crear miembros de la página, estos son aquellos que están suscritos. Nos permite asignar los siguientes campos:
    - Nombre (Formato de entrada de texto, no obligatorio)
    - Correo (Formato de correo electronico, obligatorio unico)
    - Etiquetas (Formato de texto, no obligatorio)
    - Nota (Formato de texto, maximo 500 caracteres, no obligatorio)
8. **Exportar Miembros:** Esta funcionaledad nos permite generar un archivo en formato .CSV que contiene la información de los miembros como correo, nombre, nota, fecha de creación, etc.
9. **Editar miembro:** Se pueden editar los datos de un miembro de la página existente.
10. **Eliminar miembro:** Se puede eliminar un miembro ya credo
11. **Crear etiquera:** Se puede crear una etiqueta, este es un elemento de organización bajo agrupación, se provee un nombre, descripción y post asociados.
12. **Editar una etiqueta:** Se puede editar todos los datos de una etiqueta.
13. **Eliminar una etiqueta:** Se permite eliminar una etiqueta ya creada.

## Modelo de dominio
### Glsoario
| Tabla                  | Descripción                                                                                                                                         | Tipo de Entidad |
|-----------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------|----------------|
| `newsletters`         | Contiene información sobre los boletines disponibles en el sistema para gestionar los boletines disponibles.      | class          |
| `posts`               | Almacena las publicaciones o artículos vinculados a los boletines.               | class          |
| `users`               | Gestiona la información de los usuarios del sistema para identificar y autenticar usuarios.                 | class          |
| `posts_authors`       | Define la relación entre publicaciones y autores.            | class          |
| `roles`               | Contiene los roles disponibles en el sistema (e.g., administrador, editor) para definir niveles de acceso y permisos de usuarios.                   | class          |
| `roles_users`         | Asocia roles con usuarios, permitiendo asignar permisos a los usuarios según el rol que tienen en el sistema.                                        | class          |
| `permissions`         | Define los permisos disponibles, especificando qué acciones se pueden realizar sobre ciertos objetos.              | class          |
| `permissions_roles`   | Relaciona roles con permisos para establecer las acciones permitidas según el rol.                         | class          |
| `permissions_users`   | Asocia permisos específicos a usuarios.                    | class          |
| `members`             | Gestiona la información de los miembros suscritos a los boletines, almacenando detalles como correo y estado (gratuito o de pago).                   | class          |
| `tags`                | Almacena etiquetas asociables a los miembros o las publicaciones..                             | class          |
| `subscriptions`       | Contiene información de las suscripciones de los miembros.                    | class          |
| `products`            | Define los productos o niveles de suscripción disponibles, estructurando las opciones de suscripción en el sistema.                                  | class          |
| `posts_meta`          | Almacena metadatos asociados a las publicaciones.                        | class          |
| `comments`            | Gestiona los comentarios de los miembros en las publicaciones.| class          |
| `members_products`    | Asocia miembros con los productos que han adquirido.          | class          |
| `members_stripe_customers` | Almacena la relación entre miembros y sus identificadores en Stripe para gestionar pagos y suscripciones mediante la integración con Stripe.      | class          |
| `stripe_prices`       | Define los precios de los productos en Stripe, incluyendo el monto y su relación con un producto, para la configuración de precios y facturación.    | class          |


### Modelo Entidad-Relacion
En esta imagen se describe el modelo de dominio de la aplicacion Ghost expresado con un modelo Entidad-Relacion en formato UML.
![Untitled](https://github.com/user-attachments/assets/5a568774-87f0-46c0-95da-1e458bdc7f2f)

En caso de no apreciarse bien la imagen, con el siguiente [link](https://dbdiagram.io/d/670aea1797a66db9a3c481d9) se puede tener una mejor visualizacion.

## Modelo de GUI
En esta imagen se describe todo el modelo de GUI de la seccion de Admin del software Ghost
![ModeloGUI](https://github.com/user-attachments/assets/b4ee2b6d-1942-4130-8a46-cba66160ec5b)


En caso de no apreciarse bien la imagen, con el siguiente [llnk](https://lucid.app/lucidchart/f028b547-b400-4eeb-b9eb-30760491aef1/edit?viewport_loc=-2716%2C330%2C8592%2C4647%2C0_0&invitationId=inv_bb418780-a849-4bd3-b767-c87482ee7e28) puede acceder al sitio donde esta alojado y visualizarlo de una mejor manera.

## Inventarios de pruebas
