# API Endpoints

## Microservicio de Productos

### Crear un nuevo producto
**Método:** `POST`  
**Endpoint:** `/products`  
**Descripción:** Permite añadir un nuevo producto al catálogo.  

### Obtener la lista de productos
**Método:** `GET`  
**Endpoint:** `/products`  
**Descripción:** Recupera la lista completa de productos en el catálogo.  

### Obtener un producto por ID
**Método:** `GET`  
**Endpoint:** `/products/:id`  
**Descripción:** Recupera la información de un producto específico por su ID.  

### Actualizar un producto por ID
**Método:** `PUT`  
**Endpoint:** `/products/:id`  
**Descripción:** Actualiza los datos de un producto existente por su ID.  

### Eliminar un producto por ID
**Método:** `DELETE`  
**Endpoint:** `/products/:id`  
**Descripción:** Elimina un producto del catálogo por su ID.  

---

## Microservicio de Imágenes

### Asignar una imagen a un producto
**Método:** `POST`  
**Endpoint:** `/images`  
**Descripción:** Permite asignar una nueva imagen a un producto desde el API de Unsplash.  

### Obtener todas las imágenes
**Método:** `GET`  
**Endpoint:** `/images`  
**Descripción:** Recupera la lista completa de imágenes asociadas a productos.  

### Obtener una imagen por ID
**Método:** `GET`  
**Endpoint:** `/images/:id`  
**Descripción:** Recupera una imagen específica por su ID.  

### Actualizar una imagen por ID
**Método:** `PUT`  
**Endpoint:** `/images/:id`  
**Descripción:** Actualiza los datos de una imagen existente por su ID.  

### Eliminar una imagen por ID
**Método:** `DELETE`  
**Endpoint:** `/images/:id`  
**Descripción:** Elimina una imagen por su ID.  

---

## Microservicio de Reseñas (Reviews)

### Crear una nueva reseña
**Método:** `POST`  
**Endpoint:** `/reviews`  
**Descripción:** Permite añadir una nueva reseña para un producto.  

### Obtener todas las reseñas
**Método:** `GET`  
**Endpoint:** `/reviews`  
**Descripción:** Recupera la lista completa de reseñas.  

### Obtener una reseña por ID
**Método:** `GET`  
**Endpoint:** `/reviews/:id`  
**Descripción:** Recupera una reseña específica por su ID.  

### Actualizar una reseña por ID
**Método:** `PUT`  
**Endpoint:** `/reviews/:id`  
**Descripción:** Actualiza los datos de una reseña existente por su ID.  

### Eliminar una reseña por ID
**Método:** `DELETE`  
**Endpoint:** `/reviews/:id`  
**Descripción:** Elimina una reseña por su ID.  

---

## Microservicio de Atributos

### Crear un nuevo atributo
**Método:** `POST`  
**Endpoint:** `/attributes`  
**Descripción:** Permite crear un nuevo atributo.  

### Obtener todos los atributos
**Método:** `GET`  
**Endpoint:** `/attributes`  
**Descripción:** Recupera la lista completa de atributos.  

### Obtener un atributo por ID
**Método:** `GET`  
**Endpoint:** `/attributes/:id`  
**Descripción:** Recupera un atributo específico por su ID.  

### Actualizar un atributo por ID
**Método:** `PUT`  
**Endpoint:** `/attributes/:id`  
**Descripción:** Actualiza un atributo existente por su ID.  

### Eliminar un atributo por ID
**Método:** `DELETE`  
**Endpoint:** `/attributes/:id`  
**Descripción:** Elimina un atributo por su ID.  
