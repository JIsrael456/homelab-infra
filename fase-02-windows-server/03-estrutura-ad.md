# Estrutura do Active Directory

## Objetivo

Organizar os objetos do Active Directory utilizando
Organizational Units (OUs).

## Estrutura criada

JTECHLAB
├── Administrativo
│   ├── Usuarios
│   └── Computadores
│
├── TI
│   ├── Usuarios
│   └── Computadores
│
├── Grupos
└── Usuario


## O que é uma OU?

OU (Organizational Unit) é uma unidade organizacional
utilizada para organizar objetos dentro do Active Directory.

Uma OU pode conter, por exemplo:

- usuários
- computadores
- grupos
- outras OUs

Além da organização, as OUs são importantes porque
permitem aplicar GPOs de maneira mais controlada.

## Usuários

Os usuários representam as identidades utilizadas
para autenticação no domínio.

Exemplo:

Jaco Israel

Localização:

JTECHLAB > TI > Usuarios

## Computadores

Os computadores representam máquinas ingressadas
no domínio.

Exemplo:

WS-DSK

Localização:

JTECHLAB > TI > Computadores

## Grupos

Os grupos permitem reunir usuários e computadores
para facilitar o gerenciamento de permissões e
políticas.

Exemplo:

GG-TI

## Evidências

...
