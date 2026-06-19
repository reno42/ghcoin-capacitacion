# Casos de Automatización por Industria — Catálogo de ROI

> **Fecha:** 19 Junio 2026
> **Propósito:** Catálogo de casos de automatización para distintas industrias, con perfiles reales del mercado peruano, sueldos, horas invertidas y ahorro estimado.
> **Stack base:** n8n + Supabase + Google Sheets
> **Metodología:** Ahorro = horas/mes × costo hora × % automatizable × 12 meses
> **Tasa de ahorro conservadora:** 70% del tiempo manual

---

## 📐 Metodología de Cálculo

- **Costo hora** = Sueldo mensual ÷ 176 horas
- **Ahorro mensual** = Horas manuales/mes × % automatizable × Costo hora
- **Ahorro anual** = Ahorro mensual × 12
- **Costo implementación** = 3-6 meses de licencias n8n + Supabase (~S/ 400-800/mes) + setup Futuraria
- **ROI** = (Ahorro anual − Costo herramientas) ÷ Inversión total

---

## 🏥 1. Clínicas y Centros de Salud

### Perfiles y Sueldos (Perú 2026)

| Perfil | Sueldo/mes | Costo/hr | Horas automatizables/mes | % Autom. | Ahorro/mes | Ahorro/año |
|--------|:----------:|:--------:|:------------------------:|:--------:|:----------:|:----------:|
| Recepcionista (agenda citas, confirma, registra) | S/ 1,800 | S/ 10.23 | 80 | 70% | **S/ 573** | **S/ 6,874** |
| Asistente administrativo (historias, archivo, seguros) | S/ 2,200 | S/ 12.50 | 60 | 65% | **S/ 488** | **S/ 5,850** |
| Cajero (cobranzas, facturación, conciliación) | S/ 1,800 | S/ 10.23 | 50 | 75% | **S/ 384** | **S/ 4,603** |
| Enfermera (registro de signos vitales, notas) | S/ 3,000 | S/ 17.05 | 30 | 50% | **S/ 256** | **S/ 3,069** |
| Administrador (reportes, KPIs, planificación) | S/ 5,000 | S/ 28.41 | 40 | 60% | **S/ 682** | **S/ 8,183** |
| **TOTAL** | | | **260** | | **S/ 2,383** | **S/ 28,579** |

### ¿Qué se automatiza?
- 📅 **Agenda inteligente:** Paciente agenda por WhatsApp → confirmación automática 24h antes → si cancela, se libera y notifica a lista de espera
- 📋 **Registro clínico digital:** Signos vitales → Supabase → Dashboard médico
- 💰 **Cobranza automática:** Facturación + envío WhatsApp/email + recordatorio de pago
- 📊 **Dashboard del director:** Ocupación, ingresos, satisfacción — se actualiza solo
- 🏥 **Historias clínicas digitales:** Búsqueda por paciente, alertas de alergias/condiciones

---

## 🏪 2. Retail y E-commerce

### Perfiles y Sueldos

| Perfil | Sueldo/mes | Costo/hr | Horas automatizables/mes | % Autom. | Ahorro/mes | Ahorro/año |
|--------|:----------:|:--------:|:------------------------:|:--------:|:----------:|:----------:|
| Vendedor de tienda (registro, consulta stock) | S/ 1,500 | S/ 8.52 | 40 | 50% | **S/ 170** | **S/ 2,045** |
| Community manager (publicaciones, respuestas) | S/ 2,500 | S/ 14.20 | 60 | 55% | **S/ 469** | **S/ 5,626** |
| Encargado de logística (pedidos, stock, envíos) | S/ 2,800 | S/ 15.91 | 70 | 70% | **S/ 780** | **S/ 9,352** |
| Asistente contable (facturación, conciliación) | S/ 2,500 | S/ 14.20 | 50 | 75% | **S/ 533** | **S/ 6,391** |
| Gerente de tienda (reportes, pedidos, personal) | S/ 5,500 | S/ 31.25 | 30 | 50% | **S/ 469** | **S/ 5,625** |
| **TOTAL** | | | **250** | | **S/ 2,421** | **S/ 29,039** |

### ¿Qué se automatiza?
- 🛒 **Pedidos WhatsApp → Supabase → Orden de despacho:** Catálogo digital, el cliente pide por WhatsApp, se genera orden automática
- 📦 **Control de inventario con alertas:** Stock bajo → notificación a compras → orden sugerida
- 📱 **Respuestas automáticas:** Preguntas frecuentes (horario, precio, stock) respondidas por bot
- 🧾 **Facturación electrónica automática** desde Supabase a SUNAT vía n8n
- 📊 **Dashboard de ventas por canal** que se actualiza solo

---

## 🍽️ 3. Restaurantes y Food Service

### Perfiles y Sueldos

| Perfil | Sueldo/mes | Costo/hr | Horas automatizables/mes | % Autom. | Ahorro/mes | Ahorro/año |
|--------|:----------:|:--------:|:------------------------:|:--------:|:----------:|:----------:|
| Mesero/a (toma pedidos, lleva cuenta) | S/ 1,500 | S/ 8.52 | 60 | 40% | **S/ 205** | **S/ 2,455** |
| Cajero/a (cobro, cuadre, facturación) | S/ 1,500 | S/ 8.52 | 50 | 70% | **S/ 298** | **S/ 3,578** |
| Jefe de cocina (pedidos, mermas, inventario) | S/ 4,000 | S/ 22.73 | 40 | 55% | **S/ 500** | **S/ 6,002** |
| Administrador (planillas, proveedores, reportes) | S/ 4,000 | S/ 22.73 | 50 | 60% | **S/ 682** | **S/ 8,183** |
| Encargado delivery (coordina motorizados, rutas) | S/ 1,800 | S/ 10.23 | 40 | 50% | **S/ 205** | **S/ 2,455** |
| **TOTAL** | | | **240** | | **S/ 1,890** | **S/ 22,673** |

### ¿Qué se automatiza?
- 📲 **Pedidos por WhatsApp → cocina:** Menú digital con fotos, el cliente pide, llega directo a pantalla en cocina
- 📊 **Control de mermas:** Registro rápido → dashboard de desperdicio semanal → ajuste de compras
- 🧾 **Cuadre de caja automático:** Ventas del día consolidadas, comparadas con POS, diferencias alertadas
- 📅 **Programación de personal:** Horarios, vacaciones, cambios de turno en app web
- 🛒 **Pedidos a proveedores:** Según consumo histórico + evento especial → sugerencia automática

---

## 🏗️ 4. Construcción e Inmobiliarias

### Perfiles y Sueldos

| Perfil | Sueldo/mes | Costo/hr | Horas automatizables/mes | % Autom. | Ahorro/mes | Ahorro/año |
|--------|:----------:|:--------:|:------------------------:|:--------:|:----------:|:----------:|
| Asistente de obra (partes diarios, reportes) | S/ 2,500 | S/ 14.20 | 80 | 75% | **S/ 852** | **S/ 10,224** |
| Ingeniero residente (reportes, valorizaciones) | S/ 6,000 | S/ 34.09 | 50 | 60% | **S/ 1,023** | **S/ 12,273** |
| Arquitecto/Ing de oficina técnica (planos, metrados) | S/ 4,500 | S/ 25.57 | 40 | 50% | **S/ 511** | **S/ 6,136** |
| Administrador de obra (compras, personal, proveedores) | S/ 4,000 | S/ 22.73 | 50 | 65% | **S/ 739** | **S/ 8,866** |
| Jefe de logística (materiales, equipos, almacén) | S/ 3,500 | S/ 19.89 | 45 | 60% | **S/ 537** | **S/ 6,444** |
| **TOTAL** | | | **265** | | **S/ 3,662** | **S/ 43,943** |

### ¿Qué se automatiza?
- 📋 **Parte diario digital:** Capataz reporta desde celular (offline) → se consolida solo → Dashboard avance
- 📊 **Valorizaciones automáticas:** Metrados × precios unitarios → valorización lista en minutos
- 🛒 **Control de materiales:** Pedido → aprobación → despacho → registro de uso → alerta de faltante
- 📸 **Registro fotográfico de obra:** Fotos con fecha/ubicación → organizadas por partida automáticamente
- 👷 **Control de personal en obra:** Asistencia, horas extra, EPPs entregados, charlas de seguridad

---

## ⚖️ 5. Estudios de Abogados

### Perfiles y Sueldos

| Perfil | Sueldo/mes | Costo/hr | Horas automatizables/mes | % Autom. | Ahorro/mes | Ahorro/año |
|--------|:----------:|:--------:|:------------------------:|:--------:|:----------:|:----------:|
| Secretaria legal (escritos, notificaciones, archivo) | S/ 2,500 | S/ 14.20 | 100 | 70% | **S/ 994** | **S/ 11,929** |
| Asistente legal (redacción, jurisprudencia, fichas) | S/ 3,000 | S/ 17.05 | 60 | 50% | **S/ 512** | **S/ 6,138** |
| Abogado junior (demandas, recursos, revisión) | S/ 4,500 | S/ 25.57 | 40 | 45% | **S/ 460** | **S/ 5,523** |
| Abogado senior (estrategia, revisión final, cliente) | S/ 8,000 | S/ 45.45 | 25 | 35% | **S/ 398** | **S/ 4,772** |
| Administrador del estudio (cobranzas, gastos, KPIs) | S/ 4,000 | S/ 22.73 | 35 | 65% | **S/ 517** | **S/ 6,206** |
| **TOTAL** | | | **260** | | **S/ 2,881** | **S/ 34,568** |

### ¿Qué se automatiza?
- 📅 **Control de plazos procesales:** Alertas 7-3-1 días antes del vencimiento, con escalamiento
- 📄 **Generación de escritos:** Plantillas inteligentes → llenado automático con datos del expediente
- 🔍 **Búsqueda de jurisprudencia:** IA entrenada en el código civil peruano, consultas en lenguaje natural
- 💰 **Seguimiento de honorarios:** Tiempo por caso → facturación automática → recordatorio de pago
- 📋 **Dashboard de expedientes:** Estado, próximo paso, responsable, SLA — tablero Kanban automático

---

## 🏫 6. Colegios e Instituciones Educativas

### Perfiles y Sueldos

| Perfil | Sueldo/mes | Costo/hr | Horas automatizables/mes | % Autom. | Ahorro/mes | Ahorro/año |
|--------|:----------:|:--------:|:------------------------:|:--------:|:----------:|:----------:|
| Secretaria académica (matrículas, notas, certificados) | S/ 2,000 | S/ 11.36 | 80 | 70% | **S/ 636** | **S/ 7,635** |
| Administrador (pensiones, cobranzas, proveedores) | S/ 3,500 | S/ 19.89 | 60 | 65% | **S/ 776** | **S/ 9,309** |
| Coordinador académico (horarios, docentes, planes) | S/ 3,500 | S/ 19.89 | 40 | 55% | **S/ 438** | **S/ 5,250** |
| Psicólogo/Tutor (reportes, seguimiento alumnos) | S/ 3,000 | S/ 17.05 | 30 | 50% | **S/ 256** | **S/ 3,069** |
| Director (reportes Minedu, acreditación, KPIs) | S/ 7,000 | S/ 39.77 | 25 | 50% | **S/ 497** | **S/ 5,965** |
| **TOTAL** | | | **235** | | **S/ 2,603** | **S/ 31,228** |

### ¿Qué se automatiza?
- 📝 **Matrícula digital:** Formulario web → pago → confirmación automática → asignación de sección
- 📊 **Boleta de notas automática:** Notas cargadas por docente → promedios calculados → envío a padres por WhatsApp/email
- 💰 **Control de pensiones:** Recordatorio de pago → registro automático → alerta de morosidad → reporte a dirección
- 📅 **Asistencia digital:** Docente marca desde app → reporte diario a padres → alerta de inasistencias recurrentes
- 📋 **Certificados y constancias:** Generación automática desde base de datos de alumnos

---

## 🚚 7. Logística y Transporte

### Perfiles y Sueldos

| Perfil | Sueldo/mes | Costo/hr | Horas automatizables/mes | % Autom. | Ahorro/mes | Ahorro/año |
|--------|:----------:|:--------:|:------------------------:|:--------:|:----------:|:----------:|
| Coordinador de flota (rutas, conductores, novedades) | S/ 3,500 | S/ 19.89 | 80 | 65% | **S/ 1,034** | **S/ 12,411** |
| Asistente administrativo (guías, facturas, archivo) | S/ 2,000 | S/ 11.36 | 70 | 75% | **S/ 596** | **S/ 7,157** |
| Despachador (carga, documentos, checklist) | S/ 2,200 | S/ 12.50 | 50 | 60% | **S/ 375** | **S/ 4,500** |
| Jefe de operaciones (KPIs, costos, eficiencia) | S/ 6,000 | S/ 34.09 | 40 | 55% | **S/ 750** | **S/ 9,002** |
| Facturador (guías → facturas, SUNAT) | S/ 2,500 | S/ 14.20 | 50 | 80% | **S/ 568** | **S/ 6,816** |
| **TOTAL** | | | **290** | | **S/ 3,323** | **S/ 39,886** |

### ¿Qué se automatiza?
- 🗺️ **Planificación de rutas:** Asignación automática por zona, capacidad, prioridad
- 📄 **Guía de remisión → Factura:** Flujo automático: guía firmada → factura SUNAT → envío a cliente
- 📊 **Dashboard de eficiencia:** Entregas a tiempo, consumo combustible, incidencias por conductor
- 🔔 **Alertas de mantenimiento:** Km recorrido → programación automática → notificación a taller
- 📱 **App para conductores:** Check-in/out, novedades en ruta, firma digital de conformidad

---

## 🏨 8. Hoteles y Hospedajes

### Perfiles y Sueldos

| Perfil | Sueldo/mes | Costo/hr | Horas automatizables/mes | % Autom. | Ahorro/mes | Ahorro/año |
|--------|:----------:|:--------:|:------------------------:|:--------:|:----------:|:----------:|
| Recepcionista (check-in/out, consultas, reservas) | S/ 1,800 | S/ 10.23 | 80 | 55% | **S/ 450** | **S/ 5,402** |
| Ama de llaves (asignación habitaciones, inventario) | S/ 1,800 | S/ 10.23 | 40 | 50% | **S/ 205** | **S/ 2,455** |
| Administrador (reportes, OTAs, pricing, personal) | S/ 4,500 | S/ 25.57 | 50 | 60% | **S/ 767** | **S/ 9,205** |
| Encargado de mantenimiento (reportes, insumos) | S/ 2,200 | S/ 12.50 | 30 | 50% | **S/ 188** | **S/ 2,250** |
| Ventas/Reservas (cotizaciones grupos, eventos) | S/ 2,500 | S/ 14.20 | 40 | 55% | **S/ 312** | **S/ 3,750** |
| **TOTAL** | | | **240** | | **S/ 1,922** | **S/ 23,062** |

### ¿Qué se automatiza?
- 🛎️ **Check-in digital:** Formulario pre-llegada → llave/código enviado → sin pasar por recepción
- 📊 **Revenue management básico:** Ocupación vs tarifa → sugerencia de ajuste de precios
- 🧹 **Asignación de limpieza:** Check-outs del día → asignación automática a personal → confirmación por app
- 💬 **Bot de conserjería:** Recomendaciones, pedidos al room service, solicitud de amenities
- 📈 **Dashboard del gerente:** Ocupación, RevPAR, satisfacción, origen de reservas — automático

---

## 🏢 9. Empresas de Servicios B2B (Consultoría, Marketing, IT)

### Perfiles y Sueldos

| Perfil | Sueldo/mes | Costo/hr | Horas automatizables/mes | % Autom. | Ahorro/mes | Ahorro/año |
|--------|:----------:|:--------:|:------------------------:|:--------:|:----------:|:----------:|
| Project Manager (reportes, seguimiento, actas) | S/ 5,500 | S/ 31.25 | 50 | 55% | **S/ 859** | **S/ 10,313** |
| Ejecutivo de cuenta (reportes cliente, emails) | S/ 3,500 | S/ 19.89 | 45 | 60% | **S/ 537** | **S/ 6,444** |
| Asistente administrativo (facturación, archivo) | S/ 2,200 | S/ 12.50 | 60 | 75% | **S/ 563** | **S/ 6,750** |
| Analista (reportes, dashboards, presentaciones) | S/ 3,500 | S/ 19.89 | 50 | 55% | **S/ 547** | **S/ 6,563** |
| Gerente general (pipeline, finanzas, RRHH) | S/ 12,000 | S/ 68.18 | 30 | 40% | **S/ 818** | **S/ 9,818** |
| **TOTAL** | | | **235** | | **S/ 3,324** | **S/ 39,888** |

### ¿Qué se automatiza?
- 📊 **Reportes de proyecto:** Horas × tarea × persona → facturación sugerida → dashboard cliente
- 📅 **Recordatorios de hitos:** Fechas clave → alertas a PM → si se vence sin completar, escala
- 🧾 **Facturación recurrente:** Contratos mensuales → factura automática → envío a cliente
- 📝 **Minutas y actas:** Transcripción IA de reuniones → resumen → asignación de tareas → seguimiento
- 📈 **Pipeline comercial:** Leads → propuestas enviadas → seguimiento automático → tasa de cierre

---

## 🏭 10. Manufactura y Talleres

### Perfiles y Sueldos

| Perfil | Sueldo/mes | Costo/hr | Horas automatizables/mes | % Autom. | Ahorro/mes | Ahorro/año |
|--------|:----------:|:--------:|:------------------------:|:--------:|:----------:|:----------:|
| Jefe de producción (planificación, reportes) | S/ 5,000 | S/ 28.41 | 50 | 55% | **S/ 781** | **S/ 9,375** |
| Asistente de producción (registros, hojas ruta) | S/ 2,200 | S/ 12.50 | 70 | 70% | **S/ 613** | **S/ 7,350** |
| Almacenero (inventario, despacho, recepción) | S/ 1,800 | S/ 10.23 | 60 | 65% | **S/ 399** | **S/ 4,788** |
| Control de calidad (checklists, reportes) | S/ 2,800 | S/ 15.91 | 40 | 60% | **S/ 382** | **S/ 4,582** |
| Administrador (costos, proveedores, facturación) | S/ 4,000 | S/ 22.73 | 40 | 60% | **S/ 545** | **S/ 6,546** |
| **TOTAL** | | | **260** | | **S/ 2,720** | **S/ 32,641** |

### ¿Qué se automatiza?
- 🏭 **Órdenes de producción digitales:** Cliente → orden → ruta de fabricación → seguimiento en tiempo real
- 📊 **Control de eficiencia:** Producción real vs planificada → dashboard de OEE (Overall Equipment Effectiveness)
- 📦 **Trazabilidad de lote:** Materia prima → producción → producto terminado → cliente (crítico para certificaciones)
- 🔧 **Mantenimiento de máquinas:** Horas de uso → programación automática → checklist digital
- 📋 **Control de calidad:** Inspecciones digitales → no conformidades → acciones correctivas → cierre

---

## 📊 Resumen Comparativo: Top 10 Industrias

| # | Industria | Ahorro/mes | Ahorro/año | Costo impl. (est.) | ROI Año 1 |
|:-:|-----------|:----------:|:----------:|:------------------:|:---------:|
| 1 | 🏗️ Construcción | S/ 3,662 | S/ 43,943 | S/ 8,000 | **449%** |
| 2 | 🚚 Logística y Transporte | S/ 3,323 | S/ 39,886 | S/ 8,000 | **399%** |
| 3 | 🏢 Servicios B2B | S/ 3,324 | S/ 39,888 | S/ 6,000 | **565%** |
| 4 | ⚖️ Estudios de Abogados | S/ 2,881 | S/ 34,568 | S/ 7,000 | **394%** |
| 5 | 🏭 Manufactura | S/ 2,720 | S/ 32,641 | S/ 9,000 | **263%** |
| 6 | 🏫 Colegios | S/ 2,603 | S/ 31,228 | S/ 7,000 | **346%** |
| 7 | 🏪 Retail/E-commerce | S/ 2,421 | S/ 29,039 | S/ 6,000 | **384%** |
| 8 | 🏥 Clínicas | S/ 2,383 | S/ 28,579 | S/ 8,000 | **257%** |
| 9 | 🏨 Hoteles | S/ 1,922 | S/ 23,062 | S/ 6,000 | **284%** |
| 10 | 🍽️ Restaurantes | S/ 1,890 | S/ 22,673 | S/ 5,500 | **312%** |

> **Nota:** El costo de implementación incluye setup Futuraria + 6 meses de licencias + capacitación. ROI Año 1 = (Ahorro − Costo herramientas) ÷ Inversión. Todos los casos tienen ROI positivo en menos de 6 meses.

---

## 🎯 Las 3 Automatizaciones Transversales (Aplican a TODAS las industrias)

### A. 📱 WhatsApp Business + CRM
- **Qué hace:** Cliente escribe → bot responde FAQs → si necesita humano, crea ticket → seguimiento automático
- **Industrias:** Todas. El 90% de pymes peruanas usan WhatsApp como canal principal
- **Ahorro típico:** 40-60 horas/mes de recepción/ventas = S/ 400-800/mes

### B. 🧾 Facturación Electrónica Automática
- **Qué hace:** Registro en Supabase → n8n genera XML → envía a SUNAT → guarda CDR → envía a cliente
- **Industrias:** Todas las que facturan (básicamente todas)
- **Ahorro típico:** 30-50 horas/mes de facturación manual = S/ 350-700/mes

### C. 📊 Dashboard Gerencial Automático
- **Qué hace:** Datos de hojas de cálculo/sistemas → Supabase → dashboard que se actualiza solo → alertas
- **Industrias:** Todas. Todo gerente pierde 4-8h/semana armando reportes
- **Ahorro típico:** 16-32 horas/mes de gerencia = S/ 500-2,500/mes (según nivel)

---

## 💡 Cómo Usar Este Catálogo en Ventas

1. **Identificar la industria del prospecto** → mostrar la tabla de su industria
2. **Preguntar cuántas personas tienen en ese rol** → multiplicar el ahorro
3. **Mostrar el ROI Año 1** → típicamente 250-550%
4. **Ofrecer auditoría gratuita de 60 min** → identificar los 3 procesos de mayor impacto
5. **Cerrar con:** "Si automatizamos solo 3 de estos procesos, el retorno es de X meses. El resto es ganancia."

---

## ⚠️ Lo Que NO se Promete (Expectativas Claras)

- ❌ Reemplazar sistemas legacy (SAP, Oracle) — integramos con ellos, no los reemplazamos
- ❌ Machine Learning predictivo avanzado — usamos IA para análisis, no para predicción estadística compleja
- ❌ Automatizar 100% de un proceso — siempre queda un % de revisión humana para excepciones
- ❌ Resultados en semana 1 — el setup toma 2-4 semanas; el ahorro se ve a partir del mes 2
