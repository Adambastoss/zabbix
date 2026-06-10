
#### CRIAÇÃO DO TEMPLATE
Cria template > 

**Cria item** > (O que será monitorado?)
**Tipo** > Tipo de coleta (Zabbix Agente, SNMP...)

**Chave** > "Qual dado eu quero obter desse host?"
	Exemplo: Testa a performance do serviço SSH na porta (22) usando IP do host.
	`net.tcp.service.perfil[service, <ip>, <port>]`
	`net.tcp.service.perfil[ssh]`

**Value Maping** > É um recurso utilizado para converter valores brutos coletados pelo Zabbix em textos mais amigáveis para visualização.

==Ex:== Um item retornao valor **1** > O que significa esse 1?
	Com Value Mapping: 
		1 = Online  
		0 = Offline

**Triggers** > Baseada no item que está sendo monitorado.
Nome: "O serviço está inativo em {HOST.NAME}" ({==HOST.NAME==} = Macro, tipo uma variável)

**Seleciona item** > Função > **Expressão** **(adicionar)** > Condição para alerta > **Criar Host**
Todo host precisa estar dentro de um ==Host Group==.

**Macros** > Tipo uma variável que você pode utilizar dentro do seu template. É possível criar macros que podem ser utilizadas em todo o sistema, nesse caso seria uma macro global, tipo uma "**variável global**"
EX: O serviço está inativo em {==HOST.NAME==}




