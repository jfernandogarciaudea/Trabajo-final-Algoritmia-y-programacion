MANUAL DE USUARIO – Sistema de Gestión Cinema AGORA
1. Introducción

El sistema de gestión Cinema AGORA es una aplicación de consola diseñada para realizar el control básico del cine universitario. Permite administrar:

Registro de usuarios

Reservas de tiquetes

Cancelación de reservas

Consulta de funciones del fin de semana

Gestión administrativa (estadísticas, usuarios, pagos)

El sistema funciona mediante un menú interactivo que guía al usuario paso a paso.

2. Requisitos de Uso

Ejecutar el programa desde consola (Python 3.8+).

No requiere base de datos; toda la información se almacena en estructuras internas.

Conexión a Internet no es necesaria.

3. Inicio del Sistema

Al ejecutar el archivo principal, el sistema muestra el siguiente menú:

==============================================
                CINEMA AGORA
==============================================
Bienvenido al Cinema AGORA
1. Registrar Usuario
2. Registrar Reserva
3. Cancelar Reserva
4. Consultar Funciones Fin de Semana
5. Administrador
6. Salir
==============================================


El usuario debe elegir una opción entre 1 y 6.

4. Módulos del Sistema
4.1 Registrar Usuario

Acceso por opción 1 del menú.

El sistema solicitará:

Nombre

Apellido

Documento de identidad (solo números, 3-15 dígitos)

Tipo de vínculo, con tarifas predefinidas:

Estudiantes: $7500

Docentes: $10.000

Administrativos: $8.500

Oficiales internos: $7.000

Público externo: $15.000

Si algún dato no cumple los requisitos, el sistema mostrará errores y pedirá repetir el proceso.

Si el usuario ya existe, el sistema actualiza sus datos.

4.2 Registrar Reserva

Acceso por opción 2 del menú.

El proceso es:

Ingresar documento registrado
Si no existe, se ofrece registrar al usuario.

Seleccionar función
El sistema muestra las funciones disponibles, ordenadas por día y hora.

Visualizar asientos

O → asiento libre

X → asiento ocupado

Ingresar asiento
Formatos válidos:

AB

A B

A-B

Confirmación final
El sistema muestra:

Usuario

Película

Día / hora

Asiento

Precio

ID de la reserva

Fecha de compra

La reserva se guarda como activa.

4.3 Cancelar Reserva

Acceso por opción 3 del menú.

Proceso:

Ingresar documento.

Listar reservas activas del usuario.

Seleccionar el ID de la reserva a cancelar.

El sistema:

Libera el asiento

Marca la reserva como cancelada

Actualiza estadísticas

Si el usuario no tiene reservas activas, se ofrece crear una nueva.

4.4 Consultar Funciones del Fin de Semana

Acceso por opción 4 del menú.

El sistema muestra una tabla con:

ID

Día

Hora

Película

Asientos disponibles

Las funciones corresponden a viernes, sábado y domingo.

5. Módulo Administrador

Acceso por opción 5.

Credenciales válidas (por defecto):

Usuario: agora1 → Contraseña: agora123

Usuario: agora2 → Contraseña: agora2025

Una vez dentro, se puede acceder a:
5.1 Total de reservas registradas

Cantidad total de reservas creadas en el sistema (activas + canceladas).

5.2 Total de tiquetes vendidos (activos)

Reservas que siguen activas.

5.3 Total de reservas realizadas

Número total de registros de reserva creados.

5.4 Total pago realizado

Suma del dinero recaudado por reservas activas.

5.5 Promedio de venta diaria

Calcula el promedio de ventas por día basado en las fechas registradas.

5.6 Lista de usuarios registrados

Muestra todos los usuarios en el sistema.

5.7 Usuario con mayor/menor cantidad de reservas

Analiza cuántas reservas ha hecho cada usuario y muestra:

Usuario con más reservas

Usuario con menos reservas

5.8 Ver todas las reservas

Lista completa de reservas:

Activas

Canceladas

Incluye película, asiento, precio y estado

6. Salida del Sistema

Opción 6.

Finaliza la ejecución del programa con un mensaje de despedida:

Gracias por usar el sistema. Hasta luego.

7. Glosario
Término	Descripción
Función	Proyección de una película con fecha y hora.
Reserva	Compra de un asiento para una función.
Asiento	Identificado por FILA + COLUMNA (ej: A C).
Usuario	Persona registrada que puede comprar tiquetes.
Administrador	Persona con credenciales especiales.
8. Consideraciones Finales

El sistema no usa archivos externos.

Todas las sillas comienzan como disponibles (O).

Cada reserva genera un ID único.

Cada acción del usuario se procesa en tiempo real.
