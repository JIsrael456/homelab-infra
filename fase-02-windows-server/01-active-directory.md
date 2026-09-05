# Active Directory

## Objetivo

Configurar o Active Directory Domain Services (AD DS) para centralizar a autenticação, o gerenciamento de usuários, computadores e recursos do ambiente de laboratório.

## Ambiente

- **Servidor:** SRVWIN
- **Domínio:** jtechlab.local
- **Endereço IP:** 192.168.10.10
- **Sistema:** Windows Server 2025
- **Virtualização:** VirtualBox

## O que é o Active Directory?

O Active Directory Domain Services (AD DS) é o serviço de diretório da Microsoft utilizado para centralizar o gerenciamento de identidades e recursos em ambientes Windows.

Por meio do Active Directory é possível administrar de forma centralizada:

- Usuários
- Computadores
- Grupos de segurança
- Organizational Units (OUs)
- Políticas de segurança
- Autenticação dos usuários
- Permissões de acesso

No laboratório, o Active Directory será utilizado como base para o gerenciamento centralizado da infraestrutura da JI Tech Solutions.

## Atividades realizadas

- Instalação da função Active Directory Domain Services (AD DS)
- Criação do domínio `jtechlab.local`
- Promoção do servidor SRVWIN a Controlador de Domínio
- Validação do domínio
- Abertura do Active Directory Users and Computers

## Como foi implementado

### 1. Instalação do AD DS

A função **Active Directory Domain Services** foi instalada por meio do **Server Manager**.

Caminho utilizado:

`Server Manager → Add Roles and Features → Active Directory Domain Services`

Após a instalação da função, o servidor passou a estar preparado para ser promovido a Controlador de Domínio.

### 2. Criação do domínio

Após a instalação do AD DS, foi realizada a promoção do servidor por meio da opção:

`Promote this server to a domain controller`

Foi selecionada a opção de criação de uma nova floresta e definido o domínio:

`jtechlab.local`

### 3. Promoção do servidor

O servidor `SRVWIN` foi promovido a **Domain Controller (DC)** do domínio `jtechlab.local`.

A partir desse momento, o servidor passou a fornecer os principais serviços necessários para o funcionamento do domínio, incluindo Active Directory e DNS.

### 4. Validação

Após a promoção, foi utilizado o **Active Directory Users and Computers** para verificar se o domínio estava disponível e se os objetos do Active Directory poderiam ser administrados.

O domínio `jtechlab.local` foi identificado corretamente no console administrativo.

## Resultado

O domínio `jtechlab.local` foi criado com sucesso e o servidor `SRVWIN` passou a atuar como Controlador de Domínio.

O ambiente passou a possuir uma estrutura centralizada para gerenciamento de identidades e computadores, servindo como base para as próximas configurações do laboratório.

## Conceitos aprendidos

- O Active Directory centraliza a autenticação e o gerenciamento de identidades.
- Um domínio permite administrar usuários e computadores de forma centralizada.
- O Domain Controller fornece os serviços centrais do domínio.
- O AD DS utiliza o DNS para localizar serviços e computadores dentro do domínio.
- Usuários e computadores podem ser organizados em Organizational Units (OUs).
- Grupos de segurança podem ser utilizados para facilitar o gerenciamento de permissões.
- A estrutura do Active Directory permite aplicar políticas de forma centralizada.

## Evidências

### Active Directory Users and Computers

A imagem abaixo demonstra o domínio `jtechlab.local` sendo administrado por meio do console **Active Directory Users and Computers**.

![Active Directory Users and Computers](./evidências/02-active-directory.png)
