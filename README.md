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