---
title: 'Альтернативы: использование операторов SQL'
TOCTitle: 'Alternatives: Using SQL Statements'
ms:assetid: 9ed787da-7099-2ef5-b2c6-c4f6bce5ddfe
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249727(v=office.15)
ms:contentKeyID: 48546668
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 853dfaab43d6d4c831b7ec9288bc8e9477fe2683
ms.sourcegitcommit: c557bbcccf37a6011f89aae1ddd399dfe549d087
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/31/2018
ms.locfileid: "25888099"
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

