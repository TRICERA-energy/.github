---
name: 📋 Plant Epic
about: Overview of plant specific tasks
title: "[Plant Epic]: "
labels: epic
assignees: ''

---

<!--
This is a proposed minimum (!) list of plant related tasks. Feel free to add more tasks relevant for the specific plant or to customize. But focus on an overview in this epic, i.e. do not go too much into details.
Each bullet point can easily be changed to an issue and described in more detail there.
-->

### Detailed Engineering
- [ ] Select hardware
- [ ] Create network plan
- [ ] Agree on network operator interface (to ppc)
- [ ] Create operational control concept
- [ ] Create power plant controller (*EZA-Regler*) concept (if necessary)
- [ ] Create *Regelungskonzept* for plant certificate, (if necessary)
- [ ] Agree on marketer interface (if necessary)
- [ ] Agree on customer control interface (if necessary)
- [ ] Agree on data provision to the customer (FTP, ... )

### Specific new software implementation requirements (link issues and/or prs!)
- [ ] ...

### Prepare commissioning
- [ ] Create IP list including port forwardings to other network segments (e.g. smartblue ppc)
- [ ] Prepare software commissioning protocol
- [ ] Setup wireguard VPN configuration
- [ ] Configure router
- [ ] Create project configurations
  - [ ] bcc
  - [ ] ems
  - [ ] (ucm)
- [ ] Configure IO systems (RevPi, Moxa)
- [ ] Configure server
- [ ] Setup kubernetes cluster
- [ ] Check datalogging in influx
- [ ] Check grafana

### Commissioning (goes hand in hand with the commissioning protocol)
- [ ] Establish wireguard VPN connection to the plant
- [ ] Check communication to all devices in the IP list
- [ ] Check connections to the IO systems (RevPis, Moxas)
- [ ] Check communication with smartblue router and the ppc
- [ ] Test interfaces with
  - [ ] marketer (if interfaced to ems)
  - [ ] network operator (mostly smartblue's part)
  - [ ] (customer)
- [ ] Perform power test (attach and apply some power via bcc)
- [ ] Test whole control chain, possibly with smartblue (e.g. marketer/network operator -> ems -> ppc -> bcc)
- [ ] Establish data provision to customer (e.g. FTP push to customer's endpoint or smartblue portal)

### Performance Tests
- [ ] Run capacity test
- [ ] Run double hump test (*Doppelhöckertest*) (if necessary)
- [ ] ...
