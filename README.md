# kubernetes-quickstart
Quickstart to an enterprise level Kubernetes deployment.

## Install Cert Manager for TLS certificate management and automation

https://cert-manager.io/docs/installation/helm/

## Configure Cert Manager with Let's Encrypt

https://cert-manager.io/docs/configuration/acme/

Keep in mind the specifics will vary depending on how you want it setup. The best method is not HTTP validation of domain ownership but either the cloud native approach or failing that, DNS.

## Install an Ingress Controller

Currently the most fully featured, robust, extensible, and more importantly the only ingress controller configured to work with Telepresence, a remote environment you connect your local to for kubernetes native development, Ingress Controller on the market. Telepresence is owned by Ambassador Labs, and is available with a community license which is always free, with the option to upgrade should you require it.

To this end, there are a lot of unique features unavailable anywhere else and for most organizations the best choice.

Details here: https://github.com/dallinw/ambassador-helm-chart

## Install a Service Mesh

Install a service mesh for intra-cluster mTLS and service-to-service communication. Linkerd was chosen as it is more lightweight than Istio, more performant, and the advanced features that Istio provides are better given by dedicated solutions (CD specifically such as ArgoCD to Spinnaker to be precise).

Details here: https://github.com/dallinw/linkerd-helm-chart

## Celebrate

If you made it here and all is good to go, you now have a functioning cluster!