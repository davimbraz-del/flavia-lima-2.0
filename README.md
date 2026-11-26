# Flavia Lima — Estética e Massoterapia

Landing page de uma página só, mobile-first, para a Flavia Lima (Recife – PE).
Objetivo: levar a visitante a chamar no WhatsApp para agendar uma avaliação.

Tudo está em `index.html` (HTML, CSS e JS no mesmo arquivo, sem build). Basta hospedar o arquivo
em qualquer serviço de site estático (GitHub Pages, Netlify, Vercel, Hostinger etc.).

## Antes de publicar

1. **Rastreamento:** no script do final do `index.html`, troque em `TRACKING` o ID do GA4 (`G-XXXXXXXXXX`)
   e o ID do Pixel da Meta. Enquanto estiverem com o valor de exemplo, nada é carregado.
2. **Fotos:** troque cada `<figure class="ph-img">` por uma `<img>` real (há um exemplo comentado no arquivo).
   Todas com `loading="lazy"`, exceto a foto do topo (`fetchpriority="high"`).
3. **Textos entre [colchetes]** (destacados em rosé na página): endereço, CEP, horários, anos de experiência,
   duração da sessão, valores, formas de pagamento, CNPJ e taxa de deslocamento. Também no JSON-LD do `<head>`.
4. **Método Cuidado Integral:** nome provisório, confirmar com a Flavia.
5. **Depoimentos e antes/depois:** somente reais, com autorização por escrito das clientes.
6. **Mapa:** substituir o `src` do iframe pelo código de incorporação do Google Maps do endereço real.
7. **Domínio:** trocar `SEU-DOMINIO.com.br` no canonical, nas tags Open Graph e no JSON-LD.
8. **Política de privacidade:** revisar o texto da janela com a Flavia.

## Eventos de clique no WhatsApp

Cada botão tem `data-tema` (`pele`, `dor`, `relaxamento` ou `geral`), `data-origem` (seção) e `data-servico`.

- **GA4:** `clique_whatsapp` (com tema, origem e serviço) e um evento por tema: `whatsapp_pele`,
  `whatsapp_dor`, `whatsapp_relaxamento`, `whatsapp_geral`.
- **Meta Pixel:** `Contact` e um evento personalizado por tema (`WhatsApp_Pele`, `WhatsApp_Dor`...).

O GA4 e o Pixel só carregam depois que a visitante aceita os cookies (LGPD).
