
# Table of Contents

1.  [Docker map dev directory to docker image](#orgb690c86)


<a id="orgb690c86"></a>

# Docker map dev directory to docker image

    PROS: container updates when you update local code

    service-name:
      ...
      volumes:
        - ./development/directory:/deployment/directory

