# GHCoin — Automatizaciones Complementarias

> **Fecha:** 19 Junio 2026
> **Propósito:** Automatizaciones adicionales a los 5 ejes de capacitación que NO están en la landing actual pero generan alto ROI.
> **Stack:** n8n + Supabase + Google Sheets + WhatsApp API

---

## 📋 Lo que YA está en la landing (no repetir)

| Eje | Alcance |
|-----|---------|
| Admin & Finanzas | Reportes financieros, conciliación, aprobación facturas, emisión facturas |
| Gerencia & Managers | Dashboards KPIs, alertas inteligentes, IA decisiones, reportes automáticos |
| Recursos Humanos | Onboarding digital, control asistencia, alertas certificaciones, planillas |
| Comercial & Cotizaciones | Generación cotizaciones, seguimiento propuestas, pipeline, alertas licitaciones |
| Operaciones | Digitalización OT, programación mantenimiento, reportes campo, seguimiento equipos |

---

## 🆕 Automatizaciones Complementarias

### 1. 🤖 WhatsApp Bot para Trabajadores de Campo

**Problema:** Los conductores y operadores no tienen acceso a sistemas. Todo se reporta por llamada o en persona.

**Solución:** Bot de WhatsApp conectado a Supabase que:
- Recibe reportes de incidencia (fotos, ubicación, descripción) → crea ticket automático
- Consulta de saldos: vacaciones, horas extra, fecha de pago
- Recordatorios automáticos: revisiones técnicas, SOAT, exámenes médicos
- Encuestas post-turno: checklist de seguridad en 3 taps

**ROI Estimado:**
| Proceso | Horas/mes | Perfil | Costo/hr | % Autom. | Ahorro/mes | Ahorro/año |
|---------|:---------:|--------|:--------:|:--------:|:----------:|:----------:|
| Reporte de incidencias (ya no llaman a supervisores) | 60 | Supervisor flota | S/ 31.25 | 80% | **S/ 1,500** | **S/ 18,000** |
| Consultas frecuentes RRHH (buro fax) | 30 | Analista planillas | S/ 25.57 | 90% | **S/ 690** | **S/ 8,284** |
| Recordatorios de vencimientos | 10 | Asistente admin | S/ 14.20 | 95% | **S/ 135** | **S/ 1,619** |

---

### 2. 📄 Gestión Documental Digital

**Problema:** Contratos, facturas, guías, partes diarios — todo en papel o en carpetas de red sin buscar.

**Solución:** Sistema de archivo digital con OCR y búsqueda:
- Escaneo → Supabase Storage → OCR (n8n + OpenAI Vision) → metadatos → buscable
- Alertas de vencimiento de documentos (contratos, certificaciones, permisos)
- Versionado automático: cada modificación guarda historial
- Acceso por rol: solo ve documentos de tu área

**ROI Estimado:**
| Proceso | Horas/mes | Perfil | Costo/hr | % Autom. | Ahorro/mes | Ahorro/año |
|---------|:---------:|--------|:--------:|:--------:|:----------:|:----------:|
| Búsqueda de documentos (antes 20 min, ahora 10 seg) | 40 | Asistente admin | S/ 14.20 | 95% | **S/ 540** | **S/ 6,475** |
| Control de vencimientos (ya no se pasan) | 15 | Asistente admin | S/ 14.20 | 90% | **S/ 192** | **S/ 2,302** |
| Archivo físico → digital (eliminado) | 20 | Asistente admin | S/ 14.20 | 85% | **S/ 241** | **S/ 2,897** |

---

### 3. 🛒 Procura y Órdenes de Compra

**Problema:** Las compras se aprueban por WhatsApp/email. Sin trazabilidad, sin presupuesto visible, sin control de gasto.

**Solución:** Flujo completo de procure-to-pay:
- Solicitud de compra → aprobación por monto (jefe → gerente) → OC generada → recepción → pago
- Dashboard de gasto por área, proveedor, proyecto
- Alertas: OC sin factura, factura sin OC, sobrepresupuesto
- Catálogo de proveedores aprobados con historial de precios

**ROI Estimado:**
| Proceso | Horas/mes | Perfil | Costo/hr | % Autom. | Ahorro/mes | Ahorro/año |
|---------|:---------:|--------|:--------:|:--------:|:----------:|:----------:|
| Seguimiento de aprobaciones (antes persiguiendo firmas) | 30 | Asistente admin | S/ 14.20 | 85% | **S/ 362** | **S/ 4,344** |
| Matching OC-Factura (manual hoy) | 15 | Asistente contable | S/ 15.91 | 90% | **S/ 215** | **S/ 2,577** |
| Reporte de gasto por área (antes 4h cada finde mes) | 16 | Analista contable | S/ 25.57 | 95% | **S/ 389** | **S/ 4,663** |

---

### 4. 🛡️ Gestión de Seguridad y Salud Ocupacional (SSO)

**Problema:** Checklists en papel que nadie revisa. Incidentes reportados tarde. Sin trazabilidad para fiscalización SUNAFIL.

**Solución:** Sistema digital de SSO:
- Checklists pre-operacionales en app web/PWA (funciona offline en mina)
- Reporte de incidentes con fotos, ubicación GPS, clasificación automática de gravedad
- Investigación de incidentes: flujo con responsables, plazos, acciones correctivas
- Dashboard de indicadores SSO: frecuencia, gravedad, capacitaciones vencidas
- Alertas a gerencia si no se completan checklists del día

**ROI Estimado:**
| Proceso | Horas/mes | Perfil | Costo/hr | % Autom. | Ahorro/mes | Ahorro/año |
|---------|:---------:|--------|:--------:|:--------:|:----------:|:----------:|
| Digitalización de checklists (ya cubierto en Cumplimiento K1) | — | — | — | — | — | — |
| Investigación de incidentes (flujo automático) | 20 | Supervisor flota | S/ 31.25 | 70% | **S/ 438** | **S/ 5,250** |
| Reportes SUNAFIL/OSINERGMIN (antes 2 días, ahora 30 min) | 16 | Jefe SSO | S/ 45.45 | 90% | **S/ 655** | **S/ 7,855** |
| Seguimiento acciones correctivas | 15 | Supervisor | S/ 31.25 | 80% | **S/ 375** | **S/ 4,500** |

---

### 5. 📦 Gestión de Inventario y Repuestos

**Problema:** No se sabe qué hay en stock. Se compra de emergencia (más caro). Equipos parados esperando repuestos.

**Solución:** Sistema de inventario con QR/barcode:
- Cada repuesto/insumo tiene código QR → escaneo registra entrada/salida
- Stock mínimo → alerta automática de reorden al área de compras
- Historial de consumo por equipo → mantenimiento predictivo básico (sin IoT)
- Dashboard: rotación, valor de inventario, top consumos

**ROI Estimado:**
| Proceso | Horas/mes | Perfil | Costo/hr | % Autom. | Ahorro/mes | Ahorro/año |
|---------|:---------:|--------|:--------:|:--------:|:----------:|:----------:|
| Conteo físico de inventario (antes 2 personas 2 días/mes) | 64 | Asistente admin ×2 | S/ 14.20 | 85% | **S/ 772** | **S/ 9,269** |
| Detección de stock bajo (antes reactivo, ahora proactivo) | 10 | Coordinador taller | S/ 31.25 | 90% | **S/ 281** | **S/ 3,375** |
| Reducción compras de emergencia (estimado 15% menos) | — | — | — | — | **S/ 1,500** | **S/ 18,000** |

---

### 6. 🎫 Mesa de Ayuda Interna (IT + Soporte)

**Problema:** "El sistema no funciona", "necesito acceso a X", "la impresora no imprime" — todo por WhatsApp a la persona equivocada.

**Solución:** Sistema de tickets interno:
- Portal web simple + WhatsApp para crear tickets
- Asignación automática por categoría (IT, RRHH, Admin, Flota)
- SLA por tipo de ticket con escalamiento automático si no se responde
- Base de conocimiento: soluciones frecuentes → el bot responde antes de crear ticket

**ROI Estimado:**
| Proceso | Horas/mes | Perfil | Costo/hr | % Autom. | Ahorro/mes | Ahorro/año |
|---------|:---------:|--------|:--------:|:--------:|:----------:|:----------:|
| Gestión de solicitudes (antes 30 min persiguiendo al responsable) | 40 | Asistente admin | S/ 14.20 | 70% | **S/ 398** | **S/ 4,771** |
| Tickets recurrentes que el bot resuelve solo | 20 | Personal IT | S/ 25.57 | 80% | **S/ 409** | **S/ 4,909** |
| Reporte de tiempo de resolución (antes manual) | 8 | Jefe IT | S/ 45.45 | 95% | **S/ 345** | **S/ 4,145** |

---

### 7. 🚗 Autorizaciones de Viaje y Viáticos

**Problema:** Conductores y supervisores viajan a mina/sede cliente. Las autorizaciones son papel y los viáticos se liquidan con tickets físicos.

**Solución:** Flujo digital de travel & expense:
- Solicitud de viaje → aprobación jefe → asignación de vehículo → anticipo
- Liquidación de viáticos con fotos de comprobantes (OCR extrae montos)
- Dashboard de gastos de viaje por persona, proyecto, mes
- Alertas: viajes sin liquidar después de 48h de retorno

**ROI Estimado:**
| Proceso | Horas/mes | Perfil | Costo/hr | % Autom. | Ahorro/mes | Ahorro/año |
|---------|:---------:|--------|:--------:|:--------:|:----------:|:----------:|
| Procesar autorización de viaje (antes 3 aprobaciones en papel) | 25 | Asistente admin | S/ 14.20 | 75% | **S/ 266** | **S/ 3,195** |
| Liquidación de viáticos (antes 45 min por persona) | 30 | Asistente contable | S/ 15.91 | 80% | **S/ 382** | **S/ 4,582** |
| Control de anticipos no rendidos | 10 | Analista contable | S/ 25.57 | 90% | **S/ 230** | **S/ 2,761** |

---

### 8. 🧠 IA para Análisis de Datos (No-Code)

**Problema:** Los gerentes tienen datos pero no saben analizarlos. Dependen de que alguien haga un Excel cada vez que necesitan un cruce.

**Solución:** Capa de IA conversacional sobre Supabase:
- "¿Cuál fue el margen por cliente este trimestre?" → query SQL generada por IA → respuesta en lenguaje natural + gráfico
- "¿Qué vehículos tienen el mayor costo de mantenimiento por km?" → análisis automático
- "Compara la productividad de los 3 últimos meses" → dashboard generado al instante
- Esto empodera a los gerentes sin saber SQL ni Excel avanzado

**ROI Estimado:**
| Proceso | Horas/mes | Perfil | Costo/hr | % Autom. | Ahorro/mes | Ahorro/año |
|---------|:---------:|--------|:--------:|:--------:|:----------:|:----------:|
| Consultas ad-hoc que antes iban a analista (10 consultas/sem × 30 min) | 20 | Analista contable | S/ 25.57 | 85% | **S/ 435** | **S/ 5,216** |
| Reportes especiales para gerencia (antes 4h c/u, ahora 5 min) | 16 | Analista contable | S/ 25.57 | 90% | **S/ 368** | **S/ 4,418** |
| Toma de decisiones más rápida (intangible) | — | Gerentes | S/ 79.55 | — | **Intangible** | **Alto** |

---

### 9. 📊 Evaluación de Proveedores

**Problema:** No hay criterio objetivo para evaluar proveedores. Se contrata al que "siempre se ha usado" o al que cayó bien.

**Solución:** Sistema de vendor scorecard:
- Cada OC completada → evaluación automática (tiempo entrega, calidad, precio vs cotizado)
- Dashboard de ranking de proveedores por categoría
- Alertas: proveedor con tendencia a la baja, proveedor con mejores precios no usado
- Base de datos de proveedores alternativos por categoría

**ROI Estimado:**
| Proceso | Horas/mes | Perfil | Costo/hr | % Autom. | Ahorro/mes | Ahorro/año |
|---------|:---------:|--------|:--------:|:--------:|:----------:|:----------:|
| Evaluación trimestral de proveedores (antes 3 días cada trimestre → 12 días/año) | 8 | Coordinador compras | S/ 31.25 | 90% | **S/ 225** | **S/ 2,700** |
| Ahorro por mejor selección de proveedor (estimado 5% en compras) | — | — | — | — | **S/ 2,500** | **S/ 30,000** |

---

### 10. 🔔 Sistema de Alertas Inteligentes Multicanal

**Problema:** La información está en los sistemas, pero nadie la ve hasta que es tarde. Las alertas actuales son correos que nadie lee.

**Solución:** Motor de alertas multicanal con reglas configurables:
- "Si un vehículo supera 20% de consumo de combustible vs promedio → alerta a supervisor"
- "Si un contrato vence en 30 días → WhatsApp a gerente comercial + email a legal"
- "Si un trabajador no completó su checklist de seguridad hoy a las 8am → SMS al jefe directo"
- Canales: WhatsApp, email, SMS, notificación web, dashboard de alertas
- Escalamiento: si no se atiende en X horas, sube al siguiente nivel

**ROI Estimado:**
| Proceso | Horas/mes | Perfil | Costo/hr | % Autom. | Ahorro/mes | Ahorro/año |
|---------|:---------:|--------|:--------:|:--------:|:----------:|:----------:|
| Monitoreo manual de excepciones (antes revisando planillas/reportes) | 40 | Varios roles | S/ 20.00 | 90% | **S/ 720** | **S/ 8,640** |
| Prevención de incidentes por detección temprana (intangible) | — | — | — | — | **Alto** | **Alto** |

---

## 📊 Resumen de Automatizaciones Complementarias

| # | Automatización | Ahorro/mes | Ahorro/año |
|:-:|----------------|:----------:|:----------:|
| 1 | WhatsApp Bot para Campo | S/ 2,325 | S/ 27,903 |
| 2 | Gestión Documental Digital | S/ 973 | S/ 11,674 |
| 3 | Procura y Órdenes de Compra | S/ 966 | S/ 11,584 |
| 4 | Gestión SSO Digital | S/ 1,468 | S/ 17,605 |
| 5 | Inventario con QR | S/ 2,553 | S/ 30,644 |
| 6 | Mesa de Ayuda Interna | S/ 1,152 | S/ 13,825 |
| 7 | Autorizaciones de Viaje | S/ 878 | S/ 10,538 |
| 8 | IA para Análisis de Datos | S/ 803 | S/ 9,634 |
| 9 | Evaluación de Proveedores | S/ 2,725 | S/ 32,700 |
| 10 | Alertas Inteligentes | S/ 720 | S/ 8,640 |
| **TOTAL (solo ahorro directo medible)** | **S/ 6,127** | **S/ 73,524** |

---

## 💰 Impacto Total GHCoin (Landing + Complementarias)

| Fuente | Ahorro/año |
|--------|:----------:|
| Automatizaciones base (43 procesos del ROI detallado) | S/ 191,996 |
| Automatizaciones complementarias (este documento) | S/ 73,524 |
| **Ahorro directo total** | **S/ 265,520** |
| **+ Evitación de pérdidas (mantenimiento reactivo, combustible, contratos)** | **S/ 136,000** |
| **Impacto total potencial** | **~S/ 400,000/año** |

---

## 🎯 Recomendación para la Landing

Agregar una sección al final llamada **"Automatizaciones Complementarias"** o **"Más allá de la capacitación"** con:

- 3-4 cards destacando las de mayor impacto visual:
  1. WhatsApp Bot (innovación, cercanía al trabajador)
  2. Gestión Documental (orden, compliance)
  3. Alertas Inteligentes (proactividad, prevenir > reaccionar)
  4. IA para Datos (futurista, empoderamiento)

- Un CTA adicional: *"Estas automatizaciones van más allá de la capacitación — son sistemas que quedan funcionando para siempre."*
