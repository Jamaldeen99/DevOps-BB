# TENTH DOCUMENTATION

- Connecting my instance via ssh and cloning the project repository to my instance

![1](shot/1.png)

- The project code is present in the prometheus-observability-stack folder. cd into the folder.
 
![1](shot/2.png)

- Spinning up my ec2 instance and attach the following IAM roles to it:

AmazonVPCFullAccess
AmazonEC2FullAccess

![1](shot/3.png)

![1](shot/4.png)

![1](shot/5.png)

![1](shot/6.png)

![1](shot/7.png)

![1](shot/8.png)

![1](shot/9.png)

![1](shot/10.png)

![1](shot/11.png)

![1](shot/12.png)

- Installing Terraform

![1](shot/13.png)

- Modifying the values of ec2.tfvars file present in the terraform-aws/vars folder

![1](shot/14.png)

![1](shot/15.png)

- Now we can provision the AWS EC2 & Security group using Terraform

![1](shot/16.png)

- Execute the plan and apply the changes.

![1](shot/17.png)

![1](shot/18.png)

![1](shot/19.png)

![1](shot/20.png)

- Connecting to the AWS EC2 machine just created via ssh.

![1](shot/21.png)

![1](shot/22.png)

- Checking the cloud-init logs to see if the user data script has run successfully.

![1](shot/23.png)

- Let’s verify the docker and docker-compose versions again.
]
![1](shot/24.png)

- Cloning the project code repository to the server.

![1](shot/25.png)

![1](shot/26.png)

- - On a successful execution, seeing the following output saying Running 5/5

![1](shot/27.png)

- With my servers IP address, I can access all the apps on different ports.

![1](shot/28.png)
 
![1](shot/29.png)

![1](shot/30.png)

- Accessing the Prometheus dashboard as shown below.

Validating the targets, rules and configurations as shown below. The target would be Node exporter url.

![1](shot/31.png)

![1](shot/32.png)

![1](shot/33.png)

![1](shot/34.png)

![1](shot/35.png)

![1](shot/36.png)

- Executing a promQL statement to view node_cpu_seconds_total metrics scrapped from the node exporter.

![1](shot/37.png)

![1](shot/38.png)

![1](shot/39.png)

- Configuring Grafana dashboards for the Node Exporter metrics.

![1](shot/40.png)

- Adding prometheus URL as the data source from Connections→ Add new connection→ Prometheus → Add new data source.

![1](shot/41.png)

![1](shot/42.png)

![1](shot/43.png)

![1](shot/44.png)

![1](shot/45.png)

![1](shot/46.png)

- To import a dashboard, go to Dashboards –> Create Dashboard –> Import Dashboard –> Type 10180 and click load –> Select Prometheus Data source –> Import

![1](shot/47.png)

![1](shot/48.png)

![1](shot/49.png)

![1](shot/50.png)

![1](shot/51.png)

![1](shot/52.png)

- Simulating & Testing the Alert Manager Alerts

![1](shot/53.png)

- To test the alerts, we need to simulate these alerts using few linux utilities.

![1](shot/54.png)

- Checking the Alert manager UI to confirm the fired alerts.

![1](shot/55.png)

- Rolling back the changes and see the fired alerts has been resolved.

![1](shot/56.png)

[1](shot/57.png)

- Cleaning up The Setup

![1](shot/58.png)

# Completed - THANK YOU
