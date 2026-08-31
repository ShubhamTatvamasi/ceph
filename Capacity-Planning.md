# Ceph Capacity Planning

## 1. Raw Capacity

Raw capacity is the total disk capacity of all OSDs.

Example:

- 3 nodes
- 3 OSDs per node
- 50 GB per OSD

```text
Raw Capacity = 3 × 3 × 50 GB
             = 450 GB
```

## 2. Replication

With a replicated pool, data is stored multiple times.

For 3x replication:

```text
Usable Capacity ≈ Raw Capacity / 3
```

Example:

```text
450 GB / 3 = 150 GB usable
```

| Replication | Approx. usable capacity |
|---|---:|
| 2x | 50% |
| 3x | 33% |
| 4x | 25% |

## 3. Don't Plan to 100%

Do not fill the cluster to 100%.

A simple planning rule:

```text
Target maximum usage: ~70%
```

Example with 450 GB raw and 3x replication:

```text
Raw capacity       = 450 GB
3x replicated      = 150 GB usable
70% planning limit = 105 GB usable
```

## 4. Failure Capacity

Capacity planning should also account for failures.

Example:

```text
3 nodes
3 OSDs per node
50 GB per OSD
```

If one node fails:

```text
Remaining raw capacity = 300 GB
```

The cluster must still have enough free space to recover and rebalance.

## 5. Basic Formula

```text
Raw Capacity
    = Number of OSDs × OSD Size

Usable Capacity
    ≈ Raw Capacity / Replication Factor

Planning Capacity
    ≈ Usable Capacity × 70%
```

## 6. Example

```text
Nodes:             3
OSDs per node:     3
OSD size:          50 GB
Replication:       3x

Raw:
3 × 3 × 50 GB = 450 GB

Usable:
450 / 3 = 150 GB

Recommended planning capacity:
150 × 70% = 105 GB
```

So approximately:

```text
450 GB raw
150 GB theoretical usable
105 GB recommended usable capacity
```

## 7. Important

Actual usable capacity depends on:

- Replication size
- EC (Erasure Coding), if used
- CRUSH rules
- Number of nodes
- OSD sizes
- Failure domains
- Recovery/rebalance requirements
- Ceph `nearfull` and `full` ratios

For production clusters, keep additional free capacity for **OSD/node failures and recovery**.
