# REST-as-we-use-it Meeting 2015-03-26

## Participants
 
- Matthias Kovatsch ("clean REST approach")
- Michael Richardson ("REST for security/management/diagnostics")
- Darshak Thakore ("how far to stretch REST for applications")
- Renzo Navas ("secure REST")
- Laurent Toutain ("secure REST")
- Ana He ("REST for network management")
- Robby Simpson ("REST and PubSub for smart grid")
- Andreas Scholz ("automation application use of REST")
- Joerg Heuer ("inter-domain application use of REST")
- Kerry Lynn ("ZigBee IP / SEP 2.0 background")
- Michael Koster ("PubSub, CoRE interfaces, end-to-end applications")
- Joe Hildebrand ("XMPP background")
- Carsten Bormann ("REST by Fielding")
- Klaus Hartke (remote, "REST by Fielding")

## Terminology

- Individual terms
   - *Origin state*: where is the main residence of a representation; a sleepy node might send data to a persistent storage; URI states path and authority (state owner); name does not say anything about route; resource is the rendezvous; note in CoRE authority might be independent of DNS
   - *Client-Server vs client-and-server on device = peer-to-peer*
   - *Mirror server vs broker vs Web cache*: re-naming / re-origin when origin state moves; how to translate: device to logical endpoint -- standard way?
- Design patterns (high interest)
   - *Design space*: Methods, options, parameters, payload
   - *Client vs server*: flows of data, POST vs serving resource; commissioning vs operation phase -- "PUTters" need a target URI
   - *Group communication*: Multicast PUT vs multicast Response/Notification
   - *Toggle*: who is the owner/origin; condition at different resource/endpoints; debouncing; light switch example
   - *Intermediaries*: architectures with (caching) proxies
   - Make CoRE Interfaces clear as one example/pattern
- Consistent state/event model
   - *Observe*: (send states not events)
   - *PubSub*: PUT vs PUSH vs Notify; eliminate conflict with PubSub terminology
   - *Message queuing*: message vs representation level; ETags to define where in message queue?
- Management approaches
   - CoMI
   - RESTCONF
   - Yang
   - OMA LWM2M

Andrew Biggs has internal document that might suite as straw-man proposal.

Reading Roy Fielding's thesis appears to be a good prerequisite for a discussion.

## Possible Activities

### General

- How to set up a proxy: dynamic scaling of the network; redirects 
- Proxyless PubSub (multicast PUT) -- requires consistent state/event model first
- Multicast notifications (group registrations to observable resources)
- Unsolicited notifications

### Applications

- New Internet Media Types (beyond SENML)
- QoS: device internal priorities

### Management

- What is the minimal information a monitoring server needs to look at to have a clear view of the status of a network
- Can we imagine some work on defining the data model of (1) RPL and (2) generic values like neighbor table. Data models exist for 6TiSCh and 6LoWPAN, but nothing past that
- Alarm messages (PUSH notifications when stuff goes really wrong)
- New Internet Media Types
- Dynamic QoS management: (rat-hole warning by Kerry) mapping from app/process level down to network; fire alarm priority; network virtualization in constrained networks?
- Visitors in the network
