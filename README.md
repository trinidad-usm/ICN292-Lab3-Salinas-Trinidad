# ICN292 - Laboratorio 3 - Automatización con n8n

**Nombre:** Trinidad Salinas

**S (semilla personal):** 964

**Fecha de entrega:** 21 de Septiembre 2026

## Contenido de este repositorio
- `ICN292-Lab3-Salinas-Trinidad.pdf` — Informe completo
- `ICN292-Lab3-Salinas-Trinidad.docx` — Informe en Word
- `ICN292-Lab3-Salinas-Trinidad-triage.json` — Workflow de triage (Parte A)
- `ICN292-Lab3-Salinas-Trinidad-emisor.json` — Workflow emisor de pruebas
- `ICN292-Lab3-Salinas-Trinidad-resumen.json` — Workflow de resumen diario (Parte B)

## Cómo reproducir
1. Importar cada archivo `.json` en una instancia de n8n (menú del workflow → Import from File).
2. El workflow de triage expone un Webhook; su URL se genera al activarlo en la instancia donde se importe.
3. El workflow emisor envía las 15 solicitudes de prueba al webhook del triage (ajustar la URL de destino dentro del nodo HTTP Request tras importar).
4. El workflow de resumen requiere que exista una Data Table llamada `registro_solicitudes` con las columnas: identificador, sku, monto, ruta, motivo, U_aplicado, D_aplicado.
