# Reflection

Going through this lab really helped me understand why the industry is shifting away from traditional VMs and toward containers. The difference in boot time alone was eye-opening. A Virtual Machine has to boot an entire guest operating system from scratch, which can take several minutes, while a Docker container just starts a single process on top of the host OS's existing kernel, so it's ready in seconds. That difference makes containers a much better fit for situations where you need to scale quickly or spin things up and down often.

Port mapping was something I had to think through carefully. Since a container runs in its own isolated network space, its internal port (in this case, port 80 for Nginx) isn't reachable from outside on its own. Using `-p 8080:80` bridges my host machine's port 8080 to the container's port 80, which is what let me actually reach the Nginx welcome page through `curl http://localhost:8080`.

Running `docker rm` also taught me something important about how containers handle data. Once I removed the container, any data that existed only inside its writable layer was gone for good. If I had needed to keep that data, I would have had to use a volume or bind mount to store it outside the container itself.

Thinking about DevOps, I can see how containerization closes the gap between developers and IT operations. Since everything the application needs is packaged inside the container, developers can build something that will run exactly the same way in production as it did on their own machine, which cuts down on miscommunication and "it works on my end" problems.

As for my GitHub portfolio, it's slowly turning into a real record of how my cloud computing skills are progressing, starting from basic cloud concepts, moving into infrastructure planning, then multi-cloud comparisons, and now containerization. Each lab builds on the last one.
