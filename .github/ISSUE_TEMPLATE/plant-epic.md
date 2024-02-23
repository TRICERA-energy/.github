---
name: Plant Epic
about: Epic for an overview of plant specific tasks
title: "[Plant Epic]:"
labels: epic
assignees: ''

---

**Detailed Engineering**
- [ ] Select hardware
- [ ] Create network plan
- [ ] Agree on network operator interface
- [ ] Create operational control concept
- [ ] Create powerplant controller concept
- [ ] Create *Regelungskonzept* for plant certificate, if needed
- [ ] Agree on marketer interface and implement it, if needed
- [ ] Agree on customer (control) interface, if needed
- [ ] Agree on data provision to the customer 

**Specific (new) requirements for the software**
- [ ] ...

**Prepare commissioning**
- [ ] Create IP list including port forwarding with smartblue ppc
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

**Commissioning**
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

**Performance Tests**
- [ ] Run capacity test
- [ ] Run double hump test (*Doppelhöckertest*)
- [ ] ...
