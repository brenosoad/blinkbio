# PróLINK – plataforma de link na bio

- `index.html`: template único. `?c=<slug>` carrega `clients/<slug>/config.json`.
- `clients/<slug>/`: config e imagens de cada cliente.
- `painel/`: painel do criador (acesso com `ADMIN_KEY`).
- `api/track.js`, `api/stats.js`: contagem de cliques (Upstash Redis).

## Variáveis de ambiente (Vercel)
- `UPSTASH_REDIS_REST_URL` e `UPSTASH_REDIS_REST_TOKEN` (Marketplace → Upstash Redis, geradas sozinhas)
- `ADMIN_KEY` (sua chave do painel)

## Novo cliente
Copie `clients/sancaporai`, edite `config.json` e as imagens. Cada cliente usa `"analytics": "/api/track"`.

## Teste local
`npx vercel dev` (variáveis em `.env.local`).
