### Criação de template 

1 - Criação do **template**

Cria **item** (o que será monitorado?)

**Tipo** > Tipo de coleta (Agente Zabbix, Monitoramento simples, SNMP)

**Chave** > "Qual dado eu quero obter deste host?" 
Exemplo: 
*system.cpu.load* > Indica que o Zabbix deve coletar a **carga da CPU**.

net.tcp.service.perfil[service, <ip>, <port>] > 
net.tcp.service.perfil[ssh] (substitui) > Testa a performance do servidor SSH na porta padrão (22) usando o IP do host.

#### Value Mapping (Mapeamento de valor)
É um recurso utilizado para **converter valores brutos coletados pelo Zabbix em textos mais amigáveis para visualização**.

##### Um item retorna o valor 1 