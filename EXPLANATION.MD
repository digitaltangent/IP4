# Kubernetes Objects
I created 7 different kind of objects each with a different purpose:
1) Backend Service - This enables the backend container to intereact with the other containers by mapping the port and making it available as a Cluster IP so that internally it can connect to the other parts of the app
2) Backend Deployment - this is the container for the backend image. It defines where to pull the image from and also sets the environment variable for the backend to be able to connect to the mongo database
3) Client Service - This enables the client container to intereact with the other containers by mapping the port and making it available as a Cluster IP so that internally it can connect to the other parts of the app
4) Client Deployment - this is the container for the client image. It defines where to pull the image from for the client
5) Client Service for Load Balancer - this exposes the IP and port for the client service to an external environment so that the frontened of the eCommerce application can be accessed through a web browser
6) MongoDB Service - This enables the mongodb container to interact with the other containers by mapping the port and making it available as a Cluster IP so that internally it can connect to other parts of the app
7) MongoDB StatefulSet - the statefulset enables us to create the mongodb container and install the mongo image. The use of the statefulset enables us to create persistent volumes for the data, meaning that if we destroy any of the pods in this container, the data will still be saved and can be accessed again by the new pods that are created. 
