1. Clase Application:

El punto de entrada de la aplicación Spring Boot.
Contiene el método main para iniciar la aplicación.
Define un CommandLineRunner para insertar libros de ejemplo en la base de datos al iniciar la aplicación.

2. Clase LibroController:

Define un endpoint RESTful /libros/buscar para buscar libros.
Recibe un parámetro filtro que puede ser el título del libro o vacío.
Si el filtro está vacío, devuelve todos los libros.
Si el filtro tiene contenido, busca libros por título utilizando findByTituloContainingIgnoreCase de LibroRepository.

3. Clase Libro:

Define la entidad Libro con atributos como id, titulo, autor e isbn.
Contiene getters y setters para acceder y modificar los atributos de un libro.

4. Interfaz LibroRepository:

Extiende JpaRepository<Libro, Long>, lo que le da acceso a operaciones CRUD básicas sobre libros.
Define un método findByTituloContainingIgnoreCase(String titulo) para buscar libros por título de forma no sensible a mayúsculas y minúsculas.
