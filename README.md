# Blueprint NEX — landing page

Landing page estática e questionário de 12 perguntas para solicitar uma reunião da NEX.

## Estrutura

- `dist/index.html`: landing page
- `dist/agendar.html`: questionário e solicitação de horário
- `dist/assets/`: CSS, JavaScript e imagens, incluindo a logo oficial fornecida pela NEX

## Rodar localmente

```bash
python3 -m http.server 8000 --directory dist
```

Abra `http://localhost:8000`.

## Configuração antes de divulgar

Em `dist/agendar.html`, adicione antes de `assets/booking.js`:

```html
<script>window.NEX_WHATSAPP_NUMBER = '5511999999999';</script>
```

Use o número oficial em formato internacional, apenas dígitos. Sem ele, o WhatsApp abre a mensagem preparada e pede ao visitante que escolha o contato da NEX. A data e o horário são apenas preferências; a confirmação é feita na conversa.

O primeiro e-book é prometido após a confirmação da reunião. O segundo e-book e o Growth Scan ficam para depois da participação na reunião. O envio desses materiais ainda depende da operação comercial da NEX.

A publicação feita pelo Sites tem controle de acesso próprio. Este repositório público não altera automaticamente o acesso da landing hospedada.
