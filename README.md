# procesamiento de datos
## Introdución 
Introducción:
En este proyecto se trabajará con una serie de datos para la división de préstamos de un banco.

Con esta información buscaremos la relación entre el estado civil, número de hijos que puedan tener un impacto en el préstamo de un crédito.

Con la información proporcionada por el banco como los ingresos, adeudos bancarios, propósitos para solicitar el prestamos, experiencia laboral y edad de un cliente, buscaremos la conexión entre solventar el pago de un préstamo con tener hijos, el estado civil, su nivel de ingresos y como el propósito puede afectar el pago a tiempo de un préstamo.

**Descripción de los datos**
- `children` - el número de hijos en la familia
- `days_employed` - experiencia laboral en días
- `dob_years` - la edad del cliente en años
- `education` - la educación del cliente
- `education_id` - identificador de educación
- `family_status` - estado civil
- `family_status_id` - identificador de estado civil
- `gender` - género del cliente
- `income_type` - tipo de empleo
- `debt` - ¿había alguna deuda en el pago de un préstamo?
- `total_income` - ingreso mensual
- `purpose` - el propósito de obtener un préstamo

## Preguntas a contestar 
¿Hay alguna conexión entre tener hijos y pagar un préstamo a tiempo?
- No, ya que la diferencia es minima y no trasciende para que exista una conexión

¿Existe una conexión entre el estado civil y el pago a tiempo de un préstamo?

- No, ya que la diferencia es minima y no trasciende para que exista una conexión

¿Existe una conexión entre el nivel de ingresos y el pago a tiempo de un 
préstamo?

- No, ya que la diferencia es minima y no trasciende para que exista una conexión

¿Cómo afectan los diferentes propósitos del préstamo al reembolso a 
tiempo del préstamo?
- Para los propósitos relacionados con un carro o en educación, la tabla de conversión es mayor, esto nos indica que con esos propósitos se dificulta el pago a tiempo de un préstamo

## conclusiones
- Se encontraron valores ausentes en las columnas 'days_employed' y 'total_income'
- Los valores ausentes posiblemente estuvieron, ya que las personas sin experiencia 'days_employed', no tienen trabajo y por ende no tienen un ingreso mensual 'total_income'
- Para remplazar los valores ausentes se creó una tabla dinámica donde el índice es el 'education_id' y el valor de cada índice es el promedio del sueldo dependiendo su 'education', con esa información se remplazó cada valor ausente con el promedio del sueldo con base a su educación 
- Para eliminar los valores duplicados se utilizó el metodo drop_dupiclarte ya que este método las filas duplicadas se eliminan junto con sus índices
- Ya que la tabla es una encuesta hay probabilidad de que mas de una persona este pasando por la misma situación
- Para cambiar el tipo de dato en la columna 'days_employed' recurrimos al metodo .astype ya que la función es muy útil cuando queremos poner un tipo de datos de columna en particular a otro tipo de datos.
- Se seleccionaron los diccionarios matplotlib.pyplot ya que con este diccionario nos permite grafiar los datos y con esto se puede analizar mejor los patrones
- Los datos negativos que aparecen en nuestro DataFrame son irrelevantes, estos representan información fuera de contexto en nuestra base de datos, estos datos pueden deberse a un error humano o falla en la entrada de datos

Con relación al análisis de Datos , y la información proporciona, las tasas de endeudamiento son bajas y no tiene conexión el incumplimiento de un pago con tener hijos o el propósito del mismo.
De igual manera el estdo civil como el nivel de ingreso no se obseva en las tazas de endeudamiento un patron o relación con el incumplimiento del pago
