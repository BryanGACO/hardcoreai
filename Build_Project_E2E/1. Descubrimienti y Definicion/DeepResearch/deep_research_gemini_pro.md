# Deep Research: Validación del MVP - Agente de Compras en WhatsApp

## 1. Resumen Ejecutivo: Validación de la Hipótesis Central
[cite_start]La propuesta de valor central se basa en convertir conversaciones en ventas repetibles, eliminando la fricción de descargar apps, llenar formularios o iniciar sesión[cite: 6]. [cite_start]El "Agentic Commerce" está posicionándose como una industria clave [cite: 2][cite_start], y el comercio conversacional en WhatsApp está dejando de ser un experimento para convertirse en un canal de ventas principal en Latinoamérica[cite: 8].

## 2. Sincronización con el Mercado: Casos de Éxito
Los datos del mercado respaldan fuertemente la transición hacia este modelo de negocio:
* [cite_start]**Walmart Chile:** Reportó que sus campañas por WhatsApp con carritos pre-llenados ya explican aproximadamente el 20% de su e-commerce local[cite: 9].
* [cite_start]**Magalu (Brasil):** Lanzó "Lu's WhatsApp" para completar todo el flujo E2E (recomendación, pago y postventa) dentro del chat, proyectando alcanzar más de 30 millones de clientes[cite: 10].
* [cite_start]**Adopción B2B:** El 39% de los retailers en Brasil ya realizan pedidos con proveedores por canales como WhatsApp, según datos de Yalo (2024), incluyendo sugerencias automáticas de reposición[cite: 11].

## 3. Viabilidad Técnica y de UX (Flujos y Pagos)
La arquitectura del MVP está perfectamente alineada con las capacidades actuales del ecosistema:
* [cite_start]**Captura de datos estructurados:** El uso de WhatsApp Flows permite capturar datos críticos como la cantidad, la dirección y la fecha de forma eficiente[cite: 17].
* [cite_start]**Integración de Pagos:** El sistema contempla el uso de links de pago (Stripe, Mercado Pago o Webpay) complementados con confirmación vía webhook[cite: 18].
* [cite_start]**Políticas a tu favor:** Desde enero de 2026, la plataforma de WhatsApp Business permite formalmente bots orientados a negocio, como ventas, soporte y reservas[cite: 12]. [cite_start]El producto propuesto cae exactamente en esta categoría permitida[cite: 13].
* [cite_start]**Estándares de pago "Agentic":** Visa y Mastercard impulsan pagos "agentic" con estándares seguros para transacciones iniciadas por agentes, como Mastercard Agent Pay y FIS Agentic Payments[cite: 25]. [cite_start]Además, en marzo de 2026, Delhi anunció un piloto de servicios con chatbot, Flows y pagos UPI, validando la viabilidad del flujo "trámite + pago + tracking"[cite: 24].

## 4. Diseño y "Guardrails": Decisiones Acertadas
Las restricciones de diseño planteadas son fundamentales para mitigar riesgos:
* [cite_start]**Regla de Uno (Rule of One):** Centrar el MVP en un solo tipo de producto o servicio (ej. reposición de los 20 artículos más comprados) asegura un alcance manejable y efectivo[cite: 14, 15].
* [cite_start]**Foco transaccional:** Ante la política de WhatsApp 2026 de no permitir asistentes generales, el bot debe ser claramente comercial o transaccional[cite: 22].
* [cite_start]**Mitigación de alucinaciones:** Para evitar errores en los pedidos, implementar el "Confirm-Before-Pay" como un resumen de orden obligatorio antes de ejecutar el pago es un guardrail crítico e indispensable[cite: 18, 22].
* [cite_start]**Seguridad y escala:** Para evitar fraudes, se contemplan cuentas verificadas, OTP (si hay cuenta) y límites de monto; además, el agente declara su límite y escala a un humano ante la ausencia de inventario o postventa compleja[cite: 22].