---
title: 'Aceder ao espaço de armazenamento do alojamento web'
slug: aceder-espaco-de-armazenamento-ftp-alojamento-web
excerpt: 'Saiba como aceder ao espaço de armazenamento do seu alojamento web da OVH'
section: 'FTP e SSH'
order: 1
---

**Última atualização: 09/04/2019**

## Sumário

Os planos de alojamento web da OVH dão-lhe acesso a um espaço de armazenamento que permite publicar ficheiros nos seus websites ou aplicações. O acesso a este espaço é possível através de um utilizador FTP ou SSH e das respetivas palavras-passe.

**Saiba como aceder ao espaço de armazenamento do seu alojamento web da OVH.**

## Requisitos

- Ter um serviço de [alojamento web da OVH](https://www.ovhcloud.com/pt/web-hosting/){.external}.
- Ter acesso à [Área de Cliente OVH](https://www.ovh.com/auth/?action=gotomanager&from=https://www.ovh.pt/&ovhSubsidiary=pt){.external}, na secção `Web Cloud`{.action}.

## Instruções

### 1 - Recuperar as informações de acesso

Para se ligar ao espaço de armazenamento, deve dispor dos seguintes elementos:

- um nome de utilizador FTP ou SSH ativo;
- a palavra-passe associada ao nome de utilizador FTP ou SSH;
- o endereço do servidor em questão;
- a porta de ligação ao servidor.

> [!primary]
>
> Estes elementos foram-lhe enviados por e-mail após a instalação do seu alojamento web e estão acessíveis através da Área de Cliente OVH.
>
> **Se já possuir estas informações**, passe diretamente para o passo “[2 - Aceder ao espaço de armazenamento](./#2-aceder-ao-espaco-de-armazenamento)”.
> 

Se não possuir estas informações, aceda à [Área de Cliente OVH](https://www.ovh.com/auth/?action=gotomanager&from=https://www.ovh.pt/&ovhSubsidiary=pt){.external}, na secção “Web”, e clique em `Alojamentos`{.action} na barra à esquerda. De seguida, selecione o nome do alojamento correspondente e aceda à janela `FTP - SSH`{.action}. 

Poderá ver as informações relativas ao seu espaço de armazenamento, assim como uma tabela com os utilizadores FTP e SSH criados no seu alojamento.

![ftpconnect](images/connect-ftp-step1.png){.thumbnail}

Graças a estas informações, terá a possibilidade de encontrar os elementos necessários para aceder ao seu espaço de armazenamento. Caso seja necessário, consulte a tabela abaixo para saber como identificá-los. Lembre-se de que algumas informações podem não aparecer, dependendo do plano de [alojamento web da OVH](https://www.ovhcloud.com/pt/web-hosting/){.external} que possuir.

|Informação|Descrição|
|---|---|
|Servidor FTP|Trata-se do endereço do servidor que permite aceder ao seu espaço de armazenamento. Utilize-o para aceder ao servidor através de um software FTP.<br><br> A porta clássica de acesso é a 21. Utilize a porta 22 para se ligar através do protocolo SFTP (caso este esteja ativo).|
|Acesso SSH ao cluster|Poderá consultar os seguintes dados: <br>**- o endereço do servidor**: começa depois de “ssh://” e acaba antes de “:”;<br> **- a porta de ligação**: o número é referido depois de “:”. <br><br>Por exemplo: em ssh://`ssh.cluster023.hosting.ovh.net`:`22`/, “ssh.cluster023.hosting.ovh.net” será o endereço do servidor e “22” a porta de ligação.|
|Login FTP principal|Trata-se do nome de utilizador FTP principal criado no seu alojamento. Pode consultar todos os utilizadores FTP do seu alojamento na coluna “Login FTP” da tabela.|
|Login SSH principal|Trata-se do nome de utilizador SSH principal criado no seu alojamento. Pode consultar todos os utilizadores SSH do seu alojamento na coluna “Login SSH” da tabela.|

Se não souber qual é a palavra-passe de um utilizador FTP ou SSH, pode, em função do seu alojamento, utilizar o ícone em forma de lápis ou o ícone `...`{.action} e selecionar a opção `Alterar palavra-passe`{.action}. Se precisar de ajuda no processo, consulte o nosso manual "[Alterar a palavra-passe de um utilizador FTP](../alterar-palavra-passe-utilizador-ftp/)".

![ftpconnect](images/connect-ftp-step2.png){.thumbnail}

Depois de completar estes passos, deverá ter à sua disposição os dados necessários para aceder ao espaço de armazenamento.

### 2 - Aceder ao espaço de armazenamento

A ligação ao espaço de armazenamento pode ser realizada de várias formas. Consulte este manual em função da operação que pretende realizar.

[1. Ligação através de FTP Explorer](./#1-ligacao-atraves-de-ftp-explorer): permite-lhe aceder ao espaço de armazenamento a partir do navegador.

[2. Ligação através de um software FTP](./#2-ligacao-atraves-de-um-software-ftp): permite-lhe aceder ao espaço de armazenamento através de um software (tal como FileZilla ou Cyberduck). Deverá instalar com antecedência o software no seu computador.

[3. Ligação através de um acesso SSH](./#3-ligacao-atraves-de-um-acesso-ssh): permite-lhe aceder ao espaço de armazenamento através de um acesso SSH. Tenha em atenção que este tipo de acesso requer conhecimentos técnicos avançados, bem como um plano de [alojamento web da OVH](https://www.ovhcloud.com/pt/web-hosting/){.external} específico.

#### 1. Ligação através de FTP Explorer

Aceda à [Área de Cliente OVH](https://www.ovh.com/auth/?action=gotomanager&from=https://www.ovh.pt/&ovhSubsidiary=pt){.external}, na secção “Web”, clique em `Alojamentos`{.action} na barra à esquerda e selecione o nome do alojamento correspondente. 

Aceda ao separador `FTP - SSH`{.action} e clique no botão `Explorador FTP`{.action}. 

![ftpconnect](images/connect-ftp-step3.png){.thumbnail}

Na nova janela que aparecer, indique o utilizador FTP e a respetiva palavra-passe. Se as informações estiverem corretas, poderá então interagir com o seu espaço de armazenamento.

![ftpconnect](images/connect-ftp-step4.png){.thumbnail}

#### 2. Ligação através de um software FTP

Depois de instalar o software FTP à sua escolha (FileZilla ou Cyberduck), inicie-o. 

Indique as credenciais de acesso quando forem solicitadas. Isto dependerá do tipo de software que utilizar e da sua versão, pelo que não podemos incluir todos os casos possíveis neste manual.

A seguir, apresentamos a informação que lhe será solicitada:

|Informação solicitada|Detalhes|
|---|---|
|Servidor FTP|Trata-se do endereço do servidor que lhe permite aceder ao seu espaço de armazenamento.<br><br> Em função do tipo de software, pode denominar-se “servidor”, “endereço de servidor”, “host”, “nome do host”, etc.|
|Login FTP|Trata-se do endereço do servidor que lhe permite aceder ao seu espaço de armazenamento.<br><br> Em função do tipo de software, pode denominar-se “utilizador”, “nome de utilizador”, “identificador”, “login” ou “username”.|
|Palavra-passe do utilizador FTP|Trata-se da palavra-passe associada ao login FTP.<br><br> Em função do tipo de software, pode denominar-se “palavra-passe” ou “password”.|
|Porta de ligação|Este campo é preenchido de forma automática pelo software. Se tiver de preencher alguma informação:<br><br>\- utilize a porta 21 para uma ligação através do protocolo FTP;<br>\- utilize a porta 22 para uma ligação através do protocolo SFTP (caso este esteja ativo).|

Se os dados indicados estiverem corretos, o software deverá mostrar o conteúdo do seu espaço de armazenamento. É possível que apareça uma mensagem (também chamado “status”) a confirmar que o software mostrou o conteúdo.

#### 3. Ligação através de um acesso SSH

Para estabelecer uma ligação em SSH, utilize um terminal para interagir diretamente com o espaço de armazenamento através de linhas de comando. 

Em macOS e Linux, esta ferramenta é instalada por predefinição. Num ambiente Windows, deverá instalar um programa como PuTTY ou adicionar a funcionalidade OpenSSH. Estas operações serão diferentes dependendo do sistema operativo que utilizar, pelo que não podemos incluir todos os casos possíveis neste manual.

Uma vez estabelecida a ligação SSH e em função do método selecionado, existem duas formas de se conectar: 

- através de um software: os campos de texto devem incluir a informação de ligação;
- através de uma linha de comandos: deverá respeitar uma sintaxe especifica.

Se se ligar através de uma linha de comandos, deverá: substituir os elementos “sshlogin”, “sshserver” e “connectionport” pela sua informação. Uma vez enviado o comando, deverá introduzir a palavra-passe do utilizador SSH.

```ssh
ssh sshlogin@sshserver -p connectionport
```

Se as informações estiverem corretas, poderá então interagir com o seu espaço de armazenamento. Para obter mais informações, consulte o nosso manual “[O SSH nos alojamentos partilhados](../partilhado_o_ssh_nos_alojamentos_partilhados/)”.

![ftpconnect](images/connect-ftp-step5.png){.thumbnail}

## Quer saber mais?

[Alterar a palavra-passe de um utilizador FTP](https://docs.ovh.com/pt/hosting/alterar-palavra-passe-utilizador-ftp/){.external}

[O SSH nos alojamentos partilhados](https://docs.ovh.com/pt/hosting/partilhado_o_ssh_nos_alojamentos_partilhados/){.external}

Fale com a nossa comunidade de utilizadores em <https://community.ovh.com/en/>