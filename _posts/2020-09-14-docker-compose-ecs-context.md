

# ECS context not working


## Error message

{% highlight bash %}
docker context create ecs name

  docker context create" requires exactly 1 argument.
  See 'docker context create --help'.

  Usage:  docker context create [OPTIONS] CONTEXT

  Create a context
{% endhighlight %}


## Solution

-   must update docker compose cli

    https://stackoverflow.com/questions/67236401/docker-context-create-ecs-myecs-requires-exactly-one-argument

{% highlight bash %}
curl -L https://raw.githubusercontent.com/docker/compose-cli/main/scripts/install/install_linux.sh | sh
{% endhighlight %}

-   after update, create context with access keys
-   then switch to context

{% highlight bash %}
docker context use [CONTEXT-NAME]
{% endhighlight %}
