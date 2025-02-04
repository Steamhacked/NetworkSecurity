Packet Delay Sources:
  Processing - caused by time taken to examine packet header, less than miliseconds and bounded
  Queueing - caused by input rate exceeding output rate, duration depends on network congestion level
  Transmission - caused by time taken to push the whole packet bits from router to the link, takes d = L/R; L -> packet length [bits], R -> link bandwidth [bits/s]
  Propagation - caused by time taken for signal to travel from sender to receiver, takes d_p = d/S; d -> link length, S -> speed of bits on medium
  Total Nodal - from one node/router to another - is the sum of all above-mentioned delays

  Average Link Utilization = L*a/R; L -> packet length [bits], a -> average packet arrival rate [packet/s], R -> bandwidth [bits/s]
  Average Queueing Delay ~ Average Link Utilization:
    Average Link Utilization =:
      0 -> Average Queing Delay is Small
      1 -> Average Queing Delay is Large
      >1 -> Infinite Delay

  Traceroute - network diagnostic tool that traces data packets' path from one point to another. Helps to measure delay

  RTT - Round-Trip-Time - time it takes for a packet to return after sending to router

  Throughput - actual rate of data transfer
  Packet Loss - occurs when packets drop due to queue being full, random

  Net Throughput can be calculated using bottleneck method (strength of chain is define by the weakest link), example:
  In a network with 3 links of throughputs 10, 7 and 5 MBps, the throughput of the network is 5MBps

  Net Packet Loss can be calculated by totaling percentage lost, example:
  In a network with 2 links with per-link loss rates 10% and 20%, then the net loss is:
  100 - 100 * 0.8 * 0.9 = 28%

  

  

  
