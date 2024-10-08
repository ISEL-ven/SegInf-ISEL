# Segurança Informática - Inverno 2023/24

## Informações

### Docente

- João Pedro Vitorino 
  - [email isel](mailto:joao.vitorino@isel.pt)
  - [email solvit](mailto:joaovitorino@solvit.pt)

### Horário

- 2a-feira, 20:00-23:00: G.2.07 [T] / LS1 (G.0.13)[TP]
- 4a-feira, 18:30-20:00: G.2.07 [T]

### Horário de Apoio

- Presencial / Zoom, 6a-feira, 18:00-18:45
- Agendamento via e-mail
- Link [zoom](https://videoconf-colibri.zoom.us/j/92233712551?pwd=em9mbDl6aTJJWTFxRHdPeXFNWVJXZz09)
- Sala: Sala de reuniões da Solvit (E.0.2)

### Recursos Gerais

- [Turma](https://2324moodle.isel.pt/course/view.php?id=7509)
- [Meta-disciplina](https://2324moodle.isel.pt/course/view.php?id=7503)

### Repositório GitHub

- [SegInf-public](https://github.com/isel-deetc-computersecurity/seginf-public)

### Bibliografia

- [Golmmann, Dieter, Computer Security. 3rd edition, Willey, 2011](https://annas-archive.org/md5/690cde92880ff81a41d3e00b8c3bacbb)
- [Welianng, Du, Computer Security: A Hands-on Approach, 2nd edition, 2019](https://annas-archive.org/md5/ce3cda53cae54ef32e606075554d4683)

-----------------------------

## Programa

### Parte 1 - Esquemas e protocolos ciptográficos e métodos de gestão de chaves

- esquemas de cifra simétrica e assimétrica
- esquemas MAC e de assinatura digital
- protocolos de autenticação e estabelecimento de chaves
- ifraestruturas de chave pública

### Parte 2  

### Autenticação e autorização

- vulnerabilidades e ataques á informação de autenticação (e.g., *passwords*) e métodos de mitigação

### Modelos e mecanismos para controlo de acessos

- monitor de referência
- matriz de controlo de acessos
- listas de controlo de acessos e *"capabilities"*
- modelo RBAC (*Role Based Access Control*)

### Protocolos para gestão de identidade e autorização em aplicações Web

-----------------------------

## Matéria

### 1. Apresentação e Introdução

> Bibliografia <hr>
> - [01. Apresentação](https://2324moodle.isel.pt/mod/resource/view.php?id=143550)

- **Apresentação**
  - Visão geral
    - 1. Mecanismos e protocolos criptográficos
    - 2. Autenticação e controlo de acessos
    - 2 Trabalhos (40%) + 1 Teste final (60%)
    - Regras de avaliação
- **Introdução à Segurança Informática**
  - Propriedades (Confidencialidade, Integridade, Disponibilidade)
  - Ataques (passivos e ativos)
    - Repasse
      - [Unlocking Car Doors with HackRF Replay Atack](https://www.youtube.com/watch?v=CA3XnGyD-SQ&t=144s)
      - [Relay attack Solihull](https://www.youtube.com/watch?v=8pffcngJJq0&t=20s)
    - Análise de frequência
      - [Frequency Analysis](https://www.cryptool.org/en/cto/frequency-analysis)
- **Introdução à Criptografia**
  - Exemplos clássicos (Cifras de César e Viginière; Máquina Enigma)
    - César
      - [Caesar Cipher](https://en.wikipedia.org/wiki/Caesar_cipher)
    - Viginière
      - [wikipedia](https://en.wikipedia.org/wiki/Vigen%C3%A8re_cipher)
      - [cryptii](https://cryptii.com/pipes/vigenere-cipher)
    - Enigma
      - [wikipedia](https://en.wikipedia.org/wiki/Enigma_machine)
      - [How did the Enigma Machine work? - YouTube](https://www.youtube.com/watch?v=ybkkiGtJmkM)
      - [brilliant](https://brilliant.org/wiki/enigma-machine/)
      - [Cracking Enigma - YouTube](https://www.youtube.com/watch?v=RzWB5jL5RX0)
  - Protocolos, esquemas e primitivas
  - Criptografia Computacional

### 2. Criptografia Simétrica

> Bibliografia <hr> 
> - [02. Esquemas Simétricos](https://2324moodle.isel.pt/mod/resource/view.php?id=143552)
> - Gollmann, Dieter, Computer Security, 3ª edição, 
Wiley, 2011: Secções 14.5.1-2 / 14.3.3
> - Welianng, Du, Computer Security: A Hands-on 
Approach, 2ª edição, 2019: Secções 21.3-5 / 21.4.7, 21.7, 22.5
> - Newsletter: [Schneier](https://www.schneier.com/crypto-gram/)

- **Esquemas Simétricos**
  - Cifra simétrica
    - [Fernet](https://cryptography.io/en/latest/fernet/)
    - [NaCI](https://nacl.cr.yp.to/)
    - [Libsodium](https://doc.libsodium.org/)
    - [João Vitorino - littleCryptoFunTool](https://github.com/vitorinojp/littleCryptoFunTool)
- **Criptografia Simétrica**
  - DES. Princípio / Cifra de Feistel
    - [Data Encryption Standard](https://en.wikipedia.org/wiki/Data_Encryption_Standard)
    - [Feitel Cipher](https://en.wikipedia.org/wiki/Feistel_cipher)
  - Modos de Operação em Bloco
    - *Electronic-Codebook (ECB)*
    - *CipherBlock-chaining (CBC)*
  - Princípios sobre *Initialization Vectors (IV)*
  - Padding
    - Oracle Padding Attack
      - [Security Flaws Induced by CBC Padding](https://www.iacr.org/cryptodb/archive/2002/EUROCRYPT/2850/2850.pdf)
      - [Vulnerabilities in Sogou Keyboard Encryption](https://citizenlab.ca/2023/08/vulnerabilities-in-sogou-keyboard-encryption/)
  - Modos de operação em Fluxo (*Stream*)
    - *Cipher FeedBack (CFB)*
    - *Output FeedBack (OFB)*
    - *Counter (CTR)* 
- **Message Authenticartion Codes (MAC)**
  - Propriedades
  - *MAC-then-encrypt vs Encrypt-then-MAC vs MAC-and-encrypt*
    - [Authenticated Encryption: Relations amoung Notions and Analysis of the Generic Composition Paradigm](https://link.springer.com/content/pdf/10.1007/3-540-44448-3_41.pdf)
- **Modos de Cifra Autenticada**
  - *Galois Counter Mode (GCM)*

### 3. Funções Hash e Esquemas Assimétricos

> Bibliografia <hr> 
> - [03. Funções de Hash](https://2324moodle.isel.pt/mod/resource/view.php?id=145441)
> - [04. Esquemas Assimétricos](https://2324moodle.isel.pt/mod/resource/view.php?id=145975)
> - Gollmann, Dieter, Computer Security, 3ª edição, 
Wiley, 2011: Secções 14.3.3-4
> - Welianng, Du, Computer Security: A Hands-on 
Approach, 2ª edição, 2019: Secções 21.1-5, 22.7

- **Funções de Hash**
  - Propriedades, Resistência pré-imagem, segunda-imagem e colisão
  - Famílias SHA (Secure Hash Algorithms)
    - [wikipedia](https://en.wikipedia.org/wiki/Secure_Hash_Algorithms)
    - [youtube](https://www.youtube.com/watch?v=b4b8ktEV4Bg)
  - Aplicações e Exemplos
    - [paper - github](https://github.com/DP-3T/documents/blob/master/DP3T%20White%20Paper.pdf)
  - Esquemas HMAC
    - [wikipedia](https://en.wikipedia.org/wiki/HMAC)
    - [youtube](https://www.youtube.com/watch?v=wlSG3pEiQdc)
- **Introdução À Cifra Assimétrica**
- **RSA**
- **Esquema Híbrido**

### 4. Assinatura Digital e Certificados; JCA

> Bibliografia <hr> 
> - [04. Esquemas Assimétricos](https://2324moodle.isel.pt/mod/resource/view.php?id=145975)
> - [05. JCA](https://2324moodle.isel.pt/mod/resource/view.php?id=146946)
> - [06. Certificados](https://2324moodle.isel.pt/mod/resource/view.php?id=147411)

- **Assinatura Digital**
- **Introdução ao JCA**
  - [Documentação Oracle](https://docs.oracle.com/en/java/javase/11/security/java-cryptography-architecture-jca-reference-guide.html)
- **Ifraestrutura de chave pública**
  - [Internet X.509 Public Key Infrastructure Certificate and Certificate Revocation List (CRL) Profile](https://www.rfc-editor.org/rfc/rfc5280)

### 5. TLS

> Bibliografia <hr> 
> - [07. SSL-TLS](https://2324moodle.isel.pt/mod/resource/view.php?id=147727)
> - Gollmann, Dieter, Computer Security, 3ª edição, 
Wiley, 2011: Secções 16.5

- **Apoio ao trabalho**
  - [JWT Decoder, Verifier, Generator, Decryptor](https://dinochiesa.github.io/jwt/)
  - [RFC 7519 - JSON Web Token](https://datatracker.ietf.org/doc/html/rfc7519)

- **Introdução ao TLS**
  - [RFC 8446 - The Transport Layer Security (TLS) Protocol Version 1.3](https://datatracker.ietf.org/doc/html/rfc8446)
  - [Wireshark](https://www.wireshark.org)
  - [Let's Encrypt](https://letsencrypt.org)
- **Subprotocolos**
  - Record Protocol
  - Handshake Protocol
- **HTTPS**
  - [Fiddler](https://www.telerik.com/download/fiddler)
- **SecureSockets com JCA**
  - [Documentação Oracle](https://docs.oracle.com/en/java/javase/11/security/java-cryptography-architecture-jca-reference-guide.html)

### 6. Autenticação

> Bibliografia <hr> 
> - [08. Autenticação](https://2324moodle.isel.pt/mod/resource/view.php?id=149500)
> - [09. Autenticação em aplicações Web](https://2324moodle.isel.pt/mod/resource/view.php?id=149700)

- **Autenticação em HTTP**
  - [tests httpauth](http://test.greenbytes.de/tech/tc/httpauth/)
- **JSON Web Tokens (JWT)**
  - [decode, verify and generate JWT](https://jwt.io/)

### 7. OpenID Connect / OAuth v2

> Bibliografia <hr>
> - [10. Intro Open ID Connect](https://2324moodle.isel.pt/mod/resource/view.php?id=149779)
> - [11. OAuth v2](https://2324moodle.isel.pt/mod/resource/view.php?id=150284)

- **OpenID Connect**
  - [OpenID Connect Playground](https://openidconnect.net/)
  - [Auth0](https://auth0.com/)
  - [OpenID JS code example](https://github.com/isel-deetc-computersecurity/seginf-public/blob/main/OIDC/relying-party-demo.js)
  - [OpenID JS code example 2](https://github.com/vitorinojp/oidc-webapp)
  - [SSL Client JAVA example](https://github.com/isel-deetc-computersecurity/seginf-public/blob/main/JCA/SSLClient.java)
- **OAuth v2**
  - [RFC 6749 The OAuth 2.0 Authorization Framework](https://datatracker.ietf.org/doc/rfc6749/)
  - [Documentation](https://oauth.net/2/)
  - [OAuth 2.0 Playground](https://www.oauth.com/playground/)
  - [Common OAuth implementation issues](https://salt.security/blog/oh-auth-abusing-oauth-to-take-over-millions-of-accounts)
  - [Relying Party Demo - GitHub](https://salt.security/blog/oh-auth-abusing-oauth-to-take-over-millions-of-accounts)

### 8. Modelos e mecanismos para controlo de acessos

> Bibliografia <hr>
> - [Controlo de Acessos](https://2324moodle.isel.pt/mod/resource/view.php?id=150565)

- Generalidades
  - [Role-Based Access Control in Retrospect](https://ieeexplore.ieee.org/document/6133255)

- Casbin
  - [Casbin get-started](https://casbin.org/docs/get-started/)
  - [Casbin editor](https://casbin.org/editor/)
  - [Gestão dinâmica de regras com Casbin](https://casbin.org/docs/rbac-api)


