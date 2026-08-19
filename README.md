## Importación

### Excel

**Hoja de calculo**

Se importaría todo el contenido de la hoja de Excel, de tal manera que sería necesario que nuestra base de datos empezara en la celda A1 de la hoja que vamos a importar, ya que cualquier dato que haya en dicha hoja, aunque no tenga nada que ver con la base de datos, también se importaría a la tabla de Power BI.

**Rango**

En primer lugar, habría que definir dicho rango en Excel, para luego importarlo como tabla a Power BI. El inconveniente de un rango es que, si entran filas por debajo de la última del rango o columnas a la derecha de la última, el rango no lo cogería, por lo que tendríamos que actualizar el fichero de Excel cada vez que hagamos este tipo de operaciones.


## Formato a columnas

Podemos cambiar el tipo de dato de las columnas con tipo compatible, es decir, entre columnas numéricas o fechas. No obstante, si cambiamos el tipo de dato, no lo solemos realizar desde Power BI, más bien desde Power Query

**Para cambiar el formato de una columna**, seleccionamos la misma y en la ficha HERRAMIENTAS DE COLUMNAS, en el GRUPO FORMATO, podemos ajustarlo.
> Vista Tabla > Seleccionamos columna > Herramientas de columnas > Formato

### Formatos personalizados
- Caracteres de formato de número
 0 , #, "texto"ç

 0: caracater del formato de número obligatorio. Son 0, que se colocan a la izquierda e indican el número de cifras.
 
 #: Caracter de formato de número opciona, no coloca 0 a la izquierda, se usa para indicar el separador de miles.

 texto: Texto dentro del formato, se coloca ""

>Cuando creamos un formato, el separador de miles que se utiliza en Power BI es la coma: “,” y el separador decimal es el punto: “.”. Esto solo a la hora de crearlo, ya que luego, cuando en un informe nos muestra los datos formateados Power BI, vemos el separador de miles con el punto y el decimal con la coma

 Ejemplo:

#,##0” horas”

## Informes en power BI

#### Matriz

FILAS: agrupa los campos que agreguemos mostrando cada elemento en una fila.
COLUMNAS: agrupa los campos que agreguemos mostrando cada elemento en una columna.
VALORES: los campos que agreguemos los totaliza.

### Opciones de informes
- Filtro
- Modo enfoque
- Más opciones

### Ocultar campos

ocultar campos que no vamos a utilizar en informes, por tanto, los campos que ocultemos no aparecerán en el panel de datos de la vista informe.

### Cambiar la configuración predeterminada de un campo

Para cambiar esta función predeterminada, los podemos hacer en cualquier vista, aunque lo más habitual suele ser en la vista tabla, basta con seleccionar el campo en el panel de datos e ir a la ficha HERRAMIENTAS DE COLUMNAS y en el grupo de botones PROPIEDADES seleccionamos la opción RESUMEN


### Formato de visualización
VALORES PREESTABLECIDOS	
Para poner bordes a las filas, columnas y contorno de la tabla.

CUADRICULA	
Para poner bordes a las filas, columnas y contorno de la tabla.

VALORES	
Para dar formato a los valores mostrados en la tabla.

ENCABEZADOS DE COLUMNA	
Para dar formato a los títulos de cada columna de la tabla.

TOTALES	
Para formatear la fila de totales de la tabla, mostrada siempre la última fila.

COLUMNA ESPECIFICA	
Para formatear una a una cada columna que hayamos agregado a la tabla.

### Interación en los informes

Todos los informes, sean del tipo que sean, que estén en una misma página, tienen  interacción. Es decir, seleccionando un dato quedan filtradas todas las visualizaciones de la página.

#### Más Informes - Segmentación de datos

un tipo de informe que utilizamos para filtrar todas las visualizaciones de la página. A ella solo se agrega un único campo, de tal modo, que, al seleccionar un elemento del campo agregado, se emite un filtro por dicho elemento a todos los informes de la página.

Por tanto, es un elemento visual que utilizamos para aplicar filtros a todo el lienzo.
Entre las propiedades que destacan son la configuración de la segmentación(forma de ver los elementos) y valores (elementos del campo)

#### Tarjeta 

Totaliza un campo seleccionado

>La tarjeta es el único tipo de informe que no emite filtros sobre ninguna otra visualización, pero sí recibe filtros por parte de cualquier otro informe.

Entre las propiedades que destacan estan Valor del globo (conf. del dato que totaliza la tarjeta) y Etiqueta de categoría.

#### Gráficos de columnas y líneas

 Lo utilizamos cuando queremos representar en un mismo gráfico dos campos totalizados, uno con valores altos y otro con valores bajos. De esta forma, uno se medirá en un eje vertical principal y el otro en el eje vertical secundario.

### Gráfico circular
cuando no necesitamos ejes, es decir, cuando solo queremos ver la evolución de los elementos de un solo campo. Por ejemplo, queremos ver el número de cursos que se han dado en cada jornada.

## Panel de filtros
A través del panel de filtros podemos filtrar un único informe, todos los informes de la misma página o todos los informes de todas las páginas.

Cuando se agrega un grafico, en filtro se muestra:
- FILTROS DE ESTE OBJETO VISUAL: Se ven los campos agregado y los filtros que se creen aca, *afectaran solo a dicho informe* 
> tambien podemos filtrar por campos que no hemos agregado al informe (en agregar campo de datos)
- FILTROS DE ESTA PAGINA: Los campos que agreguemos a esta área filtrarán todos los informes que tengamos en esta página.
- FILTROS DE TODAS LAS PAGINAS: Los campos que agreguemos a esta área filtrarán todos los informes de todas las páginas.

El filtro más habitual en el panel de filtros es el del objeto visual. No obstante, en todas las áreas del panel de filtros se configuran exactamente igual todos los filtros.

Los filtros de un objeto visual se pueden aplicar tanto sobre tablas como matrices como gráficos, es decir, sobre cualquier tipo de informe, y se configuran exactamente igual en todos.

### Filtros en campos totalizados

Se pueden realizar filtros por campos que tenemos totalizados en el informe.

### Filtris TOP N
Este tipo de filtro es para resaltar los valores más altos o bajos de un campo.

Por ejemplo, en nuestra tabla queremos mostrar los 3 cursos que menos veces se han dado. Para ello, en el panel de filtros del objeto visual, expandimos los filtros del campo CURSO y seleccionamos el tipo de filtro TOP N.

## Formatos condicionales 

Tanto los campos que totalizamos en una matriz como los campos que agregamos a una tabla tienen activada la propiedad formato condicional, para poder resaltar aquellos valores en los que queramos llamar la atención.

> En una matriz, el formato condicional solo se puede aplicar a los campos del área de valores, mientras que en una tabla se puede aplicar a todos los campos, tanto a los que totalizamos como a los que agrupamos.

> Habitualmente, solemos aplicarlo solo a los valores, ya que a los totales absolutos es menos frecuente al totalizar a todos los valores.

¿Cómo hacer formato condicional?

Selecciono el campo > Clic en flecha hacia abajo > Formato condicional

> Si mantenemos la opción de DEGRADADO, no estableceríamos ninguna condición, lo que haría sería dar un color más oscuro a valores altos y más claro a valores bajos

¿Cómo eliminaria un formato condicional?

" Para eliminar un formato condicional de un campo, volveríamos a mostrar las opciones o propiedades del campo del que quitar el formato, y en este caso seleccionaríamos la opción QUITAR EL FORMATO CONDICIONAL, seguido del tipo de regla que eliminar "

### Formato de barra de datos

Este formato condicional se aplica para mostrar una barra en cada valor, de tal modo que, cuanto más larga es la barra, mayor es el dato, y cuanto más corta es la barra, menor es el dato.

Se agregan barras a tablas o a matrices, pero solo a campos totalizados

> Barras de datos: necesitan un valor numérico, por lo que se aplican a campos de valores/totalizados.

¿Cómo obtenerlo?
Selecciono el campo > Clic en flecha hacia abajo > Formato condicional > Barra de datos

> Si se desea mostrar barras y etiquetas, no activar check Mostrar solo barras

### Formato de iconos
Este formato condicional lo utilizamos para marcarnos un objetivo y, mediante iconos, ver los datos que no alcanzan dicho objetivo, los datos que lo consiguen y los datos que lo superan.

> Este formato condicional se puede dar tanto al campo por el que agrupamos de la tabla como al que totalizamos. Como siempre, en las matrices, solo al campo del área de valores.

## Introducción a Power Query

Power Query es el que manda los datos a Power BI, es decir, aunque nosotros hagamos las importaciones a través de Power BI, también podríamos importar tablas a través de Power Query, donde quedan guardados los datos.

Se puede decir que Power Query es el motor de Power BI, y que Power BI es la carrocería, lo que se ve por fuera. Ya que, como hemos dicho, Power Query marca los datos con los que vamos a trabajar en Power BI, y en el propio Power BI vamos a graficar y formatear esos datos para conocer la información que guardamos en nuestras tablas.

Para acceder a la ventana de Power Query:
ficha INICIO del fichero y en el grupo de botones CONSULTAS pulsamos directamente sobre el botón TRANSFORMAR DATOS.

En la ventana de Power Query, tenemos en la parte superior la CINTA DE OPCIONES, con las fichas: ARCHIVO, INICIO, TRANSFORMAR, AGREGAR COLUMNA, VISTA, HERRAMIENTAS Y AYUDA.

### Panel de consultas
Donde se van agregando las tablas que vamos importando desde Power BI.

### Panel de contenido
Donde nos muestra el contenido de la tabla que tenemos seleccionada en el panel de consultas. En él vemos tanto los campos como los registros.

Respecto al botón de filtro, si aplicamos un filtro desde Power Query, en Power BI solo trabajaremos y graficaremos sobre dichos registros filtrados.


### Panel de pasos
Situado en la parte derecha del área de trabajo, nos muestra el nombre de la tabla seleccionado. Desde aquí podemos cambiar el nombre de la tabla Por debajo, tenemos los pasos que hayamos aplicado sobre la tabla. 

> Cada operación que hagamos en el panel de contenido se agregará al panel de pasos. De tal forma que, en Power Query, no existe el botón deshacer; si hemos hecho un paso incorrecto, lo tendremos que eliminar en el panel de pasos

vemos que la tabla tiene por defecto tres pasos aplicados en el panel de pasos:

#### Origen
En dicho paso, está indicada la ruta del fichero donde está guardada la tabla que hemos insertado

> Al dar clic, se activa la barra de formulas, tener en cuenta que Power Query utiliza el lenguaje de programación M, que es lo que expresa sobre dicha barra de fórmulas. En algunos casos podemos hacer cambios de forma intuitiva, pero, por norma general, es aconsejable que, si no sabemos el lenguaje de programación M, no hagamos uso de ella.

##### Cambiando origenes de datos
si de un mismo fichero importamos varias tablas y el fichero de origen lo movemos de carpeta, lógicamente, a las tablas importadas de dicho fichero, tendríamos que actualizar la ruta del fichero de origen. Habiéndolo hecho a través del paso origen, lo tendríamos que hacer una a una cada una de las tablas.

Otra opción más rápida en este caso es cambiar la ruta de todo el fichero, de esta forma, todas las tablas que pertenezcan a dicho archivo actualizarán a la vez la ruta del nuevo origen de datos.

Para cambiar la ruta de todo el fichero, lo hacemos a través de la FICHA INICIO, en el grupo de botones ORIGENES DE DATOS, pulsamos el botón CONFIGURACION DE ORIGEN DE DATOS

Finalmente, para replicar a todas las tablas del archivo la ruta modificada, tendríamos que ACTUALIZAR los datos desde Power Query, a través del botón ACTUALIZAR VISTA PREVIA del grupo de botones CONSULTA de la ficha INICIO:


#### Navegación
En este paso es en el que seleccionamos el nombre de la tabla que estamos importando del fichero de origen. Este paso también tiene la rueda a su derecha. Si la pulsamos, nos muestra los rangos, hojas y tablas del fichero que hemos importado en el paso anterior. De esta forma, podemos cambiar de tabla en la importación. Si en el fichero de Excel modificamos el nombre de la tabla, en este paso tendremos que actualizarlo. 

#### Tipo cambiado
Es el paso en el que se asigna el tipo de dato a cada columna. Si vamos al panel de contenido del paso, vemos como en cada columna marca a la izquierda del nombre un único icono con el tipo de dato de esta.

> En algunos casos, al realizar un paso que genere una columna, Query inserta un paso tipo cambiado. Siempre que lo veamos, nos debemos fijar en él para ver a qué columna le está cambiando el tipo de dato, y si el tipo de dato que le ha asignado encaja con el tipo de dato con el que vamos a querer trabajar sobre dicha columna.

### Operaciones básicas en Query

> En primer lugar, hay que destacar que Query diferencia entre mayúsculas y minúsculas. Para que dos elementos sean iguales, han de tener los mismos caracteres y coincidir las mayúsculas y las minúsculas.

- **Eliminar columnas**: Se selccionan la col > clic derechos > quitar
- **Copiar columna**: Seleccionar col > pulsar sobre el botón derecho > del menú emergente > DUPLICAR COLUMNA.
- ** Cambiar el nombre de un paso**: Nos colocamos sobre el paso > pulsar botón derecho > del menú emergene > CAMBIAR NOMBRE
- **Copiar una tabla**: Ubicarse en panel consulta > Sleccionar tabla > pulsar botón derechos > DUPLICAR
- **Eliminar una tabla**
- **Cambiar nombre de una tabla.**
- **Cambiar nombre a una columna:** 
    - Dos clics rápidos con el botón izquierdo sobre la col o tabla.
    - Botón derecho sobre el nombre de de la col > CAMBIAR NOMBRE
- **Quitar filas**: FICHA INICIO > en el grupo de botones REDUCIR FILAS > Pulsar QUITAR FILAS
    - Nos muestra las siguientes opciones:
        - QUITAR FILAS SUPERIORES: indicar el número de filas superiores que queremos quitar de la tabla.
        - QUITAR FILAS INFERIORES: indicar el número de filas inferiores que queremos quitar de la tabla.
        - QUITAR FILAS ALTERNAS: indicar a partir de qué fila queremos empezar a eliminar, e indicar cada cuántas filas eliminamos y cada cuántas conservamos filas.
        - QUITAR DUPLICADOS: elimina las filas repetidas de las columnas que tenemos seleccionadas de la tabla.
        - QUITAR FILAS EN BLANCO: elimina los datos vacíos o nulos de las columnas que tenemos seleccionadas de la tabla.
        - QUITAR ERRORES: elimina los datos con error de las columnas que tengamos seleccionadas de la tabla.
        - FILTRAR DATOS: a través del botón de filtro de la columna que filtrar, procederemos a seleccionar las opciones que queramos filtrar

> Debemos tener en cuenta, que, si hacemos un filtro en Power Query, al cargar los datos a Power BI solo trabajaremos y graficaremos los datos cargados, es decir, los datos que se muestran en el filtro
- **Importar datos desde power Query**: FICHA INICIO en el grupo de botones NUEVA CONSULTA, seleccionando NUEVO ORIGEN.

### Transformaciones básicas
- **Formato**:
    Seleccionamos dicha columna, vamos a la ficha TRANSFORMAR y en el grupo de botones COLUMNA DE TEXTO seleccionamos el botón FORMATO.

    - MINÚSCULAS: pone todas las letras del campo seleccionado en minúsculas.
    - MAYÚSCULAS: pone todas las letras del campo seleccionado en mayúsculas.
    - PONER EN MAYÚSCULA CADA PALABRA: pone la primera letra de cada palabra en mayúsculas.
    - RECORTAR: elimina los espacios sobrantes del campo.
    - LIMPIAR: elimina los caracteres no imprimibles del campo.
    - AGREGAR PREFIJO: agrega un texto por delante de cada valor del campo seleccionado.
    - AGREGAR SUFIJO: agrega un texto por detrás de cada valor del campo seleccionado.

    Dicha opción también la tenemos desde la ficha AGREGAR COLUMNA:

- **Dividir columnas**: Esta opción es la equivalente a la opción TEXTO EN COLUMNAS de Excel. Lo que hacer es separar en varias columnas o campos el dato que tenemos en una sola columna o campo. Esta opción solo está disponible en la FICHA TRANSFORMAR.
    - POR DELIMITADOR: Para separar el texto utilizaríamos un separador, es decir, un carácter que cada vez que aparezca en el dato del campo se genera una nueva columna.
    - POR NUMERO DE CARACTERES	Tenemos que indicar cada cuántos caracteres queremos separar el texto.
    - POR POSICIONES: Indicamos en qué posiciones del texto queremos que se separe. Debemos tener en cuenta que el primer carácter es el 0.
    - DE MINUSCULA A MAYUSCULA: Como indica, lo separa por los caracteres en minúsculas y mayúsculas.
    - DE MAYUSCULA A MINUSCULA: Separa de los caracteres en mayúsculas a los que están en minúsculas.
    - DE DIGITO A NO DIGITO: De número a texto.
    - DE NO DIGITO A DIGITO: De texto a número.

- **Combinar columnas**: Esta opción de combinar columna la tenemos disponible tanto desde la ficha TRANSFORMAR como desde la ficha AGREGAR COLUMNA.
    - Esta opción lo que hace es juntar el contenido de las columnas seleccionadas. Para que se active, debemos tener seleccionadas las columnas que queremos juntar y haberlas seleccionado en el orden que las queremos colocar.
- **Extraer**: Podemos utilizarla tanto desde la ficha TRANSFORMAR como desde la ficha AGREGAR COLUMNA.
    - Nos muestra las siguientes opciones:
        - Longitud
        - Primeros caracteres
        - Ultimos caracteres
        - Texto antes del limitador
        - Texto despues del limitador
        - Texto entre limitadores
> Lo más habitual suele ser agregar nuevas columnas sobre campos fecha.

### Cargar datos a power BI

Una vez que hemos realizado todas las transformaciones, cargaremos los datos a Power BI. Para ellos, vamos a la ficha INICIO y pulsamos el botón CERRAR Y APLICAR, siendo el primer botón de dicha ficha inicio.

Automáticamente, los datos se cargarán en Power BI, las visualizaciones insertadas se actualizarán con los datos mostrados y transformados en Power Query y, en el panel de datos y vista tabla, los campos eliminados ya no estarán. Las columnas agregadas estarán disponibles y las columnas transformadas tendrán los cambios que hemos configurado.

## Importante
- La importación más recomendable es la de una tabla de datos.
- Como hemos mencionado anteriormente, desde Power BI, no podemos agregar, eliminar o modificar datos, ya que los tenemos en lectura. Para modificar los datos, hay que hacerlo en el fichero de origen, en el Excel que acabamos de importar.
- Una vez se haga una actualización en el excel, entonces: Lo haremos desde la ficha INICIO en el GRUPO CONSULTAS, pulsando el botón ACTUALIZAR en power BI
- El tipo de dato viene dado por los datos de origen, de tal modo que, si se detecta en un campo un tipo de dato texto, es porque en el fichero de origen que hemos importado dicha columna tiene al menos un valor texto.
- Podemos cambiar el tipo de dato de las columnas con tipo compatible, es decir, entre columnas numéricas o fechas. No obstante, si cambiamos el tipo de dato, no lo solemos realizar desde Power BI, más bien desde Power Quer

## Prácticas 

### Práctica I

El fichero 06. BD FACTURAS es una base de datos en la que vamos registrando diferentes facturas realizadas a clientes, de distintos conceptos, y que tiene las siguientes columnas:
NUMERO FACTURA CLIENTE: se indica el número de la factura.
CONCEPTO: el concepto que estamos facturando.
CLIENTE: el cliente al que le emitimos la factura.
PROVINCIA: provincia en la que está el cliente al que le facturamos.
SECTOR: sector al que pertenece el cliente al que facturamos.
IMPORTE CLIENTE: importe que facturamos al cliente.
FECHA FACTURA CLIENTE: fecha de emisión de la factura.
PAGADA CLIENTE: indicamos si el cliente ha pagado o no la factura.
PROVEEDOR: cada factura que hacemos es un servicio que contratamos a un proveedor, por tanto, en esta columna indicamos el nombre del proveedor que estamos contratando para dar el servicio que estamos facturando.
ZONA: la zona que cubre el proveedor.
TIPO: qué tipo de proveedor es.
IMPORTE PROVEEDOR: el importe que nos cobra el proveedor por darnos el servicio contratado.
A continuación, realiza las siguientes operaciones:
Inserta una tabla en el fichero 06. BD FACTURAS con el nombre T_FACTURAS
Guardar los cambios y cerrar el fichero.
Abrir un Power BI en blanco
Importar la tabla T_FACTURAS del fichero 06. BD FACTURAS
Expandir los campos en el panel de datos
Ir a la vista tabla
Guardar el fichero con el nombre BD FACTURAS


### Práctica II

El fichero de texto 07. BD FACTURAS tiene los mismos datos que el fichero 06. BD FACTURAS de Excel que hemos importado en la práctica anterior. Realiza las siguientes operaciones:
Abrir un POWER BI en blanco
Importar el fichero de texto 07. BD FACTURAS
Ir a la vista tabla
Guardar el fichero con el nombre BD FACTURAS TXT

### Práctica III

Vamos a modificar el nombre de los otros dos campos de valores de la tabla:
PROMEDIO DE DURACION: mostrarlo como MEDIA HORAS
% TG SUMA DE DURACION: mostrarlo como % HORAS

### Práctica IV

Abrir el fichero de Power BI BD FACTURAS, que lo hemos guardado anteriormente.
1. Ir a la vista tabla y cambiar los formatos de los siguientes campos:

IMPORTE CLIENTE: personalizar un formato con separador de miles y dos posiciones decimales que termine con el texto: Eur. (por ejemplo, un importe de 1250,25 se mostrará como: 1.250,25 Eur.).
IMPORTE PROVEEDOR: aplicar un formato moneda con el símbolo del €.
FECHA FACTURA CLIENTE: aplicar un formato de fecha: dd/mm/yyyy.
Cambiar la función predeterminada del campo NUMERO FACTURA CLIENTE a RECUENTO.
Ocultar los campos: FECHA FACTURA CLIENTE y ZONA.
2. Ir a la vista informe e insertar una tabla que de cada CLIENTE muestre: RECUENTO DEL NUMERO FACTURA CLIENTE, SUMA IMPORTE CLIENTE, % DEL TOTAL GENERAL SOBRE LA SUMA DEL IMPORTE CLIENTE. Cambiar en dicha tabla el nombre de los siguientes campos:

RECUENTO DE NUMERO FACTURA CLIENTE: TOTAL FACTURAS
SUMA DE IMPORTE CLIENTE: TOTAL CLIENTE
% TG SUMA DE IMPORTE CLIENTE: % TOTAL CLIENTE
3. Ordenar la tabla por el campo TOTAL FACTURAS de menor a mayor. Insertar una tabla que cuente en cada PROVINCIA el número diferente de CLIENTES que hay (APLICAR AL CAMPO CLIENTE EL RECUENTO DISTINTIVO). Cambiar el campo RECUENTO CLIENTE por NUM CLIENTES.

 4. Insertar una matriz, que muestre:

FILA: CONCEPTO
COLUMNA: TIPO
VALORES: RECUENTO DE NUMERO FACTURA CLIENTE
Guardar los cambios y cerrar el fichero.


### Práctica V

Abrir el fichero de Power BI BD FACTURAS.
Seleccionar la tabla de clientes y cambiar los siguientes formatos:
Poner los encabezados en negrita y centrados.
Poner los valores en cursiva.
Poner en la fila de totales el texto: TOTALES CLIENTE
Seleccionar la tabla de clientes y cambiar los siguientes formatos:
Seleccionar la matriz y cambiar los siguientes formatos:
Poner los encabezados de columna en negrita.
Poner los encabezados de fila en negrita y cursiva.
Filtrar los informes de la página por la provincia de ALICANTE.
Guardar los cambios y cerrar el fichero.

### Práctica 5
1. Abrir el fichero BD FACTURAS e ir a la vista informe.

2. Agregar una nueva página de informe y nombrarla como GRAFICOS. Insertar un gráfico de barras 100 % apiladas que muestre:

   - EJE Y: CONCEPTO
   - EJE X: RECUENTO DE NUMERO FACTURA CLIENTE
   - LEYENDA: SECTOR
   
3. Mostrar las etiquetas de datos.

4. Insertar un gráfico de anillos que muestre:

    - LEYENDA: SECTOR
    - VALORES: RECUENTO DE NUMERO FACTURA CLIENTE

5. Cambiar el color del segmento CONTRUCCION a color GRIS

6. Insertar una tarjeta que haga el RECUENTO DE NUMERO FACTURA CLIENTE.

    - Cambiar el texto de la etiqueta por TOTAL FACTURAS.
    - Dar un color de fondo azul y una sombra amarilla.
7. Insertar una segmentación de datos del campo PROVINCIA y filtrar por la provincia de MADRID.

    Guardar los cambios y cerrar el fichero.

### Práctica 6

Insertar un gráfico de barras agrupadas en la página FILTROS del fichero BD CURSOS que muestre:

   - EJE Y: CLIENTE
   - EJE X: SUMA DE IMPORTE CLIENTE

A continuación, filtrar el gráfico por los dos clientes de ESPAÑA con la suma del importe cliente más alta.

Guardar los cambios y cerrar el fichero.

### Práctica 7

Aplicar un formato condicional al campo CURSO para poner la fuente en color azul de los cursos cuya SUMA DE DURACION es mayor de 1200.

### Práctica 8 p. 1

* Insertar una tabla en el fichero de Excel con el nombre T_CLIENTE.
* Guardar los cambios y cerrar el fichero.
* Abrir un Power BI en blanco.
* Importar la tabla T_CLIENTES al Power BI en blanco.
* Guardar el fichero con el nombre BD PERSONAS.

### Práctica 8 p. 2

Ir al editor de Query del fichero 08. BD PERSONAS y, desde la ficha transformar, realizar las siguientes transformaciones:

* Poner las columnas NOMBRE, APELLIDO1 Y APELLIDO2 con la primera letra mayúscula.
* Combinar las columnas NOMBRE, APELLIDO1 Y APELLIDO2, separando cada una por un espacio y nombrar la columna combinada como nombre completo.
* Dividir la columna NIF en dos columnas, en una los 8 números y en la otra la letra.
* Poner la columna con la letra del NIF en mayúscula.
* Combinar ambas columnas del NIF separando los números de las letras por un guion.
* Nombrar a la columna combinada como: NIF

Desde la ficha AGREGAR COLUMNA, agregar las siguientes columnas sobre la fecha incorporación:

* AÑO: el nombre de la fecha incorporación.
* TRIMESTRE: el trimestre del año de la fecha incorporación.
* Desde la ficha TRANSFORMAR, poner el prefijo: “TRIM.” delante de cada trimestre, de tal modo que se vean como: TRIM. 1, TRIM. 2, TRIM. 3, TRIM. 4.

Cargar los datos en Power BI.

Guardar los cambios al fichero BD PERSONAS.