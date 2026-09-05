# Active Directory

## Objetivo

Configurar o Active Directory Domain Services (AD DS)
para centralizar a autenticação e o gerenciamento dos
recursos do laboratório.

## Ambiente

- Servidor: SRVWIN
- Domínio: jtechlab.local
- IP: 192.168.10.10
- Sistema: Windows Server 2025

## Atividades realizadas

- Instalação da função AD DS
- Criação do domínio jtechlab.local
- Promoção do servidor a Controlador de Domínio
- Validação do domínio
- Abertura do Active Directory Users and Computers

## Resultado

O domínio `jtechlab.local` foi criado com sucesso e o
servidor SRVWIN passou a atuar como Controlador de Domínio.

## Evidências


...
![Active Directory](evidências/02-active-directory.png)
```


## Conceitos aprendidos

- O Active Directory centraliza a autenticação e o gerenciamento de identidades.
- O domínio `jtechlab.local` permite que os computadores e usuários do laboratório sejam administrados de forma centralizada.
- O Domain Controller é responsável pelos serviços centrais do domínio.
- O AD DS utiliza o DNS para localizar serviços e computadores dentro do domínio.
- Usuários e computadores podem ser organizados em Organizational Units (OUs).
