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

# Configurando o Hardware Firewall (Dedicated)
{: #configuring-the-hardware-firewall-dedicated-}

Quando o Firewall é primeiramente incluído na VLAN, um conjunto de regras é inicialmente colocado em vigor, permitindo todo o tráfego por meio do firewall. A configuração do firewall é tão simples quanto criar um conjunto de regras para permitir o acesso a determinados endereços IP/portas por meio de endereços de Internet específico enquanto nega o tráfego de outras fontes.

## Editar regras

Para editar as regras de firewall:

1. Em seu navegador, abra o [Portal do cliente ![Ícone de link externo](../../icons/launch-glyph.svg "Ícone de link externo")](https://control.softlayer.com/){: new_window} e efetue login em sua conta.
2. Na navegação do Portal do cliente, selecione **Rede > Gerenciamento de IP > VLANs**. Cada linha representa uma VLAN em sua infraestrutura.  Clique no link Firewall-vlanXXXX.networklayer.com associado à VLAN que você deseja gerenciar para levá-lo à página **Detalhes do dispositivo**. Se
houver regras, assegure-se de que o "Status" indique que o firewall está "Processando todas as regras".  Os usuários podem optar por efetuar bypass das regras no caso de as regras implementadas terem um impacto indesejado no ambiente, clicando em "Efetuar bypass das regras" nesta área.
3. Para iniciar a atualização das regras, clique na guia **Regras**. A página exibirá seções que mostram as regras atuais em vigor para os endereços IPv4 e IPv6.  Se nenhuma regra for implementada, um item temporário esmaecido será exibido.  Edite regras individuais clicando na linha correspondente.  Essa lista de regras é conhecida como a 'configuração funcional'. Uma 'configuração funcional' é um conjunto de regras que está no processo de criação, mas que ainda não foi aplicado ao Firewall. Um usuário pode editar, incluir e excluir regras até que o conjunto de regras seja concluído.  As regras são exibidas na ordem em que são processadas, com as regras de numeração inferior tendo precedência sobre as regras de numeração mais alta (se a regra 1 permitir um pacote, as regras 2 e além não serão aplicadas ao pacote).
4. Clique em uma regra para editá-la ou clique no sinal de mais na parte inferior da tabela para incluir uma regra adicional. Clicar no ícone de menos excluirá a regra. As regras são validadas automaticamente conforme são inseridas.

    Os campos são:

    **Ação:** 'permitir' ou 'negar' tráfego correspondente a essa regra

    **Origem:** pode ser 'nenhuma' ou um endereço IP específico ou o endereço de rede para uma sub-rede específica.

    **CIDR:** indica a notação CIDR padrão para a origem selecionada.  "32" implementará a regra para um único IP enquanto, por exemplo, "24" implementará a regra para 256 IPs.

    **Destino:** pode ser "qualquer um" ou um endereço IP específico ou o endereço de rede para uma sub-rede específica.

    **CIDR:** indica a notação CIDR padrão para o destino selecionado.

    **Intervalo de portas:** esses 2 campos indicam o intervalo de portas (entre 1 e 65535) ao qual a regra será aplicada.

    **Protocolo:** seleciona o protocolo ao qual a regra será aplicada (TCP/GRE/ICMP/UDP/PPTP/AH/ESP)

    **Notas:** campo para inserir qualquer nota sobre essa regra.
    
5. Depois que a 'configuração funcional' estiver concluída, pressione o botão **Atualizar regras** para que a 'configuração funcional' seja aplicada ao firewall. As regras devem entrar em vigor em dois minutos.

## Portas comuns

| Protocolo | Porta |
| :-----: | :-----: |
| FTP | 21 |
| SSH | 22 |
| Telnet | 23 |
| SMTP | 25 |
| DNS | 53 |
| HTTP | 80 |
| POP3 | 110 |
| IMAP | 143 |
| HTTPS | 443 |
| MSSQL | 1433 |
| MySQL | 3306 |
| Área de trabalho remota | 3389 |
| PostgreSQL | 5432 |
| Web VNC | 5800 |
| Cliente VNC | 5900 |
| Urchin | 9999 ou 10000 ||
