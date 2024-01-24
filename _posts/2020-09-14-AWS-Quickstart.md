

# Deploy Compose to AWS Quickstart


## Create images of all services -> then deploy to repo(eg. docker hub)

    must create single image

-   some compose services might need their own dockerfiles
-   use default context when building
-   No volume mounts, port binds, build context etc in compose file

{% highlight bash %}
docker build . --tag [REPO_USERNAME]/[IMAGE_NAME]:[VERSION]
docker login
docker image push [REPO_USERNAME]/[IMAGE_NAME]:[VERSION]
{% endhighlight %}


## Create IAM user for aws

1.  create IAM user in aws console
2.  assign roles and permissions to IAM user
    -   ECS, LoadBalancer, Cloudfront, Deploy, EC2 etc
3.  copy access keys


## Create docker ecs context then deploy

1.  must update docker compose cli

    https://stackoverflow.com/questions/67236401/docker-context-create-ecs-myecs-requires-exactly-one-argument

{% highlight bash %}
curl -L https://raw.githubusercontent.com/docker/compose-cli/main/scripts/install/install_linux.sh | sh
{% endhighlight %}

1.  after update, create context with access keys

{% highlight bash %}
docker create context ecs [CONTEXT_NAME]
{% endhighlight %}

1.  then switch to context and deploy

    compose will automatically generate cloudfront cluster
    *soon to be deprecated*

{% highlight bash %}
docker context use [CONTEXT_NAME]
docker compose -f [COMPOSE_FILE] up
{% endhighlight %}


# Update AWS Cluster

    ECS dashboard -> Task definitions -> Cluster Name -> Service Name -> -> Update Service -> new revision

![img](./aws-taskdef.png)
