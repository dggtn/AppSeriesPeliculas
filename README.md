<h1>Aplicación Java para Buscar Series y Películas</h1>

  <p>Esta es una aplicación desarrollada en Java que permite buscar información sobre series y películas desde un archivo JSON. La aplicación está diseñada para funcionar desde la consola e implementa clases, excepciones y el tipo de datos `record` de Java.</p>

  <h2>Características</h2>
  <ul>
      <li>Busqueda por nombre de series o películas.</li>
      <li>Lectura de datos desde un archivo JSON.</li>
      <li>Uso de clases y excepciones para manejar errores.</li>
      <li>Implementación de un `record` para representar las series y películas.</li>
  </ul>

  <h2>Requisitos</h2>
  <ul>
      <li>Java 17 o superior.</li>
      <li>Un archivo JSON con información sobre las películas y series.</li>
  </ul>

  <h2>Instalación</h2>
  <p>Para ejecutar esta aplicación, siga estos pasos:</p>
  <ol>
      <li>Descargue el proyecto desde el repositorio.</li>
      <li>Compile el código Java utilizando el siguiente comando:</li>
      <pre><code>javac Main.java</code></pre>
      <li>Ejecute la aplicación con el comando:</li>
      <pre><code>java Main</code></pre>
  </ol>

  <h2>Archivo JSON de Ejemplo</h2>
  <p>El archivo JSON debe tener la siguiente estructura:</p>
  <pre><code>[
{
  "titulo": "Breaking Bad",
  "tipo": "Serie",
  "anio": 2008,
  "genero": "Crimen, Drama, Suspenso"
},
{
  "titulo": "Inception",
  "tipo": "Película",
  "anio": 2010,
  "genero": "Acción, Ciencia Ficción, Suspenso"
}
]</code></pre>

  <h2>Estructura del Proyecto</h2>
  <p>El proyecto tiene la siguiente estructura:</p>
  <pre><code>/
├── Main.java                # Clase principal que ejecuta la búsqueda
├── Serie.java               # Clase que representa una serie
├── Pelicula.java            # Clase que representa una película
├── Pelicula.java            # Clase que representa una película
├── data.json                # Archivo JSON con los datos de las series y películas
└── README.html              # Este archivo</code></pre>

  <h2>Uso de la Aplicación</h2>
  <p>Al ejecutar la aplicación, podrá realizar búsquedas por consola. Por ejemplo:</p>
  <pre><code>Ingrese el nombre de la serie o película que desea buscar: Breaking Bad</code></pre>
  <p>La aplicación buscará en el archivo JSON y mostrará la información correspondiente.</p>

  <h2>Implementación Técnica</h2>

  <h3>Clases y `record`</h3>
  <p>La aplicación hace uso del tipo de datos <code>record</code> para representar las entidades de serie y película. Esto permite tener un código más limpio y conciso.</p>

  <h4>Clase Serie (record)</h4>
  <pre><code>public record Serie(String titulo, String tipo, int anio, String genero) {}</code></pre>

  <h4>Clase Pelicula (record)</h4>
  <pre><code>public record Pelicula(String titulo, String tipo, int anio, String genero) {}</code></pre>

  <h3>Excepciones</h3>
  <p>Se han implementado excepciones para manejar errores como cuando no se encuentra una serie o película o si el archivo JSON tiene un formato incorrecto.</p>

  <h4>Excepción para manejar la búsqueda no encontrada</h4>
  <pre><code>public class ElementoNoEncontradoException extends Exception {
  public ElementoNoEncontradoException(String mensaje) {
      super(mensaje);
  }
}</code></pre>

  <h2>Contribuciones</h2>
  <p>Si deseas contribuir al proyecto, por favor sigue estos pasos:</p>
  <ol>
      <li>Haz un fork del repositorio.</li>
      <li>Crea una rama para tu contribución.</li>
      <li>Realiza tus cambios y asegúrate de que todo funcione correctamente.</li>
      <li>Haz un pull request con una descripción detallada de los cambios realizados.</li>
  </ol>

  <h2>Licencia</h2>
  <p>Este proyecto está bajo la Licencia MIT - consulte el archivo <code>LICENSE</code> para más detalles.</p>

</body>
</html>
