---
title: Этап 3. Получение набора записей сервером (руководство по RDS)
TOCTitle: 'Step 3: Server Obtains a Recordset (RDS Tutorial)'
ms:assetid: fadb6a9b-ed44-264f-22fd-26b121f98040
ms:mtpsurl: https://msdn.microsoft.com/library/JJ250282(v=office.15)
ms:contentKeyID: 48548856
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: e9f3299892118d044bfcc36f3fa28e4e25eaed9b
ms.sourcegitcommit: c557bbcccf37a6011f89aae1ddd399dfe549d087
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/31/2018
ms.locfileid: "25881134"
---
# <a name="step-3-server-obtains-a-recordset-rds-tutorial"></a><span data-ttu-id="e0faa-102">Этап 3. Получение набора записей сервером (руководство по RDS)</span><span class="sxs-lookup"><span data-stu-id="e0faa-102">Step 3: Server Obtains a Recordset (RDS Tutorial)</span></span>


<span data-ttu-id="e0faa-103">**Применимо к**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="e0faa-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="e0faa-104">Программа сервера использует текст строки и команду подключение для запроса источника данных для нужного строк.</span><span class="sxs-lookup"><span data-stu-id="e0faa-104">The server program uses the connect string and command text to query the data source for the desired rows.</span></span> <span data-ttu-id="e0faa-105">ADO обычно используется для получения этого **набора записей**, несмотря на то, что другие данные Microsoft доступ к интерфейсы, такие как OLE DB, можно было бы использовать.</span><span class="sxs-lookup"><span data-stu-id="e0faa-105">ADO is typically used to retrieve this **Recordset**, although other Microsoft data access interfaces, such as OLE DB, could be used.</span></span>

<span data-ttu-id="e0faa-106">Настраиваемый серверный программы может выглядеть следующим образом:</span><span class="sxs-lookup"><span data-stu-id="e0faa-106">A custom server program might look like this:</span></span>

```vb 
 
Public Function ServerProgram(cn as String, qry as String) as Object 
Dim rs as New ADODB.Recordset 
 rs.CursorLocation = adUseClient 
 rs.Open qry, cn 
 rs.ActiveConnection = Nothing 
 Set ServerProgram = rs 
End Function 
```

