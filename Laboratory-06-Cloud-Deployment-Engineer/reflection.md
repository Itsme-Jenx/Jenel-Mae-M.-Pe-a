# Mission 6: My Reflection on Cloud Deployment

This laboratory activity helped me understand how Docker Compose makes cloud deployment easier. Instead of starting each container separately, I used a single YAML file to define Nextcloud and MariaDB. This approach saves time, reduces repeated commands, and makes the deployment easier to manage and repeat.

I also learned that YAML indentation is important. Using a Tab instead of spaces or placing a line at the wrong level can cause configuration errors. These mistakes may prevent Docker Compose from starting the application correctly. Because of this, I realized that checking the configuration before deployment is an important step.

Environment variables such as `MYSQL_DATABASE`, `MYSQL_USER`, and `MYSQL_PASSWORD` provide the settings needed for Nextcloud and MariaDB to communicate. They help keep the configuration organized and allow the application to use the correct database credentials. However, I learned that passwords should not be exposed in public repositories, especially when working on real projects.

Deploying Nextcloud was an interesting experience because I could set up a private cloud storage application in just a few minutes. Seeing the installation page in my browser helped me understand how different containers work together to provide a service. I also practiced checking container status, reviewing logs, and stopping the application properly.

Since Mission 1, my understanding of cloud computing has improved. I now understand that cloud engineering involves more than using online storage or virtual machines. It also includes configuring services, connecting applications to databases, automating deployment, and solving technical problems.

Overall, this mission introduced me to Infrastructure as Code and showed me how automation can make deployments more consistent and organized. I believe these skills will help me complete future cloud computing activities and prepare me for real-world IT projects.
