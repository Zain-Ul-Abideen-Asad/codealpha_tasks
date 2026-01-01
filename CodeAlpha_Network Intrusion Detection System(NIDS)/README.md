# Task 4: Network Intrusion Detection System (NIDS)

Tool Used

* Suricata 7.0.10

Objective

* Set up a network-based IDS to detect malicious traffic.

Installation

bash
sudo apt update
sudo apt install -y suricata


Configuration

* Monitored interface: ens33
* Custom rule added: `/var/lib/suricata/rules/local.rules`

text
alert icmp any any -> any any (msg:"ICMP Ping Detected"; sid:1000001; rev:1;)

Running Suricata

bash
sudo suricata -c /etc/suricata/suricata.yaml -i ens33 --af-packet

Test Traffic

* Ping packets generated from another machine/terminal to trigger ICMP alerts.

Logs & Alerts

* Console (real-time alerts)
* `/var/log/suricata/fast.log` shows detected alerts

1. Suricata terminal showing ICMP alerts
2. fast.log showing ICMP alerts
3. local.rules showing the custom ICMP rule
