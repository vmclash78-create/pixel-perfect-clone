# Pixel Perfect Clone

Quero implementar este projeto com 100% de fidelidade visual, estrutural e funcional (cópia exata, pixel-perfect).

URL original: https://landonorris.com/
Domínio de origem: landonorris.com
Bibliotecas detectadas no original: Tailwind CSS, Bootstrap

O ZIP anexado contém a pasta `site/` = espelho dos arquivos ORIGINAIS do site (HTML cru, JS compilado, CSS, fontes, imagens, vídeos, modelos 3D), com a mesma estrutura de pastas do servidor de origem. Ele também tem o RELATORIO-DE-CAPTURA.md (o que foi baixado e o que falhou) e um screenshot de referência.

### REGRAS FUNDAMENTAIS DE EXECUÇÃO

1. NÃO REESCREVA DO ZERO
- Não reconstrua as telas em componentes React/Tailwind simplificados, e não "converta" o site para outro framework.
- Sirva os arquivos de `site/` como estão (.html, .js, .css, libs de animação). Só edite o que for estritamente necessário (links, caminhos quebrados).
- Preserve exatamente: WebGL/Three.js, GSAP/ScrollTrigger, Lenis/Locomotive, Lottie, animações e transições CSS.

2. ONDE COLOCAR / COMO RODAR
- A raiz do servidor tem que ser a pasta `site/`, porque os caminhos dos arquivos são absolutos (ex.: `/assets/app.js`).
- Teste local: `npx serve site` ou `python -m http.server 8080 -d site` e abra http://localhost:8080. NÃO abra o .html com duplo clique (file://): módulos ES, fetch e WebGL quebram.
- Hospedagem estática (Vercel, Netlify, Cloudflare Pages, Nginx): publique o CONTEÚDO de `site/` na raiz do domínio, sem build.
- Se você usa Lovable/Bolt/v0: coloque a pasta em `public/` (ou como projeto estático) e sirva na raiz; não passe pelo bundler.

3. TRATAMENTO DE ASSETS E FONTES
- Se você TEM acesso a rede/terminal: leia o RELATORIO-DE-CAPTURA.md, baixe de landonorris.com tudo que estiver na lista "Não baixados" (mesmo caminho relativo dentro de `site/`) e confira que fontes (@font-face), texturas 3D, vídeos e imagens de fundo carregam sem 404.
- Se você NÃO TEM acesso a rede: liste exatamente quais arquivos/URLs o código ainda tenta chamar (rode grep por "http" nos .js/.css/.html) para eu baixar e te enviar, e diga em qual pasta cada um deve ficar.

4. LINKS E CHECKOUT
- Nenhum link de checkout/WhatsApp foi detectado automaticamente. Procure com grep por "checkout", "pay.", "wa.me", "whatsapp", "hotmart", "kiwify", "href=" nos arquivos e substitua [LINK_ANTIGO] por [MEU_LINK].

5. CHECKLIST QUE VOCÊ DEVE GARANTIR
- Nenhuma tag <script>/<link>/<img>/CSS url() com caminho quebrado ou absoluto apontando para localhost ou para landonorris.com (rode grep por "landonorris.com" e "localhost").
- O container do canvas 3D e os elementos com animação por scroll mantêm classes CSS e IDs originais intactos (não renomeie, não remova, não minifique de novo).
- Console do navegador sem erros 404 e sem erros de CORS; fontes carregando de arquivos locais.
- Trackers (Google Analytics, Meta Pixel, Hotjar...) foram removidos de propósito na captura; não os reinstale a menos que eu peça.
- No fim, me dê a instrução exata (comandos e pasta) liste qualquer arquivo que ainda esteja faltando.

This project was built with [Lovable](https://lovable.dev).

## Build with Lovable

Continue developing this project in the [Lovable editor](https://lovable.dev/projects/ee416f86-6307-4c14-a0e5-2f037b2dc742).

- **Ship faster**: describe what you want to build and Lovable handles the code.
- **Stay in sync**: every change made in Lovable is committed straight to this repository.
- **Full ownership**: this code is yours. Push to `main` on GitHub and your changes sync back into Lovable, ready for your next prompt.

## Development

Prefer working locally? You need Node.js and npm — [install with nvm](https://github.com/nvm-sh/nvm#installing-and-updating).

```sh
git clone <this-repository-url>
cd <repository-name>
npm i
npm run dev
```
