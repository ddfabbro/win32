---
Description: 'Proxy function for the CreateBitmapFromHBITMAP method.'
ms.assetid: 'e4e9a6b4-00d9-4f87-aeec-f2c02c3f44ab'
title: 'IWICImagingFactory\_CreateBitmapFromHBITMAP\_Proxy function'
---

# IWICImagingFactory\_CreateBitmapFromHBITMAP\_Proxy function

Proxy function for the [**CreateBitmapFromHBITMAP**](-wic-codec-iwicimagingfactory-createbitmapfromhbitmap.md) method.

## Syntax


```C++
HRESULT IWICImagingFactory_CreateBitmapFromHBITMAP_Proxy(
  _In_��IWICImagingFactory ���������*pFactory,
  _In_��HBITMAP ��������������������hBitmap,
  _In_��HPALETTE �������������������hPalette,
  _In_��WICBitmapAlphaChannelOption options,
  _Out_�IWICBitmap �����������������**ppIBitmap
);
```



## Parameters

<dl> <dt>

*pFactory* \[in\]
</dt> <dd>

Type: **[**IWICImagingFactory**](-wic-codec-iwicimagingfactory.md)\***

</dd> <dt>

*hBitmap* \[in\]
</dt> <dd>

Type: **HBITMAP**

A bitmap handle to create the bitmap from.

</dd> <dt>

*hPalette* \[in\]
</dt> <dd>

Type: **HPALETTE**

A palette handle used to create the bitmap.

</dd> <dt>

*options* \[in\]
</dt> <dd>

Type: **[**WICBitmapAlphaChannelOption**](-wic-codec-wicbitmapalphachanneloption.md)**

The alpha channel options to create the bitmap.

</dd> <dt>

*ppIBitmap* \[out\]
</dt> <dd>

Type: **[**IWICBitmap**](-wic-codec-iwicbitmap.md)\*\***

A pointer that receives a pointer to the new bitmap.

</dd> </dl>

## Return value

Type: **HRESULT**

If this function succeeds, it returns **S\_OK**. Otherwise, it returns an **HRESULT** error code.

## Remarks

## Requirements



|                                     |                                                                                                                                                                  |
|-------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Minimum supported client<br/> | Windows�XP with SP2, Windows�Vista \[desktop apps only\]<br/>                                                                                              |
| Minimum supported server<br/> | Windows Server�2008 \[desktop apps only\]<br/>                                                                                                             |
| DLL<br/>                      | <dl> <dt>Windowscodecs.dll; </dt> <dt>Wincodec.lib</dt> </dl> |



�

�



