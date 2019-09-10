---
title: Minikube
date: 2019-09-09 17:27:24
tags:
---
Minikube 기본 설정
------------------
1. 설치환경
- macOS Mojave 10.14.6
- Homebrew 설치완료
- Docker For Mac 설치완료
- Node.js 설치완료
2. 설치과정
- Minikube 설치
  >brew cask install minikube
- HyperKit Driver 설치
  >curl -Lo docker-machine-driver-hyperkit https://storage.googleapis.com/minikube/releases/latest/docker-machine-driver-hyperkit \
&& chmod +x docker-machine-driver-hyperkit \
&& sudo cp docker-machine-driver-hyperkit /usr/local/bin/ \
&& rm docker-machine-driver-hyperkit \
&& sudo chown root:wheel /usr/local/bin/docker-machine-driver-hyperkit \
&& sudo chmod u+s /usr/local/bin/docker-machine-driver-hyperkit
- Kubernetes-CLI 설치
  >brew install kubernetes-cli
- Docker 이미지확인
  >docker images
- Minikube 실행
  >minikube start --vm-driver=hyperkit
- Minikube Context 설정
  >kubectl config use-context minikube
- Cluster 정보 확인
  >kubectl cluster-info
- Dashboard 확인
  >minikube dashboard
- Minikube Add-on...
  >minikube addons list
  minikube addons enable [addon-name]
  