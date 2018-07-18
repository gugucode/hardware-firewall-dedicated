---

copyright:
  years: 2017
lastupdated: "2017-10-30"

---

{:shortdesc: .shortdesc}
{:new_window: target="_blank"}
{:codeblock: .codeblock}
{:pre: .pre}
{:screen: .screen}
{:tip: .tip}
{:download: .download}

# 알려진 제한사항
Hardware Firewall (Dedicated)에는 다음과 같은 알려진 제한사항이 있습니다.

* ARP가 처리되는 방식으로 인해 Windows NLB(Network Load Balancing)와 호환되지 않습니다.

* 고가용성 장애 복구 기능은 사용자에게 표시되지 않습니다. 마스터 방화벽이 작동되지 않는데 자동으로 장애가 복구되지 않는 경우 지원 티켓이 필요합니다. 방화벽이 트래픽을 적절하게 전달하는지 확인하기 위해 중요한 서비스에 대해서는 디바이스 모니터링을 권장합니다.

* Hardware Firewall (Dedicated)를 현재 네트워크 게이트웨이, Hardware Firewall 또는 Fortigate 보안 어플라이언스와 연관되어 있는 VLAN에 배치할 수 없습니다.
