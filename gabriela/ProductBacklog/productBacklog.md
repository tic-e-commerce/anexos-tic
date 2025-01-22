# Product Backlog

| **Historia de usuario** | **Código Tarea** | **Nombre**                                                                                         | **Complejidad** | **Prioridad** |
|--------------------------|------------------|-----------------------------------------------------------------------------------------------------|-----------------|---------------|
| **HU01**                | T01             | Implementar un endpoint en el microservicio del carrito para añadir productos al mismo.            | 5               | 4             |
|                          | T02             | Validar que el producto exista y haya stock disponible.                                            | 4               | 4             |
|                          | T03             | Implementar lógica para evitar duplicidad de productos en el carrito.                              | 3               | 3             |
|                          | T04             | Manejar errores en caso de productos agotados o cantidades excedidas.                              | 4               | 4             |
| **HU02**                | T06             | Implementar un endpoint en el microservicio del carrito para consultar los detalles del carrito del usuario autenticado. | 5               | 4             |
|                          | T07             | Implementar lógica para calcular el subtotal y el total acumulado.                                 | 4               | 4             |
|                          | T08             | Implementar la lógica para la parte del método de entrega.                                         | 3               | 3             |
|                          | T09             | Diseñar el microfrontend para la visualización del carrito.                                        | 3               | 3             |
|                          | T10             | Implementar el microfrontend para mostrar el carrito y conectarlo con el microservicio correspondiente. | 3               | 3             |
| **HU03**                | T11             | Implementar un endpoint en el microservicio del carrito para actualizar cantidades de productos añadidos al mismo. | 5               | 4             |
|                          | T12             | Validar que las cantidades solicitadas no excedan el stock disponible de los productos.            | 4               | 4             |
|                          | T13             | Recalcular los subtotales y el total del carrito al realizar cambios.                              | 3               | 3             |
|                          | T14             | Diseñar la funcionalidad en el carrito de compras para ajustar las cantidades mediante botones o campos. | 4               | 4             |
|                          | T15             | Implementar la funcionalidad en el microfrontend del carrito de compras, para que interactúe con el microservicio. | 4               | 4             |
|                          | T16             | Mostrar actualizaciones de subtotales y total al recibir datos del microservicio.                  | 4               | 4             |
|                          | T17             | Mostrar mensajes claros si se excede el stock disponible.                                          | 4               | 4             |
| **HU04**                | T18             | Implementar un endpoint en el microservicio del carrito para eliminar productos específicos.        | 5               | 4             |
|                          | T19             | Validar que la eliminación se realice correctamente y actualizar los datos almacenados.            | 4               | 4             |
|                          | T20             | Diseñar la funcionalidad en el carrito de compras para eliminar un producto.                       | 4               | 4             |
|                          | T21             | Implementar la funcionalidad en el carrito de compras para eliminar un producto.                   | 4               | 4             |
| **HU05**                | T22             | Validar que los productos tengan stock suficiente al momento de crear la orden.                    | 5               | 3             |
|                          | T23             | Diseñar una vista de órdenes que muestre los productos añadidos al carrito y el método de entrega elegido. | 4               | 3             |
|                          | T24             | Implementar en el microfrontend de órdenes que los usuarios visualicen los productos que fueron agregados previamente en su carrito y el método de entrega seleccionado. | 4               | 3             |
| **HU06**                | T25             | Implementar un endpoint en el microservicio de órdenes para cancelar aquellas en estado 'Pendiente'. | 5               | 3             |
|                          | T26             | Implementar validaciones para evitar que se cancelen órdenes ya procesadas.                        | 5               | 3             |
|                          | T27             | Actualizar el estado de la orden a 'Cancelada' en la base de datos.                                | 4               | 3             |
|                          | T28             | Diseñar una funcionalidad para que el usuario cancele la orden.                                    | 4               | 3             |
|                          | T29             | Implementar una funcionalidad en el microfrontend de órdenes para que el usuario cancele la orden. | 4               | 3             |
| **HU07**                | T30             | Implementar un microservicio para gestionar el procesamiento de pagos de manera segura.            | 5               | 3             |
|                          | T31             | Implementar la actualización del estado de la orden a "Pagada" al completar el proceso.            | 5               | 3             |
|                          | T32             | Diseñar una interfaz de pagos para seleccionar el método de pago.                                  | 4               | 3             |
|                          | T33             | Implementar en el microfrontend de pagos para seleccionar el método de pago.                       | 4               | 3             |
|                          | T34             | Mostrar mensajes de confirmación al usuario después de un pago exitoso.                            | 4               | 3             |
