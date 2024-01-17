###check nodes 

1 - kubectl get nodes

***Result:

NAME       STATUS   ROLES           AGE     VERSION
master     Ready    <none>          32d     v1.28.2
worker-1   Ready    control-plane   32d     v1.28.2
worker1    Ready    <none>          19d     v1.28.2
worker2    Ready    <none>          3h10m   v1.28.2

2 - kubectl top nodes

***Result:

NAME       CPU(cores)   CPU%   MEMORY(bytes)   MEMORY%   
master     1893m        47%    5934Mi          37%       
worker-1   2123m        53%    13229Mi         83%       
worker1    591m         7%     3534Mi          29%       
worker2    59m          1%     1384Mi          8%        


3 - kubectl get pods

AME                                    CPU(cores)   MEMORY(bytes)   
api-6b5d98c99-5s47z                     0m           52Mi            
ca-orderer-756995db47-f5xqk             0m           8Mi             
ca-org1-ffdbd4899-jq6f7                 0m           4Mi             
ca-org2-58bcccdf75-t4lgz                0m           13Mi            
ca-org3-54b597ffd6-27pfp                0m           3Mi             
chaincode-basic-org1-5cd7dfbcc9-jrj8p   0m           4Mi             
chaincode-basic-org2-6c5f68c97c-s7rf7   0m           5Mi             

***** ( so it means metrics server is installed ) *****

Ref:  https://foxutech.com/horizontal-pod-autoscaler-know-everything-about-it/

