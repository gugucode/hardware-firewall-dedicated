---

copyright:
  years: 2017,2018
lastupdated: "2018-11-30"

---

{:shortdesc: .shortdesc}
{:new_window: target="_blank"}
{:codeblock: .codeblock}
{:pre: .pre}
{:screen: .screen}
{:tip: .tip}
{:download: .download}

# Visualizar seus firewalls

Para ver quais VLANs estão protegidas com firewalls e localizar mais detalhes sobre Firewalls individuais, acesse a página VLANs:

1. Em seu navegador, abra o [Portal do cliente ![Ícone de link externo](../../icons/launch-glyph.svg "Ícone de link externo")](https://control.softlayer.com/){: new_window} e efetue login em sua conta.
2. Na navegação do Portal do cliente, selecione **Rede > Gerenciamento de IP > VLANs**.

Cada linha na tabela representa uma VLAN em sua infraestrutura. O IBM Cloud preenche as informações "Número da VLAN" e "Roteador primário" automaticamente, indicando o número verdadeiro da VLAN e o roteador no qual ela está configurada. O campo "Nome" pode ser usado para dar à VLAN um nome reconhecível (como DMZ, Intranet, Público ou Banco de dados).

A coluna da extrema direita "Gateway/Firewall" contém detalhes sobre qual proteção de firewall está em vigor, por exemplo:

- **Incluir firewall** indica que não há firewalls em vigor para servidores nessa VLAN.
- **Servidores protegidos individualmente** indica que um ou mais servidores estão utilizando um Hardware Firewall (Shared) e que não há nenhum Hardware Firewall (Dedicated), FortiGate Security Appliance ou Network Gateway em vigor. Firewalls de VLAN e gateways de rede não podem ser colocados em uma VLAN que tenha servidores protegidos individualmente.
- **Firewall-vlanXXXX.networklayer.com** indica que há um Hardware Firewall (Dedicated) ou um FortiGate Security Appliance em vigor. Somente um firewall de VLAN ou um Network Gateway pode ser associado a uma VLAN, mas um servidor pode ser protegido na VLAN pública por um firewall de VLAN e associado na rede privada a um Network Gateway.
- **GatewayName** indica que a VLAN está associada a esse Network Gateway.

## Detalhes dos servidores protegidos individualmente

Para VLANs que possuem **Servidores protegidos individualmente** no campo "Gateway/Firewall", é possível clicar no link de número de VLAN associado para exibir os detalhes da VLAN, incluindo os dispositivos associados.

Na lista de dispositivos associados, é possível clicar em cada dispositivo e rolar para a parte inferior da guia Configuração. Você verá **Firewall** na seção Complementos, com **Instalado** ou **Não instalado** para o status.

- **Não instalado** indica que nenhum firewall está em vigor para esse dispositivo.
- **Instalado** indica que um firewall está em vigor. Haverá uma guia **Firewall** disponível no dispositivo no qual é possível gerenciar a configuração de firewall.

## Detalhes do Firewall dedicado

Para VLANs que possuem **Firewall-vlanXXXX.networklayer.com** no campo "Gateway/Firewall", é possível clicar nesse link de firewall para exibir os detalhes do Firewall. Os detalhes do dispositivo incluem o roteador associado, a VLAN, as sub-redes IPv4/IPv6, os dispositivos associados a essa VLAN e os controles para rotear tráfego por meio ou ao redor do firewall.

Os dispositivos FortiGate Security Appliance terão o IP de gerenciamento, o nome do usuário e a senha.  O gerenciamento de FortiGate Security Appliances é concluído por meio de sua própria GUI ou do console baseado em SSH.

## Detalhes do Network Gateway

Para VLANs que possuem um nome de dispositivo Network Gateway no campo "Gateway/Firewall", é possível clicar no nome do Network Gateway para exibir seus detalhes. Os detalhes do dispositivo incluem as VLANs associadas de front-end (FCR) e backend (BCR) e as opções de gerenciamento do Network Gateway.
