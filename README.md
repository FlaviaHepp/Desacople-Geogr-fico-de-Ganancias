# 🌍Desacople Geográfico de Ganancias

Este proyecto implementa una consulta SQL que identifica reacciones de pánico en mercados internacionales frente a reportes de ganancias positivas, revelando desacoples geográficos entre fundamentos corporativos y percepción de riesgo local.

La señal apunta a detectar situaciones donde el mercado no castiga a la empresa, sino al contexto.

## 💡Idea central

Cuando una empresa reporta ganancias positivas en su mercado base (por ejemplo, EE.UU.), se espera una reacción neutral o positiva.

Este proyecto busca los casos en los que ocurre lo contrario:
- El evento es positivo, pero el mercado local (Europa, Asia, etc.) entra en modo sell-off técnico.

Esto suele indicar:
- riesgo macro regional
- estrés cambiario
- divergencias en política monetaria
- flujos internacionales desalineados

## 📊Valor de negocio

- Detecta ineficiencias geográficas

Útil para:
- estrategias cross-listing
- arbitraje geográfico
- análisis macro-fundamental cuantitativo
- Ayuda a separar riesgo empresa vs. riesgo país

## 🗄️Estructura de datos esperada

- eventos_corporativos
- campo	descripción
- ticker_id	Identificador del activo
- fecha	Fecha del evento
- tipo_evento	Tipo de evento (ej. Ganancias)
- tickers
- campo	descripción
- ticker_id	Identificador del activo
- bolsa_mercado	Mercado / bolsa de cotización
- precios_diarios
- campo	descripción
- ticker_id	Identificador del activo
- fecha	Fecha
- close	Precio de cierre
- indicadores_tecnicos
- campo	descripción
- ticker_id	Identificador del activo
- fecha	Fecha
- rsi_14	RSI de 14 períodos

## ⚙️Lógica de la consulta

La query identifica activos que cumplen:
- Reporte de Ganancias
- Cotización en un mercado distinto al mercado base (USA)
- RSI < 30, indicando pánico técnico

Coincidencia temporal entre:
- evento corporativo
- precio
- indicadores técnicos

## 🔎Interpretación de resultados

- Señal contrarian geográfica

El mercado castiga:
- al país
- a la moneda
- al régimen macro
- No necesariamente a la empresa

Puede ser una oportunidad si:
- el estrés es transitorio
- los fundamentales globales se mantienen sólidos

## 🚀Posibles extensiones

- Comparar reacción USA vs mercado extranjero
- Ajustar por tipo de cambio
- Incorporar CDS o spreads soberanos
- Backtesting por región

## 📝Notas finales

- No es señal de entrada inmediata
- Funciona mejor en empresas multi-listadas
- Ideal como módulo dentro de un sistema macro-cuantitativo

## 👤Autora
Flavia Hepp Proyecto de SQL aplicó un análisis de riesgo basado en eventos.

***
📊 La empresa reporta buenos resultados…
pero en otro país, el mercado vende.

¿Error? ¿Ruido?
No necesariamente.

---

Hay un fenómeno poco discutido:

👉 El mismo evento (earnings positivos) puede generar reacciones opuestas según el mercado.

---

🔍 Lo que analicé:

Casos donde:

* 📈 La empresa reporta **ganancias**
* 🌍 Pero en mercados fuera de su país base
* 📉 Se observa un **sell-off fuerte (RSI < 30)**

---

💡 ¿Por qué pasa esto?

Algunas posibles razones:

* Riesgo cambiario
* Contexto macroeconómico local
* Diferente percepción de riesgo
* Flujos de capital regionales

👉 El mercado no interpreta la noticia en el vacío.

---

🧠 Insight clave:

La información es global…
pero su interpretación es local.

---

📉 Lo más interesante:

Mientras en un mercado el evento puede ser:

* Señal de crecimiento 📈

En otro puede ser visto como:

* Riesgo o sobrevaluación 📉

---

🚀 Aplicaciones:

* Estrategias long/short entre mercados
* Detección de divergencias geográficas
* Arbitraje de percepción de riesgo
* Features para modelos multi-mercado

---

🧠 Takeaway:

No alcanza con analizar la noticia…

👉 hay que entender *cómo la interpreta cada mercado*

---

Estoy explorando insights combinando SQL + análisis cuantitativo para detectar este tipo de anomalías globales.

Si te interesa este enfoque, conversemos 👇

#DataScience #Quant #Finance #Trading #MachineLearning #SQL #Investing

