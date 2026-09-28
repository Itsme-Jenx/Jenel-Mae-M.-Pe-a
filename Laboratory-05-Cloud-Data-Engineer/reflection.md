# Mission Reflection

This laboratory activity taught me how cloud storage can be used for applications that handle many files. I learned that Object Storage is useful for storing millions of photos because photos are unstructured data. Instead of treating every photo like a part of a hard drive, Object Storage keeps each photo as an object inside a bucket. This makes it easier to organize a large collection of images. It is also useful when an application continues to receive new files from users.

Docker made the deployment of the MinIO storage server easier for me. I did not have to manually install all the software and configure every part of the server. I used one Docker command to create the container, set the ports, and provide the login information. I also used `docker ps` to check if the container was running. This helped me understand why containers are useful in cloud computing.

A bucket is like a main storage area for objects. In this activity, the bucket was named `client-photos`. I used this bucket to store the sample file that I uploaded through the Web Console. Buckets help keep objects organized and separated from other storage areas.

Companies can protect object storage data in different ways. They can make backup copies, replicate information to other servers, and store copies in different locations. They can also use redundancy so that the data can still be available when one physical server has a problem. These methods can reduce the risk of losing important files.

My confidence with the Linux command line is improving. Before this activity, I was less familiar with Docker commands and container options. After using commands such as `docker pull`, `docker run`, and `docker ps`, I became more comfortable working in the terminal. I also learned that small errors, such as spelling an image name incorrectly, can cause a command to fail. Overall, this laboratory gave me more confidence in using Linux, Docker, and cloud storage.
