# Casos de Prueba

En este documento se presentan los casos de prueba diseñados para verificar el correcto funcionamiento del Microfrontend de Catálogo de Productos. Los casos de prueba incluyen funcionalidades relacionadas con la visualización, búsqueda, filtrado, ordenamiento, enrutamiento, detalles de productos, gestión de reseñas y atributos.

---

## Caso de Prueba: Visualización de Productos en el Catálogo

| **ID**                   | CP01                                                                                                     |
| ------------------------ | ------------------------------------------------------------------------------------------------------- |
| **Historia de Usuario**  | HU01                                                                                                    |
| **Nombre**               | Visualización de Productos                                                                              |
| **Cumple (Sí/No)**       | Sí                                                                                                      |
| **Descripción**          | Verificar que el sistema permite mostrar correctamente la lista de productos disponibles en el catálogo. |
| **Precondiciones**       | 1. El microservicio de productos debe estar desplegado y funcional. <br> 2. El microfrontend debe estar correctamente integrado con el `gateway-ms`. |
| **Pasos**                | 1. Acceder a la página principal del catálogo. <br> 2. Verificar que se muestran los productos disponibles. |
| **Datos de Prueba**      | Productos en la base de datos: 10 productos con diferentes categorías y precios.                         |
| **Resultados Esperados** | Los productos se visualizan correctamente en la página principal del catálogo, incluyendo nombre, imagen, precio y categoría. |
| **Resultados Obtenidos** | Los productos se visualizan correctamente en el catálogo.                                               |

---

## Caso de Prueba: Búsqueda de Productos

| **ID**                   | CP02                                                                                                     |
| ------------------------ | ------------------------------------------------------------------------------------------------------- |
| **Historia de Usuario**  | HU02                                                                                                    |
| **Nombre**               | Búsqueda de Productos                                                                                  |
| **Cumple (Sí/No)**       | Sí                                                                                                      |
| **Descripción**          | Validar que la funcionalidad de búsqueda permite encontrar productos por nombre en el catálogo.         |
| **Precondiciones**       | 1. El microservicio de productos debe estar desplegado y funcional. <br> 2. El catálogo debe contener productos con diferentes nombres. |
| **Pasos**                | 1. Acceder a la barra de búsqueda en la página principal. <br> 2. Introducir el nombre de un producto existente. <br> 3. Presionar el botón de buscar. |
| **Datos de Prueba**      | Nombre a buscar: "Auriculares XYZ"                                                                      |
| **Resultados Esperados** | El sistema muestra únicamente los productos que coincidan con el término de búsqueda ingresado.         |
| **Resultados Obtenidos** | La búsqueda funciona correctamente, mostrando solo los productos que coinciden con el término ingresado. |

---

## Caso de Prueba: Filtrado de Productos

| **ID**                   | CP03                                                                                                     |
| ------------------------ | ------------------------------------------------------------------------------------------------------- |
| **Historia de Usuario**  | HU03                                                                                                    |
| **Nombre**               | Filtrado de Productos                                                                                  |
| **Cumple (Sí/No)**       | Sí                                                                                                      |
| **Descripción**          | Verificar que el sistema permite filtrar productos por categoría y rango de precios en el catálogo.     |
| **Precondiciones**       | 1. El catálogo debe contener productos de diferentes categorías y rangos de precios.                    |
| **Pasos**                | 1. Acceder a la página principal del catálogo. <br> 2. Seleccionar una categoría en el filtro. <br> 3. Seleccionar un rango de precios. |
| **Datos de Prueba**      | Categoría: "Electrónica" <br> Rango de precios: \$100 - \$300                                           |
| **Resultados Esperados** | El sistema filtra los productos correctamente, mostrando solo aquellos que coincidan con los criterios seleccionados. |
| **Resultados Obtenidos** | El filtrado funciona correctamente y los productos coinciden con los criterios seleccionados.           |

---

## Caso de Prueba: Ordenamiento de Productos

| **ID**                   | CP04                                                                                                     |
| ------------------------ | ------------------------------------------------------------------------------------------------------- |
| **Historia de Usuario**  | HU04                                                                                                    |
| **Nombre**               | Ordenamiento de Productos                                                                               |
| **Cumple (Sí/No)**       | Sí                                                                                                      |
| **Descripción**          | Validar que el sistema permite ordenar productos por precio (ascendente y descendente).                 |
| **Precondiciones**       | 1. El catálogo debe contener productos con diferentes precios.                                           |
| **Pasos**                | 1. Acceder a la página principal del catálogo. <br> 2. Seleccionar el criterio de ordenamiento "Precio Ascendente". <br> 3. Verificar el orden de los productos. |
| **Datos de Prueba**      | Productos con precios: \$50, \$100, \$150, \$200, \$250                                                  |
| **Resultados Esperados** | Los productos se ordenan correctamente según el criterio seleccionado (ascendente o descendente).       |
| **Resultados Obtenidos** | El ordenamiento funciona correctamente y los productos se ordenan según el criterio seleccionado.       |

---

## Caso de Prueba: Gestión de Reseñas de Productos

| **ID**                   | CP05                                                                                                     |
| ------------------------ | ------------------------------------------------------------------------------------------------------- |
| **Historia de Usuario**  | HU05                                                                                                    |
| **Nombre**               | Gestión de Reseñas                                                                                     |
| **Cumple (Sí/No)**       | Sí                                                                                                      |
| **Descripción**          | Validar que el sistema permite a los usuarios crear, editar y eliminar reseñas para productos específicos. |
| **Precondiciones**       | 1. El usuario debe estar autenticado. <br> 2. El microservicio de reseñas debe estar integrado con el catálogo. |
| **Pasos**                | 1. Acceder a la página de detalles del producto. <br> 2. Agregar una nueva reseña con calificación y comentario. <br> 3. Editar la reseña creada. <br> 4. Eliminar la reseña. |
| **Datos de Prueba**      | Calificación: 5 estrellas <br> Comentario: "Producto excelente"                                          |
| **Resultados Esperados** | Las reseñas se gestionan correctamente y los cambios se reflejan en tiempo real en la página de detalles del producto. |
| **Resultados Obtenidos** | La gestión de reseñas funciona correctamente, incluyendo la creación, edición y eliminación.            |

---

## Caso de Prueba: Gestión de Atributos de Productos

| **ID**                   | CP06                                                                                                     |
| ------------------------ | ------------------------------------------------------------------------------------------------------- |
| **Historia de Usuario**  | HU06                                                                                                    |
| **Nombre**               | Gestión de Atributos                                                                                   |
| **Cumple (Sí/No)**       | Sí                                                                                                      |
| **Descripción**          | Verificar que el sistema permite gestionar atributos dinámicos asociados a los productos.               |
| **Precondiciones**       | 1. El microservicio de atributos debe estar desplegado y funcional. <br> 2. Los productos deben tener atributos definidos en la base de datos. |
| **Pasos**                | 1. Acceder a la página de detalles del producto. <br> 2. Visualizar los atributos asociados al producto. <br> 3. Editar un atributo existente. <br> 4. Agregar un nuevo atributo. |
| **Datos de Prueba**      | Atributo a editar: "Color: Azul" <br> Nuevo atributo: "Tamaño: Grande"                                   |
| **Resultados Esperados** | Los atributos se gestionan correctamente y se reflejan en la página de detalles del producto en tiempo real. |
| **Resultados Obtenidos** | La gestión de atributos funciona correctamente, incluyendo edición y creación de nuevos atributos.      |

---

## Caso de Prueba: Navegación a Detalles del Producto

| **ID**                   | CP07                                                                                                     |
| ------------------------ | ------------------------------------------------------------------------------------------------------- |
| **Historia de Usuario**  | HU07                                                                                                    |
| **Nombre**               | Navegación a Detalles del Producto                                                                      |
| **Cumple (Sí/No)**       | Sí                                                                                                      |
| **Descripción**          | Verificar que al seleccionar un producto se redirige correctamente a su página de detalles.             |
| **Precondiciones**       | 1. El catálogo debe contener productos con detalles específicos almacenados en el backend.               |
| **Pasos**                | 1. Acceder a la página principal del catálogo. <br> 2. Seleccionar un producto. <br> 3. Verificar que se carga la página de detalles del producto. |
| **Datos de Prueba**      | Producto seleccionado: "Auriculares XYZ"                                                                |
| **Resultados Esperados** | La página de detalles muestra correctamente el nombre, descripción, imágenes y atributos del producto seleccionado. |
| **Resultados Obtenidos** | La navegación a detalles del producto funciona correctamente y muestra la información esperada.        |

---

Todos los casos de prueba han sido ejecutados con éxito y los resultados obtenidos cumplen con los resultados esperados.
