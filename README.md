## Importación

### Excel

**Hoja de calculo**

Se importaría todo el contenido de la hoja de Excel, de tal manera que sería necesario que nuestra base de datos empezara en la celda A1 de la hoja que vamos a importar, ya que cualquier dato que haya en dicha hoja, aunque no tenga nada que ver con la base de datos, también se importaría a la tabla de Power BI.

**Rango**

En primer lugar, habría que definir dicho rango en Excel, para luego importarlo como tabla a Power BI. El inconveniente de un rango es que, si entran filas por debajo de la última del rango o columnas a la derecha de la última, el rango no lo cogería, por lo que tendríamos que actualizar el fichero de Excel cada vez que hagamos este tipo de operaciones.

## Importante
- La importación más recomendable es la de una tabla de datos.
- Como hemos mencionado anteriormente, desde Power BI, no podemos agregar, eliminar o modificar datos, ya que los tenemos en lectura. Para modificar los datos, hay que hacerlo en el fichero de origen, en el Excel que acabamos de importar.
- Una vez se haga una actualización en el excel, entonces: Lo haremos desde la ficha INICIO en el GRUPO CONSULTAS, pulsando el botón ACTUALIZAR en power BI


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

