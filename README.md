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


## NEX Growth Scan

A ferramenta está em `dist/growth-scan.html`. Ela tem oito perguntas distribuídas entre marca, comercial, operação e experiência. O resultado organiza as respostas, sugere verificações concretas e pode ser copiado ou salvo pelo navegador. Não calcula um diagnóstico nem inventa uma nota.

A entrega é feita manualmente **após a reunião**, junto com o segundo e-book aprovado pela NEX. Não há link de acesso na landing nem envio automático do e-book. É possível acrescentar `?ref=CODIGO` ao link para incluir uma referência manual de atendimento no resumo copiado. Nome, empresa e respostas ficam apenas na sessão da página; ainda não existe persistência, autenticação por lead ou integração com CRM. Não use o código da URL como controle de acesso. A rota pede `noindex`, mas isso também não a protege de acesso direto se a hospedagem se tornar pública.
