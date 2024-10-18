#monitor-and-analyze-the-availability-and-downtime-of-virtual-machine-nodes
The query is designed to help administrators track the availability and failure frequency of virtual machines over time, allowing them to identify which VMs have experienced downtime and how frequently this occurred within the specified time range. It provides visibility into node uptime and downtime patterns.
The purpose of this SWQL query is to monitor and analyze the availability and downtime of virtual machine nodes in a SolarWinds environment. Specifically, it:
Identifies Virtual Machine Nodes: Filters nodes whose captions (names) start with "vm", focusing the analysis on virtual machine (VM) nodes.

Retrieves Key Data:
The name (Caption) and IP address of each VM node.
The availability percentage and the percentage of downtime (PercentDown) recorded for each VM.
The timestamp (ObservationTimestamp) when each availability measurement was taken.

Classifies Node Status:
Classifies each node as either "Up" (if availability is greater than 0%) or "Down" (if availability equals 0%).

Counts Downtime Occurrences:
Tracks how many times a node's availability has reached 0%, i.e., how many times the node has gone down during the specified time period.
Filters by Time Range: Limits the data to availability and downtime events recorded between January 1, 2023, and December 31, 2023.

Groups and Sorts Data:
Groups the results by node name, IP address, availability, and observation timestamp to ensure each VM node and its availability data are uniquely recorded.
Orders the results chronologically by observation timestamp.
