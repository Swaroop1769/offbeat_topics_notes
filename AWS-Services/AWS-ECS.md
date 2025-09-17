Introduction to ECS:

focus on using EC2 as capacity provider
Container image includes everything that the application needs in order to run(dependencies, config files etc)
containers are stored in container registry
2 purposes of container registry:
1. it's like a library where we can store all of our container images.
2. when we need to launch those containers and run them, the container image is pulled from container registry.

The container itself has to run on something, it has to run on - CONTAINER HOST. It is basically a server. In this case consider that EC2 instances can be container hosts. and we can have many containers on single EC2.

-> If More containers --> then need to check for failover and scaling --> we can install multiple container Hosts

Few decisions to make w.r.t container hosts?
which container runs on which host?
if a new container is launched, which host should it run on?
How are these multiple containers stopped and started?
What happens if one of container host fails? and what's going to happen to the containers that were running on that host?

-->Managing all of this complexity is the job of a container orchestration tool. That's given by ECS.
Container Orchestration Tool:
it monitors the container hosts, monitor state of containers. It will place container on ideal hosts.

ECS as a Container Orchestration Tool:

with ecs we will have some registry called ECR (Elastic Container Registry - contains all the container images)
with this ECR(based on container images) few containers are launched. Where are the containers going to be launched?? Container hosts....there has to be some sort of capacity provider.
In this case the capacity provider is going to be EC2 instance.

EC2 container host (Node A, Node B, Node C) == container host == virtual machines running inside AWS(OS)
And also they are having container runtime - that allow us to run multiple containers on each of these EC2 instances.
And ECS is going to do orchestration for us.

We are responsible for EC2 instances - things like patching, scaling by default 
And ECS will be responsible for handling containers themselves - will handle all of the container orchestration - also handle things like failures of one of these nodes and scheduling containers to run on different node that happens.

Even we can setup ASG - which means we can monitor things like CPU Usage - and if we reach certain threshold, it'll automatically launch additional nodes in ECS Cluster. If not needed, the ASG automatically terminate nodes within that cluster.

FARGATE Introduction: 
different from EC2 which acts as capacity provider 
