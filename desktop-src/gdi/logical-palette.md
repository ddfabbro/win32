---
Description: 'A logical palette is a color palette that an application creates and associates with a given device context.'
ms.assetid: '7cc86771-237d-4539-8f48-2474edb764a4'
title: Logical Palette
---

# Logical Palette

A *logical palette* is a color palette that an application creates and associates with a given device context. Logical palettes let applications define and use colors that meet their specific needs. Applications can create any number of logical palettes, using them for separate device contexts or switching between them for a single device context. The maximum number of palettes that an application can create depends on the resources of the system.

An application creates a logical palette by using the [**CreatePalette**](createpalette.md) function. The application fills a [**LOGPALETTE**](logpalette.md) structure, which specifies the number of entries and the color values for each entry, and then the application passes the structure to **CreatePalette**. The function returns a palette handle that the application uses in all subsequent operations to identify the palette. To use colors in the logical palette, the application selects the palette into a device context by using the [**SelectPalette**](selectpalette.md) function and then realizes the palette by using the [**RealizePalette**](realizepalette.md) function. The colors in the palette are available as soon as the logical palette is realized.

An application should limit the size of its logical palettes to just enough entries to represent the colors needed. Applications cannot create logical palettes larger than the maximum palette size, a device-dependent value. Applications can obtain the maximum size by using the [**GetDeviceCaps**](getdevicecaps.md) function to retrieve the SIZEPALETTE value.

Although an application can specify any color value for a given entry in a logical palette, not all colors can be generated by the given device. The system does not provide a way to discover which colors are supported, but the application can discover the total number of these colors by retrieving the color resolution of the device. The color resolution, specified in color bits per pixel, is equal to the COLORRES value returned by the [**GetDeviceCaps**](getdevicecaps.md) function. A device that has a color resolution of 18 has 262,144 possible colors. If an application requests a color that is not supported, the system chooses an appropriate approximation.

Once a logical palette is created, an application can change colors in the palette by using the [**SetPaletteEntries**](setpaletteentries.md) function. If the logical palette has been selected and realized, changing the palette does not immediately affect the colors being displayed. The application must use the [**UnrealizeObject**](unrealizeobject.md) and [**RealizePalette**](realizepalette.md) functions to update the colors. In some cases, the application may need to deselect, unrealize, select, and realize the logical palette to ensure that the colors are updated exactly as requested. If an application selects a logical palette into more than one device context, changes to the logical palette affect all device contexts for which it is selected.

An application can change the number of entries in a logical palette by using the [**ResizePalette**](resizepalette.md) function. If the application reduces the size, the remaining entries are unchanged. If the application extends the size, the system sets the color for each new entry to black (0, 0, 0) and the flag to zero.

An application can retrieve the color and flag values for entries in a given logical palette by using the [**GetPaletteEntries**](getpaletteentries.md) function. An application can retrieve the index for the entry in a given logical palette that most closely matches a specified color value by using the [**GetNearestPaletteIndex**](getnearestpaletteindex.md) function.

When an application no longer needs a logical palette, it can delete it by using the [**DeleteObject**](deleteobject.md) function. The application must make sure the logical palette is no longer selected into a device context before deleting the palette.

 

 


