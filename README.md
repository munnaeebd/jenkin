# jenkin
jenkin

## For K8s Deploy

```
kubectl create -f admin.yaml

# Get the token:
 kubectl -n kube-system describe secret $(kubectl -n kube-system get secret | grep kube-admin | awk '{print $1}')
```

from jenkin web-ui-->Manage Jenkins--> Manage Credentials-->global--> add credentials-->kind->secret text--> put token in the secret field--> ID to identify the credential. 

use  this ID to the pipeline "credentialsId" field


