---
title: Сохранение в объектной модели DOM XML
TOCTitle: Saving to the XML DOM Object
ms:assetid: 3c61fc30-9862-347b-c215-08597eccfead
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249160(v=office.15)
ms:contentKeyID: 48544318
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: d0118eb277f8f1cc3332aeff1880b161d62f36cb
ms.sourcegitcommit: c557bbcccf37a6011f89aae1ddd399dfe549d087
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/31/2018
ms.locfileid: "25885397"
---
# <a name="saving-to-the-xml-dom-object"></a>Сохранение в объектной модели DOM XML


**Применимо к**: Access 2013, Office 2013

## <a name="saving-to-the-xml-dom-object"></a>Сохранение в объектной модели DOM XML

**Набор записей** можно сохранить в формате XML в экземпляр объекта MSXML DOM, как показано в следующем коде Visual Basic:

```vb 
 
Dim xDOM As New MSXML.DOMDocument 
Dim rsXML As New ADODB.Recordset 
Dim sSQL As String, sConn As String 
     
sSQL = "SELECT customerid, companyname, contactname FROM customers" 
sConn="Provider=Microsoft.Jet.OLEDB.4.0;Data Source=D:\Program Files" & _ 
        "\Common Files\System\msadc\samples\NWind.mdb" 
rsXML.Open sSQL, sConn 
rsXML.Save xDOM, adPersistADO   'Save Recordset directly into a DOM tree. 
... 
```

