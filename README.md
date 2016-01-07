# Air Marshal Concourse

This is the [Concourse CI](https://concourse.ci) pipeline for [Air Marshal](https://github.com/starkandwayne/airmarshal-concourse)

## Use

You will need to create a file called `credentials.yml` in the same directory as `pipeline.yml`. **DO NOT CHECK THIS FILE INTO SOURCE CONTROL**

    docker-hub-password: your docker hubpassword
    docker-hub-email: your docker hub email


Then configure the pipeline:

    fly login -t <your concourse>
    fly --target <your concourse> set-pipeline -p airmarshal --config pipeline.yml --load-vars-from credentials.yml
