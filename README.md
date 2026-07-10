# Mickey Ever After — Link Page

Landing page estilo "linktree" da Mickey Ever After, servida em **links.mickeyeverafter.com.br** via Cloudflare Pages.

Página estática, sem build. Um único `index.html` + pasta `images/` (WebP otimizado).

## Editar os links

Todos os destinos ficam no topo do bloco `<script>` no `index.html`, no objeto `LINKS`.
Basta trocar a URL entre aspas e fazer commit — o Pages publica sozinho.

```js
const LINKS = {
  site:       "https://mickeyeverafter.com.br/",
  comunidade: "https://chat.whatsapp.com/...",   // Grupo VIP
  whatsapp:   "https://api.whatsapp.com/send/...", // Atendimento
  email:      "mailto:mickeyeverafter@gmail.com",
  instagram:  "https://www.instagram.com/mickeyeverafterstore",
  tiktok:     "https://www.tiktok.com/@mickeyeverafterstore",
  x:          "https://x.com/mickeyeverafter"
};
```

## Deploy (Cloudflare Pages via GitHub)

1. Suba esta pasta como repositório no GitHub.
2. Cloudflare Pages → **Create → Connect to Git** → selecione o repo.
3. Build settings: **Framework preset: None**, Build command: *(vazio)*, Output directory: `/`.
4. Após publicar, **Custom domains → Set up a domain** → `links.mickeyeverafter.com.br`.
5. DNS (Hostinger/Registro.br): crie um **CNAME** `links` apontando para o alvo `*.pages.dev` que o Cloudflare mostrar.

## Otimização de imagens

As imagens estão em WebP (qualidade 90, ~2x da resolução de exibição). Total ~0,56 MB.
