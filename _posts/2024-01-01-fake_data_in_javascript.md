
# Table of Contents

1.  [fake data in javascript](#org34cdf0c)


<a id="org34cdf0c"></a>

# fake data in javascript

    use faker library

    npm i faker

    import faker from "faker";
    
    const bigList = [...Array(5000)].map(() => ({
        name: faker.name.findName(),
        email: faker.internet.email(),
        avatar: faker.internet.avatar()
    }));

