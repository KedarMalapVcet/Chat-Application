# Connection

Connection is a Full Stack Chatting App.
Uses Socket.io for real time communication and stores user details in encrypted format in Mongo DB Database.

## Tech Stack

**Client:** React JS

**Server:** Node JS, Express JS

**Database:** Mongo DB

## Demo

<!-- https://talk-a-tive.herokuapp.com/ -->

![](https://github.com/KedarMalapVcet/Chat-Application/blob/master/screenshots/group%20%2B%20notif.PNG)

## Run Locally

Clone the project

```bash
  git clone https://github.com/piyush-eon/mern-chat-app
```

Go to the project directory

```bash
  cd mern-chat-app
```

Install dependencies

```bash
  npm install
```

```bash
  cd frontend/
  npm install
```

Start the server

```bash
  npm run start
```

Start the Client

```bash
  //open now terminal
  cd frontend
  npm start
```

# Features

### Authenticaton

![](https://github.com/piyush-eon/mern-chat-app/blob/master/screenshots/login.PNG)
![](https://github.com/piyush-eon/mern-chat-app/blob/master/screenshots/signup.PNG)

### Real Time Chatting with Typing indicators

![](https://github.com/piyush-eon/mern-chat-app/blob/master/screenshots/real-time.PNG)

### One to One chat

![](https://github.com/piyush-eon/mern-chat-app/blob/master/screenshots/mainscreen.PNG)

### Search Users

![](https://github.com/piyush-eon/mern-chat-app/blob/master/screenshots/search.PNG)

### Create Group Chats

![](https://github.com/piyush-eon/mern-chat-app/blob/master/screenshots/new%20grp.PNG)

### Notifications

![](https://github.com/piyush-eon/mern-chat-app/blob/master/screenshots/group%20%2B%20notif.PNG)

### Add or Remove users from group

![](https://github.com/piyush-eon/mern-chat-app/blob/master/screenshots/add%20rem.PNG)

### View Other user Profile

![](https://github.com/piyush-eon/mern-chat-app/blob/master/screenshots/profile.PNG)

## Made By

-   [@KedarMalapVcet](https://github.com/KedarMalapVcet)














KUBERNETES

-----------------> Kubectl

curl.exe -LO "https://dl.k8s.io/release/v1.25.0/bin/windows/amd64/kubectl.exe"


If there is error, use this
curl.exe -LO "https://dl.k8s.io/release/v1.25.0/bin/windows/amd64/kubectl.exe" --ssl-no-revoke


put --ssl-no-revoke if there is "The revocation function was unable to check revocation for the certificate" error



//////////////////_________________________________________________________________\\\\\\\\\\\\\\\\\\\\\\\\\

full ersion



create file in c drive (kubectl) open in cmd:

curl.exe -LO "https://dl.k8s.io/release/v1.25.0/bin/windows/amd64/kubectl.exe"

curl.exe -LO "https://dl.k8s.io/v1.25.0/bin/windows/amd64/kubectl.exe.sha256"

CertUtil -hashfile kubectl.exe SHA256
type kubectl.exe.sha256

powershell(paste this in powershell) : set path in env var

$($(CertUtil -hashfile .\kubectl.exe SHA256)[1] -replace " ", "") -eq $(type .\kubectl.exe.sha256)

cmd:
kubectl version --client

download minikube 
create folder in c drive (minikube)
set path

open powershell as administrator

Invoke-WebRequest -OutFile 'c:\minikube\minikube.exe' -Uri 'https://github.com/kubernetes/minikube/releases/latest/download/minikube-windows-amd64.exe' -UseBasicParsing

$oldPath = [Environment]::GetEnvironmentVariable('Path', [EnvironmentVariableTarget]::Machine)
if ($oldPath.Split(';') -inotcontains 'C:\minikube'){ `
  [Environment]::SetEnvironmentVariable('Path', $('{0};C:\minikube' -f $oldPath), [EnvironmentVariableTarget]::Machine) `
}

virtual box install

open cmd in minikube folder 

minikube start --driver=virtualbox

minikube config set driver virtualbox

minikube status


then open cmd in kubectl folder


kublectl get nodes

kubectl get po -A

kubectl create deployment hello-minikube --image=docker.io/nginx:123

kubectl get pods

kubectl expose deployment hello-minikube --type=NodePort --port=8080

kubectl get pods

kubectl get service hello-minikube

cmd to minikube 

minikube service hello-minikube --url

cmd to kubectl

kubectl get pods

kubectl run nginx --image=nginx

kubectl get pods

kubectl get deployments

kubectl get services

kubectl delete service hello-minikube

kubectl get services

kubectl get deployments

kubectl delete deployments hello-minikube

kubectl get deployments

kubectl get pods

cmd to minikube

minikube stop
