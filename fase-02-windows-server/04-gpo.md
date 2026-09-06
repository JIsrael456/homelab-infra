# Group Policy Objects (GPO)

## Objetivo

Criar e aplicar políticas centralizadas para controlar configurações de usuários e computadores do domínio `jtechlab.local`.

As Group Policy Objects (GPOs) permitem que administradores configurem políticas de forma centralizada, evitando a necessidade de realizar configurações individualmente em cada computador.

## O que é uma GPO?

Uma Group Policy Object (GPO) é um conjunto de configurações que pode ser aplicado a usuários e computadores de um ambiente Windows.

As GPOs podem ser utilizadas para administrar, por exemplo:

- Configurações de rede
- Restrições de acesso
- Configurações do sistema operacional
- Configurações de usuários
- Configurações de computadores
- Scripts
- Configurações de rede
- Recursos do ambiente Windows

No laboratório, as GPOs foram utilizadas para demonstrar a aplicação centralizada de políticas para a área de TI.

## Estrutura utilizada

As políticas foram organizadas de acordo com as OUs criadas no Active Directory:

```text
JTECHLAB
└── TI
    ├── Usuarios
    │   └── GPO - TI - Usuarios
    │
    └── Computadores
        └── GPO - TI - Computadores
```

Essa organização permite separar políticas destinadas a usuários das políticas destinadas a computadores.

## GPOs criadas

### GPO - TI - Usuarios

**GPO:** `GPO - TI - Usuarios`

**OU vinculada:**

```text
JTECHLAB > TI > Usuarios
```

Essa GPO foi criada para aplicar configurações relacionadas aos usuários da área de TI.

### GPO - TI - Computadores

**GPO:** `GPO - TI - Computadores`

**OU vinculada:**

```text
JTECHLAB > TI > Computadores
```

Essa GPO foi criada para aplicar configurações relacionadas aos computadores da área de TI.

## Como a GPO é aplicada

As políticas de grupo podem ser aplicadas de acordo com a localização dos objetos no Active Directory.

No laboratório:

```text
Usuário
   ↓
OU TI > Usuarios
   ↓
GPO - TI - Usuarios
```

E:

```text
Computador
   ↓
OU TI > Computadores
   ↓
GPO - TI - Computadores
```

Isso permite administrar políticas de forma centralizada.

## Atualização das políticas

Foi utilizado o comando:

```cmd
gpupdate /force
```

O comando `gpupdate` é utilizado para atualizar as políticas de grupo.

O parâmetro `/force` solicita que todas as configurações de política sejam reaplicadas, mesmo aquelas que não sofreram alterações.

Resultado obtido:

```text
A atualização de Política de Computador foi concluída com êxito.
A atualização de Política de Usuário foi concluída com êxito.
```

## Verificação das políticas aplicadas

Após a atualização das políticas, foi utilizado:

```cmd
gpresult /r
```

O comando `gpresult` apresenta informações sobre as políticas de grupo que foram aplicadas ao usuário e ao computador.

O parâmetro `/r` exibe um resumo das políticas resultantes.

Durante a validação do usuário, foi identificado:

```text
GPO - TI - Usuarios
```

como uma das políticas aplicadas à sessão do usuário.

## Validação do usuário

A sessão utilizada no laboratório pertence ao usuário:

```text
JTECHLAB\jaco
```

A política:

```text
GPO - TI - Usuarios
```

foi identificada como aplicada ao usuário.

Esse resultado demonstra que a GPO vinculada à OU de usuários da área de TI está sendo processada para o usuário localizado nessa OU.

## Validação do computador

A GPO:

```text
GPO - TI - Computadores
```

foi criada e vinculada à OU:

```text
JTECHLAB > TI > Computadores
```

A validação efetiva da aplicação dessa política ao computador `WS-DSK` será realizada novamente durante a Fase 03 - Windows Client, após o reingresso do computador no domínio.

## Resultado

Foram criadas duas Group Policy Objects para a área de TI:

- `GPO - TI - Usuarios`
- `GPO - TI - Computadores`

As GPOs foram vinculadas às respectivas OUs do Active Directory.

A aplicação da política de usuários foi validada utilizando `gpupdate /force` e `gpresult /r`, confirmando a aplicação da `GPO - TI - Usuarios` ao usuário `JTECHLAB\jaco`.

A validação da política de computadores ficará pendente até a reconstrução e o reingresso do `WS-DSK` no domínio.

## Conceitos aprendidos

- GPOs permitem administrar configurações de forma centralizada.
- GPOs podem ser aplicadas a usuários e computadores.
- O vínculo de uma GPO a uma OU determina onde a política será aplicada.
- `gpupdate /force` força a atualização das políticas.
- `gpresult /r` permite verificar as políticas resultantes.
- A organização correta das OUs facilita o gerenciamento das GPOs.
- Políticas de usuário e computador possuem escopos diferentes.
- A validação de uma GPO deve considerar se a política foi realmente aplicada ao objeto, e não apenas se ela foi criada.

## Evidências

### Group Policy Management

A evidência demonstra as GPOs criadas e seus respectivos vínculos com as OUs.

![Group Policy Management](./evidências/06-gpo.png)

### Atualização das políticas

A evidência demonstra a execução do comando `gpupdate /force`.

![GPUpdate](./evidências/07-gpupdate.png)

### Resultado das políticas aplicadas

A evidência demonstra o resultado do comando `gpresult /r`, incluindo a aplicação da `GPO - TI - Usuarios` ao usuário `JTECHLAB\jaco`.

![GPResult](./evidências/08-gpresult.png)
