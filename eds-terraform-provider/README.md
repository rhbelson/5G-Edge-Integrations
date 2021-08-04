# eds-terraform provider
Custom terraform provider for the [edge discovery service](https://www.verizon.com/business/5g-edge-portal/documentation/verizon-5g-edge-discovery-service.html).

## Motivation
To enable push-button deployment of the network infrastructure, we are trying to ensure that Terraform can support the edge discovery service via a simple module.

Requirements for the architecture include:
 - Leverage existing edge discovery service [API specifications](https://www.verizon.com/business/5g-edge-portal/documentation/verizon-5g-edge-discovery-service/try-it.html)
 - Abstract away undifferentiated heavy lifting of authentication, service profile creation, and service registry creation, modeled off of the [Python Getting Started Guide](https://github.com/Verizon/5GEdgeTutorials/blob/main/edge-discovery/edsConfig.py)


Aspirational module should look something like:
```
module "verizon_eds" {
  source                  = "terraform-vz-modules/edge-discovery/vz"
  version                 = "~> 1.0"

  name                    = "my-edge-registry"
  max_latency             = 40

  availability_zones      = ["us-east-1-wl1-bos-wlz-1","us-east-1-wl1-nyc-wlz-1"]
  carrier_ips             = ["155.146.1.2","155.146.3.4"]
  application_id          = "edge_application"

}
```


## How to Contribute
Please refer to [outstanding issues](https://github.com/rhbelson/5G-Edge-Integrations/issues) for more information about how to get involved.
