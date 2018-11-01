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
# <a name="step-3-server-obtains-a-recordset-rds-tutorial"></a>Этап 3. Получение набора записей сервером (руководство по RDS)


**Применимо к**: Access 2013, Office 2013

Программа сервера использует текст строки и команду подключение для запроса источника данных для нужного строк. ADO обычно используется для получения этого **набора записей**, несмотря на то, что другие данные Microsoft доступ к интерфейсы, такие как OLE DB, можно было бы использовать.

Настраиваемый серверный программы может выглядеть следующим образом:

```vb 
 
Public Function ServerProgram(cn as String, qry as String) as Object 
Dim rs as New ADODB.Recordset 
 rs.CursorLocation = adUseClient 
 rs.Open qry, cn 
 rs.ActiveConnection = Nothing 
 Set ServerProgram = rs 
End Function 
```

