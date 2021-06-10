---
title: Сохранение в объект XML DOM
TOCTitle: Saving to the XML DOM object
ms:assetid: 3c61fc30-9862-347b-c215-08597eccfead
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249160(v=office.15)
ms:contentKeyID: 48544318
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: 95026d878270757c983e42164c92923570c898c6
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32314730"
---
# <a name="saving-to-the-xml-dom-object"></a><span data-ttu-id="2f083-102">Сохранение в объект XML DOM</span><span class="sxs-lookup"><span data-stu-id="2f083-102">Saving to the XML DOM object</span></span>

<span data-ttu-id="2f083-103">**Область применения**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="2f083-103">**Applies to**: Access 2013, Office 2013</span></span>

## <a name="saving-to-the-xml-dom-object"></a><span data-ttu-id="2f083-104">Saving to the XML DOM Object</span><span class="sxs-lookup"><span data-stu-id="2f083-104">Saving to the XML DOM Object</span></span>

<span data-ttu-id="2f083-105">Можно сохранить набор **записей** в XML-формате до экземпляра объекта doM MSXML, как показано в следующем коде Visual Basic:</span><span class="sxs-lookup"><span data-stu-id="2f083-105">You can save a **Recordset** in XML format to an instance of an MSXML DOM object, as shown in the following Visual Basic code:</span></span>

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

