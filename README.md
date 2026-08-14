# Sorteio de Times — app standalone

Este é o mesmo app que você usa aqui no Claude, convertido para rodar
sozinho, fora da interface do Claude, direto no navegador do celular.

## O que mudou em relação à versão do Claude
- Os dados (elenco e histórico) agora são salvos com `localStorage`,
  no próprio navegador do aparelho — **não sincronizam** entre
  celular/computador nem com o Claude. Cada navegador/aparelho tem
  seu próprio elenco salvo.
- Precisa de internet na primeira vez que abrir (e sempre que abrir,
  a menos que você configure cache offline), porque React, ícones e
  fontes carregam de CDNs.

## Como colocar no ar (grátis, ~2 minutos)

### Opção A — Netlify Drop (mais simples)
1. Acesse **https://app.netlify.com/drop**
2. Arraste esta pasta inteira (`index.html`, `manifest.json`,
   `icon-192.png`, `icon-512.png`) para a página
3. Pronto — você recebe um link tipo `https://algum-nome.netlify.app`
4. Abra esse link no celular

### Opção B — GitHub Pages
1. Crie um repositório novo no GitHub
2. Suba os 4 arquivos desta pasta para a raiz do repositório
3. Vá em **Settings → Pages**, escolha a branch `main` e salve
4. Em alguns minutos o app fica em
   `https://seu-usuario.github.io/nome-do-repo/`

### Opção C — Vercel
1. Acesse **https://vercel.com/new**
2. Faça upload da pasta (ou conecte um repositório com esses arquivos)
3. Deploy — você recebe um link `https://seu-projeto.vercel.app`

## Instalar na tela inicial do celular
Depois de abrir o link no navegador do celular:

**Android (Chrome):** menu (⋮) → "Adicionar à tela inicial" /
"Instalar aplicativo"

**iPhone (Safari):** botão de compartilhar (□↑) → "Adicionar à Tela
de Início"

O app abre em tela cheia, com ícone próprio, como se fosse nativo.

## Arquivos desta pasta
- `index.html` — o app inteiro (interface + lógica)
- `manifest.json` — metadados para instalação como PWA
- `icon-192.png` / `icon-512.png` — ícone do app
