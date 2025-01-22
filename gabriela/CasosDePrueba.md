# Casos de prueba


## Microfrontend: Carrito de compras

### Caso de prueba: Agregar producto al carrito de compras del usuario autenticado.

| **ID**                   | CP01                                                                                                                        |
|--------------------------|------------------------------------------------------------------------------------------------------------------------------|
| **Historia de Usuario**  | HU01                                                                                                                        |
| **Nombre**               | Agregar producto al Carrito                                                                                                |
| **Cumple (Sí/No)**       | Sí                                                                                                                          |
| **Descripción**          | Verificar que el sistema permite al usuario agregar productos al carrito correctamente.                                      |
| **Precondiciones**       | El usuario debe estar autenticado en el sistema. <br> El catálogo de productos debe estar disponible y visible.                                                   |
| **Pasos**                | 1. Acceder a la página del catálogo de productos. <br> 2. Seleccionar un producto. <br> 3. Hacer clic en "Agregar al carrito".            |
| **Datos de Prueba**      | Producto: Laptop ASUS VivoBook 15 <br> Cantidad: 1                                                                          |
| **Resultados Esperados** | El producto se agrega al carrito, y la cantidad total de productos se actualiza correctamente.                               |
| **Resultados Obtenidos** | El producto se agregó correctamente al carrito y el sistema reflejó los cambios.                                            |

---

| **ID**                   | CP02                                                                                                                       |
|--------------------------|------------------------------------------------------------------------------------------------------------------------------|
| **Historia de Usuario**  | HU02                                                                                                                        |
| **Nombre**               | Visualizar el carrito de compras de un usuario autenticado.                                                                                               |
| **Cumple (Sí/No)**       | Sí                                                                                                                          |
| **Descripción**          | Verificar que el sistema permite al usuario pueda visualizar sus productos agregados en el carrito.                                    |
| **Precondiciones**       | El usuario debe estar autenticado en el sistema. <br> El usuario debe tener productos agregados al carrito de compras.                                                           |
| **Pasos**                | 1. Acceder al carrito de compras. <br> 2. Visualizar los productos agregados en el carrito del usuario. <br>              |
| **Datos de Prueba**      | Producto: Mouse Logitech M590                                                                                               |
| **Resultados Esperados** | Los productos se visualizan correctamente.              |
| **Resultados Obtenidos** | Los productos se visualizaron en el carrito de compras del usuario.
---


| **ID**                   | CP03                                                                                                                       |
|--------------------------|------------------------------------------------------------------------------------------------------------------------------|
| **Historia de Usuario**  | HU03                                                                                                                        |
| **Nombre**               | Actualizar cantidades de productos                                                                                               |
| **Cumple (Sí/No)**       | Sí                                                                                                                          |
| **Descripción**          | Verificar que el sistema permita actualizar las cantidades de los productos agregados en el carrito del usuario.                   |
| **Precondiciones**       | El usuario debe estar autenticado en el sistema. El usuario debe tener al menos un producto en su carrito de compras para actualizar la cantidad.                                                           |
| **Pasos**                | 1. Acceder al carrito de compras. <br> 2. Identificar el producto que se desea actualizar la cantidad. <br> 3. Incrementar o disminuir la cantidad del producto. <br> 4. En caso de no existir suficiente stock debería mostrarse un mensaje indicando que ha llegado al stock máximo.              |
| **Datos de Prueba**      | Producto: Mouse Logitech M590                                                                                               |
| **Resultados Esperados** | La cantidad del producto se actualizará conforme al stock disponible.               |
| **Resultados Obtenidos** | La cantidad del producto fue actualizada de acuerdo a lo que el usuario incrementó a disminuyó.

---
| **ID**                   | CP04                                                                                                                       |
|--------------------------|------------------------------------------------------------------------------------------------------------------------------|
| **Historia de Usuario**  | HU04                                                                                                                        |
| **Nombre**               | Eliminar Producto del Carrito                                                                                               |
| **Cumple (Sí/No)**       | Sí                                                                                                                          |
| **Descripción**          | Verificar que el sistema permite al usuario eliminar productos del carrito correctamente.                                    |
| **Precondiciones**       | El usuario debe estar autenticado en el sistema. <br> El usuario debe tener productos agregados al carrito de compras.                                                           |
| **Pasos**                | 1. Acceder al carrito de compras. <br> 2. Identificar el producto a eliminar. <br> 3. Hacer clic en el ícono para "Eliminar".              |
| **Datos de Prueba**      | Producto: Mouse Logitech M590                                                                                               |
| **Resultados Esperados** | El producto se elimina del carrito y la cantidad total de productos se actualiza correctamente.                |
| **Resultados Obtenidos** | El producto fue eliminado correctamente y el sistema reflejó los cambios.                                                   

---
---
## Microfrontend: Órdenes

| **ID**                   | CP05                                                                                                                        |
|--------------------------|------------------------------------------------------------------------------------------------------------------------------|
| **Historia de Usuario**  | HU05                                                                                                                        |
| **Nombre**               | Crear orden de compra                                                                                                       |
| **Cumple (Sí/No)**       | Sí                                                                                                                          |
| **Descripción**          | Verificar que el sistema permite al usuario crear una orden de compra correctamente.                                         |
| **Precondiciones**       | - El usuario debe estar autenticado. <br> - El usuario debe tener productos en su carrito de compras. <br> - El usuario debe pasar a la opción de checkout.              |
| **Pasos**                | 1. Acceder al carrito de compras. <br> 2. Hacer clic en "Proceder al pago". <br> 3. Confirmar los detalles y crear la orden. |
| **Datos de Prueba**      | Productos: 2 (Laptop ASUS VivoBook 15, Mouse Logitech M590) <br> Método de envío: Express |
| **Resultados Esperados** | La orden se crea correctamente, y el sistema genera un ID único para la misma.                                              |
| **Resultados Obtenidos** | La orden se creó correctamente y el sistema generó un ID único.                                                             |

---

| **ID**                   | CP06                                                                                                                        |
|--------------------------|------------------------------------------------------------------------------------------------------------------------------|
| **Historia de Usuario**  | HU06                                                                                                                        |
| **Nombre**               | Cancelar Orden                                                                                                              |
| **Cumple (Sí/No)**       | Sí                                                                                                                          |
| **Descripción**          | Verificar que el sistema permite al usuario cancelar una orden en estado "Pendiente".                                        |
| **Precondiciones**       | - El usuario debe estar autenticado. <br> - El usuario debe tener una orden creada <br> - La orden debe estar en estado "Pendiente".         |
| **Pasos**                | 1. Crear la orden. <br> 2. Hacer clic en "Cancelar". |
| **Datos de Prueba**      | ID de la orden: 12345                                                                                                       |
| **Resultados Esperados** | La orden se cancela correctamente, y el sistema actualiza el estado a "Cancelada".                                           |
| **Resultados Obtenidos** | La orden fue cancelada correctamente y el estado se actualizó.                                                              |


## Microfrontend: Pagos
| **ID**                   | CP05                                                                                                                        |
|--------------------------|------------------------------------------------------------------------------------------------------------------------------|
| **Historia de Usuario**  | HU05                                                                                                                        |
| **Nombre**               | Procesar pago                                                                                                               |
| **Cumple (Sí/No)**       | Sí                                                                                                                          |
| **Descripción**          | Verificar que el sistema permite procesar el pago de una orden correctamente.                                               |
| **Precondiciones**       | - El usuario debe estar autenticado. <br> - El usuario debe tener una orden creada <br> - La orden debe estar en estado "Pendiente".           |
| **Pasos**                | 1. Crear la orden. <br> 2. Llenar los datos para la facturación. <br> 3. Hacer clic en "Pagar".    |
| **Datos de Prueba**      | ID de la orden: 12345 <br> Método de pago: Tarjeta de crédito (Número: 4111 1111 1111 1111, Exp: 12/25, CVV: 123).           |
| **Resultados Esperados** | El pago se procesa correctamente, y el estado de la orden cambia a "Pagado".                                                |
| **Resultados Obtenidos** | El pago fue procesado correctamente y el estado cambió a "Pagado".                                                          |
