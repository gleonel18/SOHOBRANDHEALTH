# Soho Brand Health — Site institucional

Site de página única (HTML/CSS/JS, sem build). Pronto para publicar no **Cloudflare Pages** a partir de um repositório GitHub.

## Estrutura
```
index.html        → o site (entrypoint)
support.js        → runtime necessário ao index.html (NÃO remover)
assets/           → imagens do site (fotos originais + otimizadas em assets/new/)
videos/           → coloque aqui reel1.mp4 … reel4.mp4 (ver videos/README.md)
```

## Publicar no Cloudflare Pages
1. Suba esta pasta inteira para um repositório no GitHub.
2. No painel Cloudflare → **Workers & Pages → Create → Pages → Connect to Git**.
3. Selecione o repositório.
4. Configuração de build:
   - **Framework preset:** `None`
   - **Build command:** *(deixe vazio)*
   - **Build output directory:** `/`  (a raiz, onde está o `index.html`)
5. **Save and Deploy**. O site sobe em minutos e ganha uma URL `*.pages.dev`.
6. (Opcional) Aponte seu domínio próprio em **Custom domains**.

## Vídeos (seção "Vídeo em movimento")
Veja **`videos/README.md`**. Resumo:
- **Opção A:** coloque `reel1.mp4`…`reel4.mp4` na pasta `videos/`.
- **Opção B:** hospede os vídeos em outro host/CDN e defina no `index.html`:
  ```html
  <body data-video-base="https://cdn.seudominio.com/videos/">
  ```
Enquanto não houver vídeos, os quadros aparecem escuros (sem quebrar o layout).

## Editar textos, links e fotos
- **Textos:** edite diretamente no `index.html`.
- **Fotos:** substitua os arquivos em `assets/` (ou troque o `src` no `index.html`). No próprio site há o botão "Trocar foto" ao passar o mouse (troca só na visualização local).
- **WhatsApp / Instagram / cor de destaque / palavras do hero / URL-base de vídeo:** ajustáveis no topo do `index.html` (atributo `data-props`) ou pelo painel de edição.
