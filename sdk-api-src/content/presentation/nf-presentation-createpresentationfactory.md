---
UID: NF:presentation.CreatePresentationFactory
tech.root: composition_presentation
title: CreatePresentationFactory
ms.date: 06/08/2021
targetos: Windows
description: Creates a presentation factory.
prerelease: true
req.assembly: 
req.construct-type: function
req.ddi-compliance: 
req.dll: 
req.header: presentation.h
req.idl: 
req.include-header: 
req.irql: 
req.kmdf-ver: 
req.lib: 
req.max-support: 
req.namespace: 
req.redist: 
req.target-min-winverclnt: 
req.target-min-winversvr: 
req.target-type: 
req.type-library: 
req.umdf-ver: 
req.unicode-ansi: 
topic_type:
 - apiref
api_type:
 - DllExport
api_location:
 - dcomp.dll
api_name:
 - CreatePresentationFactory
f1_keywords:
 - CreatePresentationFactory
 - presentation/CreatePresentationFactory
dev_langs:
 - c++
---

## -description

Creates a presentation factory.

## -parameters

### -param d3dDevice

Type: **[IUnkown](/windows/win32/api/unknwn/nn-unknwn-iunknown)\***

The D3D device the presentation factory is bound to.

### -param riid

Type: **REFIID**

A reference to the interface identifier (IID) of the presentation factory.

### -param presentationFactory

Type: **[void](/windows/desktop/winprog/windows-data-types)\*\***

The address of a pointer to an interface with the IID specified in the _`riid`_ parameter.

## -returns

## -remarks

## -see-also

