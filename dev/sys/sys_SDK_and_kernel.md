`HI_MPI_SYS_*` and /dev/sys ioctl calls
=======================================

| SDK call                      | Status    | ioctl request                         | Notes                                                 |
|-------------------------------|-----------|---------------------------------------|-------------------------------------------------------|
| `HI_MPI_SYS_GetVersion`       |           | no kernel call                        |                                                       |
| `HI_MPI_SYS_GetChipId`        |           | [`0x80045910`](call_0x80045910.md)    |                                                       |
| `HI_MPI_SYS_Exit`             |           |                                       |                                                       |
| `HI_MPI_SYS_SetConf`          |           | [`0x40045902`](call_0x40045902.md)    | called `HI_MPI_SYS_GetConf_0`                         |
| `HI_MPI_SYS_GetConf`          |           | [`0x80045903`](call_0x80045903.md)    |                                                       |
| `HI_MPI_SYS_Init`             |           | ...loads of calls...                  |                                                       |
| `HI_MPI_SYS_Bind`             |           | [`0x40185907`](call_0x40185907.md)    | Bind data source and data receiver                    |


List of ioctl requests
----------------------

* [`0x80045903`](call_0x80045903.md) `SysGetConfig`
* [`0x80085906`](call_0x80085906.md) `SYS_GetTimeStamp`
* [`0x8008590F`](call_0x8008590F.md) returns `hrtimer` and `rrmode` 
* [`0x8004590C`](call_0x8004590C.md) `SYS_DRV_GetCustomCode`
* [`0x80045910`](call_0x80045910.md) `SYS_DRV_GetChipId`
* [`0x80045912`](call_0x80045912.md) `SYS_DRV_GetChipVer`
* [`0x801C5911`](call_0x801C5911.md) `SYS_DRV_GetSerialId`
* [`0xC004590D`](call_0xC004590D.md) `SYS_VREG_GetAddr`
* [`0xC01C590B`](call_0xC01C590B.md) `SysGetMemConf`
* [`0xC0185909`](call_0xC0185909.md) `SYS_GetBindbyDest`
* ...

`HI_MPI_SYS_Init`
-----------------

* [`0x00005900`](call_0x00005900.md)
* `MPI_AUDIO_Init()`:
* `MPI_SYS_GetKernelConfig()` ['0x8008590F'](call_0x8008590F.md)
* `SYS_BIND_Init()` no kernel module calls
* `MPI_AI_Init()`
* ...


