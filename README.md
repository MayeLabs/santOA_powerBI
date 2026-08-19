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

## Importante
- La importación más recomendable es la de una tabla de datos.
- Como hemos mencionado anteriormente, desde Power BI, no podemos agregar, eliminar o modificar datos, ya que los tenemos en lectura. Para modificar los datos, hay que hacerlo en el fichero de origen, en el Excel que acabamos de importar.
- Una vez se haga una actualización en el excel, entonces: Lo haremos desde la ficha INICIO en el GRUPO CONSULTAS, pulsando el botón ACTUALIZAR en power BI
- El tipo de dato viene dado por los datos de origen, de tal modo que, si se detecta en un campo un tipo de dato texto, es porque en el fichero de origen que hemos importado dicha columna tiene al menos un valor texto.
- Podemos cambiar el tipo de dato de las columnas con tipo compatible, es decir, entre columnas numéricas o fechas. No obstante, si cambiamos el tipo de dato, no lo solemos realizar desde Power BI, más bien desde Power Quer

## Practicas 

### Practica I

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


### Practica II

El fichero de texto 07. BD FACTURAS tiene los mismos datos que el fichero 06. BD FACTURAS de Excel que hemos importado en la práctica anterior. Realiza las siguientes operaciones:
Abrir un POWER BI en blanco
Importar el fichero de texto 07. BD FACTURAS
Ir a la vista tabla
Guardar el fichero con el nombre BD FACTURAS TXT

### Practica III

Vamos a modificar el nombre de los otros dos campos de valores de la tabla:
PROMEDIO DE DURACION: mostrarlo como MEDIA HORAS
% TG SUMA DE DURACION: mostrarlo como % HORAS

### Practica IV

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


### Practica V

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

### Practica 5
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