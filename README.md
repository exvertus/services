# Tom's Services
Internal services page code for personal and friends' projects

* See env.shadow for needed env vars
* Running on [nginx](https://www.nginx.com/) webserver
    * Build Dockerfile with ```docker build -t $SVCS_SITE_IMG .```
    * And push ```docker push $SVCS_SITE_IMG```
* Hosted on [GKE](https://cloud.google.com/kubernetes-engine)
    * Deploy with ```cat k8s-config.yaml | envsubst | kubectl apply -f -```
    * Test service with ```kubectl port-forward service/landing-page -n services 8080:8080 >> /dev/null```
