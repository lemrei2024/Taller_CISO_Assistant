# Taller guiado. Gobierno, riesgo y cumplimiento con CISO Assistant: caso Café Andino S.A.S.

**Curso:** Gobernanza en Seguridad de la Información
**Unidad:** Semana 3. Gestión de riesgos y apetito de riesgo

| Modalidad | Dedicación estimada | Puntaje | Herramienta | Productos |
|---|---|---|---|---|
| Individual | 6 horas | 100 puntos | CISO Assistant Community Edition (código abierto, AGPLv3) | Informe PDF con norma IEEE, repositorio en GitHub y video en YouTube |

## Contenido

- [Objetivo](#objetivo)
- [Resultados de aprendizaje](#resultados-de-aprendizaje)
- [Sobre la herramienta](#sobre-la-herramienta)
- [Conceptos clave](#conceptos-clave)
- [Requisitos previos](#requisitos-previos)
- [Evidencias de autoría](#evidencias-de-autoría)
- [Parte 0. Instalación de CISO Assistant](#parte-0-instalación-de-ciso-assistant)
- [Parte 1. Configuración inicial de la organización](#parte-1-configuración-inicial-de-la-organización)
- [Parte 2. Auditoría de la función GOBERNAR del NIST CSF 2.0](#parte-2-auditoría-de-la-función-gobernar-del-nist-csf-20)
- [Parte 3. Evaluación de riesgos](#parte-3-evaluación-de-riesgos)
- [Parte 4. Plan de acción e informe para la junta directiva](#parte-4-plan-de-acción-e-informe-para-la-junta-directiva)
- [Parte 5. Análisis crítico](#parte-5-análisis-crítico)
- [Productos y condiciones de entrega](#productos-y-condiciones-de-entrega)
- [Norma IEEE](#norma-ieee)
- [Criterios de evaluación](#criterios-de-evaluación-100-puntos)
- [Solución de problemas frecuentes](#solución-de-problemas-frecuentes)
- [Recursos](#recursos)

## Objetivo

Aplicar una herramienta de gobierno, riesgo y cumplimiento (GRC) de código abierto para diagnosticar la gobernanza de seguridad de la información de una organización, evaluar sus riesgos y construir un plan de acción que pueda presentarse a la alta dirección.

## Resultados de aprendizaje

Al finalizar el taller, el estudiante estará en capacidad de:

1. Instalar y configurar una plataforma GRC de código abierto en un entorno propio.
2. Modelar una organización en la herramienta mediante dominios, perímetros y activos.
3. Evaluar el cumplimiento de la función GOBERNAR (GV) del NIST CSF 2.0 con resultados justificados.
4. Construir una evaluación de riesgos con escenarios, riesgo actual, controles y riesgo residual.
5. Traducir los resultados de la herramienta en un informe para la junta directiva.
6. Analizar críticamente qué aspectos de la gobernanza resuelve una herramienta y cuáles dependen de decisiones de la dirección.

## Sobre la herramienta

CISO Assistant es una plataforma GRC desarrollada por intuitem. Su edición comunitaria (Community Edition) es de código abierto bajo licencia AGPLv3, se instala en un equipo propio mediante Docker e incluye bibliotecas con más de 200 marcos de referencia, entre ellos ISO/IEC 27001:2022, NIST CSF 2.0 y el NIST AI Risk Management Framework.

- Repositorio oficial: https://github.com/intuitem/ciso-assistant-community
- Documentación oficial: https://intuitem.gitbook.io/ciso-assistant

> **Nota sobre versiones.** La herramienta se actualiza con frecuencia. Los nombres de los menús y botones pueden variar ligeramente entre versiones y entre idiomas. Esta guía usa los nombres de los conceptos según la documentación oficial; si un menú no coincide exactamente, el estudiante debe buscar la opción equivalente o consultar la sección [Guides](https://intuitem.gitbook.io/ciso-assistant/guides/getting-started.md) de la documentación.

## Conceptos clave

| Concepto en la herramienta | Nombre en inglés | Significado en el taller |
|---|---|---|
| Dominio | Domain | Unidad organizacional que agrupa todo el trabajo y define el alcance de permisos. En el taller, la empresa Café Andino. |
| Perímetro | Perimeter | Alcance específico dentro del dominio (antes llamado "proyecto"). En el taller, la tienda en línea y los datos de clientes. |
| Activo | Asset | Elemento de valor que se protege: información, sistemas o servicios. |
| Biblioteca | Library | Paquete importable que contiene marcos, matrices de riesgo, amenazas o controles de referencia. |
| Marco | Framework | Conjunto de requisitos contra el cual se evalúa, por ejemplo el NIST CSF 2.0. |
| Auditoría | Audit | Evaluación de un perímetro frente a un marco. Genera una evaluación por cada requisito. |
| Resultado del requisito | Result | Compliant (cumple), Partially compliant (cumple parcialmente), Non compliant (no cumple) o Not applicable (no aplica). |
| Estado del requisito | Status | Avance del trabajo del evaluador: To do, In progress, In review, Done. Es distinto del resultado. |
| Control aplicado | Applied control | Medida concreta que la organización tiene o planea implementar. Un mismo control puede respaldar varios marcos y varios riesgos. |
| Evidencia | Evidence | Descripción, enlace o archivo que justifica un resultado o demuestra que un control existe. |
| Evaluación de riesgos | Risk assessment | Estudio de riesgos sobre un perímetro, asociado a una matriz de riesgo. |
| Escenario de riesgo | Risk scenario | Fila de la evaluación: une activos afectados, amenazas y controles. |
| Matriz de riesgo | Risk matrix | Escala configurable de probabilidad por impacto. |
| Riesgo actual | Current risk | Nivel de riesgo con los controles que ya existen. |
| Riesgo residual | Residual risk | Nivel de riesgo esperado cuando se implementen todos los controles planificados. |

## Requisitos previos

| Requisito | Detalle |
|---|---|
| Sistema operativo | Windows 10 u 11 (con WSL2), macOS o Linux. |
| Docker | Docker Desktop (Windows y macOS) o Docker Engine con Docker Compose (Linux), versión 27.0 o superior. |
| Git | Para descargar el repositorio de la herramienta. |
| Navegador | Chrome, Edge o Firefox actualizado. |
| Equipo | Se recomienda un equipo con al menos 8 GB de memoria RAM y 10 GB libres en disco. |
| Lecturas | Caso Café Andino (semanas 1 y 2) y el archivo [`datos/DATOS_CAFE_ANDINO.md`](datos/DATOS_CAFE_ANDINO.md) de este repositorio. |

**Alternativas si el equipo no cumple los requisitos:** el estudiante debe informar al docente en la primera semana para trabajar en la instancia que el docente habilite para el curso, o solicitar la prueba gratuita en la nube que ofrece el fabricante en https://intuitem.com/trial.

## Evidencias de autoría

Cada estudiante trabaja en su propia instancia de la herramienta. Para que el trabajo sea verificable y propio, deben cumplirse estas condiciones en todo el taller:

1. El dominio debe llamarse **`Café Andino S.A.S. - Apellido Nombre`** (con los datos del estudiante).
2. El usuario administrador debe crearse con el correo institucional del estudiante.
3. Todas las capturas de pantalla deben mostrar el nombre del dominio o el usuario con sesión iniciada.
4. Cada captura debe tomarse con la fecha y hora del sistema visibles (barra de tareas o reloj del sistema).
5. El informe debe registrar la versión de CISO Assistant instalada (se consulta en el menú de usuario o en la sección "About" o "Acerca de").
6. El video debe mostrar la instancia en funcionamiento, navegando en vivo por el dominio propio.

Capturas que no cumplan estas condiciones no se tendrán en cuenta como evidencia.

## Parte 0. Instalación de CISO Assistant

**Producto de esta parte:** la herramienta funcionando en `https://localhost:8443` con el usuario administrador del estudiante.

### Paso 0.1. Instalar Docker y Git

1. Instalar **Docker Desktop** desde https://www.docker.com/products/docker-desktop/.
   - En Windows, durante la instalación, seleccionar la opción **Use WSL 2** y reiniciar el equipo si el instalador lo solicita.
2. Abrir Docker Desktop y esperar a que indique que el motor está en ejecución (*Engine running*).
3. Instalar **Git** desde https://git-scm.com/downloads.
4. Verificar la instalación abriendo una terminal (PowerShell en Windows, Terminal en macOS o Linux) y ejecutando:

   ```bash
   docker --version
   docker compose version
   git --version
   ```

   La versión de Docker debe ser 27.0 o superior.

### Paso 0.2. Descargar CISO Assistant

En la terminal, ubicarse en la carpeta donde se guardará el proyecto (por ejemplo, Documentos) y ejecutar:

```bash
git clone --single-branch -b main https://github.com/intuitem/ciso-assistant-community.git
cd ciso-assistant-community
```

### Paso 0.3. Iniciar la herramienta

**En macOS o Linux:**

```bash
./docker-compose.sh
```

**En Windows (PowerShell):**

```powershell
Set-ExecutionPolicy -Scope Process -ExecutionPolicy Bypass
./docker-compose.ps1
```

> La primera instrucción en Windows solo habilita la ejecución del script en la ventana actual de PowerShell; no cambia la configuración permanente del equipo.

La primera ejecución descarga las imágenes de la herramienta y puede tardar entre 5 y 20 minutos, según la conexión a internet.

### Paso 0.4. Crear el usuario administrador

Cuando el script lo solicite, ingresar:

- **Correo electrónico:** el correo institucional del estudiante.
- **Contraseña:** una contraseña robusta, que el estudiante debe guardar.

### Paso 0.5. Ingresar a la herramienta

1. Abrir el navegador en **https://localhost:8443/**
2. El navegador mostrará una advertencia de certificado, porque la instalación local usa un certificado autofirmado. Seleccionar **Configuración avanzada** y luego **Continuar a localhost**.
3. Iniciar sesión con el correo y la contraseña del paso 0.4.

### Paso 0.6. Uso en sesiones posteriores

Para volver a iniciar la herramienta en otra sesión, con Docker Desktop abierto:

```bash
cd ciso-assistant-community
docker compose up -d
```

Para detenerla al terminar:

```bash
docker compose down
```

**Evidencia Fig. 1:** pantalla de inicio de CISO Assistant con el usuario del estudiante en sesión y la fecha visible.

## Parte 1. Configuración inicial de la organización

**Producto de esta parte:** el dominio, el perímetro y los activos de Café Andino registrados en la herramienta.

### Paso 1.1. Cambiar el idioma (opcional)

Desde el menú de usuario, en la configuración de idioma, seleccionar **Español** si está disponible en la versión instalada. Si se trabaja en inglés, el informe debe usar los nombres de los conceptos en español y entre paréntesis el nombre en inglés la primera vez, por ejemplo: perímetro (*perimeter*).

### Paso 1.2. Crear el dominio

1. En el menú lateral, ir a la sección de organización y abrir **Dominios** (*Domains*).
2. Seleccionar **Agregar dominio** (*Add domain*).
3. Nombre: `Café Andino S.A.S. - Apellido Nombre`.
4. Descripción: `Empresa colombiana de café especial con tienda en línea y 45.000 clientes registrados. Caso académico.`
5. Guardar.

### Paso 1.3. Crear el perímetro

1. Abrir **Perímetros** (*Perimeters*) y seleccionar **Agregar perímetro** (*Add perimeter*).
2. Nombre: `Tienda en línea y datos de clientes`.
3. Dominio: el dominio creado en el paso 1.2.
4. Descripción: `Incluye la tienda en línea, la base de datos de clientes, el correo corporativo, la consola del proveedor de nube y la integración con la pasarela de pagos.`
5. Guardar.

### Paso 1.4. Registrar los activos

1. Abrir **Activos** (*Assets*) y seleccionar **Agregar activo** (*Add asset*).
2. Registrar los cinco activos listados en la sección 1 del archivo [`datos/DATOS_CAFE_ANDINO.md`](datos/DATOS_CAFE_ANDINO.md), asociados al dominio del estudiante.
3. Para cada activo, indicar el nombre, la descripción, el tipo (primario o de soporte, según la tabla) y el responsable o dueño del activo, si la versión instalada incluye ese campo.

**Evidencia Fig. 2:** listado de activos del dominio del estudiante.

## Parte 2. Auditoría de la función GOBERNAR del NIST CSF 2.0

**Producto de esta parte:** una auditoría del perímetro frente al NIST CSF 2.0, con la función GOBERNAR evaluada y justificada.

### Paso 2.1. Importar el marco NIST CSF 2.0

1. Ir a la sección de catálogo y abrir **Bibliotecas** (*Libraries*).
2. Buscar `NIST CSF` y ubicar la biblioteca correspondiente a la **versión 2.0** (no la 1.1).
3. Seleccionar la opción para **cargar o importar** la biblioteca.
4. Verificar en **Marcos** (*Frameworks*) que el NIST CSF v2.0 aparece disponible.

### Paso 2.2. Crear la auditoría

1. Abrir **Auditorías** (*Audits*) y seleccionar **Agregar auditoría** (*Add audit*).
2. Nombre: `Diagnóstico de gobernanza NIST CSF 2.0 - Café Andino`.
3. Perímetro: `Tienda en línea y datos de clientes`.
4. Marco: NIST CSF v2.0.
5. Guardar y abrir la auditoría.

### Paso 2.3. Evaluar los requisitos de la función GOBERNAR

La función GOBERNAR (GV) del NIST CSF 2.0 tiene 6 categorías y 31 subcategorías. El estudiante debe evaluar **como mínimo dos subcategorías de cada categoría (12 en total)**. Se recomienda evaluar las 31.

| Categoría | Código | Subcategorías |
|---|---|---|
| Contexto organizacional | GV.OC | GV.OC-01 a GV.OC-05 |
| Estrategia de gestión de riesgos | GV.RM | GV.RM-01 a GV.RM-07 |
| Roles, responsabilidades y autoridades | GV.RR | GV.RR-01 a GV.RR-04 |
| Política | GV.PO | GV.PO-01 y GV.PO-02 |
| Supervisión | GV.OV | GV.OV-01 a GV.OV-03 |
| Gestión de riesgos de la cadena de suministro | GV.SC | GV.SC-01 a GV.SC-10 |

Para cada subcategoría evaluada:

1. Abrir el requisito dentro de la auditoría.
2. Asignar el **resultado**: Compliant, Partially compliant, Non compliant o Not applicable.
3. Escribir en el campo de observaciones la **justificación con hechos del caso**. Ejemplo para GV.RR-01: *"No cumple. Hasta la creación del cargo de CISO nadie tenía asignada la seguridad de la información; el área de TI reporta a la gerencia financiera y la junta nunca ha recibido informes."*
4. Si la organización ya tiene alguna medida relacionada, vincular un **control aplicado** existente (por ejemplo, "Copias de respaldo nocturnas").
5. Cambiar el **estado** del requisito a **Done**.

> Recordatorio: el **resultado** indica el nivel de cumplimiento; el **estado** indica si el evaluador terminó su revisión. Un requisito puede estar en estado *Done* con resultado *Non compliant*.

### Paso 2.4. Exportar los resultados de la auditoría

Desde la vista de la auditoría, usar las opciones de exportación disponibles. La documentación oficial incluye, entre otras, el libro de requisitos (XLSX), el resumen ejecutivo (DOCX) y la postura de la auditoría (PDF). El estudiante debe exportar **al menos uno** de estos archivos y guardarlo para el repositorio.

**Evidencias:**

- **Fig. 3:** vista general de la auditoría con las barras de avance y la distribución de resultados.
- **Fig. 4:** un requisito de la función GOBERNAR con su resultado, justificación y control vinculado.

## Parte 3. Evaluación de riesgos

**Producto de esta parte:** una evaluación de riesgos con cinco escenarios, riesgo actual, controles y riesgo residual.

### Paso 3.1. Importar la matriz de riesgo y el catálogo de amenazas

1. En **Bibliotecas** (*Libraries*), buscar e importar una **matriz de riesgo** (por ejemplo, una matriz de 4x4 o 5x5 de las disponibles).
2. Buscar e importar un **catálogo de amenazas** (*threats*).
3. Si una amenaza del caso no aparece en el catálogo, la herramienta permite crear una amenaza personalizada.

### Paso 3.2. Crear la evaluación de riesgos

1. Abrir **Evaluaciones de riesgos** (*Risk assessments*) y seleccionar **Agregar** (*Add*).
2. Nombre: `Riesgos de seguridad de la información - Café Andino 2026`.
3. Perímetro: `Tienda en línea y datos de clientes`.
4. Matriz de riesgo: la importada en el paso 3.1.
5. Guardar y abrir la evaluación. La vista muestra tres zonas: los datos de la evaluación, la lista de escenarios y la matriz.

### Paso 3.3. Registrar los escenarios de riesgo

Registrar los cinco escenarios de la sección 2 del archivo [`datos/DATOS_CAFE_ANDINO.md`](datos/DATOS_CAFE_ANDINO.md). Para cada escenario:

1. **Agregar escenario** con el nombre y la descripción indicados.
2. Vincular los **activos** afectados y la **amenaza** correspondiente.
3. Realizar la **valoración del riesgo actual**: asignar probabilidad e impacto considerando solo los controles que ya existen. La justificación debe apoyarse en hechos del caso.
4. Registrar los **controles aplicados**:
   - Los **existentes**, con estado implementado (si los hay).
   - Al menos **un control planificado** por escenario, con responsable, fecha estimada y prioridad. Los controles sugeridos están en la sección 3 del archivo de datos; el estudiante puede proponer otros.
5. Realizar la **valoración del riesgo residual**: probabilidad e impacto esperados cuando se implementen los controles planificados.
6. Indicar el **nivel de certeza** (*strength of knowledge*) de la valoración, si la versión instalada lo solicita.
7. Registrar la **decisión de tratamiento** (mitigar, transferir, evitar o aceptar) y el responsable del riesgo.

> **Regla de gobernanza:** la aceptación de un riesgo no la decide el CISO ni el área de TI. Si el estudiante propone aceptar un riesgo, debe indicar qué instancia de la dirección lo aprueba, de acuerdo con lo trabajado en la Semana 2.

**Evidencias:**

- **Fig. 5:** lista de los cinco escenarios con riesgo actual y residual.
- **Fig. 6:** vista de la matriz de riesgo con la ubicación de los escenarios.
- **Fig. 7:** detalle de un escenario con activos, amenaza y controles vinculados.

## Parte 4. Plan de acción e informe para la junta directiva

**Producto de esta parte:** el plan de acción consolidado y un informe de una página para la junta.

### Paso 4.1. Revisar el plan de acción

1. Abrir **Controles aplicados** (*Applied controls*).
2. Verificar que cada control planificado tenga responsable, fecha estimada y prioridad.
3. Verificar que los controles de gobernanza (política, comité, procedimiento de aceptación de riesgos, gestión de proveedores) estén vinculados tanto a requisitos de la auditoría como a escenarios de riesgo. Esto demuestra que **un mismo control respalda varios objetivos**.
4. Exportar el listado de controles o el plan de acción en el formato disponible.

**Evidencia Fig. 8:** listado de controles aplicados con responsables y fechas.

### Paso 4.2. Redactar el informe para la junta

Con base en los resultados de la herramienta, redactar en el documento un informe ejecutivo de **máximo una página**, sin lenguaje técnico, que incluya:

1. Estado de la función GOBERNAR: cuántos requisitos cumplen, cumplen parcialmente o no cumplen.
2. Los tres riesgos de mayor nivel actual y su nivel residual esperado.
3. Las cinco acciones prioritarias, con responsable y fecha.
4. Las decisiones que se solicitan a la junta (por ejemplo, aprobar la política, crear el comité, asignar presupuesto o aprobar la aceptación de un riesgo).

## Parte 5. Análisis crítico

Redactar entre 300 y 400 palabras que respondan:

1. ¿Qué ventajas ofrece la herramienta frente a gestionar el riesgo y el cumplimiento en hojas de cálculo?
2. ¿Qué aspectos de la gobernanza **no** puede resolver la herramienta por sí sola? Considerar las decisiones de la junta, la asignación de responsabilidades y la cultura organizacional.
3. ¿Qué limitaciones o dificultades se encontraron durante la instalación y el uso?
4. ¿Qué implica para una organización colombiana usar una herramienta de código abierto autoalojada, en términos de soporte, actualización, protección de los datos que se registran en ella y cumplimiento de la Ley 1581 de 2012?

## Productos y condiciones de entrega

### 1. Informe en formato PDF

- Contenido: portada, Partes 0 a 5 con las figuras solicitadas (Fig. 1 a Fig. 8), informe para la junta, análisis crítico y referencias.
- Extensión máxima: 15 páginas, sin contar portada ni referencias.
- Nombre del archivo: `Taller_CISO_Assistant_Apellido_Nombre.pdf`.
- Aplicación obligatoria de la **norma IEEE** (ver la sección [Norma IEEE](#norma-ieee)).
- Se recomienda usar la plantilla [`plantillas/PLANTILLA_INFORME.md`](plantillas/PLANTILLA_INFORME.md).

### 2. Repositorio en GitHub

Crear un repositorio **público** llamado `gobernanza-si-taller-ciso-assistant-apellido` con la siguiente estructura:

```text
gobernanza-si-taller-ciso-assistant-apellido/
├── README.md                                   (basado en plantillas/README_ESTUDIANTE.md)
├── Taller_CISO_Assistant_Apellido_Nombre.pdf
└── exportaciones/
    ├── auditoria_gobernar.(xlsx | pdf | docx)  (exportado en el paso 2.4)
    └── plan_de_accion.(xlsx | csv | pdf)       (exportado en el paso 4.1)
```

No deben subirse contraseñas, archivos de configuración de la instalación ni la carpeta `ciso-assistant-community`.

### 3. Video en YouTube

- Duración: entre 6 y 8 minutos.
- El estudiante debe aparecer en cámara al inicio y luego compartir la pantalla.
- El video debe mostrar **en vivo** la instancia propia de CISO Assistant (dominio con el nombre del estudiante) y recorrer:
  1. El dominio, el perímetro y los activos.
  2. La auditoría de la función GOBERNAR y la justificación de dos requisitos.
  3. La evaluación de riesgos, la matriz y un escenario completo.
  4. El plan de acción y las decisiones que se solicitarían a la junta.
- Visibilidad: **No listado** o **Público**.
- Título: `Taller CISO Assistant Gobernanza SI - Apellido Nombre`.

### 4. Entrega en Blackboard

1. Escribir en el cuadro de texto el enlace al repositorio de GitHub y el enlace al video de YouTube.
2. Adjuntar el informe PDF como respaldo.

Enlaces que no abran, repositorios privados o videos privados se calificarán como no entregados en el criterio correspondiente.

## Norma IEEE

El informe debe aplicar la norma IEEE en su totalidad. Es un criterio de evaluación independiente con peso de 15 puntos.

### Citas en el texto

- Numéricas entre corchetes, en el orden en que aparecen por primera vez: [1], [2].
- Si se vuelve a citar la misma fuente, se usa el mismo número.
- Para varias fuentes: [1], [3] o [2]-[4].
- Toda afirmación tomada de una norma, marco, documentación o artículo debe llevar su cita.

### Lista de referencias

- Al final del documento, con el título **Referencias**.
- Numerada en el mismo orden de aparición de las citas, no en orden alfabético.
- Mínimo **cinco (5) referencias**, que deben incluir: el NIST CSF 2.0, la documentación o el repositorio de CISO Assistant y al menos una norma colombiana.

### Figuras y tablas

- **Figuras:** las capturas se numeran como "Fig. 1", "Fig. 2", con el título **debajo** de la imagen, y se mencionan en el texto antes de aparecer (por ejemplo: "como se observa en la Fig. 3...").
- **Tablas:** se numeran con números romanos, "TABLA I", "TABLA II", con el título **encima** de la tabla.

### Ejemplos de referencias en formato IEEE

[1] National Institute of Standards and Technology, "The NIST Cybersecurity Framework (CSF) 2.0," NIST CSWP 29, Gaithersburg, MD, EE. UU., feb. 2024. [En línea]. Disponible: https://doi.org/10.6028/NIST.CSWP.29

[2] intuitem, "CISO Assistant Community Edition," versión X.Y.Z, software de código abierto, licencia AGPLv3, 2026. [En línea]. Disponible: https://github.com/intuitem/ciso-assistant-community

[3] intuitem, "CISO Assistant documentation," 2026. [En línea]. Disponible: https://intuitem.gitbook.io/ciso-assistant

[4] Congreso de la República de Colombia, "Ley Estatutaria 1581 de 2012, por la cual se dictan disposiciones generales para la protección de datos personales," *Diario Oficial*, no. 48.587, oct. 2012.

[5] Departamento Administrativo de la Función Pública, "Guía para la Gestión Integral del Riesgo en Entidades Públicas, versión 7," Bogotá, Colombia, sep. 2025. [En línea]. Disponible: https://www.funcionpublica.gov.co/eva_/publicaciones

> En la referencia [2], reemplazar `X.Y.Z` por la versión instalada que el estudiante registra en su informe.

## Criterios de evaluación (100 puntos)

| Criterio | Puntos | Nivel alto | Nivel medio | Nivel bajo |
|---|:---:|---|---|---|
| Partes 0 y 1. Instalación y configuración | 10 | Instancia propia funcionando; dominio, perímetro y cinco activos registrados; evidencias de autoría completas (9-10) | Configuración incompleta o evidencias sin datos de autoría (5-8) | Sin evidencia de instancia propia (0-4) |
| Parte 2. Auditoría GOBERNAR | 20 | 12 o más subcategorías evaluadas con resultado correcto, justificación basada en hechos del caso y controles vinculados; exportación incluida (17-20) | Menos de 12 subcategorías o justificaciones genéricas (10-16) | Resultados sin justificación o confusión entre estado y resultado (0-9) |
| Parte 3. Evaluación de riesgos | 20 | Cinco escenarios completos con activos, amenaza, riesgo actual y residual coherentes, controles planificados con responsable y fecha, tratamiento con instancia aprobadora (17-20) | Escenarios incompletos o valoraciones poco coherentes (10-16) | Menos de tres escenarios o valoraciones sin sustento (0-9) |
| Parte 4. Plan de acción e informe a la junta | 10 | Plan completo; informe de una página, sin tecnicismos, con decisiones concretas para la junta (9-10) | Informe técnico o sin decisiones claras (5-8) | Ausente o copia de la salida de la herramienta (0-4) |
| Parte 5. Análisis crítico | 10 | Distingue con argumentos lo que resuelve la herramienta y lo que depende de la dirección; analiza implicaciones legales y operativas (9-10) | Análisis descriptivo o superficial (5-8) | Ausente (0-4) |
| Norma IEEE | 15 | Citas numéricas correctas y consistentes; mínimo cinco referencias completas y en orden de aparición; figuras y tablas numeradas y tituladas según IEEE (13-15) | Errores menores de formato, referencias incompletas o figuras sin numerar (8-12) | Formato distinto a IEEE, citas sin referencia o menos de tres referencias (0-7) |
| Repositorio en GitHub | 5 | Público, con README completo, informe y exportaciones en la estructura indicada (5) | Estructura incompleta (3-4) | Inaccesible o vacío (0-2) |
| Video en YouTube | 10 | Duración de 6 a 8 minutos; muestra en vivo la instancia propia y recorre los cuatro puntos; explicación clara (9-10) | Omite algún punto o no muestra la instancia en vivo (5-8) | Inaccesible o sin demostración de la herramienta (0-4) |

## Solución de problemas frecuentes

| Problema | Causa probable | Solución |
|---|---|---|
| `docker: command not found` o similar | Docker no está instalado o no está en ejecución | Abrir Docker Desktop y esperar a que indique *Engine running*. |
| En Windows aparece un error relacionado con WSL | WSL2 no está habilitado | En PowerShell como administrador ejecutar `wsl --install`, reiniciar y abrir de nuevo Docker Desktop. |
| PowerShell no permite ejecutar el script | Política de ejecución restringida | Ejecutar `Set-ExecutionPolicy -Scope Process -ExecutionPolicy Bypass` en la misma ventana antes del script. |
| El navegador muestra "La conexión no es privada" | Certificado autofirmado de la instalación local | Es esperado en un entorno local: seleccionar Configuración avanzada y continuar a localhost. |
| El puerto 8443 está ocupado | Otra aplicación usa el puerto | Cerrar la otra aplicación o reiniciar el equipo y volver a iniciar con `docker compose up -d`. |
| La herramienta está muy lenta o se detiene | Memoria insuficiente | Cerrar otras aplicaciones, aumentar la memoria asignada a Docker Desktop o solicitar al docente la instancia del curso. |
| No aparece la biblioteca del NIST CSF 2.0 | Filtro de búsqueda o versión | Buscar "CSF" o "Cybersecurity Framework" en Bibliotecas y verificar que la versión sea la 2.0. |
| Se olvidó la contraseña del administrador | Contraseña no registrada | Consultar la sección [Maintenance](https://intuitem.gitbook.io/ciso-assistant/installation/maintenance.md) de la documentación oficial o volver a instalar la herramienta. |

## Recursos

- intuitem, repositorio de CISO Assistant Community: https://github.com/intuitem/ciso-assistant-community
- intuitem, documentación oficial de CISO Assistant: https://intuitem.gitbook.io/ciso-assistant
- intuitem, guía "Getting started": https://intuitem.gitbook.io/ciso-assistant/guides/getting-started.md
- NIST, El Marco de Seguridad Cibernética (CSF) 2.0, traducción oficial al español: https://nvlpubs.nist.gov/nistpubs/CSWP/NIST.CSWP.29.spa.pdf
- NIST IR 8286 Rev. 1, Integrating Cybersecurity and Enterprise Risk Management: https://nvlpubs.nist.gov/nistpubs/ir/2025/NIST.IR.8286r1.pdf
- Función Pública, Guía para la Gestión Integral del Riesgo en Entidades Públicas, versión 7: https://www.funcionpublica.gov.co/eva_/publicaciones
- Ley 1581 de 2012: https://www.funcionpublica.gov.co/eva/gestornormativo/norma.php?i=49981
- Docker, documentación de instalación de Docker Desktop: https://docs.docker.com/desktop/

## Plantillas y datos

| Archivo | Uso |
|---|---|
| [`datos/DATOS_CAFE_ANDINO.md`](datos/DATOS_CAFE_ANDINO.md) | Activos, escenarios de riesgo y controles sugeridos para registrar en la herramienta. |
| [`plantillas/PLANTILLA_INFORME.md`](plantillas/PLANTILLA_INFORME.md) | Estructura sugerida del informe en PDF con figuras, tablas y referencias IEEE. |
| [`plantillas/README_ESTUDIANTE.md`](plantillas/README_ESTUDIANTE.md) | Modelo del README del repositorio de cada estudiante. |
