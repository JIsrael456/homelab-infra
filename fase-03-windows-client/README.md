# Fase 03 - Windows Cliente

## Objetivo

Configurar uma estação de trabalho integrada ao domínio corporativo.

## Tecnologias

- Windows 11
- Active Directory

## Checklist de revalidação após reinstalação

O ingresso da estação no domínio e a aplicação de GPO foram registrados anteriormente, mas a máquina foi reinstalada. As caixas abaixo representam o **estado atual de revalidação**, não negam a execução histórica.

- [ ] Instalar Windows 11
- [ ] Configurar IP
- [ ] Entrar no domínio
- [ ] Testar login com usuário do AD
- [ ] Testar compartilhamentos
- [ ] Testar políticas de grupo (GPO)

## Evidência histórica

O arquivo `progresso` registra ingresso anterior do Windows 11 no domínio e validação de GPO de usuário. A documentação da estrutura de AD informa que a estação `WS-DSK` foi reinstalada e que o ingresso será repetido.

## Situação atual

Reingresso, login, compartilhamentos e políticas devem ser testados e documentados novamente antes de marcar esta fase como concluída.

## Resultado esperado

A estação funcionará como um computador corporativo autenticado pelo domínio.
