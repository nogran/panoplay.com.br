# panoplay.com.br

Site estático do domínio `panoplay.com.br`, publicado pelo GitHub Pages.

`/callback` é a Redirect URI do app do Mercado Livre. O ML só aceita endereço HTTPS,
então esta página recebe `code` e `state` e os repassa na hora para o backend local
(`http://127.0.0.1:8765/api/mercadolivre/callback`), que troca o código pelos tokens.
A página não guarda nem envia nada a outro lugar. O código sozinho não dá acesso à conta:
vale uma vez, por poucos minutos, e só junto com o Client Secret, que fica no servidor local.
