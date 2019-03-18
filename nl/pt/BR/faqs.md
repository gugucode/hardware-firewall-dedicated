---

copyright:
  years: 2017
lastupdated: "2018-11-30"

---

{:shortdesc: .shortdesc}
{:new_window: target="_blank"}
{:codeblock: .codeblock}
{:pre: .pre}
{:screen: .screen}
{:tip: .tip}
{:download: .download}
{:faq: data-hd-content-type='faq'}

# Perguntas frequentes para o Hardware Firewall (Dedicated)
{: #faqs-for-hardware-firewall-dedicated-}

A seguir estão as perguntas mais frequentes ao trabalhar com o firewall Fortigate Security Appliance 1g.

## O que é um firewall?
{:faq}

Um firewall é um dispositivo de rede conectado para envio de dados por meio de um servidor. O firewall bloqueia tráfego indesejado de um servidor antes que o servidor seja acessado.

## Por que devo usar um firewall?
{:faq}

A principal vantagem de se ter um firewall é que seu servidor tem apenas que manipular o tráfego "bom" - isso significa que seu recurso está sendo usado exclusivamente para seu propósito desejado, em vez de manipular tráfego indesejado também.

## Quais produtos de firewall a IBM© oferece?
{:faq}

É possível localizar uma comparação detalhada de todos os produtos de firewall oferecidos no IBM Cloud revisando este
[tópico](/docs/infrastructure/fortigate-10g?topic=fortigate-10g-exploring-firewalls). 

## O Hardware Firewall (Dedicated) é compatível com os produtos de balanceador de carga da IBM?
{:faq}

Sim. O Hardware Firewall (Dedicated) é compatível com os balanceadores de carga padrão e dedicado, bem como com o Citrix Netscaler VPX e MPX.

## Posso ter um firewall de hardware dedicado e um Network Gateway associado à mesma VLAN?
{:faq}

Não, não é possível ter um serviço de firewall (compartilhado ou dedicado) e um dispositivo Network Gateway designado à mesma VLAN. 

## O tráfego público passa pelo meu balanceador de carga ou pelo Hardware Firewall primeiro?
{:faq}

Vindo da Internet pública, os produtos Local Load Balancer, Dedicated Load Balancer ou Enterprise Load Balancer vêm primeiro, os produtos Hardware Firewall vêm em seguida e os produtos NetScaler vêm por último (junto aos servidores dos clientes).

## O SoftLayer cobra por largura de banda do firewall?
{:faq}

O Hardware Firewall (Shared), o Hardware Firewall (Dedicated) e o Fortigate Security Appliance não são medidos quanto à largura da banda.  Além disso, esses produtos podem reduzir a utilização da largura de banda total, limitando o tráfego a que os servidores devem responder.

## Quais são as portas esmaecidas no meu Firewall do Windows?
{:faq}

O SoftLayer oferece muitos serviços diferentes que podem ser utilizados com seu servidor, incluindo monitoramento de Evault, SNMP e Nagios. Esses serviços requerem que os nossos sistemas internos se comuniquem com seu servidor em algum grau. As portas esmaecidas que você vê na lista Exceções são portas abertas apenas na porta de rede interna. Elas ainda estão bloqueadas na conexão de rede pública (Internet). Como a rede interna é uma rede segura, ter essas portas abertas é considerado seguro.

Essas portas geralmente não podem ser modificadas, no entanto, se você reconfigurar as regras de firewall, ele as limpará da lista Exceções. Cuidado, pois a reconfiguração das regras de firewall poderá ter um efeito adverso não só nesses serviços adicionais, mas também poderá causar outros problemas com o servidor, dependendo de sua configuração atual.

## Quais opções de Hardware Firewall estão disponíveis para servidores de 10 Gbps?
{:faq}

Se 10 Gbps forem necessários apenas na rede privada (para banco de dados, backup, armazenamento etc.), os clientes poderão solicitar um downgrade apenas de seus uplinks públicos e pedir qualquer um dos produtos Hardware Firewall. Se 10 Gbps forem necessários na rede pública, um Network Gateway ou um Fortigate Security Appliance 10Gbps será necessário.

## Quais intervalos de IP permitir por meio do firewall?
{:faq}

Para obter a lista de endereços IP e os intervalos de IP a serem permitidos por meio do firewall, acesse [aqui](/docs/infrastructure/hardware-firewall-dedicated?topic=hardware-firewall-dedicated-ibm-cloud-ip-ranges). 

## Qual é o número máximo de servidores que o Hardware Firewall (Dedicated) ou o Fortigate Security Appliance protegerá?
{:faq}

O Dedicated Hardware Firewall e o Fortigate Security Appliance podem proteger todos os servidores em uma VLAN pública.  No entanto, é importante observar que, uma vez que esses dispositivos de FW são conectados com um Uplink de 2 Gbps, recomendamos escalar o número de instâncias de firewall para atender às necessidades de desempenho de seu app. Os clientes podem simplesmente fazer isso implementando Firewalls adicionais de VLAN pública em um pod para permitir a inclusão de recursos adicionais de firewall e de cálculo associado.

## Quais opções de VPN são incluídas com cada produto Firewall?
{:faq}

Nem todos os firewalls oferecem VPN e nem todas as opções de VPN são iguais.  As opções gerais para VPN são:

* Cada cliente recebe conexões SSL VPN ilimitadas para a nossa rede privada. Essas conexões podem ser estabelecidas clicando no link VPN na parte superior da página enquanto conectado no portal do cliente.
* Os clientes também recebem um PPTP VPN por conta. Eles podem incluir usuários PPTP VPN adicionais em suas contas em pacotes de 5 por US$ 5/mês extra.
* O SoftLayer também oferece um serviço básico IPSec VPN de diversos locatários a partir de US$ 99/mês.
* O Fortigate Security Appliance fornece opções SSL e IPSec VPN com acesso à rede pública apenas (sem acesso à rede privada do SoftLayer).
* O Network Gateway fornece os recursos SSL, IPSec e OpenVPN na rede pública ou privada.
* Os produtos NetScaler podem fornecer SSL e IPSec VPN na rede pública ou privada.
* Os clientes também podem implementar uma solução VPN em um servidor em seu ambiente do SoftLayer.

## Ao selecionar a opção Alta disponibilidade para o Hardware Firewall (Dedicated) ou o Fortigate Security Appliance, quais etapas preciso realizar para aproveitar esse recurso?
{:faq}

Nenhuma. Quando pedido em HA, o SoftLayer provisiona os dispositivos automaticamente na configuração de HA.  No caso de o dispositivo primário falhar, um dispositivo passivo secundário assumirá como a instância ativa primária e começará a passar o tráfego.  Embora esse failover seja geralmente automático, a melhor prática é monitorar os servidores e assegurar-se de que o tráfego esteja sendo passado com êxito.

## Quais produtos de firewall suportam NAT pública-para-privada e/ou segmentação de VLAN privada?
{:faq}

O Fortigate Security Appliance de 10Gbps suporta NAT pública-para-privada e segmentação de VLAN privada. 
