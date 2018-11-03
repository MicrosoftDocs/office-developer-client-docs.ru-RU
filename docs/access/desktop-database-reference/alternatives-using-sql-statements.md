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
# <a name="alternatives-using-sql-statements"></a><span data-ttu-id="fa36e-102">Альтернативы: Использование инструкций SQL</span><span class="sxs-lookup"><span data-stu-id="fa36e-102">Alternatives: Using SQL statements</span></span>


<span data-ttu-id="fa36e-103">**Применимо к**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="fa36e-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="fa36e-104">ADO также разрешает использование команд в качестве альтернативы для его встроенных свойств и методов для изменения данных.</span><span class="sxs-lookup"><span data-stu-id="fa36e-104">ADO also allows using commands as alternatives to its built-in properties and methods for editing data.</span></span> <span data-ttu-id="fa36e-105">В зависимости от поставщика, все операции, упомянутые в этой главе может также быть выполнено путем передачи команды для источника данных.</span><span class="sxs-lookup"><span data-stu-id="fa36e-105">Depending upon your provider, all operations mentioned in this chapter could also be accomplished by passing commands to your data source.</span></span> <span data-ttu-id="fa36e-106">Например инструкции для обновления SQL можно использовать для изменения данных без использования **значение** свойства **поля**.</span><span class="sxs-lookup"><span data-stu-id="fa36e-106">For example, SQL UPDATE statements can be used to modify data without using the **Value** property of a **Field**.</span></span> <span data-ttu-id="fa36e-107">Инструкции SQL INSERT можно использовать для добавления новых записей в источнике данных, а не ADO метод **AddNew**.</span><span class="sxs-lookup"><span data-stu-id="fa36e-107">SQL INSERT statements can be used to add new records to a data source, rather than the ADO method **AddNew**.</span></span> <span data-ttu-id="fa36e-108">Дополнительные сведения о SQL или язык обработки данных у поставщика обратитесь к документации источника данных.</span><span class="sxs-lookup"><span data-stu-id="fa36e-108">For more information about SQL or the data-manipulation language of your provider, see the documentation of your data source.</span></span>

<span data-ttu-id="fa36e-109">Например вы можете передать SQL строку, содержащую инструкции DELETE в базе данных, как показано в следующем коде:</span><span class="sxs-lookup"><span data-stu-id="fa36e-109">For example, you can pass a SQL string containing a DELETE statement to a database, as shown in the following code:</span></span>

```vb 
'BeginSQLDelete 
strSQL = "DELETE FROM Shippers WHERE ShipperID = " & intId 
objConn.Execute strSQL, , adCmdText + adExecuteNoRecords 
'EndSQLDelete 
```

