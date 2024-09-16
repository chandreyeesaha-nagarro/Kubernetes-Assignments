# Kubernetes-Assignments
Nagarro Kubernetes Training Assignment

#Kubernetes Basic Assignment

This project is a simple Spring Boot "Hello, World!" web application deployed to a Kubernetes cluster.

#Steps to Run the Application
#Clone the repository: 
git clone https://github.com/chandreyeesaha-nagarro/Kubernetes-Assignments.git

#Build the docker image:
 
●	docker pull chandreyees20/kubernetes-assignment:01
●	docker build -t chandreyees20/kubernetes-assignment .
     
#Deploy the application to Kubernetes:
●	kubectl apply -f deployment-springbootapp.yml
#Expose the application via a service:
●	kubectl apply -f services-springbootapp.yml
#Access the application:
●	kubectl get services
●	minikube service ‘appname’



