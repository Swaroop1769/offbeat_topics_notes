using CloudFormation template we are deploying GitLab application into ECS Cluster.


Inside ECS --> Cluster --> Services --> Task --> Task Definition

In CloudFormation template for GitLab application container a volume has to be mapped which is EFS in this case. Just in case container crashes, simply we can spin up new container and tag this EFS.

docker container requires image name


EBS is faster than EFS, and easily we can attach to container.
some networking operations in EFS are not happening properly.
previously all the projects data is stored in EFS,
for attaching repo data we separated the gitaly service from CloudFormation template to a separate instance and mapped to EBS.