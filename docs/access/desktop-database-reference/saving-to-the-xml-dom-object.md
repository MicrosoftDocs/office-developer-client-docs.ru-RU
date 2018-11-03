---
title: Сохранение в объект XML DOM
TOCTitle: Saving to the XML DOM object
ms:assetid: 3c61fc30-9862-347b-c215-08597eccfead
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249160(v=office.15)
ms:contentKeyID: 48544318
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 072e673f18a790304d7922375296d3385e4ac0dc
ms.sourcegitcommit: 558d09fad81f8d80b5ad0edd21934fc09c098f2c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 11/03/2018
ms.locfileid: "25944076"
---
# <a name="saving-to-the-xml-dom-object"></a><span data-ttu-id="03b0d-102">Сохранение в объект XML DOM</span><span class="sxs-lookup"><span data-stu-id="03b0d-102">Saving to the XML DOM object</span></span>

<span data-ttu-id="03b0d-103">**Применимо к**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="03b0d-103">**Applies to**: Access 2013, Office 2013</span></span>

## <a name="saving-to-the-xml-dom-object"></a><span data-ttu-id="03b0d-104">Сохранение в объектной модели DOM XML</span><span class="sxs-lookup"><span data-stu-id="03b0d-104">Saving to the XML DOM Object</span></span>

<span data-ttu-id="03b0d-105">**Набор записей** можно сохранить в формате XML в экземпляр объекта MSXML DOM, как показано в следующем коде Visual Basic:</span><span class="sxs-lookup"><span data-stu-id="03b0d-105">You can save a **Recordset** in XML format to an instance of an MSXML DOM object, as shown in the following Visual Basic code:</span></span>

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

