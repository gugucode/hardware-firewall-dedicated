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

# FAQs
The following are frequently asked questions when working with the Fortigate Security Appliance 1g firewall.

## What is a firewall?
{:faq}

A firewall is a network device that is connected upstream from a server. The firewall blocks unwanted traffic from a server before the server is reached.

## Why should I use a firewall?
{:faq}

The primary advantage of having a firewall is that your server only has to handle “good” traffic – this means your resource is solely being used for its intended purpose as opposed to handling unwanted traffic, too.

## What firewall products does IBM offer?
{:faq}

You can find a detailed comparison of all firewall products offered in the IBM Cloud by reviewing this [topic ![External link icon](../../icons/launch-glyph.svg "External link icon")](../../infrastructure/fortigate-10g/explore-firewalls.html#explore-firewalls){: new_window}. 

## Is the Hardware Firewall (Dedicated) compatible with IBM's load balancer products?
{:faq}

Yes. Hardware Firewall (Dedicated) is compatible with the standard and dedicated load balancers, as well as the Citrix Netscaler VPX and MPX.

## Can I have a dedicated hardware firewall and a Network Gateway associated with the same VLAN?
{:faq}

No, it is not possible to have a firewall service (shared or dedicated) and a Network Gateway device assigned to the same VLAN. 

## Does public traffic pass through my load balancer or Hardware Firewall first?
{:faq}

Coming from the public internet in, the Local Load Balancer, Dedicated Load Balancer or Enterprise Load Balancer products are first, the Hardware Firewall products are next, and the NetScaler products are last (along with the customers servers).

## Does SoftLayer charge for firewall bandwidth?
{:faq}

The Hardware Firewall (Shared), Hardware Firewall (Dedicated), and Fortigate Security Appliance are not metered for bandwidth.  Additionally, these products can reduce total bandwidth utilization by limiting the traffic that servers must respond to.

## What are the greyed out ports in my Windows Firewall?
{:faq}

SoftLayer offers many different services that you can utilize with your server including Evault, SNMP and Nagios monitoring. These services require that our internal systems communicate with your server to some degree. The grayed out ports you see in the Exceptions list are ports open on the internal network port only. They are still blocked on the public (internet) network connection. Since the internal network is a secured network having these ports open is considered secure.

These ports generally cannot be modified however if you reset the firewall rules it will clear them from the Exceptions list. Please beware that resetting the firewall rules may have an adverse affect not only on these additional services but also could cause other issues as well with your server depending on its current configuration.

## What Hardware Firewall options are available for 10Gbps servers?
{:faq}

If 10Gbps is only required on the private network (for database, backup, storage, etc), then customers can request a downgrade of only their public uplinks and order any of the Hardware Firewall products. If 10Gbps is required on the public network, a Network Gateway or Fortigate Security Appliance 10Gbps is required.

## What IP ranges do I allow through the firewall?
{:faq}

For the list of IP addresses and IP ranges to allow through the firewall, go [here](ips.html). 

## What is the maximum number of servers that the Hardware Firewall (Dedicated) or Fortigate Security Appliance will protect?
{:faq}

Both the Dedicated Hardware Firewall and the Fortigate Security Appliance can protect every server on a Public VLAN.  However it is important to note that since these FW devices are connected with 2Gbps Uplink we recommend scaling the number of firewall instances to meet the performance needs of your app. Customers can simply do so by deploying additional public VLAN Firewalls within a pod to allow for additional firewall and associated compute resources to be added.

## What VPN options are included with each Firewall product?
{:faq}

Not all firewalls offer VPN and not all VPN options are the same.  The general options for VPN are:

* Each customer receives unlimited SSL VPN connections to our private network. These connections can be established by clicking the VPN link at the top of the page while logged into the customer portal.
* Customers also receive one PPTP VPN per account. They can add additional PPTP VPN users to their account in packs of 5 for $5/month extra.
* SoftLayer also offers a basic multi-tenant IPSec VPN service starting at $99/month.
* The Fortigate Security Appliance provides SSL and IPSec VPN options with Public network access only (no access to the SoftLayer private network).
* The Network Gateway provides SSL, IPSec and OpenVPN capabilities on the public or private network
* The NetScaler products can provide SSL and IPSec VPN on the public or private network.
* Customers can also deploy a VPN solution on to a server within their SoftLayer environment.

## When I select the High Availability option for the Hardware Firewall (Dedicated) or the Fortigate Security Appliance, what steps do I have to take to leverage this feature?
{:faq}

None. When ordered in HA, SoftLayer automatically provisions the appliances in HA configuration.  In the event that the primary device fails, a secondary passive device will take over as the primary active instance and begin passing traffic.  While this failover is typically automatic, it is best practice to monitor servers and ensure traffic is being passed successfully.

## Which firewall products support public-to-private NAT and/or private VLAN segmentation?
{:faq}

Fortigate Security Appliance 10Gbps supports public-to-private NAT and private VLAN segmentation. 
