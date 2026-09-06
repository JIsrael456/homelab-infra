# Estrutura do Active Directory

## Objetivo

Organizar os objetos do Active Directory utilizando Organizational Units (OUs), grupos e usuários, criando uma estrutura que facilite a administração do ambiente.

## Estrutura criada

A estrutura principal planejada para o domínio `jtechlab.local` foi organizada da seguinte forma:

```text
JTECHLAB
├── Administrativo
│   ├── Usuarios
│   └── Computadores
│
├── TI
│   ├── Usuarios
│   └── Computadores
│
└── Grupos
```

A separação por departamento permite organizar os objetos de acordo com sua função dentro da empresa e facilita a aplicação de políticas específicas.

## O que é uma OU?

OU (Organizational Unit) é uma unidade organizacional utilizada para organizar objetos dentro do Active Directory.

Uma OU pode conter diferentes tipos de objetos, como:

- Usuários
- Computadores
- Grupos
- Outras OUs

Além da organização, as OUs são importantes porque permitem aplicar GPOs de maneira mais controlada e delegar determinadas tarefas administrativas.

## Usuários

Os usuários representam as identidades utilizadas para autenticação no domínio.

### Exemplo

**Usuário:** Jaco Israel

**Localização planejada:**

```text
JTECHLAB
└── TI
    └── Usuarios
```

O usuário também foi associado ao grupo de segurança `GG-TI`.

## Computadores

Os computadores representam as máquinas ingressadas no domínio.

### Exemplo

**Computador:** WS-DSK

**Localização planejada:**

```text
JTECHLAB
└── TI
    └── Computadores
```

> **Observação:** o computador `WS-DSK` foi anteriormente ingressado no domínio e organizado na OU de computadores da área de TI. A máquina foi posteriormente reinstalada e o ingresso no domínio será realizado novamente durante a Fase 03 - Windows Client.

## Grupos

Os grupos de segurança permitem reunir usuários e outros objetos para facilitar o gerenciamento de permissões e políticas.

Foram criados os seguintes grupos:

- `GG-Administrativo`
- `GG-TI`
- `GG-Usuarios`

### Exemplo

O usuário `Jaco Israel` foi associado ao grupo:

```text
GG-TI
```

Essa organização permite que permissões e políticas possam ser associadas a grupos em vez de serem configuradas individualmente para cada usuário.

## Organização por departamento

A estrutura foi criada pensando em um ambiente corporativo fictício da JI Tech Solutions.

### Administrativo

Responsável por organizar os usuários e computadores relacionados às atividades administrativas.

```text
Administrativo
├── Usuarios
└── Computadores
```

### TI

Responsável por organizar os usuários e computadores relacionados à área de Tecnologia da Informação.

```text
TI
├── Usuarios
└── Computadores
```

### Grupos

Centraliza os grupos de segurança utilizados no laboratório.

```text
Grupos
├── GG-Administrativo
├── GG-TI
└── GG-Usuarios
```

## Relação entre OUs, usuários, computadores e grupos

A estrutura permite separar diferentes responsabilidades:

```text
OU
│
├── Usuários
│   └── Identidades
│
├── Computadores
│   └── Máquinas do domínio
│
└── GPOs
    └── Políticas aplicadas conforme a estrutura
```

Os grupos de segurança complementam essa organização, permitindo controlar permissões e facilitar a administração dos usuários.

## Validação

A estrutura foi validada utilizando o console **Active Directory Users and Computers**.

Foi possível visualizar:

- O domínio `jtechlab.local`
- A OU `JTECHLAB`
- A OU `Administrativo`
- A OU `TI`
- As OUs `Usuarios` e `Computadores`
- A OU `Grupos`

## Resultado

A estrutura organizacional do Active Directory foi criada para representar a divisão departamental da JI Tech Solutions.

A organização por OUs fornece uma base para aplicação de políticas, gerenciamento de usuários e computadores e delegação administrativa.

Os grupos de segurança também foram criados para facilitar o gerenciamento de permissões.

## Conceitos aprendidos

- OUs são utilizadas para organizar objetos dentro do Active Directory.
- Usuários representam identidades que podem autenticar no domínio.
- Computadores representam máquinas ingressadas no domínio.
- Grupos de segurança permitem centralizar o gerenciamento de permissões.
- A organização por departamentos facilita a aplicação de GPOs.
- A estrutura de OUs influencia a forma como políticas de grupo podem ser aplicadas.
- A organização lógica do Active Directory é importante para facilitar a administração de ambientes corporativos.

## Evidências

### Estrutura do Active Directory

A imagem abaixo demonstra a estrutura organizacional criada no console **Active Directory Users and Computers**.

![Estrutura do Active Directory](./evidências/02-active-directory.png)
