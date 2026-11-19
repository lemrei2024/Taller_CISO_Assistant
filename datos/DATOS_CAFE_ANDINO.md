# Datos del caso Café Andino S.A.S. para registrar en CISO Assistant

> Caso ficticio con fines académicos. Las personas y empresas mencionadas no existen.

## Contexto resumido

Café Andino S.A.S. es una empresa colombiana de café especial con sede en Medellín, 120 empleados, tres tiendas físicas y una tienda en línea con 45.000 clientes registrados. Hace dos meses sufrió un incidente de phishing que expuso 2.300 registros de clientes. La junta creó el cargo de CISO, pero aún no existe política de seguridad aprobada, comité de seguridad ni procedimientos de aceptación de riesgos, gestión de proveedores o retiro de accesos.

**Controles que ya existen (existentes):**

- Copias de respaldo nocturnas de la base de datos de clientes (nunca se ha probado su restauración).
- Antivirus en los equipos de las tiendas y de la oficina.
- Contraseñas individuales para el correo corporativo (sin autenticación multifactor).

## 1. Activos

| N.º | Nombre del activo | Tipo | Descripción | Dueño del activo |
|---|---|---|---|---|
| A1 | Base de datos de clientes | Primario | Nombre, cédula, teléfono, dirección e historial de compras de 45.000 clientes. | Dirección comercial |
| A2 | Tienda en línea | Primario | Sitio de comercio electrónico que concentra el 40 % de las ventas. | Gerencia general |
| A3 | Correo corporativo | Soporte | Servicio de correo electrónico de los 120 empleados. | Jefe de TI |
| A4 | Consola del proveedor de nube | Soporte | Administración de la infraestructura donde se alojan la tienda y la base de datos. | Jefe de TI |
| A5 | Integración con la pasarela de pagos | Soporte | Conexión de la tienda con el proveedor externo que procesa los pagos. | Gerencia financiera |

## 2. Escenarios de riesgo

| N.º | Nombre del escenario | Descripción | Activos afectados | Amenaza sugerida |
|---|---|---|---|---|
| R1 | Robo de credenciales por phishing | Un atacante obtiene la contraseña de un empleado mediante un correo falso y accede a información de clientes. | A3, A1 | Phishing / ingeniería social |
| R2 | Acceso no autorizado con cuentas de exempleados | Personas que ya no trabajan en la empresa conservan cuentas activas en la consola de la nube y extraen información. | A4, A1 | Acceso no autorizado / abuso de privilegios |
| R3 | Explotación de una vulnerabilidad no corregida en la tienda | Un parche crítico se aplaza y un atacante aprovecha la vulnerabilidad para afectar la tienda o los pagos. | A2, A5 | Explotación de vulnerabilidades |
| R4 | Pérdida de información por ransomware sin respaldo recuperable | Un ransomware cifra la base de datos y las copias de respaldo no se pueden restaurar. | A1, A2 | Código malicioso (ransomware) |
| R5 | Tratamiento indebido de datos personales por terceros | La base de clientes se comparte con una agencia de marketing o se carga en una herramienta de IA sin autorización de los titulares ni contrato con el tercero, incumpliendo la Ley 1581 de 2012. | A1 | Divulgación no autorizada / incumplimiento legal |

> Si alguna amenaza no aparece con ese nombre en el catálogo importado, se debe elegir la más cercana o crear una amenaza personalizada.

## 3. Controles sugeridos

El estudiante puede usar estos controles o proponer otros justificados. Los marcados como **gobernanza** deben vincularse también a requisitos de la función GOBERNAR en la auditoría.

| Control | Tipo | Escenarios | Requisitos GV relacionados |
|---|---|---|---|
| Política general de seguridad de la información aprobada por la gerencia | Gobernanza | R1 a R5 | GV.PO |
| Comité de seguridad de la información con informes trimestrales a la junta | Gobernanza | R1 a R5 | GV.RR, GV.OV |
| Declaración de apetito de riesgo y procedimiento de aceptación de riesgos | Gobernanza | R3, R4 | GV.RM |
| Política de gestión de proveedores con cláusulas mínimas de seguridad | Gobernanza | R5, R3 | GV.SC |
| Procedimiento de ingreso, retiro y revisión periódica de accesos | Gobernanza / operativo | R2 | GV.RR, GV.PO |
| Autenticación multifactor en correo y consola de nube | Técnico | R1, R2 | |
| Programa de concienciación y simulaciones de phishing | Operativo | R1 | GV.RR |
| Gestión de parches con controles compensatorios y pruebas previas | Técnico / operativo | R3 | |
| Pruebas trimestrales de restauración de copias de respaldo | Operativo | R4 | |
| Verificación de autorizaciones y contratos de transmisión de datos personales | Gobernanza / legal | R5 | GV.OC, GV.SC |
