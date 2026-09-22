# Reflection

Doing this activity helped me understand why object storage is used for things like photo-sharing apps instead of a regular hard drive. Block storage works more like a single disk that you have to manage and expand yourself, but object storage can hold a huge number of files without needing that kind of setup, which makes it a better choice when you're dealing with millions of photos.

Docker made setting up MinIO pretty simple. I didn't have to install anything manually — just one `docker run` command got the server going, and I used `docker ps` and `docker logs` to check that it was actually working. It wasn't a totally smooth process though, since the image `minio/minio` from the handout gave me a "pull access denied" error. I ended up switching to `quay.io/minio/minio` instead, and that one worked right away.

A bucket, from what I learned, is basically where objects are stored and organized in object storage — kind of like a folder, but simpler and without that same nested structure. I made a bucket called `client-photos` and uploaded a file named `test-upload.txt` into it.

For keeping data safe long-term, I think large companies usually store copies of their files across multiple servers or locations, so nothing gets lost even if one server crashes.

Overall, I feel more confident with the command line now than when I started this activity. Fixing the pull error and figuring things out on my own helped me actually understand what I was doing instead of just running commands without thinking about them.
