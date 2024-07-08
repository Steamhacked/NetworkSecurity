Internet consists of:
  1) Hosts (Endsystems) - devices running network applications (E.G: laptop, smartphone, server, etc.)
  2) Communication Links - along with packet switches - responsible for connecting endsystems (E.G.: coaxial cable, copper wire, optic fibre, etc.)
  3) Packet Switches - receive and forward packets (E.G.: routers, link-layer switches)
     3.a) Packets - packages of information, consists of smaller chunks of data and header-bytes that label order of those chunks. Created by sending end system and reassembled later on the receiving end

Network Building challenges: Operability, Sharing, Complex interacting components, Scalability

Protocol - format and order, according to which, packages are sent, actions on them taken on transmission and receipt. Allows for Operability

Circuit Switching - reserve all the resources for the connection between 2 endsystems, for the duration of that connection
  Pros: Guarantees stable connection
  Cons: Expensive and results into underutilization of resources

Multiplexing - allows multiple hosts to share resources by either:
  Frequency Division - each circuit continuously utilizes certain fraction of the bandwidth
  Time Division - each circuit uses entire bandwidth of the link periodically in a brief time interval

Packet Switching - breaking of messages into smaller packets, that are then independently sent over the network
  Pros: occupies resources on demand, cheaper
  Cons: fluctuating network speed

Network Layering - division of labor, where each layer performs a set of specific tasks and can only interact with layers directly above or below.
