# Desacople-Geogr-fico-de-Ganancias
Desacople Geográfico de Ganancias

Desacople Geográfico de Ganancias

Este proyecto implementa una consulta SQL que identifica reacciones de pánico en mercados internacionales frente a reportes de ganancias positivas, revelando desacoples geográficos entre fundamentos corporativos y percepción de riesgo local.

La señal apunta a detectar situaciones donde el mercado no castiga a la empresa, sino al contexto.

🌍 Idea central

Cuando una empresa reporta ganancias positivas en su mercado base (por ejemplo, EE.UU.), se espera una reacción neutral o positiva.

Este proyecto busca los casos en los que ocurre lo contrario:

El evento es positivo, pero el mercado local (Europa, Asia, etc.) entra en modo sell-off técnico.

Esto suele indicar:

riesgo macro regional

estrés cambiario

divergencias en política monetaria

flujos internacionales desalineados

📊 Valor de negocio

Detecta ineficiencias geográficas

Útil para:

estrategias cross-listing

arbitraje geográfico

análisis macro-fundamental cuantitativo

Ayuda a separar riesgo empresa vs. riesgo país

🗄️ Estructura de datos esperada
eventos_corporativos
campo	descripción
ticker_id	Identificador del activo
fecha	Fecha del evento
tipo_evento	Tipo de evento (ej. Ganancias)
tickers
campo	descripción
ticker_id	Identificador del activo
bolsa_mercado	Mercado / bolsa de cotización
precios_diarios
campo	descripción
ticker_id	Identificador del activo
fecha	Fecha
close	Precio de cierre
indicadores_tecnicos
campo	descripción
ticker_id	Identificador del activo
fecha	Fecha
rsi_14	RSI de 14 períodos
⚙️ Lógica de la consulta

La query identifica activos que cumplen:

Reporte de Ganancias

Cotización en un mercado distinto al mercado base (USA)

RSI < 30, indicando pánico técnico

Coincidencia temporal entre:

evento corporativo

precio

indicadores técnicos

🔎 Interpretación de resultados

Señal contrarian geográfica

El mercado castiga:

al país

a la moneda

al régimen macro

No necesariamente a la empresa

Puede ser una oportunidad si:

el estrés es transitorio

los fundamentales globales se mantienen sólidos

🚀 Posibles extensiones

Comparar reacción USA vs mercado extranjero

Ajustar por tipo de cambio

Incorporar CDS o spreads soberanos

Backtesting por región

📝 Notas finales

No es señal de entrada inmediata

Funciona mejor en empresas multi-listadas

Ideal como módulo dentro de un sistema macro-cuantitativo
