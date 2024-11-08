# k8s-nti-lab4
1- How many ConfigMaps exist in the environment?
```
kubectl get configmap
NAME                DATA   AGE
kube-root-ca.crt    1      11d
```
2- Create a new ConfigMap Use the spec given below.

ConfigName Name: webapp-config-map

Data: APP COLOR=darkblue

3- Create a webapp-color POD with nginx image and use the created ConfigMap

4- How many secrets exist on the system?
```
0
```
5- How many secrets are defined in the default-token secret?

6- create a POD called db-pod with the image mysql 5.7 then check the POD status

7-why the db-pod status not ready

8- Create a new secret named db-secret with the data given below.

Secret Name: db-secret

Secret 1: MYSQL DATABASE=Sql01

Secret 2: MYSQL_USER=user1

Secret3: MYSQL PASSWORD-password

Secret 4: MYSQL_ROOT_PASSWORD=password123

9- Configure db-pod to load environment variables from the newly created secret.

Delete and recreate the pod if required.

10- Create a multi-container pod with 2 containers.

Name: yellow

Container 1 Name: lemon

Container 1 Image: busybox

Container 2 Name: gold

Container 2 Image: redis

11-Create a pod red with redis image and use an initContainer that uses the busybox image and sleeps for 20 seconds

12- Create a pod named print-envars-greeting.

1. Configure spec as, the container name should be print-env-container and use bash image.

2. Create three environment variables:

a. GREETING and its value should be "Welcome to"

b. COMPANY and its value should be "DevOps"

C. GROUP and its value should be "Industries"

4. Use command to echo "$(GREETING) $(COMPANY) $ (GROUP)"] message.

5. You can check the output using <kubet logs -f [ pod-name ]> command.

13- Where is the default kubeconfig file located in the current environment?

14- How many clusters are defined in the default kubeconfig file?

15-What is the user configured in the current context?

16- Create a Persistent Volume with the given specification.

Volume Name: pv-log

Storage: 100Mi

Access Modes: ReadWriteMany

Host Path: /pv/log

17- Create a Persistent Volume Claim with the given specification.

Volume Name: claim-log-1

Storage Request: 50Mi

Access Modes: ReadWriteMany

18- Create a webapp pod to use the persistent volume claim as its storage.

Name: webapp

Image Name: nginx

Volume: PersistentVolumeClaim-claim-log-1

Volume Mount: /var/log/nginx
