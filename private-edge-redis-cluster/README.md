# private-edge-redis-cluster
Private Redis Enterprise cluster in single Wavelength Zone on Verizon 5G Edge.


## Motivation
To enable real-time analytics and transaction processing, we are trying to ensure we have fully-featured caching capabilities at the mobile edge.

Requirements for the architecture include:

 - Repeatable infrastructure: Preliminary deliverable via CloudFormation template with all relevant parameters, mappings, and resources
 - Highly available: Implement internal cluster DNS with supporting Route53 records
 - Secure: Minimize open ports of security groups and block internet ingress traffic to cluster


## How to Contribute
Please refer to [outstanding issues](https://github.com/rhbelson/5G-Edge-Integrations/issues) for more information about how to get involved.
