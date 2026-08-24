# Ceph

https://docs.ceph.com/en/latest/

- Block Storage (RBD) - RADOS Block Device
- File System (CephFS)
- Object Storage (RGW) - RADOS Gateway


| Short Form    | Full Form                                         | Purpose                                                          |
| ------------- | ------------------------------------------------- | ---------------------------------------------------------------- |
| **Ceph**      | Named after the cephalopod                        | Distributed storage platform                                     |
| **RADOS**     | **Reliable Autonomic Distributed Object Store**   | Core distributed object storage layer                            |
| **OSD**       | **Object Storage Daemon**                         | Stores data, handles replication, recovery, and rebalancing      |
| **MON**       | **Monitor**                                       | Maintains cluster maps, state, authentication, and quorum        |
| **MGR**       | **Manager**                                       | Provides monitoring, metrics, dashboards, and management modules |
| **RBD**       | **RADOS Block Device**                            | Provides block storage                                           |
| **CephFS**    | **Ceph File System**                              | Provides distributed POSIX filesystem storage                    |
| **RGW**       | **RADOS Gateway**                                 | Provides S3 and Swift-compatible object storage                  |
| **MDS**       | **Metadata Server**                               | Manages filesystem metadata for CephFS                           |
| **CRUSH**     | **Controlled Replication Under Scalable Hashing** | Determines where data should be placed across OSDs               |
| **PG**        | **Placement Group**                               | Logical grouping used to distribute objects across OSDs          |
| **CSI**       | **Container Storage Interface**                   | Lets Kubernetes provision and manage Ceph storage                |
| **PVC**       | **PersistentVolumeClaim**                         | Kubernetes request for persistent storage                        |
| **PV**        | **PersistentVolume**                              | Kubernetes storage resource provisioned for workloads            |
| **S3**        | **Simple Storage Service**                        | Object storage API/interface originally created by AWS           |
| **EC**        | **Erasure Coding**                                | Data protection method using data + parity chunks                |
| **WAL**       | **Write-Ahead Log**                               | Stores write operations before committing data                   |
| **DB**        | **RocksDB Database**                              | Metadata database used by BlueStore OSDs                         |
| **BlueStore** | —                                                 | Default Ceph OSD storage backend                                 |




