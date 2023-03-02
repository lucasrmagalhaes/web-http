### HTTP: Entendendo a web por baixo dos panos

**HTTPS**
- Web Segura
- Certificado Digital (identidade)
- Chaves (pública e privada)

**Descobrir o IP**
```
nslookup google.com
```

**O que é um domínio na Internet?**
- O domínio é o nome do site na Web. Ele facilita a navegação do usuário, que não precisa lembrar o IP de cada site.

**Como funciona o DNS?**
- O DNS tem como função realizar a tradução do nome de um domínio para o endereço de IP correspondente.

**Porta padrão HTTP**
- 80

**Endereços**
- URL são endereços da WEB
- Uma URL começa com o protocolo (http://) seguido pelo domínio (www.alura.com.br)
- Após o domínio é especificado o caminho para um recurso (course/introducao-html-css)
- Um recurso é algo conectado que queremos acessar

![URL](https://s3.amazonaws.com/caelum-online-public/http/http-url.png)

**smb**
- Server Message Block. Ele é utilizado para compartilhar arquivos dentro de uma rede local.

**HTTP (REQUEST-RESPONSE)**
- O protocolo HTTP segue o modelo REQUISIÇÃO-RESPOSTA
- Uma requisição precisa ter todas as informações para o servidor gerar a resposta
- HTTP é STATELESS! (Não mantém informações entre requisições)
- As plataformas de desenvolvimento usam sessões para guardar informações entre requisições

Uma requisição sempre deve ser enviada com todas as informações necessárias, o que faz uma requisição ser sempre independente das demais.
