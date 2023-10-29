`HI_MPI_AO_*` SDK API and kernel devide /dev/ao
===============================================

`hi3518_ao.so` init and unload
------------------------------

From IDA decompilation (`init_module()`):
* `CMPI_CreateProc("ao", AOProcShow, 0);`
* `CMPI_RegisterDevice(char*)` with ptr to buffer with "ao" string (device name?)
* `CMPI_RegisterMod(*pstAoModule)`, pstAoModule is a structure

Unload process:
* `CMPI_UnRegisterMod(0x16);`
* `CMPI_UnRegisterDevice(char*)`, see init
* `CMPI_RemoveProc("ao");`

`AOProcShow`
------------

Good proc with a lot os useful info for decompilation.

`HI_MPI_AO_SetPubAttr`
----------------------

IDA decompilation:
* AudioDevId > 0: error 0xA0168001
* pstAttr == 0: error 0xA0168006
* check access rights to /dev/ao
* if no dev or rights: error 0xA0168010
* ioctl kernel call [`0x40045800`](call_0x40045800.md)
* if ok, ioctl kernel call [`0x40245801`](call_0x40245801.md)




