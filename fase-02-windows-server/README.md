# Fase 02 - Windows Server

## Objetivo

Implantar o servidor principal responsável pela autenticação e gerenciamento dos recursos da empresa.

## Tecnologias

- Windows Server 2025
- Active Directory
- DNS
- DHCP
- GPO

## O que será feito

- [x] Instalar Windows Server
- [x] Configurar IP fixo
- [x] Instalar Active Directory
- [x] Promover servidor a Controlador de Domínio
- [x] Criar domínio (jitech.local)
- [x] Configurar DNS
- [ ] Configurar DHCP
- [x] Criar OUs
- [x] Criar grupos
- [x] Criar usuários
- [ ] Criar compartilhamentos
- [x] Criar GPOs

OUs (Organizational Units) são usadas para organizar objetos do Active Directory, como usuários e computadores. Essa separação permite aplicar GPOs e delegar administração de forma mais controlada. No laboratório, a estrutura foi dividida inicialmente entre áreas como Administrativo e TI, cada uma podendo possuir seus próprios usuários e computadores.

## Documentação

- [01 - Active Directory](./01-active-directory.md)
- [02 - DNS](./02-dns.md)
- [03 - Estrutura do Active Directory](./03-estrutura-ad.md)
- [04 - Group Policy (GPO)](./04-gpo.md)

## Resultado esperado

Ao final desta fase, os computadores do ambiente poderão autenticar usuários utilizando o Active Directory, com usuários, grupos, OUs, DNS e políticas de grupo administrados de forma centralizada.
