  # Managing Multiple Clusters and Namespaces Like a Pro
  This is for creating multi-cluster environment using kind(config-files) and managing multiple clusters and namespaces at once using kind cluster. This is good practice before appearing for CKA exam. it will help you to manage multiple namespaces and clusters like a GURU.

1. Create three cluster of different kubernetes versions.

**dev-cluster-config.yaml**

![image](https://github.com/user-attachments/assets/2089f2b7-8649-4608-ba74-45bdfcee5812)

**staging-cluster-config.yaml**

![image](https://github.com/user-attachments/assets/258377ec-7a57-4309-a611-429f2acb37b8)

**prod-cluster-config.yaml**

![image](https://github.com/user-attachments/assets/14aae2c7-ea90-4e3e-9c3c-9eb58abc2fd2)

Note: you can also check the _config.yaml_ files in the multi-cluster-control-plane directory


2. Set context for individual environments

**Commands:** 

=> kubectl config get-contexts

![image](https://github.com/user-attachments/assets/ad5794d3-93f4-406f-81f3-f3ab7070787b)

=> kubectl config use-context kind-dev-cluster

![image](https://github.com/user-attachments/assets/bd4ef65a-8364-4f4a-bb3e-4b27f77a6632)

=> kubectl config use-context kind-staging-cluster

![image](https://github.com/user-attachments/assets/e9ddd655-f801-4785-9c71-c9cb1b060561)

=> kubectl config use-context kind-prod-cluster
![image](https://github.com/user-attachments/assets/605f4b00-669d-45ab-840c-5340a47ddc5a)


3. Create **namespace** in **kind-dev-cluster** and deploy _nginx_ application in it.

![image](https://github.com/user-attachments/assets/060538e3-fa67-4b93-84c9-3c19e5d494e6)


5. Create **namespace** in **kind-staging-cluster** and deploy _redis_ application in it.
![image](https://github.com/user-attachments/assets/2b76e119-4520-4597-b4dc-f192b5fce924)



7. Create **namespace** in **kind-prod-cluster** and deploy _python3_ application in it.

![image](https://github.com/user-attachments/assets/6be7d779-f021-4375-8282-69567b150fc9)
