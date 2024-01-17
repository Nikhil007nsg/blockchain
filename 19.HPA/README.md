###
###create 01_Deloyment.yaml 
 
 1 - apply kubectl command
 
 *** kubectl apply -f 01_Deloyment.yml 
 
 2 - apply kubectl to service
 
 ***** kubectl apply -f 02_Service.yml
 
 3 - apply to hpa
 
 *** kubectl apply -f 03_HPA.yml
 
 ### for increasing thr load apply this command on other tab 
 
 kubectl -n prometheus run -i --tty load-generator --rm --image=busybox --restart=Never -- /bin/sh -c "while sleep 0.01; do wget -q -O- http://hpa-demo-deployment; done"
