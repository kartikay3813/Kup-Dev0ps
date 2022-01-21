**What is Cidr?**
Classless inter-domain routing is a set of Internet protocol standards that is used to create unique identifiers for networks and individual devices andThe host identifier is used to determine which host or device on the network should receive incoming information packets.

**Why /16 is used in subnet?**
Class A Example - /8 - 16 Million Hosts
Class B Example - /16 - 65,000 Hosts
Class C Example - /24 - 254 Hosts

and /16 is a 

**what is difference bewteen IGW and Nat Gateway** ?
 Igw- An Internet Gateway allows resources within your VPC to access the internet, and vice versa.
 NAT-It allows resources in a private subnet to access the internet.
 It only works one way. The internet at large cannot get through your NAT to your private resources unless you explicitly allow it.
