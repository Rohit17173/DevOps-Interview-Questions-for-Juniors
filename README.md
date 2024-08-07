<p align="center">
	<img width="600" src="https://github.com/Ahmed-Moourad/DevOps-Interview-Questions-for-Juniors/assets/112473376/c2adb7f2-3245-4654-bb88-0b7102f2ce55" alt="DevOps Q&A">
</p>

# DevOps Interview Questions for Juniors
> DevOps Interview Questions and Answers for Junior DevOps Engineers 

**Disclaimer:**
- You are welcome to edit and add Questions/answers through Pull Request
- These questions are for the Junior/beginner in the DevOps field
- These questions are not for specific companies/entities, this cover the most popular DevOps tools, and these tools may vary from one company to another based on the technology stack used by it .. so you need to check the job requirements for the position you are applying and focus on what is there.

<h3 align="left">Included Tools:</h3>
<p align="left"> <a href="https://github.com/Ahmed-Moourad/DevOps-Interview-Questions-for-Juniors#aws-questions" target="_blank" rel="noreferrer"> <img src="https://raw.githubusercontent.com/devicons/devicon/master/icons/amazonwebservices/amazonwebservices-original-wordmark.svg" alt="aws" width="40" height="40"/> </a> <a href="https://github.com/Ahmed-Moourad/DevOps-Interview-Questions-for-Juniors#docker-questions" target="_blank" rel="noreferrer"> <img src="https://raw.githubusercontent.com/devicons/devicon/master/icons/docker/docker-original-wordmark.svg" alt="docker" width="40" height="40"/> </a> <a href="https://github.com/Ahmed-Moourad/DevOps-Interview-Questions-for-Juniors#linux-questions" target="_blank" rel="noreferrer"> <img src="https://raw.githubusercontent.com/devicons/devicon/master/icons/linux/linux-original.svg" alt="linux" width="40" height="40"/> </a> <a href="https://github.com/Ahmed-Moourad/DevOps-Interview-Questions-for-Juniors#general-questions" target="_blank" rel="noreferrer"> <img src="https://www.vectorlogo.zone/logos/gnu_bash/gnu_bash-icon.svg" alt="bash" width="40" height="40"/> </a> <a href="https://github.com/Ahmed-Moourad/DevOps-Interview-Questions-for-Juniors#kubernetes-questions" target="_blank" rel="noreferrer"> <img src="https://www.vectorlogo.zone/logos/kubernetes/kubernetes-icon.svg" alt="kubernetes" width="40" height="40"/> </a> <a href="https://github.com/Ahmed-Moourad/DevOps-Interview-Questions-for-Juniors#general-questions" target="_blank" rel="noreferrer"> <img src="https://www.vectorlogo.zone/logos/git-scm/git-scm-icon.svg" alt="git" width="40" height="40"/> </a> <a href="https://github.com/Ahmed-Moourad/DevOps-Interview-Questions-for-Juniors#general-questions" target="_blank" rel="noreferrer"> <img src="https://www.vectorlogo.zone/logos/jenkins/jenkins-icon.svg" alt="jenkins" width="40" height="40"/> </a> Terraform,</a> Ansible, </a> and more coming ... 



## AWS Questions:

1. **What’s EC2 Instance types?**

	- General-Purpose Instances: General purpose instances provide a balance of compute, memory and networking resources, and can be used for a variety of diverse workloads. These instances are ideal for applications that use these resources in equal proportions such as web servers and code repositories. it has mainly m4 to m7 instance family as well as t2 and t3 instance family ( have equally distibited resources )
	- Memory-Optimized Instances : Memory optimized instances are designed to deliver fast performance for workloads that process large data sets in memory. it has mainly R4 to R7 instance family  (Large Amounts of RAM:)
	- Compute-Optimized Instances : Compute Optimized instances are ideal for compute bound applications that benefit from high performance processors. Instances belonging to this category are well suited for batch processing workloads, media transcoding, high performance web servers, high performance computing (HPC), scientific modeling, dedicated gaming servers and ad server engines, machine learning inference and other compute intensive applications. it has c4 to c7 insance family (have Enhanced cpu and the cpu utilisation resources are high)
 	- Accelerated Computing :Accelerated computing instances use hardware accelerators, or co-processors, to perform functions, such as floating point number calculations, graphics processing, or data pattern matching, more efficiently than is possible in software running on CPUs. (significant power is the GPU (Graphics Processing Unit))
	- Storage Optimized Instances : Storage optimized instances are designed for workloads that require high, sequential read and write access to very large data sets on local storage. They are optimized to deliver tens of thousands of low-latency, random I/O operations per second (IOPS) to applications. (Large Local Storage: , High I/O Performance:, Optimized for Low Latency)
 	- HPC Optimized : High performance computing (HPC) instances are purpose built to offer the best price performance for running HPC workloads at scale on AWS. HPC instances are ideal for applications that benefit from high-performance processors such as large, complex simulations and deep learning workloads.it has Hpc6 and Hpc7 instance family.( CPU, GPU, networking capabilities, Large Memory Capacity) 

![image](https://github.com/Ahmed-Moourad/DevOps-Interview-Questions-for-Juniors/assets/112473376/f1cd6e00-8218-4d26-9f0e-066be57576e8)

	
 2. **What’s VPC?**
A VPC is a virtual network that closely resembles a traditional network that you'd operate in your own data center. it is logically isolated area in the aws cloud which has its own networking .

3. **What’s S3 bucket and what types of it?**
Amazon S3 is an object storage service that stores data as objects within buckets. An object is a file and any metadata that describes the file. A bucket is a container for objects.

	***Types(storage classes):***
	- S3 Standard: for frequently accessed data
	- S3 Intelligent-Tiering: for automatic cost savings for data with unknown or changing access patterns
	- S3 Standard-Infrequent Access (S3 Standard-IA) and S3 One Zone-Infrequent Access (S3 One Zone-IA) for less frequently accessed data,
	- S3 Glacier Instant Retrieval for archive data that needs immediate access
 	- S3 Glacier Flexible Retrieval (formerly S3 Glacier) for rarely accessed long-term data that does not require immediate access
  	- Amazon S3 Glacier Deep Archive (S3 Glacier Deep Archive) for long-term archive and digital preservation with retrieval in hours at the lowest cost storage in the cloud. If you have data residency requirements that can’t be met by an existing AWS Region 

4. **Is there a difference between SG and NACL?**
Security groups are associated with an instance of a service. It can be associated with one or more security groups that have been created by the user. (Stateful)
A security group can be understood as a firewall to protect EC2 instances.
NACL can be understood as the firewall or protection for the subnet. (stateless)

5. **What’s the difference between Public Subnet and Private Subnet?**
The instances in the public subnet can send outbound traffic directly to the internet.(Via Internet Gatway).
Whereas the instances in the private subnet can't. Instead, the instances in the private subnet can access the internet by using a network address translation (NAT) gateway that resides in the public subnet.

6. **How can an application access Internet without receiving requests from the internet?**
Using NAT configured in the Routing Table.
The database servers can connect to the internet for software updates using the NAT gateway, but the internet cannot establish connections to the database servers.

  
7. **Design Architecture for web application contains 3 tiers: Frontend, Backend, and Database?**

  ![image](https://github.com/Ahmed-Moourad/DevOps-Interview-Questions-for-Juniors/assets/112473376/cc5d5560-885f-42a0-8a9c-371baff370ac)


  

8. **How you can cost optimize  your infrastructure?**
obtaining the best pricing and terms for IT purchases, standardizing, simplifying, and rationalizing assets such as platforms and applications, as well as processes and services, automating and digitalizing both the IT and business operations. Monitor billing · Reduce manual processes

  

	**On AWS** : 
	- stop guessing capacity (use Autoscaling Group).
	- Choose the right pricing models.
	- Use Reserved Instances (RI) to reduce RDS, Redshift, ElastiCache, and Elasticsearch costs.
	- Match Capacity with Demand.
	- Identify Amazon EC2 instances with low utilization and reduce cost by stopping or rightsizing.
	- Implement processes to identify resource waste.

  

9. **What are the types of Database engines on AWS?**
	- Amazon RDS is available on several database instance types - optimized for memory, performance, or I/O – and provides you with **six familiar database engines** to choose from, including: 
Amazon Aurora, PostgreSQL, MySQL, MariaDB, Oracle Database, and SQL Server.
	- Ledger: Amazon Quantum Ledger Database (Amazon QLDB)
	- Document: Amazon DocumentDB (with MongoDB compatibility)
	- No SQL: DynamoDB
	- In-memory: Amazon ElastiCache
	- Graph: Amazon Neptune

  

10. **What’s the difference between AWS Shield vs AWS WAF vs AWS Guard-Duty?**

	**Shield** is DDoS protection and is also located "at the edge".

	**AWS WAF** focuses on Layer 7 protection(Application Layer)
Your subscription to Shield Advanced covers the basic AWS WAF fees for web ACLs, rules, and web requests.

	**GuardDuty** is intelligent threat detection. That means without much configuration, it reads your CloudTrail, Config, and VPC FlowLogs and notifies you if something unexpected happened.

	**Amazon Inspector** is more for applications. It's an automated security assessment service that helps improve the security and compliance of applications.

  

11. **What’s the difference between S3 vs EBS vs EFS?**
**S3**: Object Storage
**EBS**: File System Storage (Connected to one EC2) scalable network file storage
**EFS**: scalable network file storage (Can be connected to many EC2)

  
12. **Is it possible to host an application on S3?**
Only one can host a static website on Amazon S3.
by configuring your bucket for website hosting and then uploading your content to the bucket.

  

13. **What’s SSM ?**
Amazon EC2 Simple Systems Manager (SSM) is a tool that allows an IT professional to automatically configure virtual servers in a cloud or in an on-premises data center. Need to install an agent.

  

14. **What is the difference between Latency Based Routing and Geo DNS in Route53?**
Amazon maps out typical latency between IP addresses and AWS regions.
	- Choose Latency-based Routing to have the fastest response.
	- Geolocation maps the IP addresses to geographic locations. This permits rules like "send all users from Côte d'Ivoire to the website in France", so they see a language-specific version.

  

15. **What is RTO and RPO in AWS?**
**RTO** (Recovery Time Objective): is a measure of how quickly can your application recover after an outage
**RPO** (Recovery Point Objective): is a measure of the maximum amount of data loss that your application can tolerate.

  
16. ** What are DevOps tools on AWS?**
	- AWS CodePipeline: Software Release Workflows
	- AWS CodeBuild: Build and Test Code
	- AWS CodeDeploy: Deployment Automation
	- AWS CodeStar: Unified CI/CD Projects
	- AWS CodeCommit: Private Git Hosting
	- Lambda, Amazon Elastic Container Registry (ECR), Amazon Elastic Kubernetes Service (EKS)


17. **What is VPC peering?**
A virtual private cloud (VPC) is a virtual network dedicated to your AWS account. It is logically isolated from other virtual networks in the AWS Cloud. You can launch AWS resources, such as Amazon EC2 instances, into your VPC.

A VPC peering connection is a networking connection between two VPCs that enables you to route traffic between them using private IPv4 addresses or IPv6 addresses. Instances in either VPC can communicate with each other as if they are within the same network. You can create a VPC peering connection between your own VPCs, or with a VPC in another AWS account. The VPCs can be in different Regions (also known as an inter-Region VPC peering connection).


18. **What is VPC Flow Logs?**
You can create a flow log for a VPC, a subnet, or a network interface. If you create a flow log for a subnet or VPC, each network interface in that subnet or VPC is monitored. Flow log data can be published to the following locations: Amazon CloudWatch Logs, Amazon S3, or Amazon Kinesis Data Firehose.Flow logs can help you with a number of tasks, such as:
	- Diagnosing overly restrictive security group rules
 	- Monitoring the traffic that is reaching your instance
  	- Determining the direction of the traffic to and from the network interfaces  

19. **How Many Buckets can be created in s3 ?**
in S3 100 buckets can be created in aws account.


20. **How Many Elastic ip can be created in aws ?**
there are 5 ELastic ip can be created in aws account.


21. **in vpc how many ip address ae reseved by aws ? **
In any given VPC, 5 IP addresses are reserved by AWS. In the above VPC with CIDR 10.0. 0.0/16, the following are reserved by AWS.
	- 10.0.0.0: Network address.
 	- 10.0.0.1: Reserved by AWS for the VPC router.
  	- 10.0.0.2: Reserved by AWS for DNS
	- 10.0.0.3: Reserved by AWS for future use.
 	- 10.0.0.255: Network broadcast address- Broadcast is not supported in VPC but, AWS reserves this IP address.

22. **What are Regions, Edge location and Availability Zones in aws?**
Regions: A region is a geographical area which consists of 2 or more availability zones. A region is a collection of data centers which are completely isolated from other regions.

Availability zones: An Availability zone is a data center that can be somewhere in the country or city. Data center can have multiple servers, switches, firewalls, load balancing. The things through which you can interact with the cloud reside inside the Data center.
Edge Locations: Edge locations are the endpoints for AWS used for caching content. it stores the recent searched static data in the edge location and delivers to the user when it searched again and the other data or processing is loaded to user from the server which makes faster acces to the websites.
  

23. **What is the minimum and maximum size that you can store in S3?**
The minimum size of an object that you can store in S3 is 0 bytes and the maximum size of an object that you can store in S3 is 5 TB.


24. **What are EBS Volumes?**
Elastic Block Store is a service that provides a persistent block storage volume for use with EC2 instances in aws cloud. EBS volume is automatically replicated within its availability zone to prevent from the component failure. It offers high durability, availability, and low-latency performance required to run your workloads


25. **What is Auto Scaling?**
Auto Scaling is a feature in aws that automatically scales the capacity to maintain steady and predictable performance. While using auto scaling, you can scale multiple resources across multiple services in minutes. If you are already using Amazon EC2 Auto- scaling, then you can combine Amazon EC2 Auto-Scaling with the Auto-Scaling to scale additional resources for other AWS services.


26. **What are the main elements of Bucket policy**
 	- Sid: A Sid determines what the policy will do. For example, if an action that needs to be performed is adding a new user to an Access Control List (ACL), then the Sid would be AddCannedAcl. If the policy is defined to evaluate IP addresses, then the Sid would be IPAllow.
	- Effect: An effect defines an action after applying the policy. The action could be either to allow an action or to deny an action.
	- Principal: A Principal is a string that determines to whom the policy is applied. If we set the principal string as '*', then the policy is applied to everyone, but it is also possible that you can specify individual AWS account.
	- Action: An Action is what happens when the policy is applied. For example, s3:Getobject is an action that allows to read object data.
	- Resource: The Resource is a S3 bucket to which the statement is applied. You cannot enter a simply bucket name, you need to specify the bucket name in a specific format. For example, the bucket name is javatpoint-bucket, then the resource would be written as "arn:aws:s3""javatpoint-bucket/*".


27. **What is the maximum size of messages in SQS?**
The maximum size of message in SQS IS 256 KB.


28. **How many subnets can you have per VPC?**
You can have 200 subnets per VPC.

28. **How many vpc can you have per region?**
You can have 5 vpc per region.

29. **Explain the type of auto scalling?**
	- vertical scaling: Vertical scaling means scaling the compute power such as CPU, RAM to your existing machine
	- Horizontal Scallling:horizontal scaling means adding more machines to your server or database. Horizontal scaling means increasing the number of nodes, and distributing the tasks among different nodes. Horizontally scalable systems are oftentimes able to outperform vertically scalable systems by enabling parallel execution of workloads and distributing those across many different computers.



30. **How can you login/recover to an ec2 instance for which you have lost the key?**

Steps
	- Check the Ec2Config Service
 	- Remove the instance root volume
  	- Connect your volume to a temporary instance
   	- Change the configuration file
    	- relaunch the origional instance


32. **What is Load Balancer and What are the types of load balancer?**
In the context of Amazon Web Services (AWS), Elastic Load Balancing (ELB) is a managed service that acts as a load balancer. It automatically distributes incoming traffic across multiple resources, such as EC2 instances, containers, or Network Load Balancers, within your VPC (Virtual Private Cloud).

31. **What is Application load Balancer load balancer?**
 - An Application Load Balancer (ALB) is a type of load balancer offered by Amazon Web Services (AWS) within its Elastic Load Balancing (ELB) service.
 - It operates at the application layer (layer 7).
 - An Application Load Balancer makes routing decisions at the application layer (HTTP/HTTPS).
 - supports path-based routing Path-based routing: Route requests to different backend resources based on specific URL paths. it is achieved through listner
 - and can route requests to one or more ports on each container instance in your cluster.
 - Host-based routing: Route traffic based on the hostname specified in the request.
 - Sticky sessions: Maintain user sessions on the same backend instance for consistent user experience.
 - It automatically distributes incoming traffic across multiple resources, such as EC2 instances, containers, or Lambda functions.


 31. **What is Network load Balancer ?**
 - An Network Load Balancer (ALB) is a type of load balancer offered by Amazon Web Services (AWS) within its Elastic Load Balancing (ELB) service.
 - A Network Load Balancer functions at the fourth layer (network layer) of the Open Systems Interconnection (OSI) model.
 - It operates at layer 4 of the Open Systems Interconnection (OSI) model, meaning it distributes incoming network traffic across multiple resources (e.g., EC2 instances, containers, or Network Load Balancers) based on IP addresses and ports. This ensures efficient utilization of resources and improved performance for your applications.
 - It can handle millions of requests per second.
 - routing traffic based on IP addresses and ports. it is designed to handle high throughtput, low lagtency trafic.
 - it is suitable for the tcp/udp and tls traffic and i often used for extreme performance scenarios.


31. **What is Gateway load Balancer ?**
    - A Gateway Load Balancer operates at the third layer of the Open Systems Interconnection (OSI) model,the network layer.
    - A gateway load balancer is a specific type of load balancer designed to distribute traffic across multiple virtual network appliances (NVAs) in a network , such as firewalls, intrusion detection and prevention systems, and deep packet inspection systems.
    - It acts as a single entry and exit point for all traffic, ensuring that incoming requests are efficiently routed to the appropriate NVA based on predefined rules.
    - helps you run and scale 3rd party applications.
    - The Gateway Load Balancer and its registered virtual appliance instances exchange application traffic using the GENEVE(Generic Network Virtualization Encapsulation
Abstract) protocol on port 6081.

33. **What are the routing policies in the route53?**
	- Simple Routing:
		- The most basic policy, it's suitable for single resource setups. It directs all traffic for a specific domain or subdomain to the resource record's IP address (e.g., A record for a web server).
  		- use asimple routing policy when we have a single resource that performs a given function for your domain. 
	-  Failover Routing:
		- Ensures high availability by providing a backup resource in case the primary resource becomes unavailable. Route 53 routes traffic to the primary resource by default. If the health checks detect an issue with the primary, it automatically switches traffic to the healthy backup resource.
  	- Weighted Routing:
 		- Distributes traffic across multiple healthy resources based on pre-defined weights. You assign a weight to each resource record, determining the percentage of traffic it receives. This allows for load balancing among resources with varying capacities.

	- Latency-based Routing:
    		 - Routes traffic to the resource that provides the lowest latency (response time) for the user's location. Route 53 considers the geographic location of your resources and the user's IP address to determine the optimal route.
   	- Geolocation Routing:
      		 - Directs traffic to the resource that's geographically closest to the user's location. This can improve user experience by reducing latency, especially for geographically distributed resources.
  	- GeoProximity Routing (Traffic Flow only):
     		 - A variation of geolocation routing, it's specifically designed for Route 53 Traffic Flow, a premium routing control feature. It allows you to route traffic based on the proximity of your resources, not just the user's location. This is useful for scenarios where resources are geographically dispersed and latency optimization is crucial.
	- Multivalue Answer Routing:
   		- Provides redundancy by returning multiple healthy resource records in the DNS response. This allows clients to choose the optimal resource based on their own criteria (e.g., round robin selection).     

      			 

35. **Difference between Dedicated Host And Dedicated instace?**

36. **Define the purchasing options in instance?**

36. **What is AMI aand its types**
37. **What is template**
38. **what is nat gateway**
39. **load balancer , auto scalling, state, configuration**
40. **s3 lifecycle rule/storage types**
41. **static:min=max=desired/dynamic:min!=max!=desired/scheduled autoscaling**
42. **load balancer**
43. **vpc NAT Gateway**
44. **what is elastic ip=static public ip**
45. **diff nat gateway nat instance**
 nat gateway = service of aws vpc
43. **VPC endpoint**
44. **all limitations**
45. **alarms, log management, metrics , events**
46. **we strem logs in aws cloudwatch**
47. **routing policies and dns records**
48. ****

## linux

how to set the permission for the rohit user to use the command dmidecode?
rohit ALL=(ALL) NOPASSWD: /usr/sbin/dmidecode

How to resolve the error in linux booting process?
What to do when there is error at starting of the linux operating system and message comes as epress ctrl + d?
how to troubleshoot the network?
all networking commands?
how to show the linux file with highest size at top?
how to remove the disk from the server? and if used umount command then there is errror called the busy how will you deal with it?

## DEVOPS
47. **routing policies and dns records**
48. how to execute the next stage in jenkins pipline even if there one stage is failing

  ``` pipeline {
    agent any
    stages {
        stage('1') {
            steps {
                sh 'exit 0'
            }
        }
        stage('2') {
            steps {
                catchError(buildResult: 'SUCCESS', stageResult: 'FAILURE') {
                    sh "exit 1"
                }
            }
        }
        stage('3') {
            steps {
                sh 'exit 0'
            }
        }
    }
}
```

50. how to execute if else block of based pipeline in jenkins
```
pipeline {
    agent any

    stages {
        stage('Example') {
            steps {
                script {
                    // Define variables or conditions
                    def condition = true
                    def anotherCondition = false

                    // Example of if-else block
                    if (condition) {
                        echo 'Condition is true'
                        // Perform actions if condition is true
                    } else if (anotherCondition) {
                        echo 'Another condition is true'
                        // Perform actions if another condition is true
                    } else {
                        echo 'Neither condition is true'
                        // Perform default actions if no condition is true
                    }
                }
            }
        }
    }
}
```


51. how to clear the workspace after every build
52. if there are not any files present in the workspace then how to resolve this error
53. Describe when and expression in Declarative Pipeline.
```
pipeline {
    agent any
    stages {
        stage('Build') {
            steps {
                echo 'Building...'
                // Build steps
            }
        }
        stage('Test on master') {
            when {
                branch 'master'
            }
            steps {
                echo 'Running tests on master branch...'
                // Test steps
            }
        }
        stage('Deploy to production') {
            when {
                allOf {
                    branch 'master'
                    environment name: 'DEPLOY_ENV', value: 'production'
                }
            }
            steps {
                echo 'Deploying to production...'
                // Deploy steps
            }
        }
        stage('Conditional based on expression') {
            when {
                expression {
                    return env.BUILD_NUMBER.toInteger() % 2 == 0
                }
            }
            steps {
                echo 'Running because build number is even...'
                // Steps to run if condition is met
            }
        }
    }
}
```


54. how to clean the workspace after every build
```
pipeline {
    agent any
    stages {
        stage('Build') {
            steps {
                cleanWs()
                echo 'Building...'
                // Build commands
            }
        }
        stage('Test') {
            steps {
                echo 'Testing...'
                // Test commands
            }
        }
    }
    post {
        always {
            cleanWs()
        }
    }
}
```


55. explain parallel pipeline in jenkins
```
pipeline {
    agent any
    stages {
        stage('Parallel Stage') {
            parallel {
                stage('Task 1') {
                    steps {
                        echo 'Running Task 1'
                        // Task 1 commands go here
                    }
                }
                stage('Task 2') {
                    steps {
                        echo 'Running Task 2'
                        // Task 2 commands go here
                    }
                }
                stage('Task 3') {
                    steps {
                        echo 'Running Task 3'
                        // Task 3 commands go here
                    }
                }
            }
        }
    }
}
```
56. you see the execution of the jenkins server is slow how will you troubleshhot the jenkins server?

Check System Resources
CPU and Memory Usage 
```
top
htop
```
Free Memory: 
```
free -m
```
Disk Usage: 
```
df -h
```
Analyze Jenkins Logs
```
tail -f /var/log/jenkins/jenkins.log
```
Review Jenkins Configuration
Number of Executors: Adjust the number of executors to match your hardware capabilities.
rust
Build History: Clean up old builds that are no longer needed.
Plugin Management: Remove or update unused plugins.
Check Network and Disk I/O :
Disk I/O: Use tools like iostat to check for disk I/O issues
```
iostat -xz 1 10
```
 Update Jenkins and Plugins
Review Job Configuration
Parallel Jobs:
Limit the number of parallel jobs to prevent overloading the server.
Heavy Jobs:
Identify and optimize jobs that consume a lot of resources.









## Docker Questions:
1. write all docker commands
2. 

  

17. **What’s the difference between container vs VM?**

![image](https://github.com/Ahmed-Moourad/DevOps-Interview-Questions-for-Juniors/assets/112473376/e5eb4f75-82d4-4b39-8ac7-e5c5a428fb0d)

**VM**: uses separate OS for each VM
**Containers**:
- Use the Host OS
- Less utilization
- Your app is backed in a container and shared between environments: DEV, TEST, OPERATION
- Less size
- Fast boot up
containers abstract application layer, vm abstract os

  

18. **What are Docker Image layers?**
Layers are a result of the way Docker images are built. Each step in a Dockerfile creates a new “layer” that’s essentially a diff of the filesystem changes since the last step.
Metadata instructions such as LABEL and MAINTAINER do not create layers because they don’t affect the filesystem.

  

19. **What’s the difference between Entrypoint and CMD?**
**CMD** describes the default container parameters or commands. The user can easily override the default command when you use this.

	**ENTRYPOINT** - A container with an ENTRYPOINT is preferred when you want to define an executable.
You can only override it if you use the --entrypoint flag
entrypoint not override, CMD overwrite with before actions

	**RUN** - To run this command you will need a separate new layer and this command is mainly used to build images, and install packages and applications.

	CMD commands are ignored by Daemon when there are parameters stated within the docker run command while ENTRYPOINT instructions are not ignored but instead are appended as command line parameters by treating those as arguments of the command

  

20. **What are multiple base images on Dockerfile?**
	It allows you to create multiple image layers on top of the previous layers and the **AS** command provides a virtual name to the intermediate image layer. The last FROM command in the dockerfile creates the actual final image
- the idea that you have two images, the first one you build your binaries files and copy them to the second one, and the second image is the final image which from it you run your container. the first image helped you to build the second one.
- The benefits you get from this are that you built your app on a large image and the final result is a lightweight image that is on your containers.  

<img width="306" alt="image" src="https://github.com/Ahmed-Moourad/DevOps-Interview-Questions-for-Juniors/assets/112473376/2736c1b5-540a-40a4-833d-d38efaf2dc0e">


  

21. **What are types of Docker volumes?**
**Named volumes** have a specific source from outside the container, for example, awesome:/bar.

	**Anonymous volumes** have no specific source, therefore, when the container is deleted, you can instruct the Docker Engine daemon to remove them.
	
	bind volumes, tmpfs volumes

	 **Types of Mount** : 
	1. Volumes
	2. Bind mounts
	3. tmpfsmounts
	4. named pipes

  

22. **What are the types of Docker networks?**
bridge, overlay, host, none

23. **What’s the difference between CMD and ENtryPoint?**
    cmd : command will execute only recent and only one from the dockerfile and if a command is passed while creating the container it will replace the cmd inside dockerfile only command passed through command line will be executed
    EntryPoint : this can be run multiple times in a dockerfile and it executes the command inside it.

23. **What’s the difference between COPY and ADD?**

	**COPY** takes in a source and destination. It only lets you copy in a local or directory from your host (the machine building the Docker image) into the Docker image itself.
	
	**ADD** does the same but in addition, it also supports 2 other sources:
A URL instead of a local file/directory. &&&& Extract tar from the source directory into the destination.





24. **How could you secure your Dockerfile?**
	- Run the container as a non-root user. ...
	- Remove unnecessary packages/software from the image. ...

	Enable Docker Content Trust (DCT) ... Content trust is disabled by default in the Docker Client. To enable it, set the DOCKER\_CONTENT\_TRUST environment variable to 1. This prevents users from working with tagged images unless they contain a signature.
	- Use COPY instead of ADD in Dockerfile. ...
	- Do not store any secrets in Dockerfile. ...
	- Install verified packages and use trusted base images.
\-----

	1. Continuous Approach. ...
	2. Image Vulnerabilities. ...
	3. Policy Enforcement. ...
	4. Create a User for the Container Image. ...
	5. Use Trusted Base Images for Container Images. ...
	6. Do Not Install Unnecessary Packages in the Container. ...
	7. Add the HEALTHCHECK Instruction to the Container Image.

25. **What are the Stages of DevSecOps?**
To adapt, software development, maintenance, and upgrading must incorporate security awareness into each stage.

	- Plan. The planning phases of DevSecOps are the least automated with the involvement of collaboration, discussion, review, and a strategy for security analysis. ...
	- Code. ...
	- Build. ...
	- Test. ...
	- Release. ...
	- Deploy. ...
	- Operation. ...
	- Monitor.

  
<img width="460" alt="image" src="https://github.com/Ahmed-Moourad/DevOps-Interview-Questions-for-Juniors/assets/112473376/57c095a5-d0d5-4315-9854-17fb10b08706">
  

## Linux Questions:

  

26. **What’s the difference between Reverse Proxy and Web Server?**

	**A web server** listens for HTTP requests and reacts to them by sending back an HTTP response.
	
	**A reverse proxy** is a web server that determines what response to make by also implementing an HTTP client. Client A makes an HTTP request to the reverse proxy. The reverse proxy makes an HTTP request to Server B.

Reverse proxies are typically implemented to help increase security, performance, and reliability.

  

<img width="353" alt="image" src="https://github.com/Ahmed-Moourad/DevOps-Interview-Questions-for-Juniors/assets/112473376/bc363971-d20d-423e-9382-20d2b11ccfd0">



27. **How can optimize performance for Nginx?**

	**7 Tips for NGINX Performance Tuning**:
	Tip 1 – Adjust Worker Processors & Worker Connections.
	Tip 2 – Enabling Gzip Compression.
	 Tip 3 – Change static content caching duration on Nginx.
	Tip 4 – Change the size of the Buffers.
	Tip 5 – Reducing Timeouts.
	Tip 6 – Disabling access logs (If required)
Tip 7 – Configure HTTP/2 Support.



29. **How can list all processes?**

		ps
		ps -A
		ps -e

	There is `top` also not for all

30. **How can list live processes?**

	    ps -aux | less

31. **How could you check memory space?**

	    cat /proc/meminfo

	  `	free` >>> checks memory and SWAP memory


32. **How could you check storage space?**	
		
    df -H

  
33. **What’s file management in Linux?**
	In Linux, most of the operations are performed on files. And to handle these files Linux has directories also known as folders which are maintained in a tree-like structure. Though, these directories are also a type of file themselves

  
34. **What’s LVM and how can using it?**
	Logical volume management (LVM) is a form of storage virtualization that offers system administrators a more flexible approach to managing disk storage space than traditional partitioning.

  

35. **How could you mount a volume in Linux?**
	1. Identify the USB drive using the `lsblk` command.
	2. Create a directory to mount the USB drive into. 
	3. Check if it formatted or not
	4. Mount the USB drive to the /media/pendrive directory using the `mount` command. 
	5. Check the drive has been mounted by re-running lsblk.

  


36. **What are Linux bootstrap processes?**
Bootstrapping in computer science is **the technique for producing a self-compiling compiler**. That is compiler/assembler written in the source programming

  

	**The booting process takes the following 4 steps that we will discuss in greater detail:**
	1. BIOS Integrity check (POST)
	1. Loading of the Boot loader (GRUB2)
	1. Kernel initialization.
	1. Starting systemd, the parent of all processes.

	  

37. **Tell me about Linux file systems.**

	  The Linux filesystem unifies all physical hard drives and partitions into a single directory structure, this is how you sort your data inside the storage.

<img width="275" alt="image" src="https://github.com/Ahmed-Moourad/DevOps-Interview-Questions-for-Juniors/assets/112473376/c38ac75e-00ce-4d18-8f03-90ee27605f3e">



  

37. **What’s WAF in Linux ?**
	a firewall specifically designed to handle "web" traffic; that is, traffic using the HTTP protocol. Generally speaking, the role of a WAF is to inspect all HTTP traffic destined for a web server, discard "bad" requests, and pass "good" traffic on

	  

38. **What’s Selinux and how can use it?**
SELinux defines access controls for the applications, processes, and files on a system. It uses security policies, which are a set of rules that tell SELinux what can or can't be accessed, to enforce the access allowed by a policy

  


39. **What’s the /dev/null directory?**
The null device is typically used for disposing of unwanted output streams of a process, or as a convenient empty file for input streams. This is usually done by redirection. The /dev/null device is **a special file, not a directory, so one cannot move a whole file or directory into it with the Unix mv command**.

  
  
  
  
  

## Kubernetes Questions:

  

40. **What are Kubernetes architecture components and explain them?**
The main componehnts of a Kubernetes cluster include: **Nodes, Image Registry, Pods**
\-------------------------------------------
**Kubernetes Core Components: Control Plane(Master Node):**
	-  **kube-apiserver**. Provides an API that serves as the front end of a Kubernetes control plane. ...
	-  **etcd**: The key-value store where all data relating to the cluster is stored
	-  **kube-scheduler**. When a new Pod is created, this component assigns it to a node for execution based on resource requirements, policies, and ‘affinity’ specifications regarding geolocation and interference with other workloads.
	-  **kube-controller-manager**. Although a Kubernetes cluster has several controller functions, they are all compiled into a single binary known as kube-controller-manager.
\-----------------------------------------------
	**Node components include: (Worker Node)**
	- **kubelet**: Every node has an agent called kubelet. It ensures that the container described in PodSpecs is up and running properly.
	- **kube-proxy**: A network proxy on each node that maintains network nodes that allow for the communication from Pods to network sessions, whether inside or outside the cluster, using operating system (OS) packet filtering if available.
	- **container runtime**: Software responsible for running the containerized applications. Although Docker is the most popular, Kubernetes supports any runtime that adheres to the Kubernetes CRI (Container Runtime Interface).

41. **What’s the difference between Master and Worker Node?** 
**Worker Node**:
	- Do all the Work
	- Responsible for running the containers and doing any work assigned to them by the master node
	- Many nodes
	- Consist of **3** components: kubelet, kube-proxy, container runtime

	**Master Node**:
	- Create the control plane
	- Looks after scheduling and scaling applications. maintaining the state of the cluster.
	- 1 or two nodes
	- Consist of **4** components: etcd, kube controller manager, kube-API-server, kube-schedular

  

42. **What are service types?**
	-  **ClusterIP** (default): Internal clients send requests to a stable internal IP address.

	-  **NodePort**: Clients send requests to the IP address of a node on one or more nodePort values that are specified by the Service.

	-  **LoadBalancer:** Clients send requests to the IP address of a network load balancer.

	-  **ExternalName**: Internal clients use the DNS name of a Service as an alias for an external DNS name.

	-  **Headless**: when you want a Pod grouping, but don't need a stable IP address.

  
	The **NodePort** type is an extension of the **ClusterIP** type. So a Service of the type NodePort has a cluster IP address.

	  

	The **LoadBalancer** type is an extension of the **NodePort** type. So a Service of type **LoadBalancer** has a cluster IP address and one or more **nodePort** values.

  
![image](https://github.com/Ahmed-Moourad/DevOps-Interview-Questions-for-Juniors/assets/112473376/e4e43c46-7a7d-4e2f-9bd8-5b20aff34df5)

![image](https://github.com/Ahmed-Moourad/DevOps-Interview-Questions-for-Juniors/assets/112473376/e43b8466-69ab-48fa-a5b9-d22adaf53c3f)


43. **What’s the difference between deployment vs DaemonSet vs StatfulSet?**
- **Deployments** and ReplicationControllers are meant for stateless usage and are rather lightweight.
- **Statefulsets**: is used for Stateful applications (DB), each replica of the pod will have its own state, and will be using its own Volume.
- **DaemonSet**: is a controller similar to **ReplicaSet** that ensures that the pod runs on all the nodes of the cluster.

  

	**A Daemonset will not run more than one replica per node**. Another advantage of using a Daemonset is that, if you add a node to the cluster, then the Daemonset will automatically spawn a pod on that node, which a deployment will not do

  
![image](https://github.com/Ahmed-Moourad/DevOps-Interview-Questions-for-Juniors/assets/112473376/aac25788-f74c-4d3e-9a15-7d0174fb3980)


![image](https://github.com/Ahmed-Moourad/DevOps-Interview-Questions-for-Juniors/assets/112473376/67c1aaa1-18e8-4384-ab7e-41f2a65aa832)


![image](https://github.com/Ahmed-Moourad/DevOps-Interview-Questions-for-Juniors/assets/112473376/df977628-dd54-481b-9b88-95a573f47be3)


  

44. **What’s the difference between ReplicaController and ReplicaSet?**
The rolling-update command works with Replication Controllers, but won't work with a Replica Set.

  

45. **What is the difference between ReplicaSet and Deployment?**
	- **A ReplicaSet** ensures that a specified number of pod replicas are running at any given time.
	- **Deployment** is a higher-level concept that manages ReplicaSets and provides declarative updates to Pods along with a lot of other useful features.

  
  

46. **How can create a variable for your deployment and how can secure it?**

	  **Secrets** can be mounted as data volumes or exposed as environment variables to be used by a container in a Pod.
Secrets can also be used by other parts of the system, without being directly exposed to the Pod.

23. **Which command is used to encrypt the password to store inside the secreats dockerfile?**  
	echo -n "My@password" | base64

47. **Is it possible to create multiple containers in one pod?**
YES – but better be one container/Pod
because each container should do one task so if you have 2 containers in a pod and you are near to increase one container because its service/task has a lot of traffic ... then k8s will create a new pod with two containers that the second is not doing anything so you are wasting your compute capacity.


48. **What’s a Sidecar container?**
	- Sidecar containers are containers that run along with the main container in a pod. You can define any number of sidecar containers to run alongside the main container
	- The sidecar containers can also share storage volumes with the main containers, allowing the main containers to access the data in the sidecars.
	- The primary application can run independently in one container while the sidecar hosts complementary processes and tools

  

49. **What’s CustomResourcesDefination (CRD)?**
API resource allows you to define custom resources. Defining a CRD object creates a new custom resource with a name and schema that you specify. The Kubernetes API serves and handles the storage of your custom resource. The name of a CRD object must be a valid DNS subdomain name

  

50. **What’s kube-proxy?**
a network proxy that runs on each node in your cluster, implementing part of the Kubernetes Service concept. kube-proxy maintains network rules on nodes. These network rules allow network communication to your Pods from network sessions inside or outside of your cluster

  

51. **What’s the difference between liveness vs readiness vs startup probes?**
**liveness**:
  **Liveness Probe**: Checks if a container is running properly and restarts it if the probe fails.
**Readiness Probe**: Checks if a container is ready to receive network traffic and delays routing until it becomes ready.
**Startup Prob**e: Checks the initial startup readiness of a container, helping differentiate slow starts from unresponsive containers.

52. **What’s the operator of the Database?**
The DB Operator eases the pain of managing PostgreSQL and MySQL instances for applications running in Kubernetes. The Operator creates databases and makes them available in the cluster via Custom Resource. It is designed to support the on-demand creation of test environments in CI/CD pipelines.

  

53. **What are the static pods?**
Static Pods are managed directly by the kubelet daemon on a specific node, without the API server observing them

  

54. **What are helm and helm charts?**
Helm helps you manage Kubernetes applications — Helm Charts help you define, install, and upgrade even the most complex Kubernetes application. Charts are easy to create, version, share, and publish — so start using Helm and stop the copy-and-paste.
Helm uses a packaging format called charts. A chart is a collection of files that describe a related set of Kubernetes resources

  

55. **What’s custom resources in K8s?**
A custom resource is an **extension of the Kubernetes API** that is not necessarily available in a default Kubernetes installation. It represents a customization of a particular Kubernetes installation. However, many core Kubernetes functions are now built using custom resources, making Kubernetes more modular

  

56. **What’s the difference between Ingress and IngressPolicy?**
**Ingress Resource**: an object with a set of routing rules.
The Ingress concept lets you map traffic to different backends based on rules you define via the Kubernetes API.
**IngressPolicy** (Ingress rules) allows connections to all pods in the "default" namespace with the label "role=db" on TCP port 6379 from: any pod in the "default" namespace with the label "role=frontend" and any pod in a namespace with the label "project=myproject"

  

## **General Questions:**

  

57. **What’s CICD?**
CI/CD is a method to frequently deliver apps to customers by introducing automation into the stages of app development.
continuous integration, continuous delivery, and continuous deployment.

  
  

58. **What’s Jenkins pipeline?**

  

a suite of plugins that supports implementing and integrating continuous delivery pipelines into Jenkins. A continuous delivery pipeline is an automated expression of your process for getting software from version control right through to your users and customers.

  

59. **What’s Jenkins Master and Slave?**

  

The Jenkins master acts to schedule the jobs, assign slaves, and send builds to slaves to execute the jobs. It will also monitor the slave state (offline or online) and get back the build result responses from slaves and display build results on the console output.

  

60. **What’s Jenkins Shared Library?**
It is a feature that allows you to define reusable code in a version-controlled repository and share it across Jenkins pipelines. It promotes code reuse, and consistency, and simplifies pipeline maintenance.
 A shared library in Jenkins is a collection of Groovy scripts shared between different Jenkins jobs
Each shared library requires users to define a name and a method of retrieving source code.

61. **What’s Java Spring Boot?**
Java Spring Boot (Spring Boot) is a tool that makes developing web applications and microservices with Spring Framework faster and easier through three core capabilities: Autoconfiguration. An opinionated approach to configuration. The ability to create standalone applications.

  

62. **What’s the difference between Rolling Strategy and Blue-Green Strategy?**
**Rolling deployments** follow a staggered delivery pattern that gradually replaces instances of the existing environment with updated versions. 
**Blue-green deployments** involve creating a rigorously-tested second environment before completely shifting the current instance to the new environment.

63. **What’s SonarQube?**
empowers all developers to write cleaner and safer code
Code Quality Assurance tool that collects and analyzes source code, and provides reports for the code quality of your project

64. **What’s API?**
a set of functions and procedures allowing the creation of applications that access the features or data of an operating system, application, or another service

  

65. **How can writing a bash script?**
	1. create a file using a vi editor(or any other editor). Name script file with extension.sh.
	2. Start the script with #! /bin/sh.
	3. Write some code.
	4. Save the script file as filename.sh.
	5. For executing the script type bash filename.sh.

  
  

66. **What’s the difference between `awk` vs `sed`?**
**`sed`** is a command utility that works with streams of characters for searching, filtering and text processing
**`awk`** is more powerful and robust than sed with sophisticated programming constructs such as ifelse, while, do/while

  

67. **How can create variables in Ansible?**
 define a variable dynamically when you run a playbook, **use the --extra-vars option along with the key and value of the variable you want to define**. In this example, the key is my\_var because that's the string referenced in the playbook, and the value is any string you want the variable to contain

68. **What are modules and tasks in Ansible playbook?**
Ansible Playbooks are **lists of tasks that automatically execute against hosts**. Groups of hosts form your Ansible inventory. Each module within an Ansible Playbook performs a specific task
  
**Modules**: Standalone code units in Ansible for specific tasks on managed hosts.

**Tasks**: Actions in Ansible playbooks defining desired system state using modules.
  
  

69. **Difference between Dynamic Inventory and Multiple Inventory?**
**Dynamic Inventory**: Retrieves inventory information dynamically from external sources.
**Multiple Inventory**: Allows the use of multiple static inventory files for organizing and managing inventory across different environments or projects.
Using inventory directories and multiple inventory sources. Static groups of dynamic groups. If your Ansible inventory fluctuates over time with hosts spinning up and shutting down in response to business demands, the static inventory solutions will not serve your needs.
Multiple Inventory:You may need to track hosts from multiple sources: cloud providers, LDAP, Cobbler, and/or enterprise CMDB systems.

  

71. **What’s the path of ansible configuration?**
/etc/ansible/ansible. cfg

  

72. **What’s the difference between ansible and chef?**
Ansible: uses YAML (easy), Agentless
Chef and Puppet: uses Ruby (Difficult), needs an agent and updates are a headache.

  

73. **What’s privilege escalation in Ansible?**
Ansible uses existing privilege escalation systems to execute tasks with root privileges or with another user’s permissions. Because this feature allows you to ‘become’ another user, different from the user that logged into the machine (remote user), we call it become. The become keyword uses existing privilege escalation tools like *sudo*, *su*, *pfexec*, *doas*, *pbrun*, *dzdo*, *ksu*, *runas*, *machinectl* and others.


74. **What’s Azure DevOps?**
Azure DevOps supports a collaborative culture and set of processes that bring together developers, project managers, and contributors to develop

![image](https://github.com/Ahmed-Moourad/DevOps-Interview-Questions-for-Juniors/assets/112473376/d18bb3ef-b8c2-4fbc-a400-1a62fafde352)

74. **What’s Git forking?**
Forking is a git clone operation executed on a server copy of a project's repo.
A fork in Git is simply a copy of an existing repository in which the new owner disconnects the codebase from previous committers. A fork often occurs when a developer becomes dissatisfied or disillusioned with the direction of a project and wants to detach their work from that of the original project.

  

75. **Is it better to fork or clone in Git?**
If you would like to make changes directly to a repository you have permission to contribute to, then **cloning** will be the first step before we implement the actual changes and push.
If you don't have permission to contribute to the repository but would like to implement changes anyway, a **fork** is the way to go.

  

76. **What’s the difference between stateful vs stateless?**
**stateless** system sends a request to the server and relays the response (or the state) back without storing any information.
**Stateful** systems expect a response, track information, and resend the request if no response is received.
- Stateless Protocol is a network protocol in which the Client sends a request to the server and the server responds back as per the given state.
- Stateful Protocol is a network protocol in which if a client sends a request to the server then it expects some kind of response, in case of no response then it resends the request.

  

77. **What’s a message broker? Or message queue (MQ)**
Way of how the microservices communicate
A message broker is a software that enables applications, systems, and services to communicate with each other and exchange information. EX: redis, Rabbit MQ

  

78. **What’s CDN?**
A content delivery network (CDN) refers to a geographically distributed group of servers which work together to provide fast delivery of Internet content. Ex: Amazon CloudFront.


79. **What are types of API?**
Five types of APIs are:
1) Open API
2) Partner API 4) High-level
3) Internal API 5) Low-level API

  

80. **What is Web APIs ?**
- Open APIs. Open APIs, also known as external or public APIs, are available to developers and other users with minimal restrictions. ...
- Internal APIs. In contrast to open APIs, internal APIs are designed to be hidden from external users. ...
- Partner APIs. ...
- Composite APIs. ...
- REST. ...
- JSON-RPC and XML-RPC. ...
- SOAP.

  
81. **What’s the terraform state?**
Terraform must store state about your managed infrastructure and configuration. This state is used by Terraform to map real world resources to your configuration, keep track of metadata, and to improve performance for large infrastructures. This state is stored by default in a local file named **"terraform.tfstate”**
but it can also be stored remotely, which works better in a team environment.
