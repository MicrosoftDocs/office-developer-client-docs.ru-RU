---
title: Пример использования свойства Version (VB)
TOCTitle: Version property example (VB)
ms:assetid: ffb7b04a-55b9-fa2f-41ec-44af225bd15f
ms:mtpsurl: https://msdn.microsoft.com/library/JJ250315(v=office.15)
ms:contentKeyID: 48548968
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: f76455c78c7c58b81a327d883cdd47821f42ac6d
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32312077"
---
# <a name="version-property-example-vb"></a><span data-ttu-id="bec34-102">Пример использования свойства Version (VB)</span><span class="sxs-lookup"><span data-stu-id="bec34-102">Version property example (VB)</span></span>


<span data-ttu-id="bec34-103">**Область применения**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="bec34-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="bec34-104">В этом примере [свойство Version](version-property-ado.md) объекта [Подключения](connection-object-ado.md) используется для отображения текущей версии ADO.</span><span class="sxs-lookup"><span data-stu-id="bec34-104">This example uses the [Version](version-property-ado.md) property of a [Connection](connection-object-ado.md) object to display the current ADO version.</span></span> <span data-ttu-id="bec34-105">Он также использует несколько динамических свойств, чтобы показать:</span><span class="sxs-lookup"><span data-stu-id="bec34-105">It also uses several dynamic properties to show:</span></span>

  - <span data-ttu-id="bec34-106">текущее имя и версия DBMS.</span><span class="sxs-lookup"><span data-stu-id="bec34-106">the current DBMS name and version.</span></span>

  - <span data-ttu-id="bec34-107">Версия OLE DB.</span><span class="sxs-lookup"><span data-stu-id="bec34-107">OLE DB version.</span></span>

  - <span data-ttu-id="bec34-108">имя и версия поставщика.</span><span class="sxs-lookup"><span data-stu-id="bec34-108">provider name and version.</span></span>

  - <span data-ttu-id="bec34-109">Версия ODBC.</span><span class="sxs-lookup"><span data-stu-id="bec34-109">ODBC version.</span></span>

  - <span data-ttu-id="bec34-110">Имя и версия драйвера ODBC.</span><span class="sxs-lookup"><span data-stu-id="bec34-110">ODBC driver name and version.</span></span>

<!-- end list -->

```vb 
 
'BeginVersionVB 
Public Sub Main() 
 On Error GoTo ErrorHandler 
 
 Dim Cnxn As ADODB.Connection 
 Dim strCnxn As String 
 Dim strVersionInfo As String 
 
 ' Open connection 
 Set Cnxn = New ADODB.Connection 
 strCnxn = "Provider='sqloledb';Data Source='MySqlServer';" & _ 
 "Initial Catalog='Pubs';Integrated Security='SSPI';" 
 Cnxn.Open strCnxn 
 
 strVersionInfo = "ADO Version: " & Cnxn.Version & vbCr 
 strVersionInfo = strVersionInfo & "DBMS Name: " & Cnxn.Properties("DBMS Name") & vbCr 
 strVersionInfo = strVersionInfo & "DBMS Version: " & Cnxn.Properties("DBMS Version") & vbCr 
 strVersionInfo = strVersionInfo & "OLE DB Version: " & Cnxn.Properties("OLE DB Version") & vbCr 
 strVersionInfo = strVersionInfo & "Provider Name: " & Cnxn.Properties("Provider Name") & vbCr 
 strVersionInfo = strVersionInfo & "Provider Version: " & Cnxn.Properties("Provider Version") & vbCr 
 
 MsgBox strVersionInfo 
 
 ' clean up 
 Cnxn.Close 
 Set Cnxn = Nothing 
 Exit Sub 
 
ErrorHandler: 
 ' clean up 
 If Not Cnxn Is Nothing Then 
 If Cnxn.State = adStateOpen Then Cnxn.Close 
 End If 
 Set Cnxn = Nothing 
 
 If Err <> 0 Then 
 MsgBox Err.Source & "-->" & Err.Description, , "Error" 
 End If 
End Sub 
'EndVersionVB 
```

