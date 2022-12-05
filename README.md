---
marp: true
theme: default
style: |
    img[alt~="center"] {
      display: block;
      margin: 0 auto;
    }
---

# En grundläggande kurs i Kubernetes

```
 _  __     _                          _            
| |/ /   _| |__   ___ _ __ _ __   ___| |_ ___  ___ 
| ' / | | | '_ \ / _ \ '__| '_ \ / _ \ __/ _ \/ __|
| . \ |_| | |_) |  __/ |  | | | |  __/ ||  __/\__ \
|_|\_\__,_|_.__/ \___|_|  |_| |_|\___|\__\___||___/


```
##### presenterad av Dominic Chan, dominic.chan@knowit.se

---

Mentimeter - gå till menti.com och ange koden: 4241 7027

---

| Deltagare 	| AWS host	|
|-----------	|----------	|
| Azeb      	|       	|
| Dennis    	|  	|
| Erik      	|  	|
| Emelie    	|  	|
| Johan B   	|  	|
| Johan Å   	|  	|
| Jonathan  	|  	|
| Patrik    	| 	|
| Simon     	|  	|
| Sofie     	|  	|
| Louise B  	|  	|
| Louise J  	|  	|
| Josefine  	|  	|
| Emil Ö    	|  	|
| Emil T    	|  	|
| Olof      	| 	|
| Frida     	|  	|
| Jennifer  	|  	|
| John      	| 	|
| Extra 1   	|  	|
| Extra 2   	| 	|
| Extra 3   	| 	|
| Extra 4   	| 	|
| Extra 5   	| 	|
| Extra 6   	| 	|

---

# Vad är Docker?

- Containrar är som snabba och lättviktiga virtuella maskiner.
- Docker gör det enkelt att bygga och köra våra applikationer i containrar.
- docker start | stop | delete

---

# Vad är K8s

- Kubernetes (helmsman) "Rorsman" 
- Orkestrerar container via container runtime t.ex. Docker
- deploy | scale | heal

---

# Google - containers
![h:400px center](./images/google_container.png)


---

# Omega / Borg
![h:400px center](./images/borg_omega.png)


---

# Cloud Native Opensource
![h:400px center](./images/cloud_native_k8s.png)

---

# SSH till er AWS instans

`ssh -i ~/.ssh/aws-linux-demo.pem ubuntu@ubuntu@ec2-16-171-26-141.eu-north-1.compute.amazonaws.com`

---

# Installera Minikube

`cd knowit-kubernetes-kurs`
`cat minikube.sh`
`sudo chmod +x minikube.sh`
`./minikube.sh`

---

# Lista alla namespaces

Använd kommandot `kubectl get ns`

---

# Lista alla nodes

Använd kommandot `kubectl get nodes`

---

# Lista alla pods

Använd kommandot `kubectl get pods`

`kubectl get pods -n kube-system`

---

# Kör en deploy med Nginx

Kör kommandot `kubectl create deployment nginx-deploy --image=nginx`

---

# Lista deployment

Använd kommandot `kubectl get deployment`

---

# Exponera deployment genom att skapa en service

Kör kommandot `kubectl expose deployment nginx-deploy --port=8080`
`kubectl get svc nginx-deploy`

---

# Ändra targetPort till 80

`kubectl edit svc nginx-deploy`
`i` för Insert mode
`ESC` och sedan `:wq!` för att spara och gå ut

---

# Skapa en proxy till klustret

Använd kommandot ``

---

# Testa göra anrop till den nya deployment

Kör kommandot `curl localhost:8080`


---

# Skala upp deployment

Använd kommandot `kubectl scale deployment nginx-deploy --replicas=10`

---

# Skala ned deployment

Använd kommandot `kubectl scale deploment nginx-deploy --replicas=2`

---

#

---

# Övningar:
1. Starta container imagen bkimminich/juice-shop som lyssnar på port 3000.
2. Testa att containern bkimminich/juice-shop körs.
3. Stoppa containern som du startade i steg 1.

---


# Avslut och utvärdering:

Mentimeter - gå till menti.com och ange koden: 2179 658 

---
