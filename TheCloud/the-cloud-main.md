# The Cloud

Cloud computing is the delivery of computing services over the internet. Computing services include common IT infrastructure such as Virtual Machines, Storage, Databases, and Networking.

Because cloud computing uses the internet to deliver these services, it doesn't have to be constrained by physcial infrastructure the same way that a traditional datacenter is. That means if you need to increase your IT infrastructure rapidly, you don't have to wait to build a new datacentre - you can use the cloud to rapdily expand your IT footprint.

You can see more notes on either of the two main hyperscalars:
- [AWS](https://github.com/TSimmo123/simmo-repo-1/blob/main/TheCloud/AWS/aws-ccp.md)

## The Benefits of Cloud Computing
- Trade capital expense for variable expense
- Benefit from massive economies of scale
- Stop guessing capacity
- Increase speed and agility
- Stop spending money maintaining datacentres
- Go global in minutes
- Elasticity - the ability to acquire resources as you need them and release resources when you no longer need them. In the cloud, you want to do this `automatically`
- Relaibility - A solutions ability to provide functionality for its users when it is needed.

## Define Cloud Models

This is the varying ways in which cloud resources can be deployed.

>`Public Cloud` - Deployed onto a public cloud provider like AWS, MIcroosft Azure and the Google Cloud Platform.

>`Private Cloud` - Deployed in a private datacentre using a cloud-like platform provided by vendors like VMWare.

>`Hybrid Cloud` - Deployed with a mix of the previous two options.

The table below highlights a few key comparative aspects between the cloud models.

![Git Commit](../images/cloud-models-table.png)

## The Shared Responsibility Model

This model dictates what responsibilities are shared between which parties (whether it is the responsibility of the cloud provider or the consumer).

![Git Commit](../images/shared-responsibility.svg)

As depicted, the consumer will always be responsible for:
- The information and data stored in the cloud
- Devices that are allowed to connect to your cloud
- The accounts and identities pf the people, services, and devices within your organisation

The cloud provider is always repsonsible for:
- The physical datacenter
- The physical hosts
- The physcial network

Your service model will determine respponsibility for things like:
- Opearting systems
- Network controls
- Identity and infrastructure