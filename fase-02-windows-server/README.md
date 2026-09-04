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

- [ ] Instalar Windows Server
- [ ] Configurar IP fixo
- [ ] Instalar Active Directory
- [ ] Promover servidor a Controlador de Domínio
- [ ] Criar domínio (jitech.local)
- [ ] Configurar DNS
- [ ] Configurar DHCP
- [ ] Criar OUs
- [ ] Criar grupos
- [ ] Criar usuários
- [ ] Criar compartilhamentos
- [ ] Criar GPOs

OUs (Organizational Units) são usadas para organizar objetos do Active Directory, como usuários e computadores. Essa separação permite aplicar GPOs e delegar administração de forma mais controlada. No laboratório, a estrutura foi dividida inicialmente entre áreas como Administrativo e TI, cada uma podendo possuir seus próprios usuários e computadores.

## Resultado esperado

Todos os computadores poderão autenticar usuários utilizando o Active Directory.
