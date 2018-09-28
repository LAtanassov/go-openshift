# go-openshift
practice CI and CD deployment using OpenShift

# Overview

Layer 0: OpenShift images  
Layer 1: Builds - BuildConfig describes how to transform source to images  
Layer 2: Images - ImageStream   
Layer 3: Deployments - DeploymentConfig describes how to deploy the image  
Layer 4: Abstractions - Additional Config (Service, Route, PVC) needed to run the application  

more details in [oc blog about template]

![Template Overview][overview]


[oc blog about template]: https://blog.openshift.com/part-2-creating-a-template-a-technical-walkthrough/

[overview]: https://i0.wp.com/blog.openshift.com/wp-content/uploads/OSEv3-Template.png?w=1140&ssl=1 "Template Overview"
