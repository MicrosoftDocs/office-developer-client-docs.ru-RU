---
title: 'Альтернативы: Использование инструкций SQL'
TOCTitle: 'Alternatives: Using SQL statements'
ms:assetid: 9ed787da-7099-2ef5-b2c6-c4f6bce5ddfe
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249727(v=office.15)
ms:contentKeyID: 48546668
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 4bcda13d8b785f1048890d1ed9492f5da3e7288b
ms.sourcegitcommit: 558d09fad81f8d80b5ad0edd21934fc09c098f2c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 11/03/2018
ms.locfileid: "25945560"
---
# <a name="alternatives-using-sql-statements"></a>Альтернативы: Использование инструкций SQL


**Применимо к**: Access 2013, Office 2013

ADO также разрешает использование команд в качестве альтернативы для его встроенных свойств и методов для изменения данных. В зависимости от поставщика, все операции, упомянутые в этой главе может также быть выполнено путем передачи команды для источника данных. Например инструкции для обновления SQL можно использовать для изменения данных без использования **значение** свойства **поля**. Инструкции SQL INSERT можно использовать для добавления новых записей в источнике данных, а не ADO метод **AddNew**. Дополнительные сведения о SQL или язык обработки данных у поставщика обратитесь к документации источника данных.

Например вы можете передать SQL строку, содержащую инструкции DELETE в базе данных, как показано в следующем коде:

```vb 
'BeginSQLDelete 
strSQL = "DELETE FROM Shippers WHERE ShipperID = " & intId 
objConn.Execute strSQL, , adCmdText + adExecuteNoRecords 
'EndSQLDelete 
```

