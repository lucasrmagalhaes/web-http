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

**Sessão HTTP**
- É o tempo que o cliente utiliza um web app.
- Uma sessão HTTP nada mais é que um tempo que o cliente permanece ativo no sistema! Isso é parecido com uma sessão no cinema. Uma sessão, nesse contexto, é o tempo que o cliente usa a sala no cinema para assistir a um filme. Quando você sai da sala, termina a sessão. Ou seja, quando você se desloga, a Alura termina a sua sessão.

Uma comunicação com HTTP sempre é iniciada pelo cliente que manda uma requisição ao servidor esperando por uma resposta.

* [Status Code](https://www.w3schools.com/tags/ref_httpmessages.asp)
* [HTTP STATUS DOGS](https://httpstatusdogs.com/)
* [HTTP Cats](https://http.cat/)
* [HTTP Status Codes Glossary](https://www.webfx.com/web-development/glossary/http-status-codes/)

```
200, 203, 207 -> Respostas de Sucesso
300, 301, 302 -> Mensagem de redirecionamento
401, 404, 405 -> Respostas de erro do cliente
500, 502, 503 -> Respostas de erro do servidor
```

**Sobre o HTTP**
- Requisições HTTP podem ser enviadas através de qualquer aplicativo/software que entenda o protocolo.
- HTTP é totalmente independente do formato dos dados.
- HTTP pode trafegar tanto dados binários quanto dados textuais.

**Sobre o formato**
- Pelo cabeçalho Accept.

```
Accept: text/html, Accept: text/css, Accept: application/xml, Accept: application/json, Accept:image/jpeg e Accept: image/*
```

```
Accept: */*
```

**REST (Representational State Transfer - Transferência de Estado Representacional)**
- É um padrão arquitetural para comunicações entre aplicações
- Aproveita da estrutura que o HTTP proporciona
- Recursos são definidos via URI
- Operações com os métodos do HTTP (GET/POST/PUT/DELETE)
- Cabeçalhos (Accept/Content-Type) para especificar a representação (JSON, XML, ...) 

![REST](https://s3.amazonaws.com/caelum-online-public/http/images/08/imagem2-cap8-rest-http.png)

[MIME types](https://developer.mozilla.org/en-US/docs/Web/HTTP/Basics_of_HTTP/MIME_types)

**HTTP2 - Dados binários, GZIP ativo e TLS**
```
curl -v google.com.br
```

![CURL - divisão](https://s3.amazonaws.com/caelum-online-public/http/images/08/curl.png)

![GZIP](https://s3.amazonaws.com/caelum-online-public/http/images/08/gzip.png)

![Binário](https://s3.amazonaws.com/caelum-online-public/http/images/08/binario.png)

![HPACK](https://s3.amazonaws.com/caelum-online-public/http/images/08/hpack.png)

![TLS](https://s3.amazonaws.com/caelum-online-public/http/images/08/tls.png)

**Motivos por trás do HTTP/2**
- Com o crescimento do número de dispositivos móveis conectados a Web, é cada vez mais importante que a quantidade de dados trafegada seja a menor possível, afinal este tipo de dispositivo não costuma ter uma conexão com muita banda larga. O protocolo HTTP/2 traz diversas tecnologias para diminuir o tamanho das requisições.
- Por padrão, no protocolo HTTP versão 1.1 não é necessário o uso da camada de segurança TSL/SSL. Como hoje em dia trafegamos muitos dados críticos na Web, como senhas, logins e dados bancários, um protocolo atualizado que faz uso dessa segurança parece quase uma necessidade.

**Para que serve a tecnologia HPACK implementada no protocolo HTTP/2 ?**
- Para comprimir os Headers da comunicação HTTP, deixando-os mais leves.

**Selecione as afirmativas verdadeiras sobre as versões 1.1 e 2.0 do protocolo HTTP:**
- No HTTP/1.1 o Gzip não é nativo do protocolo, no HTTP/2 ele já vem por padrão.
- No HTTP/2 o uso do HTTPS é obrigatório, no HTTP/1.1 não.
- No HTTP/2 os dados são trafegados em binário, no HTTP/1.1 eles são trafegados como texto.
