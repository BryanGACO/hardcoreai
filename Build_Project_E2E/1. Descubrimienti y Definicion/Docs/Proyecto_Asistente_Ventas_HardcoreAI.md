# Producto 1 — Agente de Compras en WhatsApp
**Industria:** Agentic Commerce

---

## Qué construyes
Un agente conversacional en WhatsApp que acompaña al cliente desde la intención de compra hasta el pago, de forma autónoma y con confirmación explícita del usuario. El agente entiende qué quiere el cliente, arma el carrito, propone precio y entrega, y cierra la venta en 1–2 interacciones.

**Propuesta de valor central:** convertir conversaciones en ventas repetibles, sin fricción de app, sin formularios, sin login.

---

## Por qué este producto importa ahora
El comercio conversacional en WhatsApp está dejando de ser un experimento para convertirse en un canal de ventas principal en Latinoamérica:

- **Walmart Chile** reportó que sus campañas por WhatsApp con carritos pre-llenados (basados en historial de compras) ya explican ~20% de su e-commerce local.
- **Magalu (Brasil)** lanzó “Lu’s WhatsApp” para completar todo el flujo E2E — recomendación, pago y postventa — dentro del chat, proyectando alcanzar 30M+ de clientes.
- **39%** de retailers en Brasil ya realizan pedidos con proveedores por canales como WhatsApp (Yalo, 2024), con sugerencias automáticas de reposición.

Desde enero 2026, **WhatsApp Business Platform sí permite bots orientados a negocio** (ventas, soporte, reservas). El producto que construirás cae exactamente en esta categoría permitida.

---

## Qué construyes en el MVP (Rule of One)
El MVP se centra en **un solo tipo de producto o servicio** — por ejemplo, reposición de los 20 artículos más comprados, compra de entradas, o reserva + prepago.

Los componentes clave que implementarás:

- **WhatsApp Flows** para capturar datos estructurados (cantidad, dirección, fecha)
- **Chat conversacional** para capturar intención y responder preguntas
- **Payment link** (Stripe / Mercado Pago / Webpay) + confirmación por webhook
- **Confirm-Before-Pay:** resumen de orden obligatorio antes de ejecutar el pago

---

## Restricciones de diseño (críticas)

| Restricción | Cómo la manejas |
|---|---|
| Política WhatsApp 2026 (no asistentes generales) | El bot debe ser claramente comercial/transaccional |
| Riesgo de error en pedido (alucinación) | Guardrail obligatorio: Confirm-Before-Pay + resumen |
| Fraude y suplantación | Cuenta verificada, OTP si hay cuenta, límites de monto |
| Inventario y postventa ausentes | El agente declara límite y escala a humano |

---

## Señal de mercado (2026)
Delhi anunció en marzo 2026 un piloto de servicios gubernamentales con chatbot + Flows + pagos UPI dentro de WhatsApp, validando la viabilidad de “trámite + pago + tracking” en el canal. Visa y Mastercard impulsan pagos “agentic” con estándares seguros para transacciones iniciadas por agentes (Mastercard Agent Pay, FIS Agentic Payments).
