---
title: Этап 3. Получение набора записей сервером (руководство по RDS)
TOCTitle: 'Step 3: Server Obtains a Recordset (RDS Tutorial)'
ms:assetid: fadb6a9b-ed44-264f-22fd-26b121f98040
ms:mtpsurl: https://msdn.microsoft.com/library/JJ250282(v=office.15)
ms:contentKeyID: 48548856
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: ddd306e95ccf9ed68848b516c6d23d45286edf63
ms.sourcegitcommit: 558d09fad81f8d80b5ad0edd21934fc09c098f2c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 11/03/2018
ms.locfileid: "25943838"
---
# <a name="step-3-server-obtains-a-recordset-rds-tutorial"></a>Шаг 3: Сервер получает набор записей (учебник служб удаленных рабочих СТОЛОВ)

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

