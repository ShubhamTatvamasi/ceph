# network

### Ceph Network Design

For Ceph, we should use **2 separate networks**:

* **Public Network** → client/data traffic
* **Cluster Network** → OSD replication, recovery & backfill traffic

```mermaid
flowchart LR
    C[Clients] --> P[Public Network]
    
    P --> N1[Ceph Node 1]
    P --> N2[Ceph Node 2]
    P --> N3[Ceph Node 3]

    N1 <--> CL[Cluster Network]
    N2 <--> CL
    N3 <--> CL

    CL --> R[OSD Replication<br/>Recovery / Backfill]
```

**Example:**

```text
Public  : 10.10.10.0/24
Cluster : 10.20.20.0/24
```

This keeps **client traffic separate from heavy Ceph internal traffic**.
