# Manual de Instrucciones y Guía de Uso - SimoHora v5.3
## Planificador y Simulador de Cargas Horarias Docentes (Ley 20.903 / Ley 21.625)

---

## 1. Introducción y Propósito

**SimoHora v5.3** es una herramienta web integral desarrollada especialmente para **Equipos Directivos, Jefes UTP y Sostenedores de Establecimientos Educacionales en Chile**. 

Su principal objetivo es optimizar y validar la distribución de cargas horarias docentes, garantizando el cumplimiento estricto de las proporciones legales de **Horas Lectivas** y **Horas No Lectivas** establecidas por la **Ley 20.903 (Carrera Docente)** y las modificaciones introducidas por la **Ley 21.625**.

---

## 2. Marco Legal y Normativo

La aplicación realiza automáticamente el cálculo de capacidades y límites legales basándose en la normativa chilena vigente:

### 2.1. Proporción de Carga Lectiva / No Lectiva
* **Proporción General (Ley 20.903):** 
  * **65% Horas Lectivas** (Máximo asignable en aula/clases).
  * **35% Horas No Lectivas** (Presupuesto obligatorio para preparación, evaluación y gestión directiva).
* **Proporción Prioritaria (Ley 21.625 - 1° a 4° Año de Educación Básica):**
  * Para establecimientos con **más del 80% de alumnos prioritarios (SEP)**, se aplica una proporción de **60% Horas Lectivas** y **40% Horas No Lectivas** en los cursos de 1° a 4° básico.

### 2.2. Distribución Obligatoria de las Horas No Lectivas (50/50)
De la totalidad de Horas No Lectivas asignadas al docente:
* **50% Inamovible:** Destinado exclusivamente a la preparación de clases y evaluación de aprendizajes.
* **50% Actividades de Dirección:** Destinado a Consejos de Profesores, atención a apoderados, trabajo colaborativo (GPT), labor UTP o actividades asignadas por la Dirección.

### 2.3. Conversión de Tiempos y Reglas de Cálculo Matemático
* **Hora Cronológica:** 60 minutos.
* **Hora Pedagógica:** 45 minutos ($0.75$ horas cronológicas).
* **Cálculo de Recreos:** Las horas de recreo se obtienen **siempre** a partir de las horas del contrato efectivo multiplicando las horas de contrato por **4 minutos**:
  $$\text{Recreo (minutos)} = \text{Horas Contrato Efectivo} \times 4 \text{ minutos}$$
* **Proporción 65/35 (Regla General):**
  * Horas Lectivas Máximas = $\text{Contrato Efectivo} \times 0.65$
  * Horas No Lectivas puras = $(\text{Contrato Efectivo} \times 0.35) - \text{Recreos}$
* **Proporción 60/40 (1° a 4° Básico Prioritario >80% SEP):**
  * Horas Lectivas Máximas = $\text{Contrato Efectivo} \times 0.60$
  * Horas No Lectivas puras = $(\text{Contrato Efectivo} \times 0.40) - \text{Recreos}$

### 2.4. Contratos Mixtos (Aula + Administración / Gestión)
Muchos profesores realizan clases y, adicionalmente, tienen asignadas horas fijas para coordinar un departamento, proyectos o ejercer funciones administrativas. En estos casos, la aplicación aplica el cálculo secuencial exacto exigido por la normativa:

1. **Paso 1:** Se toma el **Contrato Total de horas** (ej. 44 horas).
2. **Paso 2:** Se restan por completo las **Horas Administrativas asignadas** (ej. 14 horas para coordinación/gestión).
3. **Paso 3:** Con el saldo que queda (**Horas de Aula Restantes / Contrato Efectivo**, en este ejemplo, 30 horas), se aplica la regla legal del **65/35** (o 60/40 en 1° Ciclo prioritario).

#### 📊 Ejemplo Visual con un Contrato de 44 Horas:

| Detalle del Contrato | Distribución del Tiempo | ¿Cómo se calcula? |
| :--- | :--- | :--- |
| **Horas Administrativas fijas** | **14 horas** | Se apartan directamente para la gestión administrativa. |
| **Horas restantes para Aula** | **30 horas** | Sobre este saldo se aplica la regla legal (65/35). |
| **Horas Lectivas (Máx. 65%)** | **19,5 horas** | Tiempo máximo real dictando clases (26 hrs pedagógicas). |
| **Horas No Lectivas (Mín. 35%)** | **10,5 horas** | Tiempo para planificar, evaluar y trabajo colaborativo. |

> [!IMPORTANT]
> **⚠️ Regla de oro:** Las horas administrativas **jamás se deben descontar del 35% del tiempo no lectivo del profesor**. Ese 35% está protegido por ley exclusivamente para planificar clases, evaluar alumnos y realizar trabajo colaborativo.

### 2.5. Cargas Mixtas por Ciclo (1° Ciclo 60/40 + 2° Ciclo / Media 65/35)
Cuando un docente imparte clases tanto en Primer Ciclo (1° a 4° Básico) como en Segundo Ciclo / Enseñanza Media dentro de un establecimiento vulnerable (**>80% alumnos prioritarios SEP**), la capacidad máxima lectiva se calcula dividiendo la bolsa de contrato en dos bloques proporcionales:

$$\text{Lectivas Totales Máximas} = (\text{Horas Contrato 1° Ciclo} \times 0,60) + (\text{Horas Contrato Restantes 2° Ciclo} \times 0,65)$$

#### 📊 Ejemplo Matemático con un Contrato de 44 Horas:
* **Asignación 1° Ciclo:** 10 horas de contrato asignadas a 1° a 4° básico ($10 \text{ hrs} \times 0,60 = \mathbf{6,0 \text{ horas lectivas}}$ = 8 hrs ped).
* **Asignación 2° Ciclo / Media:** 34 horas de contrato restantes ($34 \text{ hrs} \times 0,65 = \mathbf{22,1 \text{ horas lectivas}}$).
* **Resultado Lectivo Máximo:** El docente puede realizar hasta **28,1 horas lectivas totales** frente a alumnos.
* **Bolsa No Lectiva + Recreos:** El saldo del contrato ($44 - 28,1 = \mathbf{15,9 \text{ horas}}$) se destina íntegramente a recreos, planificación inamovible (50%) y gestión directiva (50%).

---

## 3. Guía Paso a Paso de Uso

El sistema está organizado en **3 módulos principales** accesibles desde la barra superior de navegación y el menú lateral.

---

### Módulo 1: Simulación & Planificador Docente

Este módulo permite simular de forma individual la carga horaria de un profesor antes o durante la confección de los horarios.

#### Pasos para registrar un docente:
1. **Ingresar Datos Básicos:**
   * **Nombre del Docente:** Nombre o identificación del profesor/a.
   * **Contrato (hrs 60m):** Total de horas cronológicas contratadas semanalmente (máximo 44 hrs).
   * **Días de Presencia:** Seleccione la cantidad de días a la semana que el docente debe asistir al establecimiento.

2. **Asignación de Cursos y Horas (Hasta 16 espacios):**
   * Complete el nombre del **Curso**, **Asignatura**, seleccione el **Tipo de Carga** (1° Ciclo Ped/PIE o 2° Ciclo Ped/PIE) e ingrese la cantidad de **Horas Pedagógicas** impartidas.
   * El sistema convertirá automáticamente las horas pedagógicas a horas cronológicas equivalentes.

3. **Horas Administrativas / Fijadas en Contrato (Contratos Mixtos):**
   * Ingrese el nombre y la duración (horas/minutos) de funciones fijas en el contrato (ej. Inspectoría, Coordinación UTP/PIE, Encargado de Enlaces). 
   * *Secuencia de Cálculo:* Estas horas se apartan en el **Paso 2** directamente del Contrato Total, obteniendo el saldo efectivo sobre el cual se calcula el 65% de aula y el 35% no lectivo inamovible (**Regla de Oro**).

4. **Asignación de Actividades Directivas (Horas No Lectivas):**
   * Configure los tiempos asignados a:
     * Consejo de Profesores (ej. 2 horas pedagógicas o 1.5 horas cronológicas).
     * Atención a Apoderados.
     * Trabajo Colaborativo / GPT.
     * Gestión Técnica / UTP.
     * Otras actividades personalizadas.

5. **Análisis de Resultados en Tiempo Real:**
   * **Indicador / Semáforo de Cumplimiento:**
     * 🟢 **Verde (Cumple):** La carga asignada cumple con todos los límites legales y contractuales.
     * 🟡 **Amarillo (Al Límite / Tolerancia):** La carga lectiva o no lectiva está al límite de la capacidad o presenta pequeñas variaciones de redondeo.
     * 🔴 **Rojo (Infracción):** La carga lectiva excede el tope legal (65% o 60%), o las actividades no lectivas superan las horas disponibles en el contrato.
   * **Gráfico de Carga Apilada (Stacked Chart):** Visualización interactiva que muestra el porcentaje de contrato ocupado por Clases, Planificación, Recreos, Actividades Directivas y Horas Sobrantes/Sin Asignar.

6. **Guardar Docente:**
   * Haga clic en **"Guardar Docente"** para registrar los datos en la planta general.

---

### Módulo 2: Horario del Establecimiento

Permite definir los parámetros del horario escolar y verificar la permanencia requerida.

#### Configuración de la Jornada Escolar:
1. Ingrese la hora de **Entrada** y **Salida** para cada día de la semana (Lunes a Viernes).
2. Especifique los minutos asignados a la **Colación / Almuerzo**.
3. El sistema calculará el **Total de Permanencia Semanal Exigida** en el establecimiento.
4. Active la casilla **">80% SEP (Vulnerabilidad Elevada)"** en la barra superior si el colegio aplica la regla prioritaria del 60/40 para 1° Ciclo Básico bajo la Ley 21.625.

---

### Módulo 3: Planta Docente & Consolidado

Consolida la información de todos los profesores ingresados en el establecimiento.

#### Funcionalidades:
* **Tabla General de Profesores:** Muestra de forma unificada el contrato, distribución de horas lectivas, no lectivas, recreos y el estado de cumplimiento legal de cada docente.
* **Filtros y Búsqueda:**
  * Filtrar por estado: *Todos*, *Solo Cumplen (Verde)* o *Con Infracción (Rojo)*.
  * Buscador rápido por nombre del docente.
* **Edición y Eliminación:** Permite modificar o eliminar docentes registrados.
* **Exportación a Excel / CSV:** 
  * Haga clic en el botón **"Exportar a CSV"** para descargar un archivo `.csv` con la información completa de la planta docente, listo para abrir en Microsoft Excel o Google Sheets.

---

### Módulo 4: Página Maestra / Monitoreo Admin (Exclusivo)

* Módulo protegido por autenticación destinado exclusivamente a usuarios administradores (`admin@simohora.cl`).
* Ofrece métricas globales del sistema, estado de servidores y supervisión general.

---

## 4. Funciones Adicionales y Atajos

* **Cambio de Tema (Claro / Oscuro):** Haga clic en el ícono de Sol/Luna en la esquina superior derecha para alternar la apariencia del sistema.
* **Restablecer Sistema:** El botón con el ícono de recarga 🔄 elimina los datos simulados y reinicia la aplicación a sus valores de fábrica.
* **Impresión de Reportes:** Utilice el comando del navegador `Ctrl + P` (o `Cmd + P` en Mac). El sistema formateará automáticamente la pantalla eliminando la navegación para generar un reporte limpio en formato impreso o PDF.

---

## 5. Almacenamiento de Datos

SimoHora trabaja utilizando el almacenamiento local del navegador (**LocalStorage**). Esto garantiza que:
1. Sus datos se mantengan **100% privados** en su dispositivo.
2. No se requiere conexión constante a servidores externos para almacenar los borradores.
3. Al volver a abrir la aplicación en el mismo navegador, sus docentes y horarios se cargarán automáticamente.

---

## 6. Soporte y Consultas

Para sugerencias o dudas normativas sobre la aplicación de las leyes 20.903 y 21.625 en el sistema SimoHora, contacte al equipo de Coordinación UTP del establecimiento.

---

## 7. Tablas Oficiales de Referencia MINEDUC

### 7.1. Tabla 65/35 (Regla General - Arts. 69 y 80 DFL N° 1/1996 MINEDUC)
| Jornada Semanal | Horas Lectivas (HA) | Horas Lectivas (HC) | Recreo | Horas No Lectivas |
| :---: | :---: | :---: | :---: | :---: |
| **44 hrs** | 38 hrs ped | 28h 30m | 3h 00m | 12h 30m |
| **43 hrs** | 37 hrs ped | 27h 45m | 2h 56m | 12h 19m |
| **42 hrs** | 36 hrs ped | 27h 00m | 2h 52m | 12h 08m |
| **41 hrs** | 35 hrs ped | 26h 15m | 2h 48m | 11h 57m |
| **40 hrs** | 35 hrs ped | 26h 15m | 2h 44m | 11h 01m |
| **39 hrs** | 34 hrs ped | 25h 30m | 2h 40m | 10h 50m |
| **38 hrs** | 33 hrs ped | 24h 45m | 2h 35m | 10h 40m |
| **37 hrs** | 32 hrs ped | 24h 00m | 2h 31m | 10h 29m |
| **36 hrs** | 31 hrs ped | 23h 15m | 2h 27m | 10h 18m |
| **35 hrs** | 30 hrs ped | 22h 30m | 2h 23m | 10h 07m |
| **30 hrs** | 26 hrs ped | 19h 30m | 2h 03m | 8h 27m |
| **20 hrs** | 17 hrs ped | 12h 45m | 1h 22m | 5h 53m |
| **10 hrs** | 9 hrs ped | 6h 45m | 0h 41m | 2h 34m |

### 7.2. Tabla 60/40 (Ley 21.625 / Art. Cuarto Transitorio Ley N° 20.903 - 1° a 4° Básico &gt;80% SEP)
| Jornada Semanal | Horas Lectivas (HA) | Horas Lectivas (HC) | Recreo | Horas No Lectivas |
| :---: | :---: | :---: | :---: | :---: |
| **44 hrs** | 35 hrs ped | 26h 15m | 3h 00m | 14h 45m |
| **43 hrs** | 34 hrs ped | 25h 30m | 2h 56m | 14h 34m |
| **42 hrs** | 33 hrs ped | 24h 45m | 2h 52m | 14h 23m |
| **41 hrs** | 33 hrs ped | 24h 45m | 2h 48m | 13h 27m |
| **40 hrs** | 32 hrs ped | 24h 00m | 2h 44m | 13h 16m |
| **39 hrs** | 31 hrs ped | 23h 15m | 2h 40m | 13h 05m |
| **38 hrs** | 30 hrs ped | 22h 30m | 2h 35m | 12h 55m |
| **37 hrs** | 29 hrs ped | 21h 45m | 2h 31m | 12h 44m |
| **36 hrs** | 29 hrs ped | 21h 45m | 2h 27m | 11h 48m |
| **35 hrs** | 28 hrs ped | 21h 00m | 2h 23m | 11h 37m |
| **30 hrs** | 24 hrs ped | 18h 00m | 2h 03m | 9h 57m |
| **20 hrs** | 16 hrs ped | 12h 00m | 1h 22m | 6h 38m |
| **10 hrs** | 8 hrs ped | 6h 00m | 0h 41m | 3h 19m |
| **2 hrs** | 2 hrs ped | 1h 30m | 0h 08m | 0h 22m |

### 7.3. Cuadro de Factores de Equivalencia de Horas Contrato (Número Final)

Este cuadro permite obtener directamente el **Factor (Número Final)** a partir de las **Horas Aula Pedagógicas** para verificar rápidamente el total de horas de contrato requeridas:

$$\text{Horas Contrato} = \text{Horas Aula Pedagógicas Totales} + \text{Horas PIE} + \text{Horas Administrativas} + \text{Número Final}$$

#### 7.3.1. Regla 1: 2° Ciclo Básico, Enseñanza Media y Educación Parvularia (Pre-Kinder y Kinder)
*(Aplica también a 1° Ciclo Básico en colegios con ≤80% de estudiantes prioritarios)*

| Horas Aula Pedagógicas | Número / Factor |
| :---: | :---: |
| 35 a 38 hrs | **6** |
| 29 a 34 hrs | **5** |
| 22 a 28 hrs | **4** |
| 16 a 21 hrs | **3** |
| 10 a 15 hrs | **2** |
| 4 a 9 hrs | **1** |
| 1 a 3 hrs | **0** |

#### 7.3.2. Regla 2: 1° Ciclo Básico (1° a 4° Básico) con >80% SEP (Prioritarios)

| Horas Aula Pedagógicas | Número / Factor |
| :---: | :---: |
| 33 a 35 hrs | **9** |
| 29 a 32 hrs | **8** |
| 25 a 28 hrs | **7** |
| 21 a 24 hrs | **6** |
| 18 a 20 hrs | **5** |
| 14 a 17 hrs | **4** |
| 10 a 13 hrs | **3** |
| 6 a 9 hrs | **2** |
| 2 a 5 hrs | **1** |
| 1 hr | **0** |

#### 7.3.3. Cargas Mixtas (Docentes que imparten clases en 2 o más ciclos)
En caso de que un docente realice clases en varios ciclos (incluyendo 1° ciclo), se obtiene el factor de cada ciclo y se suman para obtener el **Número Final**:

* **Ejemplo Práctico:**
  * 10 hrs pedagógicas en 5° Básico (2° Ciclo) $\rightarrow$ **Factor 2** (Tabla Regla 1)
  * 10 hrs pedagógicas en 1° Básico con >80% SEP $\rightarrow$ **Factor 3** (Tabla Regla 2)
  * **Número Final (Suma de Factores):** $2 + 3 = \mathbf{5}$
  * **Horas de Contrato Totales:** $10 \text{ (aula 5°)} + 10 \text{ (aula 1°)} + 0 \text{ (PIE)} + 0 \text{ (Admin)} + 5 \text{ (Número Final)} = \mathbf{25 \text{ horas de contrato}}$.

---
*SimoHora v5.3 — Diseñado para UTP y Equipos Directivos de Chile.*
