# MinIO Deployment

## Docker Command Used

The original command from the handout used `minio/minio`, but it returned a "pull access denied" error on Docker Hub. I used the following command instead, pulling from Quay.io:

    docker run -d -p 9000:9000 -p 9001:9001 --name minio-server \
    -e "MINIO_ROOT_USER=cloudadmin" \
    -e "MINIO_ROOT_PASSWORD=CloudNova2026!" \
    quay.io/minio/minio server /data --console-address ":9001"

## Port Used to Access the Web Console

I accessed the MinIO Web Console through **port 9001**, which I opened using KillerCoda's Traffic/Ports option.

## Bucket Created

I created a bucket named **client-photos** and uploaded a test file named `sample.txt` into it to confirm the setup worked.

## Explanation of the -e Flags (Environment Variables)

- `-e "MINIO_ROOT_USER=cloudadmin"` sets the root **username** used to log in to the MinIO Web Console.
- `-e "MINIO_ROOT_PASSWORD=CloudNova2026!"` sets the root **password** paired with that username.

These flags pass login credentials into the container at startup so MinIO knows what username and password to require, instead of using an insecure default login.
