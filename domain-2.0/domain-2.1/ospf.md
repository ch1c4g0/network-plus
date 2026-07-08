

# Open Shortest Path First (OSPF)

A common interior gateway protocol and used within a single autonomous system (AS)

This is a common, well-established standard, it is available on routers from many different manufacturers

OSPF is a link-state protocol with cost being measured by bandwidth.

OSPF calculates best path itself using the Shortest Path First (SPF)/Dijkstra algorithm rather than trusting neighbor hop counts.

## Areas

OSPF splits large networks into areas to reduce overhead, with **Area0** as the mandatory backbone all other areas connect to.

# Convergence

Done quickly when topology changes, which makes it more desireable than RIP.
