# Reflection

In this laboratory activity, I learned the difference between block, file, and object storage, and why object storage is the best option for storing a lot of user-uploaded photos. Unlike block storage, which is more like a single hard drive that has to be managed and expanded manually, object storage can hold a large number of files without needing a complicated file system, which makes it a better fit for something like a photo-sharing app.

Docker made deploying MinIO a lot easier because instead of installing everything manually, I only needed one `docker run` command with a few flags to get the server working. I used commands like `docker run`, `docker ps`, and `docker logs` to deploy the container and check that it was actually running.

I ran into a couple of problems along the way. When I first tried `docker run` using the image `minio/minio` from the handout, I got a "pull access denied" error. After looking into it, I found out that MinIO moved their images to a different registry, so I used `quay.io/minio/minio` instead, and it pulled successfully. Later, when I tried uploading a file through the web console, I kept getting an "Error: something went wrong" message even though the upload bar showed 100%. I learned this was because port 9000, which handles the actual file transfer, also needed to be opened in KillerCoda alongside port 9001, which is only for the console interface.

A bucket is basically a container used to organize and store objects in object storage, similar to a folder but without the same file system structure. For this activity, I created a bucket named `client-photos` and uploaded a file called `test-upload.txt` to it.

To prevent losing data if a physical server crashes, large companies usually store multiple copies of the same data across different servers or even different locations, so if one server fails, the data can still be accessed from another copy.

After finishing this activity, I feel more confident using the Linux command line than before. Running Docker commands, fixing the pull error, and figuring out the port issue on my own made me understand what each command was actually doing instead of just typing them without thinking about it.
