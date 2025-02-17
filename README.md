# capex vs opex
	- CAPEX - Despesa Capital: Gastos iniciais com infra, data centers, investimento inicial com data center
		- CAPEX tende a diminuir o custo conforme o tempo
	- OPEX - Despesa de Oeração: Custo pago conforme o uso, pay as you go, etc

# Beneficios:
	- Alta disponibilidade (SLA (Quantos 9), multi az, etc)
	- Escalabilidade 
	- Elasticidade (Vertical, Horizontal, auto ou manual)
	- Confiabilidade/ resiliencia
		- Microsoft Well Archtecture Framework
		- DR, Replication
	- Previsibilidade
	- Segurança (Compartilhada)
	- Governança
	- Gerenciabilidade (IAC, APIS, PWSH, ETC)
		
# SLA
	- 99%	
		semana: 1,68 hora
		mes: 7,2 horas
		ano: 3,65 dias
	- 99,9%
		dia: 10,2 minutos
		mes: 42,3 minutos
		ano: 8,76 horas
	- 99,95%
		dia: 5 minutos
		mes: 21,6 minutos
		ano: 4,38 horas
	- 99,99%
		dia: 1,01 minutos
		mes: 4,32 minutos
		ano: 52,56 minutos
	- 99,999%
		dia: 6 segundos
		mes: 25,9 segundos
		ano: 5,26 segundos 

	Quanto mais noves, mais tempo de disponibilidade

# Modelos de Serviçp
IaaS, PaaS, SaaS

# Regiões
 Dominio de atualização e dominio de falha 
Regiões, Zona de disponibilidade, pares de região
	Replicação automatica, DR
	Sul do Brasil replica ainda para o Centro Sul dos EUA (Par de região de DR)
	Região militar EUA (Governamental)
	Azure China (21Vianet)

# Grupo de recursos
	- Organização logica de recursos da Azure
	- Não é organizado por região
	- É possivel migrar recursos do RG
	- não é possivel renomear RG

# Assinaturas
 É possivel criar diversas assinaturas
	- Assinatura de Desenvolvimento
	- Assinatura de teste
	- Assinatura de produção
 Uma pessoa pode ter N assinaturas. 
 Uma assinatura só pode ter uma conta (Billing)
	Limite de cobrança e acesso


# Grupo de gerenciamento (ORG)
 > Assinaturas 
   > Grupo de recursos
    > Recursos

# Replicação global
https://datacenters.microsoft.com/globe/explore?info=region_brazilsouth

# Computação e rede
Tipos de computação
	- Container (PaaS)
	- VM (IaaS)(Controle sobre S.O e personalização)
		Conjuntos de disponibilidade
			Dominios de falhas (Racks)
			Dominio de atualização (Pelo menos tres dominios de falha)
			Manutenções preventivas são avisadas pelo portal
	- Função (PaaS)
		Baseado em eventos
	- AKS (Orquestração de containers)
	- dimensionamento (Disco, rede, processador etc)
	- area de trabalho virtual (Desktop virtual)
		pool (Varias instancias por user, limite de sessão)
		pessoal (Maquina esxclusiva de usuario, licenciamento, etc)
 lift and shift (Levar como esta) 
		

Hospedagem de aplicativos
	- Serviços de aplicativos (PaaS)
		Aplicativos API e Web de forma rapida e gerenciada
		.NET, .NET Core, NodeJs, Java, Python PHP
Redes Virtuais
	- VNET, comunicaçã entre recursos
		- SubRedes
	- duas VNETS não se omunicam por defaul, precisa de aparelhamento
	- Camadas de redes (Overlaps de endereços)
	- Gateway de VPN (Site to Site pela internet)
	- Express ROute (Rede via Cabo, link dedicado)
	- DNS
		- Redes e nomes customizados e privados 
