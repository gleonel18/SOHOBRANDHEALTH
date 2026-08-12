# Pasta de vídeos — Reels ("Vídeo em movimento")

Coloque aqui os 4 vídeos verticais (9:16) da seção **Vídeo em movimento**.

## Nomes exatos dos arquivos (obrigatório)

| Arquivo         | Reel na página        |
|-----------------|-----------------------|
| `reel1.mp4`     | Apresentação          |
| `reel2.mp4`     | Na clínica            |
| `reel3.mp4`     | Depoimento em vídeo   |
| `reel4.mp4`     | Consultório           |

Opcional — pôster/thumbnail de cada vídeo (mostrado antes de tocar):
`reel1.jpg`, `reel2.jpg`, `reel3.jpg`, `reel4.jpg`

## Requisitos técnicos
- Formato: **MP4 (H.264 + AAC)** — melhor compatibilidade em iOS/Android/desktop.
- Proporção: **9:16 vertical** (ex.: 1080×1920).
- Os vídeos tocam automaticamente **mudos** em loop ao entrar na tela; ao clicar, ativam o som.
- Mantenha cada arquivo leve (idealmente < 8–10 MB) para carregar rápido.

## Duas formas de hospedar os vídeos

### 1) Junto com o site (nesta pasta) — mais simples
Basta soltar `reel1.mp4`…`reel4.mp4` aqui. O site já aponta para `./videos/reelN.mp4`.
Funciona direto no Cloudflare Pages, sem configuração extra.

### 2) Hospedados em outro lugar (CDN, Cloudflare R2/Stream) — recomendado p/ vídeos grandes
Não coloque os vídeos aqui. Em vez disso, defina a URL-base no `index.html`:

```html
<body data-video-base="https://cdn.seudominio.com/videos/">
```

O site vai buscar `https://cdn.seudominio.com/videos/reel1.mp4` etc. automaticamente.
Deixe `data-video-base=""` (vazio) para usar esta pasta local.
