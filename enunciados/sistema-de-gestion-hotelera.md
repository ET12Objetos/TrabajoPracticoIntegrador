<h1 align="center">Sistema de Gestion Hotelera</h1>
<h3 align="center">Realizar el diseño e implementación de una aplicación de gestión hotelera</h3>

**Relevamiento:**

* [Requerimientos](#requerimientos)
* [Diagrama de Casos de Uso](#diagrama-de-casos-de-uso)
* [Diagrama de Clases](#diagrama-de-clases)
* [Diagrama de Actividad](#diagrama-de-actividad)

Un sistema de gestión hotelera es un software creado para manejar todas las actividades hoteleras en línea de manera fácil y segura. Este Sistema le dará a la administración del hotel poder y flexibilidad para administrar todo el sistema desde un único portal en línea. El sistema le permite al administrador realizar un seguimiento de todas las habitaciones disponibles en el sistema, así como reservar habitaciones y generar facturas.

<p align="center">
    <img src="/media-files/hotel-management-system.png" alt="Hotel Management System">
</p>

### Requerimientos

Nos centraremos en el siguiente conjunto de requisitos al diseñar el sistema de gestión hotelera:

1. El sistema debe admitir la reserva de diferentes tipos de habitaciones, como estándar, de lujo, suite familiar, etc.
2. Los huéspedes deben poder buscar en el inventario de habitaciones y reservar cualquier habitación disponible.
3. El sistema debe poder recuperar información, como quién reservó una habitación en particular o qué habitaciones reservó un cliente específico.
4. El sistema debería permitir a los clientes cancelar su reserva y proporcionarles un reembolso completo si la cancelación se produce antes de las 24 horas de la fecha de llegada.
5. El sistema debería poder enviar notificaciones cada vez que la reserva se acerque a la fecha de entrada o salida.
6. El sistema debe mantener un registro de limpieza de la habitación para realizar un seguimiento de todas las tareas de limpieza.
7. Cualquier cliente debe poder agregar servicios de habitación y alimentos.
8. Los clientes pueden solicitar diferentes amenidades.
9. Los clientes deben poder pagar sus cuentas a través de tarjeta de crédito, cheque o efectivo.

### Diagrama de Casos de Uso

Here are the main Actors in our system:

* **Huésped:** Todos los huéspedes pueden buscar las habitaciones disponibles, así como hacer una reserva.
* **Recepcionista:** Principalmente responsable de agregar y modificar habitaciones, crear reservas de habitaciones, hacer el check-in y check-out de los clientes.
* **Sistema:** Principalmente responsable de enviar notificaciones de reservas de habitaciones, cancelaciones, etc.
* **Gerente:** Principalmente responsable de agregar nuevos trabajadores.
* **Ama de llaves:** Para agregar/modificar registro de limpieza de habitaciones.
* **Servidor:** Para agregar/modificar registro de servicio de habitaciones de habitaciones.

Estos son los principales casos de uso del sistema de gestión hotelera:

* **Agregar/Eliminar/Editar sala:** Para agregar, eliminar o modificar una sala en el sistema.
* **Buscar habitación:** Para buscar habitaciones por tipo y disponibilidad.
* **Registrar o cancelar una cuenta:** Para agregar un nuevo miembro o cancelar la membresía de un miembro existente.
* **Reservar habitación:** Para reservar una habitación.
* **Check-in:** Para permitir que el huésped se registre para su reserva.
* **Check-out:** Para realizar un seguimiento del final de la reserva y la devolución de las llaves de la habitación.
* **Agregar cargo de habitación:** Para agregar un cargo por servicio de habitación a la factura del cliente.
* **Actualizar registro de limpieza:** Para agregar o actualizar la entrada de limpieza de una habitación.

Aquí está el diagrama de casos de uso de nuestro Sistema de Gestión Hotelera:

<p align="center">
    <img src="/media-files/hms-use-case-diagram.svg" alt="Hotel Management System Use Case Diagram">
</p>

### Diagrama de Clases

Estas son las principales clases de nuestro Sistema de Gestión Hotelera:

* **Hotel y HotelLocation:** Nuestro sistema admitirá múltiples ubicaciones de un hotel.
* **Habitación:** El componente básico del sistema. Cada habitación será identificada de forma única por el número de habitación. Cada habitación tendrá atributos como estilo de habitación, precio de reserva, etc.
* **Cuenta:** Tendremos diferentes tipos de cuentas en el sistema: una será de invitado para buscar y reservar habitaciones, otra será de recepcionista. El servicio de limpieza realizará un seguimiento de los registros de limpieza de una habitación y un servidor se encargará del servicio de habitaciones.
* **RoomBooking:** Esta clase será responsable de gestionar las reservas de una habitación.
* **Notificación:** Se encargará de enviar notificaciones a los invitados.
* **RoomHouseKeeping:** para realizar un seguimiento de todos los registros de limpieza de las habitaciones.
* **RoomCharge:** resume los detalles sobre los diferentes tipos de servicios de habitación que los huéspedes han solicitado.
* **Factura:** Contiene diferentes artículos de factura para cada cargo contra la habitación.
* **RoomKey:** A cada habitación se le puede asignar una tarjeta llave electrónica. Las llaves tendrán un código de barras y se identificarán de forma única mediante un ID de llave.

### Diagrama de Actividad

**Hacer una reserva de habitación:** Cualquier huésped o recepcionista puede realizar esta actividad. Aquí está el conjunto de pasos para reservar una habitación:

<p align="center">
    <img src="/media-files/hms-room-booking-activity-diagram.svg" alt="Hotel Management System Room Booking">
    <br />
    Activity Diagram for Hotel Management System Room Booking
</p>

**Check in:** El huésped se registrará para su reserva. El Recepcionista también puede realizar esta actividad. Aquí están los pasos:

<p align="center">
    <img src="/media-files/hms-check-in-activity-diagram.svg" alt="Hotel Management System Check in">
    <br />
    Activity Diagram for Hotel Management System Check in
</p>

**Cancelar una reserva:** El huésped puede cancelar su reserva. Recepcionista puede realizar esta actividad. Estos son los diferentes pasos de esta actividad:

<p align="center">
    <img src="/media-files/hms-cancel-booking-activity-diagram.svg" alt="Hotel Management System Cancel Booking">
    <br />
    Activity Diagram for Hotel Management System Cancel Booking
</p>
