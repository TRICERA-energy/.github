---
name: 📋 Site Epic
about: Overview of site specific tasks
title: "[Site Epic]: "
labels: epic
assignees: ''

---

<!--
This is a proposed minimum (!) list of plant related tasks. Feel free to add more tasks relevant for the specific plant or to customize. But focus on an overview in this epic, i.e. do not go too much into details.
Each bullet point can easily be changed to an issue and described in more detail there.
-->

### Detailed Engineering
- [ ] Collect SW related requirements from offer, contract and other binding documents together with the project manager
- [ ] Create network plan including all relevant components to be integrated in the software
- [ ] Create concept for site peripheries (e.g. for temperature/humidity sensors, hvac, fire alarm, emergency relais, insulation monitoring devices, fans, ...)
- [ ] Select hardware
- [ ] Agree on network operator interface (to PPC) including protection devices and (mv) switches
- [ ] Agree on marketer interface (if necessary)
- [ ] Create operational control concept
- [ ] Create power plant controller (PPC: *EZA-Regler*) concept (if necessary)
- [ ] Create *Regelungskonzept* for plant certificate according to E.9 (if necessary)
- [ ] Agree on customer control interface (if necessary)
- [ ] Agree on data provision to the customer (e.g. FTP, live-data interface via mqtt, interface to *Gebäudeleittechnik (GLT)*, ...)
- [ ] Agree on visualization for the customer (e.g. grafana dashboard access, smartblue control portal, ...)

### Ordering
- [ ] Make sure the relevant hardware is correctly ordered together with project manager
- [ ] PPC with relevant requirements (6 weeks in advance)

### Specific new software implementation requirements (link issues and/or prs!)
- [ ] ...

### Prepare commissioning
- [ ] Create IP list including port forwardings / interfaces to other network segments (e.g. customer and smartblue's PPC network)
- [ ] Prepare software commissioning protocol
- [ ] Configure router
  - [ ] Setup login credentials  
  - [ ] Setup IP address  
  - [ ] Setup DHCP Server  
  - [ ] Setup wireguard VPN configuration 
- [ ] Create project configurations
  - [ ] bcc
  - [ ] ems
  - [ ] (ucm)
  - [ ] (revpi)
- [ ] Setup site server
  - [ ] Setup IP address of OS and IPMI
  - [ ] Setup kubernetes cluster
  - [ ] Rollout: MetalLB, Traefik, Prometheus, Loki, MariaDB, EMQX, Grafana, InfluxDB, Telegraf
  - [ ] Rollout: ESF (former: Betsi)
  - [ ] Rollout: BCC
  - [ ] Rollout: EMS
  - [ ] Rollout: UCM
  - [ ] Check datalogging in influx
  - [ ] Check grafana access
  - [ ] Optional: setup customer specific alerts
- [ ] Preconfigure IO systems (RevPi, Moxa)

### Commissioning (goes hand in hand with the commissioning protocol)
- [ ] Establish wireguard VPN connection to the plant
- [ ] Check communication to all devices in the IP list
- [ ] Check communication with smartblue router and PPC
- [ ] Check connections to the IO systems (RevPis, Moxas)
- [ ] Configure inverters according to E.9
- [ ] Configure powermeters
- [ ] Perform BCC power test (attach and apply some power via BCC, check mapping of switchgears and inverters is correct)
- [ ] Test interfaces with
  - [ ] marketer (if interfaced to ems)
  - [ ] network operator (*Bittest* or *Signaltest*, mostly smartblue's part)
  - [ ] customer (if necessary)
- [ ] Configure PPC according to E.9  
- [ ] Test whole control chain, possibly with smartblue (e.g. marketer/network operator -> ems -> ppc -> bcc)  
- [ ] Perfom function tests with network operator and create the protocol (together with smartblue)
- [ ] Prepare necessary documents for conformity declaration (*Konformitätserklärung*) and collect them from smartblue
- [ ] Establish data provision to customer (e.g. FTP/FTPS, SFTP, MQTT, ...)

### Performance Tests
- [ ] Run capacity test
- [ ] FCR: Run double hump test (*Doppelhöckertest*) and 4h test (if necessary)
- [ ] ...

### Handover
- [ ] Handover to O&M / customer, documentation
- [ ] ... 
