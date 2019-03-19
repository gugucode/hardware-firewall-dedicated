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

# Incluindo um Hardware Firewall (Dedicated) em uma VLAN pública
{: #adding-a-hardware-firewall-dedicated-to-a-public-vlan}

Um Hardware Firewall (Dedicated) não pode ser pedido como parte de um pedido do servidor e deve ser colocado depois de pelo menos um nó de cálculo público ser estabelecido e a VLAN associada ter sido incluída.

Para incluir proteção em uma VLAN, peça um Hardware Firewall (Dedicated) da página VLANs:

1. Em seu navegador, abra o [Portal do cliente ![Ícone de link externo](../../icons/launch-glyph.svg "Ícone de link externo")](https://control.softlayer.com/){: new_window} e efetue login em sua conta.
2. Na navegação do Portal do cliente, selecione **Rede > Gerenciamento de IP > VLANs** para acessar a página VLANs. Cada linha representa uma VLAN em sua infraestrutura. O IBM Cloud preenche as informações "Número da VLAN" e "Roteador primário" automaticamente, indicando o número
verdadeiro da VLAN e o roteador no qual ela está configurada. O campo "Nome" pode ser usado para definir um nome reconhecível. A coluna da extrema direita "Gateway/Firewall" contém detalhes sobre qual proteção de firewall, se houver, está em vigor para essa VLAN. 

	**Dica:** para filtrar a tabela VLANs para mostrar apenas VLANs públicas, clique na guia **Filtrar**, insira "fcr" no campo Roteador primário e clique no botão **Filtrar**.
3. Localize a VLAN que você deseja proteger e clique no link **Incluir firewall** na mesma linha. Esse link abre a página **Pedir Hardware Firewall (Dedicated)**. Se a coluna "Gateway/Firewall" já estiver preenchida, um Firewall ou um Network Gateway já estará associado à VLAN e o dispositivo deverá ser removido antes que você possa continuar.
4. Selecione **Hardware Firewall (Dedicated)** ou **Hardware Firewall (High Availability)**. 

	A opção Alta disponibilidade implementa o mesmo hardware e interface, mas implementa um segundo nó passivo para continuar o processamento de tráfego se o nó ativo falhar. A Alta disponibilidade reduz o risco de tempo de inatividade excessivo. 

5. Clique no botão **Servidores nessa VLAN** para verificar se você está selecionando a VLAN apropriada.
6. Insira sua opção de pagamento e clique em **Continuar**.
7. Na próxima tela, insira os códigos promocionais, se aplicável, leia e concorde com o Contrato de Prestação de Serviços Principal e clique em **Fazer o pedido**. 
