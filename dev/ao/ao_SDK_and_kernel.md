`HI_MPI_AO_*` SDK API and kernel devide /dev/ao
===============================================


`HI_MPI_AO_SetPubAttr`
----------------------

IDA decompilation:
* AudioDevId > 0: error 0xA0168001
* pstAttr == 0: error 0xA0168006
* check access rights to /dev/ao
* if no dev or rights: error 0xA0168010
* ioctl kernel call [`0x40045800`](call_0x40045800.md)
* if ok, ioctl kernel call [`0x40245801`](call_0x40245801.md)




