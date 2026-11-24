# SEM LEGENDA — site

## O que tem nesta pasta

- `index.html`: o site inteiro (layout, textos permanentes, animações e formulário)
- `edicao.js`: **os dados da edição** (data, horário, local, endereço, preços, status das inscrições). É o único arquivo que você precisa mexer a cada novo workshop.
- `assets/`: logo, foto do Bruno, ícone, imagem de compartilhamento (`og.jpg`) e as fontes do site.

## Como atualizar para uma nova edição

1. Abra `edicao.js` em qualquer editor de texto (Bloco de Notas, VS Code).
2. Troque os valores: `event_date`, horários, `event_address`, preços etc. As instruções estão no topo do arquivo.
3. Salve e suba **só esse arquivo** de novo na hospedagem.

Exemplos:
- Abrir uma edição nova: troque a data e deixe `registration_status: "open"`.
- Fechar as inscrições: `registration_status: "closed"`. Os botões viram "Avise-me da próxima" e o formulário passa a gerar uma mensagem de lista de espera.
- Tirar a promoção: `promotion_active: false`.
- Usar Sympla ou outro link de pagamento: coloque o link em `registration_link`.
- Colocar um vídeo: cole o link do YouTube em `event_video_url`.

## Como colocar no ar em semlegendateacherbruno.com.br

Qualquer hospedagem de site estático serve. Algumas opções:

- **Hostinger, Locaweb, HostGator** (se o domínio já está lá): no Gerenciador de Arquivos, envie todo o conteúdo desta pasta para `public_html`.
- **Netlify** (gratuito): arraste a pasta para app.netlify.com/drop e depois conecte o domínio em "Domain settings".
- **Vercel ou Cloudflare Pages** (gratuitos): mesma ideia, envie a pasta e aponte o domínio.

## Observações

- O formulário não guarda dados em servidor: ele monta a mensagem e abre o WhatsApp do Bruno (+55 87 99186-3260) já preenchido. A vaga só é confirmada no atendimento.
- O endereço exato ainda está como "enviado na confirmação pelo WhatsApp". Quando tiver, troque `event_address` em `edicao.js`.
- Para testar no computador antes de subir, abra `index.html` direto no navegador.
