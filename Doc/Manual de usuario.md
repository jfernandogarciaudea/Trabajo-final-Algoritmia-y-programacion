# MANUAL DE USUARIO – Sistema de Gestión Cinema AGORA

## 1. Introducción

El sistema de gestión **Cinema AGORA** es una aplicación de consola diseñada para realizar el control básico del cine universitario. Permite administrar:

- Registro de usuarios  
- Reservas de tiquetes  
- Cancelación de reservas  
- Consulta de funciones del fin de semana  
- Gestión administrativa (estadísticas, usuarios, pagos)

El sistema funciona mediante un menú interactivo que guía al usuario paso a paso.

---

## 2. Requisitos de Uso

- Ejecutar el programa desde consola (**Colab**).  
- No requiere base de datos; toda la información se almacena en estructuras internas.  
- No requiere conexión a Internet.

---

## 3. Inicio del Sistema

Al ejecutar el archivo principal, el sistema muestra el siguiente menú:

==============================================

**CINEMA AGORA**
Bienvenido al Cinema AGORA

1. Registrar Usuario

2. Registrar Reserva

3. Cancelar Reserva

4. Consultar Funciones Fin de Semana

5. Administrador

6. Salir

==============================================

El usuario debe elegir una opción entre **1 y 6**.

---

## 4. Módulos del Sistema

### 4.1 Registrar Usuario

Acceso por **opción 1** del menú.

El sistema solicitará:

- Nombre  
- Apellido  
- Documento (solo números, 3–15 dígitos)  
- Tipo de vínculo, con tarifas:

| Tipo de Usuario       | Tarifa |
|-----------------------|--------|
| Estudiantes           | $7.500 |
| Docentes              | $10.000 |
| Administrativos       | $8.500 |
| Oficiales internos    | $7.000 |
| Público externo       | $15.000 |

Si algún dato no cumple los requisitos, el sistema mostrará errores y pedirá repetir el proceso.

Si el documento del usuario ya existe, el sistema **no permitira registrarlo de nuevo**.

---

### 4.2 Registrar Reserva

Acceso por **opción 2** del menú.

Proceso:

1. Ingresar documento registrado  
   - Si no existe, se ofrece registrar al usuario.
2. Seleccionar función  
   - Se muestran las funciones disponibles por día y hora.
3. Visualizar asientos — Mapa:
   - **O** → asiento libre  
   - **X** → asiento ocupado
4. Ingresar asiento  
   - Formatos válidos:  
     - AB  
     - A B  
     - A-B
5. Confirmación final  
   El sistema muestra:  
   - Usuario  
   - Película  
   - Día / hora  
   - Asiento  
   - Precio  
   - ID de la reserva  
   - Fecha de compra  

La reserva queda almacenada como **activa**.

---

### 4.3 Cancelar Reserva

Acceso por **opción 3** del menú.

Proceso:

1. Ingresar documento.
2. Listar reservas activas del usuario.
3. Seleccionar el ID de la reserva a cancelar.

El sistema:

- Libera el asiento  
- Marca la reserva como **cancelada**  
- Actualiza estadísticas  

Si el usuario no tiene reservas activas, se ofrece crear una nueva.

---

### 4.4 Consultar Funciones del Fin de Semana

Acceso por **opción 4** del menú.

El sistema muestra una tabla con:

- ID  
- Día  
- Hora  
- Película  
- Asientos disponibles  

Las funciones corresponden a **viernes, sábado y domingo**.

---

## 5. Módulo Administrador

Acceso por **opción 5**.

Credenciales válidas:

| Usuario | Contraseña |
|---------|------------|
| agora1  | agora123   |
| agora2  | agora2025  |

Una vez dentro, se accede a:

### 5.1 Total de reservas registradas
Cantidad total de reservas creadas (activas + canceladas).

### 5.2 Total de tiquetes vendidos (activos)
Contabiliza solo las reservas activas.

### 5.3 Total de reservas realizadas
Número total de reservas creadas por el sistema.

### 5.4 Total pago realizado
Suma del dinero recaudado por reservas **activas**.

### 5.5 Promedio de venta diaria
Basado en las fechas registradas en el sistema.

### 5.6 Lista de usuarios registrados
Muestra todos los usuarios en el sistema.

### 5.7 Usuario con mayor/menor cantidad de reservas
Incluye:

- Usuario con más reservas  
- Usuario con menos reservas  

### 5.8 Ver todas las reservas
Lista completa de:

- Activas  
- Canceladas  

Incluye película, asiento, precio y estado.

---

## 6. Salida del Sistema

La opción **6** finaliza la ejecución con el mensaje:

> Gracias por usar el sistema. Hasta luego.

---

## 7. Glosario

| Término        | Descripción |
|----------------|-------------|
| Función        | Proyección de una película con fecha y hora. |
| Reserva        | Compra de un asiento para una función. |
| Asiento        | Identificado por FILA + COLUMNA (ej: A C). |
| Usuario        | Persona registrada que puede comprar tiquetes. |
| Administrador  | Persona con credenciales especiales. |

---

## 8. Consideraciones Finales

- El sistema no usa archivos externos.  
- Todas las sillas comienzan como disponibles (**O**).  
- Cada reserva tiene un **ID único**.  
- Todo se procesa en tiempo real.  
