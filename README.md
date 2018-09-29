# go-openshift
GOAL: of this repository is to evaluate - how to deploy CI and CD pipeline for golang on using OpenShift

# Finding

* CI - from source to docker image is difficult
  * no dedicated jenkins slave with golang build env. available - need to be created
  * build within a docker container difficult to setup


# Minishift init

```sh
> minishift start
> eval $(minishift oc-env)
> source <(oc completion bash)
```

# BuildConfig

```sh
> oc new-app https://github.com/LAtanassov/go-openshift --strategy=pipeline
```

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
