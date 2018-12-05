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

# 공용 VLAN에 Hardware Firewall (Dedicated) 추가

Hardware Firewall (Dedicated)는 서버 주문의 일부로 주문할 수 없으며 하나 이상의 공용 컴퓨팅 노드가 설정되고 연관된 VLAN이 추가된 후에 배치해야 합니다.

VLAN에 보호를 추가하려면 VLAN 페이지에서 Hardware Firewall (Dedicated)를 주문하십시오.

1. 브라우저에서 [고객 포털 ![외부 링크 아이콘](../../icons/launch-glyph.svg "외부 링크 아이콘")](https://control.softlayer.com/){: new_window}을 열고 계정에 로그인하십시오.
2. 고객 포털 탐색에서 **네트워크 > IP 관리 > VLAN**을 선택하고 VLAN 페이지로 이동하십시오. 각 행은 인프라에 있는 VLAN을 표시합니다. IBM Cloud는 실제 VLAN 번호와 구성되어 있는 라우터를 나타내는 "VLAN 번호" 및 "기본 라우터" 정보를 자동으로 채웁니다. 인식 가능한 이름을 정의하는 데 "이름" 필드를 사용할 수 있습니다. 맨 오른쪽 열 "게이트웨이/방화벽"에는 해당 VLAN에 어떤 방화벽 보호가 준비되어 있는지(있는 경우)에 대한 세부사항이 포함됩니다. 

	**팁:** 공용 VLAN만 표시하도록 VLAN 테이블을 필터링하려면, **필터** 탭을 클릭하고 기본 라우터 필드에 "fcr"을 입력하고 **필터** 단추를 클릭하십시오.
3. 보호하려는 VLAN을 찾아서 동일한 행에 있는 **방화벽 추가** 링크를 클릭하십시오. 이 링크를 클릭하면 **Hardware Firewall (Dedicated) 주문** 페이지가 열립니다. "게이트웨이/방화벽" 열이 이미 채워져 있는 경우 방화벽 또는 네트워크 게이트웨이가 이미 VLAN과 연관되어 있음을 의미하며 계속하기 전에 디바이스를 제거해야 합니다.
4. **Hardware Firewall (Dedicated)** 또는 **Hardware Firewall (고가용성)**을 선택하십시오. 

	고가용성 옵션은 동일한 하드웨어와 인터페이스를 배치하지만, 활성 노드가 실패하는 경우 두 번째 수동 노드를 배치하여 트래픽 처리를 계속합니다. 고가용성은 작동 중단이 늘어나는 위험을 줄여줍니다. 

5. **이 VLAN의 서버** 단추를 클릭하여 적합한 VLAN을 선택했는지 확인하십시오.
6. 지불 방법을 입력하고 **계속**을 클릭하십시오.
7. 다음 화면에서 해당되는 경우 프로모션 코드를 입력하고, 마스터 서비스 계약을 읽고 동의한 후 **주문하기**를 클릭하십시오. 
