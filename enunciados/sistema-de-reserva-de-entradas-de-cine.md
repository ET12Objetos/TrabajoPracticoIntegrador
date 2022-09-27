<h1 align="center">Sistema de reserva de entradas de cine</h1>
<h3 align="center">Realizar el diseño e implementación de una aplicación reservar entradas de cine</h3>

**Relevamiento:**

* [Requerimientos](#requerimientos)
* [Diagrama de Casos de Uso](#diagrama-de-casos-de-uso)
* [Diagrama de Clases](#diagrama-de-clases)
* [Diagrama de Actividad](#diagrama-de-actividad)

Un sistema de reserva de entradas de cine en línea facilita la compra de entradas de cine a sus clientes. Los sistemas de venta de entradas electrónicas permiten a los clientes navegar a través de las películas que están cartelera actualmente y reservar asientos, en cualquier lugar y en cualquier momento.

<p align="center">
    <img src="https://github.com/ET12Objetos/TrabajoPracticoIntegrador/blob/main/diagramas/sistema-de-reserva-de-entradas-de-cine/movie-ticket-booking-system.png" alt="Movie Ticket Booking System">        
</p>

### Requerimientos

Nuestro servicio de reserva de entradas debe cumplir los siguientes requisitos:

1. Debe poder enumerar las ciudades donde se encuentran los cines afiliados.
2. Cada cine puede tener varias salas y cada sala puede presentar una película a la vez.
3. Cada película tendrá múltiples espectáculos.
4. Los clientes deberían poder buscar películas por título, idioma, género, fecha de estreno y nombre de la ciudad.
5. Una vez que el cliente selecciona una película, el servicio debe mostrar los cines que proyectan esa película y sus programas disponibles.
6. El cliente debe poder seleccionar un espectáculo en un cine en particular y reservar sus entradas.
7. El servicio debe mostrar al cliente la disposición de los asientos de la sala de cine. El cliente debe poder seleccionar varios asientos según sus preferencias.
8. El cliente debe poder distinguir entre los asientos disponibles y los reservados.
9. El sistema debe enviar notificaciones cada vez que haya una nueva película, así como cuando se realice o cancele una reserva.
10. Los clientes de nuestro sistema deben poder pagar con tarjetas de crédito o en efectivo.
11. El sistema debe garantizar que dos clientes no puedan reservar el mismo asiento.
12. Los clientes deberían poder agregar un cupón de descuento a su pago.

### Diagrama de Casos de Uso

Tenemos cinco Actores principales en nuestro sistema:

* **Administrador:** Responsable de agregar nuevas películas y sus programas, cancelar cualquier película o programa, bloquear/desbloquear clientes, etc.
* **Recepción:** Puede reservar/cancelar boletos.
* **Cliente:** Puede ver horarios de películas, reservar y cancelar boletos.
* **Invitado:** Todos los invitados pueden buscar películas, pero para reservar asientos deben convertirse en miembros registrados.
* **Sistema:** Principalmente responsable de enviar notificaciones de nuevas películas, reservas, cancelaciones, etc.

Estos son los principales casos de uso del sistema de reserva de entradas para el cine:

* **Buscar películas:** Para buscar películas por título, género, idioma, fecha de estreno y nombre de la ciudad.
* **Crear/Modificar/Ver reserva:** Para reservar una entrada para un espectáculo de cine, cancelarla o ver detalles sobre el espectáculo.
* **Realizar el pago de la reserva:** Para pagar la reserva.
* **Agregar un cupón al pago:** Para agregar un cupón de descuento al pago.
* **Asignar asiento:** A los clientes se les mostrará un mapa de asientos para permitirles seleccionar asientos para su reserva.
* **Reembolso de pago:** Tras la cancelación, se reembolsará a los clientes el importe del pago siempre que la cancelación se produzca dentro del plazo permitido.

Aquí está el diagrama de caso de uso del sistema de reserva de entradas de cine:

<p align="center">
    <img src="https://github.com/ET12Objetos/TrabajoPracticoIntegrador/blob/main/diagramas/sistema-de-reserva-de-entradas-de-cine/mtbs-use-case-diagram.svg" alt="Movie Ticket Booking System Use Case Diagram">
</p>

### Diagrama de Clases

Estas son las principales clases del Sistema de reserva de entradas para el cine:

* **Cuenta:** El administrador podrá agregar/eliminar películas y programas, así como bloquear/desbloquear cuentas. Los clientes pueden buscar películas y hacer reservas para espectáculos. FrontDeskOffice puede reservar entradas para espectáculos de cine.
* **Invitado:** Los invitados pueden buscar y ver descripciones de películas. Para hacer una reserva para un espectáculo, deben convertirse en miembros registrados.
* **Cine:** La parte principal de la organización para la que se ha diseñado este software. Tiene atributos como 'nombre' para distinguirlo de otros cines.
* **CinemaHall:** Cada cine tendrá varias salas con varios asientos.
* **Ciudad:** Cada ciudad puede tener varios cines.
* **Película:** La entidad principal del sistema. Las películas tienen atributos como título, descripción, idioma, género, fecha de lanzamiento, nombre de la ciudad, etc.
* **Funcion/Proyeccion:** Cada película puede tener muchas funciones/proyecciones; cada funcion/proyeccion se realiza en una sala de cine.
* **CinemaHallSeat:** Cada sala de cine tendrá muchos asientos.
* **ShowSeat:** Cada ShowSeat corresponderá a un Show de cine y un CinemaHallSeat. Los clientes harán una reserva contra un ShowSeat.
* **Reserva:** una reserva es para un programa de cine y tiene atributos como un número de reserva único, número de asientos y estado.
* **Pago:** Responsable de cobrar los pagos de los clientes.
* **Notificación:** Se encargará de enviar notificaciones a los clientes.

### Diagrama de Actividad

**Hacer una reserva:** Cualquier cliente puede realizar esta actividad. Estos son los pasos para reservar una entrada para un espectáculo:

<p align="center">
    <img src="https://github.com/ET12Objetos/TrabajoPracticoIntegrador/blob/main/diagramas/sistema-de-reserva-de-entradas-de-cine/mtbs-make-booking-activity-diagram.svg" alt="Movie Ticket Booking System Make Booking Activity Diagram">
    <br />
    Diagrama de actividad para el sistema de reserva de entradas de cine Hacer reserva
</p>

**Cancelar una reserva:** El cliente puede cancelar sus reservas. Estos son los pasos para cancelar una reserva:

<p align="center">
    <img src="https://github.com/ET12Objetos/TrabajoPracticoIntegrador/blob/main/diagramas/sistema-de-reserva-de-entradas-de-cine/mtbs-cancel-booking-activity-diagram.svg" alt="Movie Ticket Booking System Cancel Booking Activity Diagram">
    <br />
    Diagrama de actividad para el sistema de reserva de entradas de cine Cancelar reserva
</p>
