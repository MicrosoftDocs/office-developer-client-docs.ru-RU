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
ms.sourcegitcommit: d6695c94415fa47952ee7961a69660abc0904434
ms.translationtype: Auto
ms.contentlocale: ru-RU
ms.lasthandoff: 01/17/2019
ms.locfileid: "28711352"
---
# <a name="alternatives-using-sql-statements"></a>Альтернативы: использование операторов SQL


**Применимо к**: Access 2013, Office 2013

ADO также разрешает использование команд в качестве альтернативы для его встроенных свойств и методов для изменения данных. В зависимости от поставщика, все операции, упомянутые в этой главе может также быть выполнено путем передачи команды для источника данных. Например инструкции для обновления SQL можно использовать для изменения данных без использования **значение** свойства **поля**. Инструкции SQL INSERT можно использовать для добавления новых записей в источнике данных, а не ADO метод **AddNew**. Дополнительные сведения о SQL или язык обработки данных у поставщика обратитесь к документации источника данных.

Например вы можете передать SQL строку, содержащую инструкции DELETE в базе данных, как показано в следующем коде:

```vb 
'BeginSQLDelete 
strSQL = "DELETE FROM Shippers WHERE ShipperID = " & intId 
objConn.Execute strSQL, , adCmdText + adExecuteNoRecords 
'EndSQLDelete 
```

