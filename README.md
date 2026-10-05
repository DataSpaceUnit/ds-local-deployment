This repository contains the code for the automated deployment of elements of the Zaragoza's data space building blocks.

It is based in Kubernetes and Helm charts.

THe deployment of a working platform is divided in 3 different steps:

- Deploying the common services (POstgres Database, Minio Object Storage, Keycloak Identity Provider), which will be common
to all the platform, and will be shared by all the different deployments.
- Deploying a dataspace, which in its core is nothing more than a set of configurations for the platform and common services, 
and a public website. This deployment will be launched for every dataspace desired in the platform. 
- Deploying a connector, which is the main element that an organization will use to connect their data to the dataspace.
A complete connector is composed by the main backend service and a optionall frontend SPA web interface.

## Requirements

- A Kubernetes cluster (Minikube for local deployment).
- kubectl and helm installed locally. 

## Deploying a dataspace

The dataspace wil deployed using the Helm chart in the `dataspace` folder.
Steps:
- Creating a new namespace for the dataspace.
- Create a Keycloak Realm for the dataspace.
- Deploy the public web portal.

Follow the steps provided in the file DEMO.md

## Deploying a connector

The connector will be deployed using the Helm chart in the `connector` folder.

Follow the steps provided in the file DEMO.md


## Acknowledgements

This project has been funded by the European Union's European Data Space far Smart Communities - DS4SSCC-DEP action under grant agreement no.101123342 in the Digital Europe Programme as part of the Piloting Programme in relation to the Project 2025-3-1 - IPPCP.
It reuses components of the INESData project (Infraestructura para la INvestigación de ESpacios de DAtos distribuidos en UPM), a project funded under the call UNICO I+D CLOUD of Ministerio para la Transformación Digital y de la Función Pública framed within PRTR funded by the Europen Union (NextGenerationEU)

<img height="100" alt="logo-color" src="https://github.com/user-attachments/assets/50712b11-ec2d-4947-8313-a35ffe94fd5d" /> <img src="https://images.squarespace-cdn.com/content/v1/63718ba2d90d0263d7fc1857/415e1aec-464c-4e5a-aa59-4e11ee295281/Logo+Color-min.png?format=300w" height="80"/> <img height="80" alt="EN_Co-fundedbytheEU_RGB_POS" src="https://github.com/user-attachments/assets/826c43cb-e649-436b-be92-1940da9d21fd" /> <br><br>
<img height="150" src="https://github.com/INESData/SHACLGeneratorScripts/blob/f65e39450bc0ec71345705c18ddd4b056dccf34b/logos/ack.png" /> 
