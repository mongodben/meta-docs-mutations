---
title: Code Examples
updated: '2024-08-13T13:16:43.865Z'
url: https://mongodb.com/docs/meta/style-guide/style/code-examples/
---

# Code Examples

Use the following guidelines when creating code examples:

- Don't use screenshots to show code examples. Format them as blocks of code by using the appropriate markup in your authoring tool. For more information about formatting, see Text Formatting.

- Ensure that any placeholder text in code is obvious.

- For large code examples, use `:emphasize-lines:` to highlight the sections most relevant to the user.

- Follow the conventions of the programming language used and preserve the capitalization that the author of the code used.

For shell commands, use the following guidelines when creating blocks of code as input or output examples:

- When showing input, do not include a command prompt (such as $).

- As often as necessary, show input and output in separate blocks and provide explanations for each. For example, if the input contains arguments or parameters, explain those. If the user should expect something specific in the output, or you want to show only part of lengthy output, provide an explanation.

- When the command is simple, and there's nothing specific to say about the output, you can show the input and output using the `.. io-code-block::` directive.

- For readability, you can break up long lines of shell input into readable blocks by ending each line with a backslash.

- If the input includes a list of arguments or parameters, show the important or relevant ones first, and group related ones. If no other order makes sense, use alphabetical order. If you explain the arguments or parameters in text, show them in the same order that they appear in the code block.

The following examples illustrate many of these guidelines:

## Create a VM Running a Docker Host

1. Show all the available virtual machines (VMs) that are running Docker.

   ```sh
   docker-machine ls
   ```

   If you have not created any VMs yet, your output should look as follows:

   ```sh
   NAME ACTIVE DRIVER STATE URL
   ```

2. Create a VM that's running Docker.

   ```sh
   docker-machine create --driver virtualbox test
   ```

   The `--driver` flag indicates what type of driver the machine runs on. In this case, `virtualbox` indicates that the driver is Oracle VirtualBox. The final argument in the command gives the VM a name, in this case, `test`.

   The output should look as follows:

   ```sh
   Creating VirtualBox VM...
   Creating SSH key...
   Starting VirtualBox VM...
   Starting VM...
   To see how to connect Docker to this machine, run:
   docker-machine env test
   ```

3. Run the following command to see the VM that you created.

   ```sh
   docker-machine ls
   ```

   ```sh
   NAME ACTIVE DRIVER STATE URL SWARM
   test virtualbox Running tcp://192.168.99.101:237
   ```

## Run the Application

1. Run a container from the image. The application code uses the environment variables that you defined to connect to the MongoDB container.

   ```sh
   docker run --detach \
   --env MONGO_HOST=$MONGO_HOST \ env MONGO_PORT=$MONGO_PORT \ env
   --MONGO_SSL=$MONGO_SSL \ env MONGO_DATABASE=$MONGO_DATABASE \ env
   --MONGO_USER=$MONGO_USER \ env MONGO_PASSWORD=$MONGO_PASSWORD \ publish
   --5000:5000 \
   ```

   ```sh
   guestbook-mongo:1.0
   ```

2. View the status of the container by using the `--latest` parameter.

   ```sh
   docker ps --latest
   ```

   The status of the container should begin with `Up`.

## Remove the Containers Already using the Port

1. To identify the containers that are using the port, run the following command, changing `<port>` to the port number that you want to use.

   ```sh
   docker ps -a | grep <port>/tcp
   ```

2. To remove the containers, run the following command for each container identified in step 1, changing `<containerId>` to the ID of the container.

   The `--force` argument ensures that the container is removed even if it's currently running.

   ```sh
   docker rm --force --volumes <containerId>
   ```

## Troubleshooting

Sometimes, when you use a docker command, you receive the following output:

```sh
docker info Get http:///var/run/docker.sock/v1.20/info: dial unix
```

```sh
/var/run/docker.sock: no such file or directory.
* Are you trying to connect to a TLS-enabled daemon without TLS?
* Is your docker daemon up and running?
```

If you receive this output, your VM isn't running on a Docker host.