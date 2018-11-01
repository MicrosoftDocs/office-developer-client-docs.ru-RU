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
# <a name="alternatives-using-sql-statements"></a><span data-ttu-id="96a25-102">Альтернативы: использование операторов SQL</span><span class="sxs-lookup"><span data-stu-id="96a25-102">Alternatives: Using SQL Statements</span></span>


<span data-ttu-id="96a25-103">**Применимо к**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="96a25-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="96a25-104">ADO также разрешает использование команд в качестве альтернативы для его встроенных свойств и методов для изменения данных.</span><span class="sxs-lookup"><span data-stu-id="96a25-104">ADO also allows using commands as alternatives to its built-in properties and methods for editing data.</span></span> <span data-ttu-id="96a25-105">В зависимости от поставщика, все операции, упомянутые в этой главе может также быть выполнено путем передачи команды для источника данных.</span><span class="sxs-lookup"><span data-stu-id="96a25-105">Depending upon your provider, all operations mentioned in this chapter could also be accomplished by passing commands to your data source.</span></span> <span data-ttu-id="96a25-106">Например инструкции для обновления SQL можно использовать для изменения данных без использования **значение** свойства **поля**.</span><span class="sxs-lookup"><span data-stu-id="96a25-106">For example, SQL UPDATE statements can be used to modify data without using the **Value** property of a **Field**.</span></span> <span data-ttu-id="96a25-107">Инструкции SQL INSERT можно использовать для добавления новых записей в источнике данных, а не ADO метод **AddNew**.</span><span class="sxs-lookup"><span data-stu-id="96a25-107">SQL INSERT statements can be used to add new records to a data source, rather than the ADO method **AddNew**.</span></span> <span data-ttu-id="96a25-108">Дополнительные сведения о SQL или язык обработки данных у поставщика обратитесь к документации источника данных.</span><span class="sxs-lookup"><span data-stu-id="96a25-108">For more information about SQL or the data-manipulation language of your provider, see the documentation of your data source.</span></span>

<span data-ttu-id="96a25-109">Например вы можете передать SQL строку, содержащую инструкции DELETE в базе данных, как показано в следующем коде:</span><span class="sxs-lookup"><span data-stu-id="96a25-109">For example, you can pass a SQL string containing a DELETE statement to a database, as shown in the following code:</span></span>

```vb 
'BeginSQLDelete 
strSQL = "DELETE FROM Shippers WHERE ShipperID = " & intId 
objConn.Execute strSQL, , adCmdText + adExecuteNoRecords 
'EndSQLDelete 
```

