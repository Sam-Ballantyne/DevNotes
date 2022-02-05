# AWS Infrastructure

- - - -

## Table of Contents

* [Top Level View](https://github.com/Sam-Ballantyne/DevNotes/blob/main/AWS/AwsInfrastructure.md#top-level-view)
* [Support](https://github.com/Sam-Ballantyne/DevNotes/blob/main/AWS/AwsInfrastructure.md#support)
* [Definitions](https://github.com/Sam-Ballantyne/DevNotes/blob/main/AWS/AwsInfrastructure.md#definitions)
* [Amazon address](https://github.com/Sam-Ballantyne/DevNotes/blob/main/AWS/AwsInfrastructure.md#amazon-address)

## Top Level view

* __AWS Region:__ Geographical location with a cluster of  data centres (e.g. US-West)
* __Availability zones:__ One or more data centres, each Region has at least 2 zones
* __Edge Location:__ Nodes for a content delivery network (CDN)
    Used for Amazon Cloud Front (AWS Global CDN) and Amazon Route 53 (DNS Service)

## Support

* Different tiers of support for AWS resources which are running in the cloud
* Tiers differ based on requirements, cost and response times

### Support Tools

* __Personal Health Dashboard:__ Generates alerts for if there are issues outage which might impact you e.g. an outage
* __Truster Advisor:__ Checks AWS resources and suggests improvements based on 5 categories (cost, performance, security, fault tolerance, service limits)

## Definitions

* __Highly availabile application:__ An application with no single point of failure

## Amazon address

> You read Amazon addresses in the following way: \<area\>-\<subarea>-\<regionNum, availability zone\> e.g. us-east-2a