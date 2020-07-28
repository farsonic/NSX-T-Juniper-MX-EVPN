## NSX-T-Juniper-MX-EVPN

### Introduction

VMware NSX-T 3.0 introducted support for BGP based EVPN Type-5 NRLI advertistment, allowing for multi-tenant exchange of routes between the NSX-T Edge Gateways (Both virtual and bare metal) to supporting gateway devices. Typically EVPN is supported on datacenter switches and gateway routers with either VXLAN or MPLS being used for the overlay protocol. NSX-T 3.0 implemenents BGP/EVPN with VXLAN overlay. 

!image 

With this implementation tenants is isolated into their own EVPN based VRF instance on the edge with isolation provided by unique VNI, there is no need with this implemtnation to allocate a VLAN per tenant (VRF-Lite) or to deploy multiple edge nodes for isolation. Routes are advertised using BGP with a unique Route-distinquisher for each tenant. 
