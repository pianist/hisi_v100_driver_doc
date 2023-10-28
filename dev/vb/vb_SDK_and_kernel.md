`HI_MPI_VB_*` and /dev/vb ioctl calls
=====================================

| SDK call                      | Status    | ioctl request                         | Notes                                                 |
|-------------------------------|-----------|---------------------------------------|-------------------------------------------------------|
| `HI_MPI_VB_GetFileHandle`     |           | no kernel module call                 | returns /dev/vb file descriptor, not declared in `*.h`|
| `HI_MPI_VB_SetConf`           |           | [`0x4184420A`](call_0x4184420A.md)    | Usually called first in apps                          |
| `HI_MPI_VB_GetConf`           |           | [`0x81844209`](call_0x81844209.md)    |                                                       |
| `HI_MPI_VB_Init`              |           | [`0x00004207`](call_0x00004207.md)    | Allocated all buffers (set in SetConf)                |
| `HI_MPI_VB_Exit`              |           | [`0x00004208`](call_0x00004208.md)    |                                                       |
| `HI_MPI_VB_CreatePool`        |           | [`0xC0244201`](call_0xC0244201.md)    |                                                       |
| `HI_MPI_VB_GetBlock`          |           | [`0xC0244203`](call_0xC0244203.md)    |                                                       |
| `HI_MPI_VB_ReleaseBlock`      |           | [`0xC0044204`](call_0xC0044204.md)    |                                                       |
| `HI_MPI_VB_ReleaseBlock_0`    |           | [`0xC0044202`](call_0xC0044202.md)    | diff 0xC0044204(?)                                    |
| `HI_MPI_VB_GetBlkVirAddr`     |           | no kernel module call                 |                                                       | 
| `HI_MPI_VB_MmapPool`          |           |                                       |                                                       |
| `HI_MPI_VB_MunmapPool`        |           |                                       |                                                       |
| `HI_MPI_VB_Handle2PhysAddr`   |           |                                       |                                                       |
| `HI_MPI_VB_Handle2PoolId`     |           |                                       |                                                       |

