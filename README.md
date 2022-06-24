# Nitro


Nitro is a dedicated CLI that empowers python developers to take advantage of kubernetes without the devops overhead. 

- It acts as glue between multiple open source platforms to create a unified developer experience. 
- Allows you to skip all the boilerplate and focus on your application. 

⚠️ This is an experimental project. Please do not launch into your production environment. 

![Containerz Overview (3)](https://user-images.githubusercontent.com/91840749/171413936-28548467-3940-4dd9-9e4d-bfb9a2e89dd8.png)


Requirements for examples
- Language: Python3.8+ 
- Dependency Management:[Poetry](https://github.com/python-poetry/poetry)
- Managed Container Registry: [Dockerhub](https://docs.github.com/en/actions/publishing-packages/publishing-docker-images)
- Managed Kubernetes Cluster: [Azure Container Apps](https://azure.microsoft.com/en-us/services/container-apps/)
- Secrets Management Platform: [Doppler](https://doppler.com/)
- Infrastructure as Code Platform: [Pulumi](https://github.com/pulumi/pulumi)

# Get Started 

```
$ pip install nitro
```
## Declare Environment variables 
  You will need to declare the following variables in the environment. Be sure to safegaurd your secrets using a managed platform or package like [Azure Key Vault](https://azure.microsoft.com/en-us/services/key-vault/), [Doppler](https://doppler.com/join?invite=5F20C8D0), or roll your own with  [dot.](https://pypi.org/project/python-dotenv/)

```  
ARM_CLIENT_ID
ARM_CLIENT_SECRET
ARM_SUBSCRIPTION_ID
ARM_TENANT_ID
AZURE_CREDENTIALS
DOCKERHUB_TOKEN
DOCKERHUB_USERNAME
PULUMI_ACCESS_TOKEN
PULUMI_ORG
PULUMI_PROJECT
PULUMI_STACK_NAME
```
  
```
$ export [env_var_name]=[env_var_value]
```

## Deploy your Image ( Comming Soon ) 

You should have a publically available image ready for deployment. Note `nitro` does not build and push your image for you. 
Use the `docker` cli for those purposes. For help configuring pulumi, doppler, or dockerhub refer to the documentation listed in the requirements section.

```
$ nitro deploy --image <public dockerhub image url> --region <supported region name>
``` 


  
 
