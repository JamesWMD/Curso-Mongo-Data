docker-compose.yml: es para configura la coneccion con Docker
.editorconfig: es para configura mi entorno en Visual Studio Code
-------------------------------------------------------------------------

Tipos BSON (https://www.mongodb.com/docs/manual/reference/bson-types/)
BSON es un formato de serialización binaria que se utiliza para almacenar documentos y realizar llamadas a procedimientos remotos en MongoDB.
La especificación BSON se encuentra en bsonspec.org.

Cada tipo de BSON tiene identificadores de cadena y enteros, como se indica en la siguiente tabla:
___________________________________________________________________--__________________
Type                        |Number | Alias                 | Notes
____________________________|______ |_______________________|__________________________
Double                      |  1    | "double"              |
String                      |  2    | "string"              |
Object                      |  3    | "object"              |
Array                       |  4    | "array"               |
Binary data                 |  5    | "binData"             |
Undefined                   |  6    | "undefined"           | Deprecated.
ObjectId                    |  7    | "objectId"            |
Boolean                     |  8    | "bool"                |
Date                        |  9    | "date"                |
Null                        |  10   | "null"                |
Regular Expression          |  11   | "regex"               |
DBPointer                   |  12   | "dbPointer"           | Deprecated.
JavaScript                  |  13   | "javascript"          |
Symbol                      |  14   | "symbol"              | Deprecated.
JavaScript code with scope  |  15   | "javascriptWithScope" | Deprecated in MongoDB 4.4.
32-bit integer              |  16   | "int"                 |
Timestamp                   |  17   | "timestamp"           |
64-bit integer              |  18   | "long"                |
Decimal128                  |  19   | "decimal"             |
Min key                     |  -1   | "minKey"              |
Max key                     |  127  | "maxKey"              |
________________________________________________________________________________________

* El $type operador admite el uso de estos valores para consultar campos por su tipo BSON.
  $type también admite el numberalias, que coincide con los tipos de BSON entero, decimal, doble y largo.

* El $typeo perador de agregación devuelve el tipo BSON de su argumento.

* El $isNumber operador de agregación devuelve truesi su argumento es un número entero, decimal, doble o largo de BSON. Nuevo en la versión 4.4

Para determinar el tipo de un campo, consulte Type Checking.
https://www.mongodb.com/docs/mongodb-shell/reference/data-types/#std-label-check-types-in-shell


Si convierte BSON a JSON, consulte la referencia de JSON extendido Extended JSON.
https://www.mongodb.com/docs/manual/reference/mongodb-extended-json/

-------------------------------------------------------------------------------------------------


DESNORMALIZACION:
Es el proceso de optimizar el funcionamiento de una DB agregando datos redundantes

Computed pattern:
1- Requerimientos (Workload)
2- Identificar ER (Entidad-Relacion)
3- Aplicar patrones
