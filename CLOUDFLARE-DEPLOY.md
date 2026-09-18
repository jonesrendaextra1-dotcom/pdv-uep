# UEP Cafeteria — Deploy no Cloudflare Pages

## Via GitHub/GitLab

- Framework preset: Vite
- Build command: `npm run build`
- Build output directory: `dist`
- Node.js version: `22`

## Variáveis de ambiente

Se o sistema usar Supabase, cadastre no Cloudflare Pages as variáveis públicas exigidas pelo código, normalmente:

- `VITE_SUPABASE_URL`
- `VITE_SUPABASE_ANON_KEY`

Se houver uso da API Gemini no navegador, não coloque uma chave privada em código público. Prefira uma função/Worker no servidor.

## Deploy manual

No computador com Node.js 22 ou superior:

```bash
npm install
npm run build
```

Depois envie o conteúdo da pasta `dist` para o Cloudflare Pages.

O arquivo `_redirects` garante o fallback para `index.html` em aplicações SPA.
