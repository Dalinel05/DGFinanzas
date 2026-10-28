
# Especificación de Requisitos

## 1. Propósito

Definir los requisitos funcionales y no funcionales
del Gestor de Gastos Personales.

## 2. Alcance

La aplicación permitirá administrar ingresos y gastos
personales, consultar movimientos y gestionar categorías.

La primera versión funcionará localmente y estará
orientada a un único usuario.

## 3. Requisitos funcionales

### RF-01: Registrar ingresos
El sistema deberá permitir registrar ingresos
indicando el monto, la fecha y una categoría.

### RF-02: Registrar gastos
El sistema deberá permitir registrar gastos
indicando el monto, la fecha y una categoría.

### RF-03: Consultar movimientos
El sistema deberá mostrar los movimientos registrados,
incluyendo monto, tipo, categoría y fecha.

### RF-04: Consultar saldo
El sistema deberá calcular y mostrar el saldo
a partir de los ingresos y gastos registrados.

### RF-05: Gestionar categorías
El sistema deberá ofrecer categorías predefinidas
y permitir crear categorías personalizadas.

### RF-06: Archivar categorías
El sistema deberá permitir archivar categorías
personalizadas sin eliminar los movimientos asociados.

### RF-07: Reactivar categorías
El sistema deberá permitir reactivar categorías
personalizadas previamente archivadas.

### RF-08: Modificar movimientos
El sistema deberá permitir corregir los datos
de movimientos registrados anteriormente.

## 4. Requisitos no funcionales

### RNF-01: Usabilidad
El sistema deberá permitir registrar un ingreso
o gasto en un máximo de tres pasos desde
la pantalla principal.

### RNF-02: Persistencia
El sistema deberá conservar los movimientos
después de cerrar y volver a abrir la aplicación.

### RNF-03: Funcionamiento local
La primera versión deberá funcionar sin conexión
a Internet, siempre que el servicio local de
SQL Server se encuentre disponible.

## 5. Historias de usuario

### HU-01: Registrar ingresos
Como usuario, quiero registrar mis ingresos
para conocer cuánto dinero recibo y mantener
actualizado mi saldo disponible.

### HU-02: Registrar gastos
Como usuario, quiero registrar mis gastos
para conocer en qué utilizo mi dinero.

### HU-03: Consultar saldo
Como usuario, quiero consultar mi saldo disponible
para conocer mi situación financiera registrada.

### HU-04: Administrar categorías
Como usuario, quiero organizar mis movimientos
mediante categorías para facilitar su consulta.

## 6. Criterios de aceptación

### CA-01: Ingreso válido
DADO QUE el usuario está en el formulario de ingresos,
CUANDO introduce un monto positivo y datos válidos,
ENTONCES el sistema debe guardar el ingreso.

### CA-02: Monto inválido
DADO QUE el usuario intenta registrar un movimiento,
CUANDO introduce un monto menor o igual a cero,
ENTONCES el sistema debe rechazar el registro
y mostrar un mensaje de error.

### CA-03: Gasto superior al saldo
DADO QUE un gasto supera el saldo disponible,
CUANDO el usuario intenta registrarlo,
ENTONCES el sistema debe mostrar una advertencia
y permitir confirmar o cancelar la operación.

### CA-04: Categoría archivada
DADO QUE una categoría tiene movimientos asociados,
CUANDO el usuario la archiva,
ENTONCES los movimientos históricos deben conservarse.

### CA-05: Actualización del saldo
DADO QUE existen ingresos y gastos registrados,
CUANDO el usuario consulta el saldo,
ENTONCES el sistema debe calcular la diferencia
entre ingresos y gastos.
