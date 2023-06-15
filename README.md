# Ejercicio-Integracion-POO

Ejercicio-Integracion-POO es un proyecto en el cual se implementa la lógica de un dispositivo POSNET que procesa pagos con tarjetas de crédito.

## Uso

```java
package posnet;

public static void main(String args[]) {
    // Crea una instancia de Posnet
        Posnet posnet = new Posnet();
        // Crea una instancia de Persona
        Persona p = new Persona("12312312","Pedro","Juan","1112345678","pedro@gmail.com");
        // Crea una instancia de TarjetaDeCredito
        TarjetaDeCredito t = new TarjetaDeCredito("VISA","1234567890123456", 15000, p, EntidadFinanciera.BIRZA);

    // Realiza el pago con Posnet y genera un Ticket
    System.out.println("Ticket tras pagar...");
    Ticket ticketGenerado = posnet.efectuarPago(t, 10000, 5);

    // Imprime los datos del Ticket generado
    System.out.println(ticketGenerado);

    // Imprime el estado de la TarjetaDeCredito después del pago
    System.out.println("Tarjeta despues del pago");
    System.out.println(t);
}
```
