Espesificaciones y requisitos

Requisitos funcionales

Validaciones de datos de usuario

El nombre debe tener mínimo tres letras y no puede contener números.

El apellido debe tener mínimo tres letras y no puede contener números.

El documento debe tener entre 3 y 15 dígitos y solo permite números.

El tipo de vínculo debe seleccionarse entre las siguientes opciones, con su respectivo valor de tiquete:

Estudiantes → $7.500

Docentes → $10.000

Administrativos → $8.500

Oficiales internos → $7.000

Público externo → $15.000

En caso de error en estas validaciones, el sistema debe informar al usuario. Si existen múltiples errores, pueden mostrarse en lista o de manera secuencial.

Gestión de reservas

El sistema solo permitirá registrar reservas a usuarios registrados.

El usuario podrá seleccionar la película y un asiento. Inicialmente solo podrá reservar un asiento por transacción.

El sistema debe mostrar la disponibilidad con el símbolo “O” para asiento libre y “X” para asiento ocupado.

Al confirmar la reserva, el asiento cambia de “O” a “X”, se genera el tiquete y la factura, y el usuario vuelve al menú inicial.

El sistema permitirá cancelar reservas activas. Si un usuario no tiene reservas, debe mostrarse un mensaje informando la situación.

Al cancelar, un asiento reservado (“X”) vuelve a estar disponible (“O”).

Si un usuario tiene varias reservas, deberá indicar cuál desea cancelar.

Consulta de funciones

El sistema mostrará en orden de día, hora y nombre las películas programadas exclusivamente para el próximo fin de semana.

Se incluirá la disponibilidad de asientos.

Ejemplo de cartelera: Interstellar, Oppenheimer y The Imitation Game, con un total de 9 funciones y disponibilidad por función.

Administración

Solo los usuarios con credenciales válidas podrán acceder al módulo de administración.

El módulo de administración ofrecerá los siguientes reportes:

Total de reservas registradas.

Total de tiquetes vendidos.

Total de reservas realizadas.

Total de pagos recibidos.

Promedio de ventas diarias del cine.

Lista de usuarios registrados.

Usuario con mayor y menor cantidad de reservas.

Requisitos no funcionales

El sistema debe ejecutar operaciones básicas (reserva, cancelación, consulta) en un tiempo máximo de 2 segundos.

Se deben validar credenciales para el acceso administrativo y proteger datos sensibles.

Los mensajes de error deben ser claros y comprensibles.

La visualización de butacas debe ser simple, usando “X” y “O” para representar asientos ocupados y disponibles.

El sistema debe garantizar consistencia en el registro y cancelación de reservas.

La primera versión debe ejecutarse en consola (Python), con posibilidad de evolucionar a una interfaz gráfica o web.

Criterios de aceptación

Si el documento contiene letras, debe rechazarse y mostrarse un mensaje de error.

Al reservar un asiento disponible, este debe cambiar de “O” a “X” y emitirse la factura correspondiente.

Si un usuario intenta cancelar sin tener reservas activas, debe mostrarse un mensaje de advertencia.

La consulta de funciones debe mostrar únicamente las películas del próximo fin de semana.

Solo los usuarios con credenciales correctas deben acceder al módulo de administración.
