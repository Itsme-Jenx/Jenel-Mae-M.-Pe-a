# MinIO Deployment Documentation

## Introduction

For this activity, I created a simple object storage environment using Docker. I used a MinIO-compatible server and exposed its API and Web Console through two ports.

The server was run inside the KillerCoda Ubuntu Playground.

## Docker Command

The Docker command I used was:

```bash
docker run -d \
-p 9000:9000 \
-p 9001:9001 \
--name minio-server \
-e "MINIO_ROOT_USER=cloudadmin" \
-e "MINIO_ROOT_PASSWORD=CloudNova2026!" \
pgsty/minio:latest server /data --console-address ":9001"
```

## Explanation of the Command

The `docker run` command creates a new container and starts it.

The `-d` option allows the container to run in the background.

The following option:

```text
-p 9000:9000
```

maps port 9000 from the host to port 9000 inside the container. This port is used for the storage API.

The following option:

```text
-p 9001:9001
```

maps port 9001 from the host to port 9001 inside the container. I used this port to open the Web Console.

The option:

```text
--name minio-server
```

gives the container a simple name.

## Environment Variables

The Docker command contains two `-e` options.

The first one is:

```text
-e "MINIO_ROOT_USER=cloudadmin"
```

This provides the administrator username.

The second one is:

```text
-e "MINIO_ROOT_PASSWORD=CloudNova2026!"
```

This provides the administrator password.

Environment variables allow configuration information to be provided when the container starts.

## Checking the Container

I checked the container using:

```bash
docker ps
```

The expected container name was:

```text
minio-server
```

The container should have a running status.

## Web Console

I used port:

```text
9001
```

to access the Web Console through the KillerCoda browser access feature.

The login details were:

```text
Username: cloudadmin
Password: CloudNova2026!
```

## Bucket Created

After logging in, I created the following bucket:

```text
client-photos
```

This bucket was used to store the sample file for the laboratory activity.

## File Upload

I opened the `client-photos` bucket and uploaded a sample file.

The uploaded file appeared in the bucket, showing that the object storage service was working.

## Ports

| Port | Function |
|---|---|
| 9000 | Storage API |
| 9001 | Web Console |

## Evidence

### Running Container

![MinIO Deployment](screenshots/minio-deployed.png)

### Bucket and Uploaded File

![Bucket Upload](screenshots/minio-bucket-upload.png)

## Conclusion

The deployment gave me practical experience with Docker and object storage. I learned how to expose container ports, configure a container using environment variables, open a web console, create a bucket, and upload an object.
