﻿---
Description: 'Retrieves the Direct3D device associated with the environment map.'
ms.assetid: '15f342c5-7665-443a-b7b8-32cc67034c41'
title: 'ID3DXRenderToEnvMap::GetDevice method'
---

# ID3DXRenderToEnvMap::GetDevice method

Retrieves the Direct3D device associated with the environment map.

## Syntax


```C++
HRESULT GetDevice(
  [out, retval] LPDIRECT3DDEVICE9 *ppDevice
);
```



## Parameters

<dl> <dt>

*ppDevice* \[out, retval\]
</dt> <dd>

Type: **[**LPDIRECT3DDEVICE9**](idirect3ddevice9.md)\***

Address of a pointer to an [**IDirect3DDevice9**](idirect3ddevice9.md) interface that represents the Direct3D device object associated with the environment map.

</dd> </dl>

## Return value

Type: **[**HRESULT**](455d07e9-52c3-4efb-a9dc-2955cbfd38cc)**

If the method succeeds, the return value is D3D\_OK. If the method fails, the return value can be D3DERR\_INVALIDCALL. Calling this method increases the internal reference count on the [**IDirect3DDevice9**](idirect3ddevice9.md) interface. Be sure to call [**IUnknown**](com.iunknown) when you are done using this **IDirect3DDevice9** interface or you will have a memory leak.

## Requirements



|                    |                                                                                        |
|--------------------|----------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>D3dx9core.h</dt> </dl> |
| Library<br/> | <dl> <dt>D3dx9.lib</dt> </dl>   |



## See also

<dl> <dt>

[ID3DXRenderToEnvMap](id3dxrendertoenvmap.md)
</dt> </dl>

 

 



