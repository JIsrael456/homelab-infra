
# Group Policy Objects (GPO)

## Objetivo

Criar políticas centralizadas para controlar
configurações de usuários e computadores do domínio.

## GPOs criadas

### GPO - TI - Usuários

Aplicada à OU:

JTECHLAB > TI > Usuarios

### GPO - TI - Computadores

Aplicada à OU:

JTECHLAB > TI > Computadores

## Validação

Foi utilizado:

gpupdate /force

O comando força a atualização das políticas de
grupo no computador.

Também foi utilizado:

gpresult /r

O comando apresenta um resumo das políticas de grupo
aplicadas ao usuário e ao computador.

## Resultado

A GPO `GPO - TI - Usuarios` foi identificada
como aplicada ao usuário `JTECHLAB\jaco`.

## Evidências

...
![nslookup](evidências/0.png)
...
