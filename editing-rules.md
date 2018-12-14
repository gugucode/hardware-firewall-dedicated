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

# Configure the Hardware Firewall (Dedicated)

When the Firewall is first added to the VLAN, a set of rules is initially put in place that allows all traffic through the firewall. Configuring the firewall is as simple as creating a set of rules to allow access to certain IP addresses/ports from specific internet addresses while denying traffic from other sources.

## Edit Rules

To edit the firewall rules:

1. From your browser, open [Customer Portal ![External link icon](../../icons/launch-glyph.svg "External link icon")](https://control.softlayer.com/){: new_window} and log into your account.
2. In the Customer Portal navigation, select **Network > IP Management > VLANs**. Each row represents a VLAN in your infrastructure.  Click on the Firewall-vlanXXXX.networklayer.com link associated with the VLAN you want to manage to take you to the **Device Details** page. Ensure the "Status" indicates that the firewall is "Processing All Rules."  Users can choose to bypass the rules in the event that implemented rules have an unintended impact on their environment by clicking "Bypass Rules" in this area.
3. To start updating rules, click on the **Rules** tab. The page will display sections showing the current rules in effect for IPv4 and IPv6 addresses.  If no rules are implemented, a faded placeholder will be displayed.  Edit individual rules by clicking on the corresponding row.  This list of rules is known as the 'working config'. A 'working config' is a set of rules that is in the process of being created but has not yet been applied to the Firewall. A user may edit, add, and delete rules until the rule set is completed.  Rules are displayed in the order in which they are processed with lower numbered rules having precedence over higher number rules (if rule 1 allows a packet through, rules 2 and beyond are not applied to the packet).
4. Click on a rule to edit it or click on the plus sign at the bottom of the table to add an additional rule. Clicking on the minus icon will delete the rule. The rules are automatically validated as you enter them.

    The fields are:

    **Action:** 'permit' or 'deny' traffic matching this rule

    **Source:** Can be either 'any' or a specific ip address or the network address for a specific subnet.

    **CIDR:** Indicates the standard CIDR notation for the selected source.  "32" will implement the rule for a single IP while, for example, "24" will implement the rule for 256 IPs.

    **Destination:** Can be either 'any' or a specific ip address or the network address for a specific subnet.

    **CIDR:** Indicates the standard CIDR notation for the selected destination.

    **Port Range:** These 2 fields indicate the range of ports (between 1 and 65535) that the rule will apply to.

    **Protocol:** Selects the protocol the rule will apply to (TCP/GRE/ICMP/UDP/PPTP/AH/ESP)

    **Notes:** Field to enter any note about this rule.
    
5. Once the 'working config' is complete, press the **Update Rules** button to have the 'working config' applied to the firewall. The rules should take effect within two minutes.

## Common Ports

| Protocol | Port |
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
| Remote Desktop | 3389 |
| PostgreSQL | 5432 |
| VNC Web | 5800 |
| VNC Client | 5900 |
| Urchin | 9999 or 10000 ||
