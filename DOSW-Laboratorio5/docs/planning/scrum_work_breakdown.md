# 📄 Planeación del Sistema

## Desglose de trabajo: Épicas, Historias de Usuario y Tareas

La implementación de los requerimientos identificados de Bankify se desglosa de la siguiente manera:

### 1. Épica:

| Campo | Descripción |
|------|-------------|
| **ID** | EP-01 |
| **Título** | Realizar Depsito |
| **Descripción** | *Bankify necesita esta épica porque debe permitir a sus clientes ralizar depósitos de forma controlada y segura para permitir las operaciones de esta primer versión del sistema.* |
| **Stakeholder** | *Gerente de Financiero/Clientes* |

### 2. Historias de usuario:

### HU-01

| Campo | Descripción |
|------|-------------|
| **ID** | HU-01 |
| **Título** | Validar datos de la cuenta antes del depósito |
| **Descripción** | *Como cliente quiero que el sistema valide el número de cuenta antes de realizar el depósito para poder evitar erroes o fraudes.* |
| **Prioridad** | *[Alta] [Media] [Baja] Lo hace el product owner* |
| **Estimación** | *Puntos de historia (Se hace en parte 4)* |

---

### HU-02

| Campo | Descripción |
|------|-------------|
| **ID** | HU-02 |
| **Título** | Registrar depósito vía PSE |
| **Descripción** | *Como cliente quiero realizar un depósito mediante PSE para transferir dinero de manera electrónica y segura.* |
| **Prioridad** | ** |
| **Estimación** | ** |

---

### HU-03

| Campo | Descripción |
|------|-------------|
| **ID** | HU-03 |
| **Título** | Actualizar saldo automáticamente |
| **Descripción** | *Como cliente quiero que el saldo de mi cuenta se actualice automáticamente después del depósito para ver reflejado mi dinero en tiempo real.* |
| **Prioridad** | ** |
| **Estimación** | ** |

---

### HU-04

| Campo | Descripción |
|------|-------------|
| **ID** | HU-04 |
| **Título** | Registrar historial de transacciones |
| **Descripción** | *Como cliente quiero que el sistema registre el depósito en mi historial de movimientos para poder consultar mis transacciones posteriormente.* |
| **Prioridad** | ** |
| **Estimación** | ** |

### 3. Tareas:

### TR-01

| Campo | Descripción |
|-------|------------|
| **ID** | TR-01 |
| **Título** | Validar formato del número de cuenta |
| **ID de la Historia de Uso asociada** | HU-01 |
| **Descripción** | *Verificar que el número de cuenta tenga exactamente 10 dígitos numéricos sin caracteres especiales.* |
| **Tareas requisito** | *Ninguna* |

---

### TR-02

| Campo | Descripción |
|-------|------------|
| **ID** | TR-02 |
| **Título** | Validar banco registrado |
| **ID de la Historia de Uso asociada** | HU-01 |
| **Descripción** | *Verificar que los dos primeros dígitos correspondan a un banco registrado.* |
| **Tareas requisito** | *TR-01* |

---

### TR-03

| Campo | Descripción |
|-------|------------|
| **ID** | TR-03 |
| **Título** | Mostrar mensaje de error |
| **ID de la Historia de Uso asociada** | HU-01 |
| **Descripción** | *Implementar un mensaje claro cuando la cuenta no cumpla las reglas de negocio.* |
| **Tareas requisito** | *TR-01, TR-02* |

---

### TR-04

| Campo | Descripción |
|-------|------------|
| **ID** | TR-04 |
| **Título** | Integrar servicio PSE |
| **ID de la Historia de Uso asociada** | HU-02 |
| **Descripción** | *Implementar integración con el servicio PSE para realizar el depósito electrónico.* |
| **Tareas requisito** | *TR-03* |

---

### TR-05

| Campo | Descripción |
|-------|------------|
| **ID** | TR-05 |
| **Título** | Validar monto del depósito |
| **ID de la Historia de Uso asociada** | HU-02 |
| **Descripción** | *Verificar que el monto ingresado sea mayor a cero.* |
| **Tareas requisito** | *Ninguna* |

---

### TR-06

| Campo | Descripción |
|-------|------------|
| **ID** | TR-06 |
| **Título** | Registrar confirmación de pago |
| **ID de la Historia de Uso asociada** | HU-02 |
| **Descripción** | *Registrar confirmación exitosa del depósito en el sistema.* |
| **Tareas requisito** | *TR-04* |

---

### TR-07

| Campo | Descripción |
|-------|------------|
| **ID** | TR-07 |
| **Título** | Calcular nuevo saldo |
| **ID de la Historia de Uso asociada** | HU-03 |
| **Descripción** | *Sumar el monto del depósito al saldo actual de la cuenta.* |
| **Tareas requisito** | *TR-06* |

---

### TR-08

| Campo | Descripción |
|-------|------------|
| **ID** | TR-08 |
| **Título** | Persistir saldo actualizado |
| **ID de la Historia de Uso asociada** | HU-03 |
| **Descripción** | *Guardar el nuevo saldo en la base de datos.* |
| **Tareas requisito** | *TR-07* |

---

### TR-09

| Campo | Descripción |
|-------|------------|
| **ID** | TR-09 |
| **Título** | Mostrar saldo actualizado |
| **ID de la Historia de Uso asociada** | HU-03 |
| **Descripción** | *Mostrar al usuario el saldo actualizado después del depósito.* |
| **Tareas requisito** | *TR-08* |

---

### TR-10

| Campo | Descripción |
|-------|------------|
| **ID** | TR-10 |
| **Título** | Crear registro de transacción |
| **ID de la Historia de Uso asociada** | HU-04 |
| **Descripción** | *Crear un registro con fecha, monto y tipo de operación.* |
| **Tareas requisito** | *TR-06* |

---

### TR-11

| Campo | Descripción |
|-------|------------|
| **ID** | TR-11 |
| **Título** | Asociar transacción a cuenta |
| **ID de la Historia de Uso asociada** | HU-04 |
| **Descripción** | *Relacionar la transacción con la cuenta correspondiente.* |
| **Tareas requisito** | *TR-10* |

---

### TR-12

| Campo | Descripción |
|-------|------------|
| **ID** | TR-12 |
| **Título** | Habilitar consulta de historial |
| **ID de la Historia de Uso asociada** | HU-04 |
| **Descripción** | *Permitir al cliente consultar el historial de transacciones.* |
| **Tareas requisito** | *TR-11* |