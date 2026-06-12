# Painel de Criativos — Google & Meta

Dashboard estático (HTML único, sem build) com análise de criativos, ROAS, CPL,
públicos, combinações e simulador de projeção. Os dados já estão embutidos no
`index.html`. A única dependência externa é a biblioteca de gráficos (Chart.js),
carregada via CDN — por isso o navegador precisa de internet ao abrir.

## Arquivos
- `index.html` — o dashboard completo (abra direto no navegador para testar).
- `vercel.json` — configuração mínima (opcional; a Vercel também serve sem ele).
- `README.md` — este arquivo.

## Publicar na Vercel via GitHub

1. Crie um repositório novo no GitHub (ex.: `painel-criativos`).
2. Suba estes arquivos na raiz do repositório:
   ```
   git init
   git add index.html vercel.json README.md
   git commit -m "Dashboard de criativos Google e Meta"
   git branch -M main
   git remote add origin https://github.com/SEU-USUARIO/painel-criativos.git
   git push -u origin main
   ```
3. Em https://vercel.com → "Add New… → Project" → importe o repositório.
4. Em "Framework Preset" selecione **Other** (é site estático, sem build).
   Deixe "Build Command" e "Output Directory" em branco.
5. Clique em **Deploy**. Em segundos a Vercel gera a URL pública.

## Alternativa sem GitHub (mais rápido)
- Instale o CLI: `npm i -g vercel`
- Na pasta com o `index.html`, rode `vercel` e siga as instruções.
- Ou, no site da Vercel, arraste a pasta na opção de deploy manual.

## Atualizar os dados depois
O `index.html` contém os dados em um bloco `const DATA = {...}` no início do
`<script>`. Para atualizar com novos números, basta substituir esse objeto e
fazer um novo commit/deploy.
