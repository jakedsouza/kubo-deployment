# Exposing deployed applications directly

The only way to expose Kubernetes applications running in Kubo is to use a 
[`NodePort`](https://kubernetes.io/docs/concepts/services-networking/service/#type-nodeport). 

We do not currently support the type [`LoadBalancer`](https://kubernetes.io/docs/concepts/services-networking/service/#type-loadbalancer),
but we plan to soon with Github issue [#47](https://github.com/cloudfoundry-incubator/kubo-release/issues/47)
in the [kubo-release](https://github.com/cloudfoundry-incubator/kubo-release) 
repository. 

## Accessing an application on GCP with IaaS Load-Balancing

On GCP you can expose routes using service type LoadBalancer for your Kubernetes deployments. See the [Kubernetes docs](https://kubernetes.io/docs/tutorials/kubernetes-basics/expose-intro/) for more details.

> **Note:** Any resources that are provisioned by Kubernetes will not be deleted by BOSH when you delete your Kubo deployment. You will need to manage these resources if they are not deleted by Kubernetes before the deployment is deleted.
