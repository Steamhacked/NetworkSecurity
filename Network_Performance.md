Packet Delay Sources:
  Processing - caused by time taken to examine packet header, less than miliseconds and bounded
  Queueing - caused by input rate exceeding output rate, duration depends on network congestion level
  Transmission - caused by time taken to push the whole packet bits from router to the link, takes d = L/R; L -> packet length in bits, R -> link bandwidth in bits/s
  Propagation - caused by time taken for signal to travel from sender to receiver, takes d_p = d/S; d -> link length, S -> speed of bits on medium
  Total Nodal - from one node/router to another - is the sum of all above-mentioned delays
