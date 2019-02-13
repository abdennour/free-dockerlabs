
Lab 1 - • Chapter 5.3
• •

# Screenshots

Complete the following activities:
Show 2 screen shots of the labs to show progress, and a final screen shot to demonstrate your completion of the lab

**Building a Jenkins & Docker Server**

# Explain why continuous integration is important to corporations.


- Time Saving: Developers don't need to wait until the Sprint to finish to merge their efforts. But rather, all efforts are merged continuously, which shows the value of their work early and avoid/minimizes regression bugs.

- Quality: CI makes sure that any change committed by a developer is buildable and shippable. This gives more confidence and enables the Quality by design.

- Risk mitigation and Avoid Single point of failure: By having conitnuous integration is a central place, no hidden code or dependency will exist. Hence, any developer can take over the app and move on.


# How does Docker support continuous integration?

Docker provides an isolated environment where CI pipeline will run. By having an isolated environments for CI pipelines, we gain the following: 

1. NoOps (No Ops): 

  -  No need to manage capabilities at the CI machine level. All capabilities are offloaded from VMs to containers. Indeed, Docker will be the only required agent capability.

  - No conflicts of versions ( java6, java8, ... ). Each Build has an isolated environment. 

2. Cost Effectiveness: 

   - Because all are running in containers & docker is the only required capability, all agents are similars. As a consequence, any agent can run the Build and takes over from the other agent which reduces the idle time of agents and take benefits from the running agents. 

 - Because all container images are downloaded from Nexus (artifactory), the CI (Bamboo) agent does not need a huge storage to persist capabilities. Rather, the agent will download the docker image (which include the required capabilities), run the Build, then it may delete it.

 

3. Concurrency: Concurrent Builds can be running simultaneously which saves a lot of time with zero wait for a queue of Build.



4. Portability: The same CI pipeline can be transfered from tools to another (i.e: Jenkins, Sider,...) with zero effort. Indeed, the environment of the pipeline is baked in a container image.



5. Local Test: By now, all developers can test their Build locally. Indeed, the environment is a docker image that anyone can download it from the artifacts repository (nexus), open it and run the Build inside it.



6. Single Source of Truth: Because it is running in isolated & shippable environment (docker image), running the Build locally or by the CI tools  must give the same result/ the same truth.



7. Control the Version of Build Environments & Plans: Because the Docker image ( Build environment) is written as code.
