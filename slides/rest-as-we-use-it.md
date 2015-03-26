# REST-as-we-use-it Meeting 2015-03-26

## Terminology

- Individual terms
   - Origin state
   - ...
- Design patterns
   - Client vs server (POST vs resource, commissioning vs operation phase)
   - Methods, options, parameters, payload
   - Architectures with (caching) intermediaries
- Consistent state/event model
   - Observe (send states not events)
	 - PubSub
	 - Message queuing (message vs representation level)
- Management approaches
   - CoMI
   - RESTCONF
   - NETCONF
   - OMA LWM2M

## Possible Activities

### General

- Multicast notifications (group registrations to observable resources)

### Applications

- New Internet Media Types (beyond SENML)

### Management

- what is the minimal information a monitoring server needs to look at to have a clear view of the status of a network
- can we imagine some work on defining the data model of (1) RPL and (2) generic values like neighbor table. Data models exist for 6TiSCh and 6LoWPAN, but nothing past that
- alarm messages (PUSH notifications when stuff goes really wrong)
- New Internet Media Types
