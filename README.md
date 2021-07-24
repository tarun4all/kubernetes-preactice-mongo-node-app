# kubernetes-preactice-mongo-node-app

First we will create mongo DB pod.
Then need internal service of mongo db so that no outsider could join
Then will add Mongo express to access that

To use this in browser, will create external service

values in secret are base encode 64 values,

to generate use "echo -n 'username' | base64"
use `kubectl apply -f mongo-secret.yaml` to generate secret the ref in mongo.yaml

now apply with kubectl apply -f mongo.yaml

same for mongo-express.yaml and configmap

after all applied.

To bind local IP of mongo-express-service cluster
Use: minikube service mongo-express-service
