---
title: 'Альтернативы: использование операторов SQL'
TOCTitle: 'Alternatives: Using SQL statements'
ms:assetid: 9ed787da-7099-2ef5-b2c6-c4f6bce5ddfe
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249727(v=office.15)
ms:contentKeyID: 48546668
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: 185f5c1eb7e11a9425ff6cc4a16f1387424f3219
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32297153"
---
# <a name="alternatives-using-sql-statements"></a>Альтернативы: использование операторов SQL


**Область применения**: Access 2013, Office 2013

ADO также позволяет использовать команды в качестве альтернативы встроенным свойствам и методам редактирования данных. В зависимости от поставщика все операции, упомянутые в этой главе, также можно выполнить, передав команды в источник данных. Например, SQL UPDATE можно использовать для изменения данных без использования свойства **Value** **поля.** SQL INSERT можно использовать для добавления новых записей в источник данных, а не метод ADO **AddNew.** Дополнительные сведения о SQL или языке обработки данных поставщика см. в документации к источнику данных.

Например, можно передать строку SQL, содержащую строку DELETE, в базу данных, как показано в следующем коде:

```vb 
'BeginSQLDelete 
strSQL = "DELETE FROM Shippers WHERE ShipperID = " & intId 
objConn.Execute strSQL, , adCmdText + adExecuteNoRecords 
'EndSQLDelete 
```

