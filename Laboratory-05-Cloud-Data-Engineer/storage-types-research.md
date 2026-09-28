# Cloud Storage Types Research

Cloud storage allows applications and users to save data without depending only on a local computer. There are different storage types, and each one has a different purpose.

## Storage Comparison

| Storage Type | Description | Primary Use Case | Cloud Provider Example |
|---|---|---|---|
| Block Storage | Data is divided into blocks and presented like a virtual disk. | Virtual machines, databases, and operating systems. | AWS EBS |
| File Storage | Data is arranged as files and folders that can be shared over a network. | Shared documents, application files, and team folders. | AWS EFS |
| Object Storage | Data is stored as objects with information or metadata and placed inside buckets. | Photos, videos, backups, documents, and other unstructured data. | Amazon S3 |

## Difference Between the Three

### Block Storage

Block Storage works much like a hard drive. The storage can be attached to a virtual machine and used by an operating system or database.

### File Storage

File Storage organizes information using folders and files. It is useful when different users or systems need to access the same files.

### Object Storage

Object Storage keeps files as individual objects. Each object can contain the actual data and additional information called metadata. Objects are normally placed inside buckets.

## Recommendation for the Photo Application

For the client's photo-sharing application, Object Storage is suitable because photos are unstructured files that can be stored as individual objects. It also allows the application to organize a large number of photos inside buckets instead of storing everything directly on the web server.

## Conclusion

The three storage types have different purposes. Block Storage is useful for disks and databases, File Storage is useful for shared folders, and Object Storage is useful for large collections of files such as photos and videos.
