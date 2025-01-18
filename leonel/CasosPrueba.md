# Casos de Prueba

En este documento se presentan los casos de prueba diseñados para verificar el correcto funcionamiento de los microfrontends y microservicios desarrollados en el proyecto. Los casos de prueba se basan en las historias de usuario definidas en el documento del TIC.

## Caso de Prueba: Registro de Usuario

| **ID**                   | CP01                                                                                                                        |
| ------------------------ | --------------------------------------------------------------------------------------------------------------------------- |
| **Historia de Usuario**  | HU01                                                                                                                        |
| **Nombre**               | Registro de Usuario                                                                                                         |
| **Cumple (Sí/No)**       | Sí                                                                                                                          |
| **Descripción**          | Verificar que el sistema permite a los usuarios registrarse proporcionando los datos requeridos.                            |
| **Precondiciones**       | El microfrontend de autenticación debe estar configurado y desplegado.                                                      |
| **Pasos**                | 1. Acceder a la página de registro. <br> 2. Completar el formulario con los datos requeridos. <br> 3. Enviar el formulario. |
| **Datos de Prueba**      | Nombre: Juan <br> Apellido: Pérez <br> Correo: juan.perez@example.com <br> Contraseña: ContraseñaSegura123                  |
| **Resultados Esperados** | El sistema registra al usuario con los datos proporcionados y retorna un mensaje de éxito.                                  |
| **Resultados Obtenidos** | El sistema registró al usuario correctamente y retornó un mensaje de éxito.                                                 |

---

## Caso de Prueba: Inicio de Sesión

| **ID**                   | CP02                                                                                                                                                          |
| ------------------------ | ------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| **Historia de Usuario**  | HU02                                                                                                                                                          |
| **Nombre**               | Inicio de Sesión                                                                                                                                              |
| **Cumple (Sí/No)**       | Sí                                                                                                                                                            |
| **Descripción**          | Verificar que el sistema permite a los usuarios autenticarse proporcionando credenciales válidas y retorna un token JWT junto con la información del usuario. |
| **Precondiciones**       | El usuario debe estar registrado y activo. <br> El microfrontend de autenticación debe estar configurado y desplegado.                                        |
| **Pasos**                | 1. Acceder a la página de inicio de sesión. <br> 2. Completar el formulario con correo y contraseña válidos. <br> 3. Enviar el formulario.                    |
| **Datos de Prueba**      | Correo: juan.perez@example.com <br> Contraseña: ContraseñaSegura123                                                                                           |
| **Resultados Esperados** | El sistema autentica al usuario y retorna un token JWT junto con los datos del usuario.                                                                       |
| **Resultados Obtenidos** | El sistema permitió la autenticación del usuario y retornó el token JWT y los datos correspondientes.                                                         |

---

## Caso de Prueba: Recuperación de Contraseña

| **ID**                   | CP03                                                                                                                                   |
| ------------------------ | -------------------------------------------------------------------------------------------------------------------------------------- |
| **Historia de Usuario**  | HU02                                                                                                                                   |
| **Nombre**               | Recuperación de Contraseña                                                                                                             |
| **Cumple (Sí/No)**       | Sí                                                                                                                                     |
| **Descripción**          | Verificar que el sistema permite al usuario recuperar su contraseña enviando un enlace de restablecimiento al correo proporcionado.    |
| **Precondiciones**       | El usuario debe estar registrado y activo. <br> El microfrontend de autenticación debe estar configurado y desplegado.                 |
| **Pasos**                | 1. Acceder a la página de recuperación de contraseña. <br> 2. Ingresar el correo del usuario registrado. <br> 3. Enviar el formulario. |
| **Datos de Prueba**      | Correo: juan.perez@example.com                                                                                                         |
| **Resultados Esperados** | El sistema genera un token único, envía un correo con el enlace de restablecimiento y desactiva el token tras su uso.                  |
| **Resultados Obtenidos** | El sistema generó el token, envió el correo y desactivó el token después de su uso.                                                    |

---

## Caso de Prueba: Actualización de Información Personal

| **ID**                   | CP04                                                                                                                                                 |
| ------------------------ | ---------------------------------------------------------------------------------------------------------------------------------------------------- |
| **Historia de Usuario**  | HU03                                                                                                                                                 |
| **Nombre**               | Actualización de Información Personal                                                                                                                |
| **Cumple (Sí/No)**       | Sí                                                                                                                                                   |
| **Descripción**          | Verificar que el usuario puede actualizar su información personal desde la pantalla de perfil.                                                       |
| **Precondiciones**       | El usuario debe estar autenticado. <br> El microfrontend de perfil debe estar configurado y desplegado.                                              |
| **Pasos**                | 1. Acceder a la pantalla de perfil. <br> 2. Editar los campos de información personal (por ejemplo, nombre, dirección). <br> 3. Guardar los cambios. |
| **Datos de Prueba**      | Nombre: Juan Carlos <br> Dirección: Calle Principal 456                                                                                              |
| **Resultados Esperados** | El sistema actualiza los datos del usuario y muestra un mensaje de confirmación.                                                                     |
| **Resultados Obtenidos** | Los datos fueron actualizados correctamente y se mostró el mensaje esperado.                                                                         |

---

## Caso de Prueba: Cambio de Contraseña desde Perfil

| **ID**                   | CP05                                                                                                                                                                                     |
| ------------------------ | ---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| **Historia de Usuario**  | HU04                                                                                                                                                                                     |
| **Nombre**               | Cambio de Contraseña desde Perfil                                                                                                                                                        |
| **Cumple (Sí/No)**       | Sí                                                                                                                                                                                       |
| **Descripción**          | Verificar que el usuario autenticado puede cambiar su contraseña desde la pantalla de perfil.                                                                                            |
| **Precondiciones**       | El usuario debe estar autenticado. <br> El microfrontend de perfil debe estar configurado y desplegado.                                                                                  |
| **Pasos**                | 1. Acceder a la pantalla de perfil. <br> 2. Navegar al formulario de cambio de contraseña. <br> 3. Proporcionar la contraseña actual y la nueva contraseña. <br> 4. Guardar los cambios. |
| **Datos de Prueba**      | Contraseña actual: ContraseñaSegura123 <br> Nueva contraseña: NuevaContraseña456                                                                                                         |
| **Resultados Esperados** | El sistema valida la contraseña actual, actualiza la contraseña a la nueva y muestra un mensaje de confirmación.                                                                         |
| **Resultados Obtenidos** | La contraseña fue cambiada correctamente y el sistema mostró el mensaje de confirmación.                                                                                                 |

---

## Caso de Prueba: Gestión de Productos Favoritos

| **ID**                   | CP06                                                                                                                                                             |
| ------------------------ | ---------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| **Historia de Usuario**  | HU05                                                                                                                                                             |
| **Nombre**               | Gestión de Productos Favoritos                                                                                                                                   |
| **Cumple (Sí/No)**       | Sí                                                                                                                                                               |
| **Descripción**          | Verificar que el usuario puede agregar, listar y eliminar productos en la lista de favoritos.                                                                    |
| **Precondiciones**       | El usuario debe estar autenticado. <br> El microfrontend de preferencias debe estar configurado y desplegado.                                                    |
| **Pasos**                | 1. Acceder a la pantalla de favoritos. <br> 2. Agregar un producto a la lista. <br> 3. Listar los productos favoritos. <br> 4. Eliminar un producto de la lista. |
| **Datos de Prueba**      | Producto: Producto 1 (ID: 101)                                                                                                                                   |
| **Resultados Esperados** | El sistema permite agregar, listar y eliminar productos favoritos, mostrando un mensaje de confirmación para cada acción.                                        |
| **Resultados Obtenidos** | Todas las acciones se realizaron correctamente, con los mensajes esperados.                                                                                      |
