# Clase 1: ¿Qué es SASS y en qué se diferencia de otros procesadores?
SASS: Syntactcally Awesome Style Sheets procesador de CSS se utiliza para trabajar estilos de proyectos agregando funcionalidades que no cuenta CSS. Basado en Ruby.
Caracteristicas:
* Variables: almacenan datos
* Mixins: parecido a funciones reciben parametros de entrada
* Selectores anidados menos codigo y es más mantenible
* Herencia permite compartir propiedades entre selectores
### Tipos de archivos
Es flexible es compatible con CSS, se puede utilizar .sass o .scss
-.sass: sintaxis identada, se quita {} y ; tras cada declaracion
-.scss: utiliza sintaxis Css incluye {} y ; tras cada declaracion 
Presentacion de proyecto en Figma Eco-Store Mockups
# Clase 2: ¿Comó funcionan los procesadores?
Preprocesador: herramienta que permite escribir pseudocodigo  recibiendo como parametro de entrada los estilos que posteriormente se convierten a CSS nativo.
En SASS se incluyen: variables, mixins,herencia de clases hacen que el Css sea mas facil y rapido 
### Ventajas:
-Rapidez y productividad 
-Mantenimiento del código los estilos se guardan en un solo archivo
-Reutilizacion de código
-Mas sencillo para trabajar una página web manera responsiva
# Clase 3: Anatomía de proyecto SASS  e instalación y configuración del entorno de trabajo
Proceso de compilación:
Imput file (archivo de entrada) —> Es donde vamos a escribir nuestros estilos haciendo uso de la sintaxis de Sass, incluyendo la extensión .scss en el nombre del archivo. .
Output file (archivo de salida) —> Es donde se colocarán los estilos finales con CSS nativo, que provienen del archivo de entrada. (nunca se debe editar directamente el archivo de salida) .
Los comandos para ejecutar y compilar Sass —> Hay varias formas de ejecutar y compilar Sass, cada una con sus propios comandos y herramientas. La elección del método dependerá del entorno de desarrollo y las preferencias personales del desarrollador.