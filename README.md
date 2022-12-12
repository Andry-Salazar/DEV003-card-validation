# Tarjeta de crédito válida

## Índice

- [1. Preámbulo](#1-preámbulo)
- [2. Resumen del Proyecto y Objetivos Principales](#2-resumen-del-proyecto)

## 1. Preámbulo

El [algoritmo de Luhn](https://es.wikipedia.org/wiki/Algoritmo_de_Luhn),
también llamado algoritmo de módulo 10, es un método de suma de verificación,
se utiliza para validar números de identificación; tales como el IMEI de los
celulares, tarjetas de crédito, etc.

Este algoritmo es simple. Obtenemos la reversa del número a verificar (que
solamente contiene dígitos [0-9]); a todos los números que ocupan una posición
par se les debe multiplicar por dos, si este número es mayor o igual a 10,
debemos sumar los dígitos del resultado; el número a verificar será válido si
la suma de sus dígitos finales es un múltiplo de 10.

![gráfica de algoritmo de Luhn](https://www.101computing.net/wp/wp-content/uploads/Luhn-Algorithm.png)

## 2. Resumen del Proyecto y Objetivos Principales

En este proyecto cree una aplicación web que le permite a un usuario validar el número de una tarjeta de crédito, y enmascara todos los dígitos de la tarjeta excepto los últimos cuatro.

Esta aplicación puede ser utilizada en pymes para efecto de pagos.

**Interfaz:**

- Un formulario de pago, de una pyme de Ropa de Dama.
- Requiere un campo de texto para nombre del titular de la tarjeta.
- Requiere insertar un numero de tarjeta (texto) valida. Usa solo caracteres numéricos (dígitos) en la tarjeta a validar [0-9] y valida que el campo de texto no este vacío.
- Verifica la validez de la tarjeta, cumpliendo los parametros del Algoritmo de Luhn.
- Al salir del campo de texto del "numero de la tarjeta" enmascara todos los dígitos a excepción de los últimos 4 caracteres.
- Requiere un input de ingreso de mes y año de expiración de la tarjeta.
- Requiere un input de CVV de 3 dígitos de la tarjeta a validar.
- No permite ingresar un campo vacío.

**Diseño de Interfaz**

- Pensé en un formulario de pago de una pyme de Ropa para damas, en donde el usuario deba ingresar sus datos para efectos de pago.
- Diseñé un wireframe, escogiendo una paleta de 5 colores y un diseño sencillo y sutil que se adapta a la marca.

  https://www.figma.com/file/9y0TPUDRhdv3DiH7pp1uLN/Ecommerce-%22Magari-Shop%22?node-id=0%3A1&t=qsjphaEDsPZftj78-1

**Proceso de Desarrollo de la página y Objetivos de aprendizaje**

- Comencé desarrollando los metódos de `validator` (`isValid` y `maskify`) en JS, usando datos primitivos, ciclo for y condicional if/else, método de string (substring y padstar).
  Dentro del objeto validator, cree la funciones isValid, maskify y setInputFilter(esta última función valida el tipo de dato, que luego usé para validar que sea solo dígitos) realicé los test de pruebas unitarias usando la terminal y el comando npm test.
- Luego la maquetación con HTML, seccionando la pagina de la siguiente manera: header, barra de navegacion, una seccion para el formulario de pago y una seccion para el detalle del producto seleccionado para comprar, por último el footer. Usé validaciones del navegador como required, para los input.
  -Agregué estilos con CSS, usé las propiedades de flexbox ,margin, padding.
  -Manipulación del DOM y Manejo de eventos del DOM.
