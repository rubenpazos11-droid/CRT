# CRT‑Q — Paquete Render con Telegram incluido

## Pasos rápidos
1) Sube esto a GitHub (privado)
2) Crea PostgreSQL en Render y ejecuta `db/schema.sql`
3) Render → New → Blueprint → Deploy
4) En `crtq-api` añade:
   - DATABASE_URL (de tu Postgres)
   - INGEST_SHARED_KEY (secreto fuerte)
   - CRTQ_CORS (dominio del frontend)
   - TELEGRAM_BOT_TOKEN (ya puesto)
   - TELEGRAM_CHAT_ID (tu número de @userinfobot)
5) Probar Telegram:
   curl -X POST https://<TU_API>.onrender.com/alerts/signal -H 'Content-Type: application/json' -d '{"text":"CRT-Q Telegram OK"}'
