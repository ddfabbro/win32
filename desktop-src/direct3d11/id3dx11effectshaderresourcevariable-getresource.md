---
title: ID3DX11EffectShaderResourceVariable GetResource method
description: Get a shader resource.
ms.assetid: '7c56aba0-ce60-4b50-9c1a-802bf1d73c6b'
keywords: ["GetResource method Direct3D 11", "GetResource method Direct3D 11 , ID3DX11EffectShaderResourceVariable interface", "ID3DX11EffectShaderResourceVariable interface Direct3D 11 , GetResource method"]
topic_type:
- apiref
api_name:
- ID3DX11EffectShaderResourceVariable.GetResource
api_location:
- N/A
- N/A.dll
api_type:
- COM
---

# ID3DX11EffectShaderResourceVariable::GetResource method

Get a shader resource.

## Syntax


```C++
HRESULT GetResource(
  �ID3D11ShaderResourceView **ppResource
);
```



## Parameters

<dl> <dt>

*ppResource* 
</dt> <dd>

Type: **[**ID3D11ShaderResourceView**](id3d11shaderresourceview.md)\*\***

The address of a pointer to a shader-resource-view interface. See [**ID3D11ShaderResourceView**](id3d11shaderresourceview.md).

</dd> </dl>

## Return value

Type: **[**HRESULT**](455d07e9-52c3-4efb-a9dc-2955cbfd38cc)**

Returns one of the following [Direct3D 11 Return Codes](d3d11-graphics-reference-returnvalues.md).

## Remarks

> [!Note]  
> The DirectX SDK does not supply any compiled binaries for effects. You must use Effects 11 source to build your effects-type application. For more information about using Effects 11 source, see [Differences Between Effects 10 and Effects 11](d3d11-graphics-programming-guide-effects-differences.md).

�

## Requirements



|                    |                                                                                                                                              |
|--------------------|----------------------------------------------------------------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>D3dx11effect.h</dt> </dl>                                                    |
| Library<br/> | <dl> <dt>N/A (An Effects 11 library is available online as shared source.)</dt> </dl> |



## See also

<dl> <dt>

[ID3DX11EffectShaderResourceVariable](id3dx11effectshaderresourcevariable.md)
</dt> </dl>

�

�




