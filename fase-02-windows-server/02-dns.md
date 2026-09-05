# DNS

## Objetivo

Configurar e validar o serviço DNS responsável pela
resolução de nomes do domínio `jtechlab.local`.

## Configuração

- Servidor DNS: SRVWIN
- IP: 192.168.10.10
- Domínio: jtechlab.local

## Atividades realizadas

- Instalação/configuração do DNS
- Criação/validação da zona `jtechlab.local`
- Verificação dos registros DNS
- Testes de resolução de nomes

![DNS](evidências/03-dns.png)

## Testes realizados

### nslookup

Foi utilizado o comando:

```powershell
nslookup srvwin.jtechlab.local
```
![nslookup](evidências/04-nslookup-srvwin.png)
