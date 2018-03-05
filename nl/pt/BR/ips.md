---

copyright:
  years: 2017, 2018
lastupdated: "2018-01-16"

---

{:shortdesc: .shortdesc}
{:new_window: target="_blank"}
{:codeblock: .codeblock}
{:pre: .pre}
{:screen: .screen}
{:tip: .tip}
{:download: .download}

# Intervalos de IP do IBM Cloud

Uma pergunta mais frequente é **Quais intervalos de IP permitir por meio do firewall?** A lista a seguir contém o intervalo completo de IPs para usar com um Hardware Firewall (Dedicated).

## Rede de front-end (pública)

|Datacenter|Cidade|Estado|Country|Intervalo de IP|
|---|---|---|---|---|
|ams01|Amsterdã|-|NLD|159.253.158.0/23|
|ams03|Amsterdã|-|NLD|159.8.198.0/23|
|che01|Chennai|-|IND|169.38.118.0/23|
|dal01|Dallas|Texas|EUA|66.228.118.0/23|
|dal05|Dallas|Texas|EUA|173.192.118.0/23|
|dal06|Dallas|Texas|EUA|184.172.118.0/23|
|dal07|Dallas|Texas|EUA|50.22.118.0/23|
|dal08|Dallas|Texas|EUA|192.255.18.0/24|
|dal09|Dallas|Texas|EUA|198.23.118.0/23|
|dal10|Dallas|Texas|EUA|169.46.118.0/23|
|dal12|Dallas|Texas|EUA|169.47.118.0/23|
|dal13|Dallas|Texas|EUA|169.48.118.0/24|
|fra02|Frankfurt|-|DEU|159.122.118.0/23|
|hkg02|Hong Kong|-|CHN|119.81.138.0/23|
|hou02|Houston|Texas|EUA|173.193.118.0/23|
|lon02|Londres|-|ENG|5.10.118.0/23|
|lon04|Londres|-|ENG|169.62.118.0/24|
|lon06|Londres|-|ENG|158.176.118.0/23|
|mel01|Melbourne|-|AUS|168.1.118.0/23|
|mex01|Cidade do México|-|MEX|169.57.118.0/23|
|mil01|Milão|-|ITA|159.122.138.0/23|
|mon01|Montreal|-|CAN|169.54.118.0/23|
|par01|Paris|-|FRA|159.8.118.0/23|
|osl01|Oslo|-|NOR|169.51.118.0/24|
|sao01|São Paulo|-|BRA|169.57.138.0/23|
|sea01|Seattle|Washington|EUA|67.228.118.0/23|
|seo01|Seul|-|KOR|169.56.118.0/24|
|sjc01|São José|Califórnia|EUA|50.23.118.0/23|
|sjc03|São José|Califórnia|EUA|169.45.118.0/23|
|sjc04|São José|Califórnia|EUA|169.62.118.0/24|
|sng01|Jurong do leste|-|SGP|174.133.118.0/23|
|syd01|Sydney|-|AUS|168.1.18.0/23|
|syd04|Sydney|-|AUS|130.198.118.0/23|
|tok02|Tóquio|-|JPN|161.202.118.0/23|
|tor01|Toronto|-|CAN|158.85.118.0/23|
|wdc01|Washington D.C.|-|EUA|208.43.118.0/23|
|wdc03|Washington D.C.|-|EUA|192.255.38.0/24|
|wdc04|Washington D.C.|-|EUA|169.55.118.0/23|
|wdc06|Washington D.C.|-|EUA|169.60.118.0/23|
|wdc07|Washington D.C.|-|EUA|169.61.118.0/23|

Portas a serem permitidas:<br>
Todas as portas TCP/UDP<br>
ICMP – ping (para resolução de problemas de suporte e monitoramento)

## IPs do balanceador de carga

|Datacenter|Cidade|Estado|Country|Intervalo de IP|
|---|---|---|---|---|
|ams01|Amsterdã|-|NLD|159.253.157.0/24|
|ams03|Amsterdã|-|NLD|159.8.197.0./24|
|che01|Chennai|-|IND|169.38.117.0/24|
|dal01|Dallas|Texas|EUA|67.228.66.0/24, 75.126.76.0/24, 174.35.17.0/24, 208.43.15.0/24|
|dal05|Dallas|Texas|EUA|50.23.203.0/24, 108.168.157.0/24 173.192.117.0/24, 192.155.205.0/24|
|dal06|Dallas|Texas|EUA|184.172.117.0/24|
|dal07|Dallas|Texas|EUA|50.22.117.0/24|
|dal09|Dallas|Texas|EUA|169.46.187.0/24, 198.23.117.0/24|
|dal10|Dallas|Texas|EUA|169.46.117.0/24|
|dal12|Dallas|Texas|EUA|169.47.117.0/24|
|dal13|Dallas|Texas|EUA|169.48.117.0/24|
|fra02|Frankfurt|-|DEU|159.122.117.0/24|
|hkg02|Hong Kong|-|CHN|119.81.137.0/24|
|hou02|Houston|Texas|EUA|173.193.118.0/23|
|lon02|Londres|-|ENG|5.10.117.0/24|
|lon04|Londres|-|ENG|158.175.117.0/24|
|lon06|Londres|-|ENG|158.176.117.0/24|
|mel01|Melbourne|-|AUS|168.1.117.0/24|
|mex01|Cidade do México|-|MEX|169.57.117.0/24|
|mil01|Milão|-|ITA|159.122.137.0/24|
|mon01|Montreal|-|CAN|169.54.117.0/24|
|par01|Paris|-|FRA|159.8.117.0/24|
|osl01|Oslo|-|NOR|169.51.117.0/24|
|sao01|São Paulo|-|BRA|169.57.137.0/24|
|sea01|Seattle|Washington|EUA|67.228.117.0/24|
|seo01|Seul|-|KOR|169.56.117.0/24|
|sjc01|São José|Califórnia|EUA|50.23.117.0/24|
|sjc03|São José|Califórnia|EUA|169.45.117.0/24|
|sng01|Jurong do leste|-|SGP|174.133.117.0/24|
|syd01|Sydney|-|AUS|168.1.17.0/24|
|syd04|Sydney|-|AUS|130.198.117.0/24|
|tok02|Tóquio|-|JPN|161.202.117.0/24|
|tor01|Toronto|-|CAN|158.85.117.0/24|
|wdc01|Washington D.C.|-|EUA|50.22.248.0/25, 169.54.27.0/24, 198.11.250.0/24, 208.43.117.0/24|
|wdc04|Washington D.C.|-|EUA|169.55.117.0/24|
|wdc06|Washington D.C.|-|EUA|169.60.117.0/24|
|wdc07|Washington D.C.|-|EUA|169.61.117.0/24|

## Sistemas de mitigação do DOS

|Datacenter|Cidade|Estado|Country|Intervalo de IP|
|---|---|---|---|---|
|AMS|Amsterdã|-|NLD|159.253.156.0/24, 159.8.196.0/24|
|CHE|Chennai|-|IND|169.38.116.0/24|
|DAL|Dallas|Texas|EUA|75.126.61.0/24|
|FRA|Frankfurt|-|DEU|159.122.116.0/24|
|HKG|Hong Kong|-|CHN|119.81.136.0/24|
|HOU|Houston|Texas|EUA|173.193.116.0/24|
|KOR|Seul|-|Coreia do Sul|169.56.116.0/24|
|LON|Londres|-|ENG|5.10.116.0/24|
|MEL|Melbourne|-|AUS|168.1.116.0/24|
|MEX|Cidade do México|-|MEX|169.57.116.0/24|
|MIL|Milão|-|ITA|159.122.136.0/24|
|MON|Montreal|-|CAN|169.54.116.0/24|
|NOR|Oslo|-|Noruega|169.56.116.0/24|
|PAR|Paris|-|FRA|159.8.116.0/24|
|SAO|São Paulo|-|BRA|169.57.136.0/24|
|SEA|Seattle|Washington|EUA|50.23.167.0/24|
|SJC|São José|Califórnia|EUA|50.23.116.0/24|
|SNG|Jurong do leste|-|SGP|174.133.116.0/24|
|SYD|Sydney|-|AUS|168.1.16.0/24|
|TOK|Tóquio|-|JPN|161.202.116.0/24|
|TOR|Toronto|-|CAN|158.85.116.0/24|
|WDC|Washington D.C.|-|EUA|50.22.255.0/24|

Portas a serem permitidas: <br>
Todas as portas TCP/UDP

## Varreduras de vulnerabilidade
Para assegurar a conclusão bem-sucedida de uma varredura de vulnerabilidade, permita acesso aos endereços IP a seguir: **173.192.255.232** e **172.17.19.38**.

## Rede de backend (privada)

Bloco de IP: seu bloco de IP privado para comunicações servidor-para-servidor (10.X.X.X/X)<br>
Portas a serem permitidas:<br>
ICMP – ping (para resolução de problemas de suporte)<br>
Todas as portas TCP/UDP<br>
Para obter informações específicas de porta do EVault, [clique aqui](https://console.bluemix.net/docs/infrastructure/Backup/evault-port-information.html#evault-port-information).

## Rede de serviço (na rede de backend/rede privada)
Certifique-se de incluir regras para DAL01 e o local de seu servidor. Se o seu servidor estiver em AMS01, será necessário incluir regras que permitam o tráfego de ambos DAL01 e AMS01.

Para Provisões de imagem flex (tanto criação de imagem quanto provisões do servidor), também será necessário permitir DAL05.

|Datacenter|Cidade|Estado|Country|Intervalo de IP|
|---|---|---|---|---|
|Todos|-|-|-|161.26.0.0/16
|ams01|Amsterdã|-|NLD|10.2.64.0/20|
|ams03|Amsterdã|-|NLD|10.3.128.0/20|
|che01|Chennai|-|IND|10.200.16.0/20|
|dal01|Dallas|Texas|EUA|10.0.64.0/19|
|dal05|Dallas|Texas|EUA|10.1.128.0/19|
|dal06|Dallas|Texas|EUA|10.2.128.0/20|
|dal07|Dallas|Texas|EUA|10.1.176.0/20|
|dal08|Dallas|Texas|EUA|100.100.0.0/20|
|dal09|Dallas|Texas|EUA|10.2.112.0/20 e 10.3.192.0/24|
|dal10|Dallas|Texas|EUA|10.200.80.0/20|
|dal12|Dallas|Texas|EUA|10.200.112.0/20|
|dal13|Dallas|Texas|EUA|10.200.128.0/20|
|fra02|Frankfurt|-|DEU|10.3.80.0/20|
|hkg02|Hong Kong|-|CHN|10.2.160.0/20|
|hou02|Houston|Texas|EUA|10.1.160.0/20|
|lon02|Londres|-|ENG|10.1.208.0/20|
|lon04|Londres|-|ENG|10.201.32.0/20|
|lon06|Londres|-|ENG|10.201.64.0/20|
|mel01|Melbourne|-|AUS|10.2.80.0/20|
|mex01|Cidade do México|-|MEX|10.2.176.0/20|
|mil01|Milão|-|ITA|10.3.144.0/20|
|mon01|Montreal|-|CAN|10.3.112.0/20|
|par01|Paris|-|FRA|10.2.144.0/20|
|osl01|Oslo|-|NOR|10.200.96.0/20|
|sao01|São Paulo|-|BRA|10.200.0.0/20|
|sea01|Seattle|Washington|EUA|10.1.64.0/19|
|seo01|Seul|-|KOR|10.200.64.0/20|
|sjc01|São José|Califórnia|EUA|10.1.192.0/20|
|sjc03|São José|Califórnia|EUA|10.3.176.0/20|
|sjc04|São José|Califórnia|EUA|10.201.80.0/20|
|sng01|Jurong do leste|-|SGP|10.2.32.0/20|
|syd01|Sydney|-|AUS|10.3.96.0/20|
|syd04|Sydney|-|AUS|10.201.16.0/20|
|tok02|Tóquio|-|JPN|10.3.64.0/20|
|tor01|Toronto|-|CAN|10.2.48.0/20|
|wdc01|Washington D.C.|-|EUA|10.1.96.0/19|
|wdc03|Washington D.C.|-|EUA|100.100.32.0/20|
|wdc04|Washington D.C.|-|EUA|10.3.160.0/20 e 10.201.0.0/20|
|wdc06|Washington D.C.|-|EUA|10.200.160.0/20|
|wdc07|Washington D.C.|-|EUA|10.200.176.0/20|

## Rede SSL VPN (na rede de backend/privada)
ICMP – ping (para resolução de problemas de suporte) <br>
Todas as portas TCP/UDP (para acesso de sua estação de trabalho local)

## Data centers SSL VPN

|Datacenter|Cidade|Estado|Country|Intervalo de IP|
|---|---|---|---|---|
|ams01|Amsterdã|-|NLD|10.2.200.0/23|
|ams03|Amsterdã|-|NLD|10.3.220.0/24|
|che01|Chennai|-|IND|10.200.232.0/24|
|dal01|Dallas|Texas|EUA|10.1.0.0/23|
|dal05|Dallas|Texas|EUA|10.1.24.0/23|
|dal06|Dallas|Texas|EUA|10.2.208.0/23|
|dal07|Dallas|Texas|EUA|10.1.236.0/24|
|dal09|Dallas|Texas|EUA|10.2.232.0/24|
|dal10|Dallas|Texas|EUA|10.200.228.0/24|
|dal12|Dallas|Texas|EUA|10.200.216.0/22|
|dal13|Dallas|Texas|EUA|10.200.212.0/22|
|fra02|Frankfurt|-|DEU|10.2.236.0/24|
|hkg02|Hong Kong|-|CHN|10.2.216.0/24|
|hou02|Houston|Texas|EUA|10.1.56.0/23|
|lon02|Londres|-|ENG|10.2.220.0/24|
|lon04|Londres|-|ENG|10.200.196.0/24|
|lon06|Londres|-|ENG|10.3.200.0/24|
|mel01|Melbourne|-|AUS|10.2.228.0/24|
|mex01|Cidade do México|-|MEX|10.3.232.0/24|
|mil01|Milão|-|ITA|10.3.216.0/24|
|mon01|Montreal|-|CAN|10.3.224.0/24|
|par01|Paris|-|FRA|10.3.236.0/24|
|osl01|Oslo|-|NOR|10.200.220.0/22|
|sao01|São Paulo|-|BRA|10.200.236.0/24|
|sea01|Seattle|Washington|EUA|10.1.8.0/23|
|seo01|Seul|-|KOR|10.200.224.0/22|
|sjc01|São José|Califórnia|EUA|10.1.224.0/23|
|sjc03|São José|Califórnia|EUA|10.3.204.0/24|
|sjc04|São José|Califórnia|EUA|10.200.192.0/24|
|sng01|Jurong do leste|-|SGP|10.2.192.0/23|
|syd01|Sydney|-|AUS|10.3.228.0/24|
|syd04|Sydney|-|AUS|10.200.200.0/24|
|tok02|Tóquio|-|JPN|10.2.224.0/24|
|tor01|Toronto|-|CAN|10.1.232.0/24|
|wdc01|Washington D.C.|-|EUA|10.1.16.0/23|
|wdc04|Washington D.C.|-|EUA|10.3.212.0/24|
|wdc06|Washington D.C.|-|EUA|10.200.208.0/24|
|wdc07|Washington D.C.|-|EUA|10.200.204.0/24|

## SSL VPN POPs

|POP|Cidade|Estado|Country|Intervalo de IP|
|---|---|---|---|---|
|atl01|Atlanta|Geórgia|EUA|10.1.41.0/24|
|chi01|Chicago|Illinois|EUA|10.1.49.0/24|
|den01|Denver|Colorado|EUA|10.1.53.0/24|
|lax01|Los Angeles|Califórnia|EUA|10.1.33.0/24|
|mia01|Miami|Flórida|EUA|10.1.37.0/24|
|nyc01|Nova York|Nova York|EUA|10.1.45.0/24|

## Data centers PPTP VPN

|Datacenter|Cidade|Estado|Country|Intervalo de IP|
|---|---|---|---|---|
|ams01|Amsterdã|-|NLD|10.2.203.0/24|
|ams03|Amsterdã|-|NLD|10.3.221.0/24|
|che01|Chennai|-|IND|10.200.233.0/24|
|dal01|Dallas|Texas|EUA|10.1.3.0/24|
|dal05|Dallas|Texas|EUA|10.1.27.0/24|
|dal06|Dallas|Texas|EUA|10.2.211.0/24|
|dal07|Dallas|Texas|EUA|10.1.238.0/24|
|dal09|Dallas|Texas|EUA|10.2.233.0/24|
|dal10|Dallas|Texas|EUA|10.200.229.0/24|
|dal12|Dallas|Texas|EUA|10.200.217.0/24|
|fra02|Frankfurt|-|DEU|10.2.237.0/24|
|hkg02|Hong Kong|-|CHN|10.2.217.0/24|
|hou02|Houston|Texas|EUA|10.1.59.0/24|
|lon02|Londres|-|ENG|10.2.221.0/24|
|lon04|Londres|-|ENG|10.200.197.0/24|
|lon06|Londres|-|ENG|10.3.201.0/24|
|mel01|Melbourne|-|AUS|10.2.229.0/24|
|mil01|Milão|-|ITA|10.3.217.0/24|
|mon01|Montreal|-|CAN|10.3.255.0/24|
|mex01|Cidade do México|-|MEX|10.3.233.0/24|
|par01|Paris|-|FRA|10.3.237.0/24|
|sao01|São Paulo|-|BRA|10.200.237.0/24|
|sea01|Seattle|Washington|EUA|10.1.11.0/24|
|seo01|-|Coreia do Sul|KOR|10.200.225.0/24|
|sjc01|São José|Califórnia|EUA|10.1.227.0/24|
|sjc03|São José|Califórnia|EUA|10.3.205.0/24|
|sng01|Jurong do leste|-|SGP|10.2.195.0/24|
|syd01|Sydney|-|AUS|10.3.229.0/24|
|syd04|Sydney|-|AUS|10.200.201.0/24|
|tok02|Tóquio|-|JPN|10.2.225.0/24|
|tor01|Toronto|-|CAN|10.1.233.0/24|
|wdc01|Washington D.C.|-|EUA|10.1.19.0/24|
|wdc04|Washington D.C.|-|EUA|10.3.213.0/24|
|wdc06|Washington D.C.|-|EUA|10.200.209.0/24|
|wdc07|Washington D.C.|-|EUA|10.200.205.0/24|

## PPTP VPN POPs

|POP|Cidade|Estado|Country|Intervalo de IP|
|---|---|---|---|---|
|atl01|Atlanta|Geórgia|EUA|10.1.42.0/24|
|chi01|Chicago|Illinois|EUA|10.1.40.0/24|
|den01|Denver|Colorado|EUA|10.1.54.0/24|
|lax01|Los Angeles|Califórnia|EUA|10.1.34.0/24|
|mia01|Miami|Flórida|EUA|10.1.38.0/24|
|nyc01|Nova York|Nova York|EUA|10.1.46.0/24|

## Redes anteriores

|Intervalo de IP|
|---|
|12.96.160.0/24|
|66.98.240.192/26|
|67.18.139.0/24|
|67.19.0.0/24|
|70.84.160.0/24|
|70.85.125.0/24|
|75.125.126.8|
|209.85.4.0/26|
|216.12.193.9|
|216.40.193.0/24|
|216.234.234.0/24|

Se o seu servidor usar uma licença **Red Hat Enterprise Linux (RHEL)** fornecida pelo SoftLayer, você precisará, além disso, permitir acesso à rede de serviço conforme a seguir, caso contrário, as atualizações e o licenciamento não funcionarão corretamente:

|Local do servidor|Permitir rede de serviço para este data center|
|---|---|
|Amsterdã (AMS01, AMS03)|LON02|
|Chennai (CHE01)|TOK02 e SYD01|
|Dallas (DAL01, DAL05, DAL07, DAL09)|DAL09|
|Dallas (DAL06, DAL10)|DAL06|
|Houston (HOU02)|DAL09|
|Frankfurt (FRA02)|LON02|
|Hong Kong (HKG02)|TOK02 e SYD01|
|Londres (LON02)|LON02|
|Melbourne (MEL01)|SYD01|
|México (MEX01)|DAL06|
|Milão (MIL01)|LON02|
|Montreal (MON01)|MON01|
|Paris (PAR01)|LON02|
|San Jose (SJC01, SJC03)|SJC03 e DAL06|
|São Paulo (SAO01)|SAO01 e DAL09|
|Singapura (SNG01)|TOK02 e SYD01|
|Seattle (SEA01)|SJC03 e DAL06|
|Sydney (SYD01, SYD04)|SYD01|
|Toronto (TOR01)|TOR01|
|Washington DC (WDC01, WDC04, WDC06, WDC07)|MON01|
|Qualquer DC não listado acima|DAL09|
