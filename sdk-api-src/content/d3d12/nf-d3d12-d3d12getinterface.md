---
UID: NF:d3d12.D3D12GetInterface
title: D3D12GetInterface
description: Selects an SDK version at runtime when the system is in Windows Developer Mode.
tech.root: direct3d12
ms.date: 08/25/2021
req.construct-type: function
req.header: d3d12.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: 
req.target-min-winversvr: 
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: D3D12.lib
req.dll: D3D12.dll
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
f1_keywords:
 - D3D12GetInterface
 - d3d12/D3D12GetInterface
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - D3D12.dll
api_name:
 - D3D12GetInterface
---

## -description

Selects an SDK version at runtime when the system is in Windows Developer Mode.

## -parameters

### -param rclsid

Type: \_In\_ **[REFCLSID](/openspecs/windows_protocols/ms-oaut/bbde795f-5398-42d8-9f59-3613da03c318)**

The CLSID associated with the data and code that will be used to create the object.

Specify **CLSID_D3D12SDKConfiguration** to retrieve the [ID3D12SDKConfiguration](nn-d3d12-id3d12sdkconfiguration.md) interface.

These CLSIDs are also defined.

* DEFINE_GUID(CLSID_D3D12Debug,                        0xf2352aeb, 0xdd84, 0x49fe, 0xb9, 0x7b, 0xa9, 0xdc, 0xfd, 0xcc, 0x1b, 0x4f);
* DEFINE_GUID(CLSID_D3D12Tools,                        0xe38216b1, 0x3c8c, 0x4833, 0xaa, 0x09, 0x0a, 0x06, 0xb6, 0x5d, 0x96, 0xc8);
* DEFINE_GUID(CLSID_D3D12DeviceRemovedExtendedData,    0x4a75bbc4, 0x9ff4, 0x4ad8, 0x9f, 0x18, 0xab, 0xae, 0x84, 0xdc, 0x5f, 0xf2);
* DEFINE_GUID(CLSID_D3D12SDKConfiguration,             0x7cda6aca, 0xa03e, 0x49c8, 0x94, 0x58, 0x03, 0x34, 0xd2, 0x0e, 0x07, 0xce);

### -param riid

Type: \_In\_ **[REFIID](/openspecs/windows_protocols/ms-oaut/bbde795f-5398-42d8-9f59-3613da03c318)**

The globally unique identifier (**GUID**) for the SDK configuration interface. The **REFIID**, or **GUID**, of the interface can be obtained by using the `__uuidof` macro. For example, `__uuidof(ID3D12SDKConfiguration)` will retrieve the **GUID** of the debug interface.

### -param ppvDebug

Type: \_COM\_Outptr\_opt\_ **[void](/windows/win32/winprog/windows-data-types)\*\***

The `out` parameter that contains the requested interface on return (for example, the SDK configuration interface), as a pointer to pointer to void. See [ID3D12SDKConfiguration](nn-d3d12-id3d12sdkconfiguration.md).

## -returns

Type: **[HRESULT](/windows/win32/com/structure-of-com-error-codes)**

If the function succeeds, then it returns **S_OK**. Otherwise, it returns one of the [Direct3D 12 return codes](/windows/win32/direct3d12/d3d12-graphics-reference-returnvalues).

## -remarks

Tools that playback API capture such as PIX, and test harnesses such as the HLK, require modification to support the redist. Such tools can choose to ship with the latest redist. Direct3D's API compatibility through updates should mean that an API capture tool can capture on an older version of the Direct3D 12 SDK, and play it back on the newer version. However, some scenarios require more flexibility in selecting the SDK version. The **D3D12GetInterface** function exists to accommodate that.

## -see-also

* [ID3D12SDKConfiguration](nn-d3d12-id3d12sdkconfiguration.md)
