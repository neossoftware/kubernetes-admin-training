
Get all namespaces

```
kubectl get namespaces
```

Get pods in specific namespace

```
kubectl get pods --namespace my-namespace
```

```
kubectl get pods --all-namespaces
```


Create namespace
```
kubectl create namespace my-namespace
```


2. Admin commands

Drain a NODE

```
kubectl drain <node_name> --ignore-daemonsets 
```

vi pod1.yml

kubectl apply -f pod1.yml





GKE sample cluster

gcloud beta container --project "playground-s-11-83826fc3" clusters create "cluster-1" --zone "us-central1-c" --no-enable-basic-auth --cluster-version "1.27.3-gke.100" --release-channel "regular" --machine-type "e2-micro" --image-type "COS_CONTAINERD" --disk-type "pd-balanced" --disk-size "100" --metadata disable-legacy-endpoints=true --scopes "https://www.googleapis.com/auth/devstorage.read_only","https://www.googleapis.com/auth/logging.write","https://www.googleapis.com/auth/monitoring","https://www.googleapis.com/auth/servicecontrol","https://www.googleapis.com/auth/service.management.readonly","https://www.googleapis.com/auth/trace.append" --num-nodes "2" --logging=SYSTEM,WORKLOAD --monitoring=SYSTEM --enable-ip-alias --network "projects/playground-s-11-83826fc3/global/networks/default" --subnetwork "projects/playground-s-11-83826fc3/regions/us-central1/subnetworks/default" --no-enable-intra-node-visibility --default-max-pods-per-node "110" --security-posture=standard --workload-vulnerability-scanning=disabled --no-enable-master-authorized-networks --addons HorizontalPodAutoscaling,HttpLoadBalancing,GcePersistentDiskCsiDriver --enable-autoupgrade --enable-autorepair --max-surge-upgrade 1 --max-unavailable-upgrade 0 --enable-managed-prometheus --enable-shielded-nodes --node-locations "us-central1-c"