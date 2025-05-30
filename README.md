# MODULE 11 - 2306170446 - SAMUELLA PUTRI NADIA PAUNTU

1. ![](img/ss1.png)
![](img/ss2.png)
Before exposing the application as a service, the logs only showed the server starting on ports 8080 and 8081. After exposing it, and running the proxy, new log entries began to appear when the app was accessed. Each time the app was opened in the browser, a new GET / request was logged. This indicates that traffic from the proxy is reaching the application pod. The number of GET logs increased with each access, confirming the connection works. This shows that exposing the deployment as a service correctly forwards user requests to the application.

2. ![](img/ss3.png)
The -n option in kubectl stands for namespace. When we use -n kube-system, it tells kubectl to only show resources from the kube-system namespace. This namespace contains system-level components like metrics-server. On the other hand, running kubectl get pods without -n shows resources in the default namespace. That's why the explicitly created pods/services didn't appear when using -n kube-system, they exist in the default namespace. Each namespace isolates resources, so we must specify the correct one to see what we're looking for.







