# Prerequisites
* Kubernetes 환경
* Helm 2 혹은 3 설치

## Helm을 이용한 설치
**1.Wavefront helm repo 추가**
~~~
helm repo add wavefront https://wavefronthq.github.io/helm/
helm repo update
~~~

**2. Wavefront Collector 및 Proxy 설치**
- helm 2 사용
~~~
helm install wavefront/wavefront --name wavefront --set wavefront.url=https://YOUR_CLUSTER.wavefront.com --set wavefront.token=YOUR_API_TOKEN --set clusterName=<YOUR_CLUSTER_NAME> --namespace wavefront
~~~

- helm 3 사용
~~~
 kubectl create namespace wavefront
 helm install wavefront wavefront/wavefront --set wavefront.url=https://YOUR_CLUSTER.wavefront.com --set wavefront.token=YOUR_API_TOKEN --set clusterName=<YOUR_CLUSTER_NAME> --namespace wavefront
~~~

Kubernetes 연동 Lab을 정상적으로 완료하셨습니다.