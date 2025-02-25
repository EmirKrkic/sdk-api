---
UID: NS:iphlpapi._INTERFACE_SOFTWARE_TIMESTAMP_CAPABILITIES
title: INTERFACE_SOFTWARE_TIMESTAMP_CAPABILITIES
description: Describes the software timestamping capabilities of a NIC's miniport driver.
helpviewer_keywords: ["*PINTERFACE_SOFTWARE_TIMESTAMP_CAPABILITIES","INTERFACE_SOFTWARE_TIMESTAMP_CAPABILITIES","INTERFACE_SOFTWARE_TIMESTAMP_CAPABILITIES structure [IP Helper]","PINTERFACE_SOFTWARE_TIMESTAMP_CAPABILITIES","PINTERFACE_SOFTWARE_TIMESTAMP_CAPABILITIES structure pointer [IP Helper]","iphlp.INTERFACE_SOFTWARE_TIMESTAMP_CAPABILITIES","iphlpapi/INTERFACE_SOFTWARE_TIMESTAMP_CAPABILITIES","iphlpapi/PINTERFACE_SOFTWARE_TIMESTAMP_CAPABILITIES"]
tech.root: IpHlp
ms.date: 12/16/2020
req.header: iphlpapi.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: 
req.target-min-winversvr: Windows Server 2022
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: 
req.dll: 
req.irql: 
targetos: Windows
req.typenames: INTERFACE_SOFTWARE_TIMESTAMP_CAPABILITIES, *PINTERFACE_SOFTWARE_TIMESTAMP_CAPABILITIES
req.redist: 
f1_keywords:
 - _INTERFACE_SOFTWARE_TIMESTAMP_CAPABILITIES
 - iphlpapi/_INTERFACE_SOFTWARE_TIMESTAMP_CAPABILITIES
 - PINTERFACE_SOFTWARE_TIMESTAMP_CAPABILITIES
 - iphlpapi/PINTERFACE_SOFTWARE_TIMESTAMP_CAPABILITIES
 - INTERFACE_SOFTWARE_TIMESTAMP_CAPABILITIES
 - iphlpapi/INTERFACE_SOFTWARE_TIMESTAMP_CAPABILITIES
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - iphlpapi.h
api_name:
 - _INTERFACE_SOFTWARE_TIMESTAMP_CAPABILITIES
 - PINTERFACE_SOFTWARE_TIMESTAMP_CAPABILITIES
 - INTERFACE_SOFTWARE_TIMESTAMP_CAPABILITIES
---

## -description

Describes the software timestamping capabilities of a NIC's miniport driver.

For more info, and code examples, see [Packet timestamping](/windows/win32/iphlp/packet-timestamping).

## -struct-fields

### -field AllReceive

Type: **[BOOLEAN](/windows/win32/winprog/windows-data-types)**

Also contains members that describe the software timestamping capabilities of a NIC's miniport driver.
Not a hardware capability. **TRUE** indicates that the NIC's miniport driver can generate a software timestamp for all received packets. A value of **FALSE** indicates that the software is not capable of this.

### -field AllTransmit

Type: **[BOOLEAN](/windows/win32/winprog/windows-data-types)**

Not a hardware capability. Analogous to *AllReceiveSw*, except it applies to the transmit direction. **TRUE** indicates that the NIC's miniport driver can generate a software timestamp for all transmitted packets. A value of **FALSE** indicates that the software is not capable of this.

### -field TaggedTransmit

Type: **[BOOLEAN](/windows/win32/winprog/windows-data-types)**

Not a hardware capability. **TRUE** indicates that the NIC's miniport driver can generate a software timestamp for any specific transmitted packet when indicated to do so by the application. A value of **FALSE** indicates that the software is not capable of this.
See [**TIMESTAMPING_CONFIG**](/windows/win32/api/mstcpip/ns-mstcpip-timestamping_config) (and **TIMESTAMPING_FLAG_TX**) to determine how to request a timestamp when sending UDP packets through [Windows Sockets](/windows/win32/winsock/windows-sockets-start-page-2).

## -remarks

All of the **INTERFACE_SOFTWARE_TIMESTAMP_CAPABILITIES** structure's members represent software timestamp capabilities. The software timestamp generated by the NIC driver corresponds to a counter value obtained by calling [**QueryPerformanceCounter**](/windows/win32/api/profileapi/nf-profileapi-queryperformancecounter).

Having both hardware and software timestamps enabled together isn't supported.

## -see-also

* [Packet timestamping](/windows/win32/iphlp/packet-timestamping)
