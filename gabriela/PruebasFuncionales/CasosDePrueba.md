# Casos de prueba
Este documento detalla los casos de prueba elaborados para garantizar el funcionamiento de los microfrontends y microservicios implementados en el proyecto. Estos casos de prueba están fundamentados en las historias de usuario especificadas en el documento de trabajo de integración curricular (TIC) y haciendo referencia a [historias de usuario](../HistoriasDeUsuario/).

## Microfrontend: Carrito de compras

### Caso de prueba: Agregar producto al carrito de compras del usuario autenticado.

| **ID**                   | CP01                                                                                                                        |
|--------------------------|------------------------------------------------------------------------------------------------------------------------------|
| **Historia de Usuario**  | HU01                                                                                                                        |
| **Nombre**               | Agregar producto al carrito de compras.                                                                                               |
| **Cumple (Sí/No)**       | Sí                                                                                                                          |
| **Descripción**          | Verificar que el sistema permite al usuario agregar productos al carrito de compras correctamente.                                      |
| **Precondiciones**       | - El usuario debe estar autenticado en el sistema. <br> - El catálogo de productos debe estar disponible y visible.                                                   |
| **Pasos**                | 1. Acceder a la página del catálogo de productos. <br> 2. Seleccionar un producto. <br> 3. Hacer clic en el ícono que representa la opción "Agregar al carrito".            |
| **Datos de Prueba**      | - Producto: Laptop ASUS VivoBook 15 <br> - Cantidad: 1                                                                          |
| **Resultados Esperados** | El producto se agrega al carrito de compras, y la cantidad total de productos se actualiza correctamente.                               |
| **Resultados Obtenidos** | El producto se agregó correctamente al carrito de compras y el sistema reflejó los cambios.                                            |

---

### Caso de prueba: Visualizar el carrito de compras de un usuario autenticado.

| **ID**                   | CP02                                                                                                                       |
|--------------------------|------------------------------------------------------------------------------------------------------------------------------|
| **Historia de Usuario**  | HU02                                                                                                                        |
| **Nombre**               | Visualizar el carrito de compras de un usuario autenticado.                                                                                               |
| **Cumple (Sí/No)**       | Sí                                                                                                                          |
| **Descripción**          | Verificar que el sistema permite al usuario visualizar sus productos agregados en el carrito de compras.                                    |
| **Precondiciones**       | - El usuario debe estar autenticado en el sistema. <br> - El usuario debe tener productos agregados al carrito de compras.                                                           |
| **Pasos**                | 1. Acceder al carrito de compras. <br> 2. Visualizar los productos agregados en el carrito del usuario. <br>              |
| **Datos de Prueba**      | - Producto: Mouse Logitech M590                                                                                               |
| **Resultados Esperados** | Los productos se visualizan correctamente.              |
| **Resultados Obtenidos** | Los productos se visualizaron en el carrito de compras del usuario.
---

### Caso de prueba: Actualizar la cantidad de un producto en el carrito de compras. 

| **ID**                   | CP03                                                                                                                       |
|--------------------------|------------------------------------------------------------------------------------------------------------------------------|
| **Historia de Usuario**  | HU03                                                                                                                        |
| **Nombre**               | Actualizar cantidades de productos                                                                                               |
| **Cumple (Sí/No)**       | Sí                                                                                                                          |
| **Descripción**          | Verificar que el sistema permita actualizar las cantidades de los productos agregados en el carrito del usuario.                   |
| **Precondiciones**       | - El usuario debe estar autenticado en el sistema. <br> - El usuario debe tener al menos un producto en su carrito de compras para actualizar la cantidad de dicho producto.                                                           |
| **Pasos**                | 1. Acceder al carrito de compras. <br> 2. Identificar el producto que se desea actualizar la cantidad. <br> 3. Incrementar o disminuir la cantidad del producto. <br> 4. En caso de no existir suficiente stock debería mostrarse un mensaje indicando que ha llegado al stock máximo.              |
| **Datos de Prueba**      | - Producto: Mouse Logitech M590                                                                                               |
| **Resultados Esperados** | La cantidad del producto se actualiza correctamente en el carrito, respetando el stock máximo y reflejando los cambios en el total. Si se excede el stock, se muestra un mensaje de disponibilidad.            |
| **Resultados Obtenidos** | La cantidad del producto se actualizó según la acción del usuario, reflejando los cambios en el total del carrito. No se permitió exceder el stock y se mostró un mensaje adecuado.

---

### Caso de prueba: Eliminar un producto en el carrito de compras.

| **ID**                   | CP04                                                                                                                       |
|--------------------------|------------------------------------------------------------------------------------------------------------------------------|
| **Historia de Usuario**  | HU04                                                                                                                        |
| **Nombre**               | Eliminar producto del carrito de compras.                                                                                                |
| **Cumple (Sí/No)**       | Sí                                                                                                                          |
| **Descripción**          | Verificar que el sistema permite al usuario eliminar productos del carrito correctamente.                                    |
| **Precondiciones**       | - El usuario debe estar autenticado en el sistema. <br> - El usuario debe tener productos agregados al carrito de compras.                                                           |
| **Pasos**                | 1. Acceder al carrito de compras. <br> 2. Identificar el producto a eliminar. <br> 3. Hacer clic en el ícono para "Eliminar".              |
| **Datos de Prueba**      | - Producto: Mouse Logitech M590                                                                                               |
| **Resultados Esperados** | El producto se elimina correctamente del carrito de compras. La cantidad total de productos y el total del carrito de compras se actualizan automáticamente. Si el carrito queda vacío, se muestra un mensaje indicándole al usuario que no hay productos en el carrito.                |
| **Resultados Obtenidos** | El producto fue eliminado correctamente del carrito de compras. La cantidad total de productos y el total del carrito de compras se actualizaron de manera precisa. Cuando el carrito quedó vacío, el sistema mostró un mensaje informando que no había productos en el carrito.                                                   

---
---
## Microfrontend: Órdenes

### Caso de prueba: Crear una orden de compra.


| **ID**                   | CP05                                                                                                                        |
|--------------------------|------------------------------------------------------------------------------------------------------------------------------|
| **Historia de Usuario**  | HU05                                                                                                                        |
| **Nombre**               | Crear orden de compra                                                                                                       |
| **Cumple (Sí/No)**       | Sí                                                                                                                          |
| **Descripción**          | Verificar que, al presionar el botón "Proceed to Checkout" en la pantalla del carrito de compras, el usuario es redirigido correctamente a la pantalla de Checkout, donde se crea automáticamente una orden de compra con los detalles correctos.                                       |
| **Precondiciones**       | - El usuario debe estar autenticado. <br> - El carrito de compras debe contener al menos un producto. <br> - El usuario debe haber presionado el botón "Proceed to Checkout" situado en el carrito de compras.           |
| **Pasos**                | 1. Acceder al carrito de compras. <br> 2. Hacer clic en el botón "Proceed to Checkout". <br> 3. Verificar que el sistema redirige automáticamente a la pantalla Checkout.
| **Datos de Prueba**      | - Productos: 2 (Laptop ASUS VivoBook 15, 1 Mouse Logitech M590) <br> - Método de envío: Express |
| **Resultados Esperados** | - En la pantalla Checkout, se crea una orden de compra automáticamente. <br> - Los detalles de la orden incluyen correctamente los productos seleccionados, sus cantidades, precios, método de envío y total.                                                |
| **Resultados Obtenidos** | - La orden se creó automáticamente.  <br> - Los detalles de la orden incluyeron correctamente los productos seleccionados, cantidades, método de envío y total.                                                   |

---

### Caso de prueba: Cancelar una orden

| **ID**                   | CP06                                                                                                                        |
|--------------------------|------------------------------------------------------------------------------------------------------------------------------|
| **Historia de Usuario**  | HU06                                                                                                                        |
| **Nombre**               | Cancelar Orden                                                                                                              |
| **Cumple (Sí/No)**       | Sí                                                                                                                          |
| **Descripción**          | Verificar que el sistema permite al usuario cancelar una orden en estado "Pendiente".                                        |
| **Precondiciones**       | - El usuario debe estar autenticado. <br> - El usuario debe tener una orden creada <br> - La orden debe estar en estado "Pendiente".         |
| **Pasos**                | 1. Hacer clic en el botón "Cancelar". |
| **Datos de Prueba**      | ID de la orden: 12345                                                                                                       |
| **Resultados Esperados** | La orden se cancela correctamente, el sistema actualiza el estado a "Cancelada" y retorna al carrito de compras.                                           |
| **Resultados Obtenidos** | La orden fue cancelada correctamente, el estado se actualizó y se retornó al usuario a su carrito de compras.                                                              |


## Microfrontend: Pagos 

### Caso de prueba: Procesar un pago
| **ID**                   | CP07                                                                                                                        |
|--------------------------|------------------------------------------------------------------------------------------------------------------------------|
| **Historia de Usuario**  | HU07                                                                                                                        |
| **Nombre**               | Procesar pago                                                                                                               |
| **Cumple (Sí/No)**       | Sí                                                                                                                          |
| **Descripción**          | Verificar que el sistema permite procesar el pago de una orden correctamente.                                               |
| **Precondiciones**       | - El usuario debe estar autenticado. <br> - El usuario debe tener una orden creada <br> - La orden debe estar en estado "Pendiente".           |
| **Pasos**                | 1. Llenar los datos para la facturación. <br> 3. Hacer clic en "Pagar". <br> 4. Verificar que los productos y totales mostrados en la nueva ventana sean correctos. <br> 5. Introducir los datos de la tarjeta (número, fecha de expiración, CVV). <br> 6. Confirmar el pago |
| **Datos de Prueba**      | - ID de la orden: 12345 <br> - Método de pago: Tarjeta de crédito (Número: 4111 1111 1111 1111, Exp: 12/25, CVV: 123).           |
| **Resultados Esperados** | El pago se procesa correctamente, y el estado de la orden cambia a "Pagado".                                                |
| **Resultados Obtenidos** | El pago fue procesado correctamente y el estado cambió a "Pagado".                                                          |
