# CNX CONCEITO 171

Loja digital dark, inspirada na arte enviada, com catálogo de arquivos, painel administrativo e Mercado Pago Checkout Pro.

## Rodar
1. Instale Node.js 20+.
2. `npm install`
3. Copie `.env.example` para `.env`.
4. Defina `MP_ACCESS_TOKEN`, `SITE_URL`, `ADMIN_USER` e `ADMIN_PASSWORD`.
5. `npm start`
6. Acesse `http://localhost:3000` e `/admin.html`.

## Mercado Pago
O projeto cria uma Preference no backend e redireciona para o Checkout Pro. Após a aprovação, o webhook/consulta de pagamentos libera o download. Para produção, `SITE_URL` precisa ser uma URL HTTPS pública para que as notificações funcionem corretamente.

## Uploads
O painel aceita PDF, APK, ZIP/RAR/7Z e alguns formatos de mídia/documento. O limite padrão é 500 MB e pode ser alterado por `MAX_UPLOAD_MB`.

## Produção
Use HTTPS, senha de admin forte, armazenamento de arquivos dedicado/S3 e backup do `data/db.json`. Não coloque o Access Token do Mercado Pago no frontend.
