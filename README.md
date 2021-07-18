# k8s docker desktop

https://kubernetes.io/blog/2019/07/23/get-started-with-kubernetes-using-python/


Mục đích của mình là test việc expose service của docker-desktop windows.

Mình thấy k8s trên docker desktop thực sự expose đc localhost:6000.

điều này đã giúp mình giải đáp đc thắc mắc:
- mình thấy docs và khi search lỗi load balancer ko expose đc external-ip đều nói là load balancer yêu cầu k8s cluster sử dụng cloud provider (AWS, Azure, GCP).  (mình đã sử dụng minikube mà test thì đúng là như vậy)
- nhưng khi thấy trong hdan của https://github.com/noahgift/kubernetes-hello-world-python-flask, tác giả có expose đc ra localhost

=> thực tế là do khi dùng k8s trên docker-desktop thì có thể sử dụng load balancer
