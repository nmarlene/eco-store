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
# Clase 4: Estructura de hoja de estilos y variables
Estructura de la hoja de estilos
Algunos statements contienen bloques y se definen entre un par de llaves { } , son separados mediante punto y coma ;

Top-level statements
Son declaraciones que solo se pueden usar en la parte superior de la hoja de estilos

Imports
Definición de un Mixin
Definición de una Función
Módulos
Universal statements
Son statements que podemos usar en cualquier parte de la hoja de estilos.

Variables, estructuras de control y las reglas @error, @warn y @debug.
Declaraciones CSS: Reglas de estilo, At-rules y Mixis.
Variables
Es un espacio de memoria asignado en memoria y únicamente puede almacenar un dato.

Las variables pueden ser declaradas en cualquier parte de la hoja de estilos.
Para asignar un valor a una variable se hace uso del simbolo $ de esta manera es posible referenciar dentro de la hoja de estilos.
Diferencias en Variables en CSS y SASS
CSS Variable	Sass Variables
Pueden tener diferentes valores para distintos elementos	Tienen un valor único correspondiente a un elemento
Son declarativas	Son imperativas (en el momento en el que actualicemos el valor de nuestra variables va a cambiar en automático)
!default flag
Se encarga de asignar un valor a la variable si y solo si esa variable no esta definida o su valor en null.
# Clase 5: Uso de selectores, scope variables y shadowing 
Selector define sobre qué elementos se aplica un conjunto de reglas CSS
Tipos:
-Clase
-ID
-Tipo
-Atributo
Scope: Hace referencia al contexto en el q son declaradas las variables y donde es posible hacer uso de las mismas
Variables locales: se declaran dentro de un bloque {}  y cualquier selector anidado puede acceder a las variables locales declaradas dentro del selector
Variables globales:Por default, son declaradas fuera de un selector. Se puede acceder en cualquier parte de nuestra hoja de estilos
Shadowing: Las variables locales y globales pueden tener los mismos nombres si se encuentran en diferente nivel del scope. Esto ayuda a que no se llegue modificar por error el valor de las variables globales 
!global flag en caso que se quiere modificar el valor global de una variable dentro del scope de una variable local
# Clase 6: At Rules: Css y nesting 
At-rules en CSS:
Declaracion que cumple con diferentes funciones, se inicializa con el simbolo @ y cuenta con sintaxis propia. Mantiene compatibilidad con versiones futuras de Css
Tipos:
@use: importa, modulos estilos y funciones de otras hojas de estilos. la diferencia con @import es que import se encarga de hacer los estilos globales.
@function: permite crear funciones personalizadas, sin embargo Sass cuenta con funciones ya existentes.
@forward: Recibe como parametro una URL y nos ayuda a cargar los estilos de nuestra hoja de estilos, es muy importante hacer uso de @use para que los modulos esten disponibles en nuestra hoja de estilos.
@extend: tiene que ver con el concepto de herencia.
@at-root: se encarga de cargar nuestros estilos en el root del css.
At-rules para compilacion
@include: nos ayuda a invocar los mixins.
@error, @warn @debug: sirver para cuando hay un error, una advertencia o se quiere debugear, respectivamente
@for, @if, @each, @while: tienen que ver con estructuras de control, se pueden usar dentro de una función
Nesting: la anidacion permite tener selectores dentro de otros, simplifican el codigo. Se escriben en el orden que estan en HTML
# Clase 7: Expresiones: literales y operaciones
Las expresiones es todo lo que va del lado derecho de una variable, admitiendo varios tipos de valores. Ya que se pasan como argumentos a mixins y funciones
Expresiones literales:
-Numeros, Strings, Colores,Booleanos, Null, Listas y Mapas
# Clase 8: ¿Qué es Herencia y cómo funciona SASS?
Herencia mecanismo mediante el cual un selector puede recibir estilos CSS q viene de variables utilizadas previamente
@extend permite organizar el codigo y crear CSS mas limpio
# Clase 9 : Mixins en CSS
Mixins permiten definir estilos q se pueden reutilizar en toda su hoja de estilos y facilitan evitar el uso de clase no semanticas 
Se declara con regla @minxin seguido del nombre que queremos que se asigne y se invoca con @include seguido del nombre del mixin
Argumentos en mixin es el nombre de la variable que esta separado por una coma
# Clase 10: Funciones
Las funciones permiten definir operaciones complejas en valores de SASS, se definen usando la regla @function
Tipos:
- RGB 
- HSL
- Opacidad
- Strings
- Numeros
Sass es compatible con operadores utiles para trabajar valores, incluyen operadores estandar y otros tipos == y !=
Jerarquia de operaciones:
1. Unarios not, + y -;
2. *, / y %;
3. + Y -;
4. >,>=,< Y <=
5. == Y !=
6. logico AND
7. logico OR
8. asignacion =
Declaracion de funcion: se llaman utilizando de sintaxis de funcion CSS normal