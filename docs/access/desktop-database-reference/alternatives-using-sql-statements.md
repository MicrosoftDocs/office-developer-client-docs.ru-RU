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
# <a name="alternatives-using-sql-statements"></a><span data-ttu-id="59de3-102">Альтернативы: использование операторов SQL</span><span class="sxs-lookup"><span data-stu-id="59de3-102">Alternatives: Using SQL statements</span></span>


<span data-ttu-id="59de3-103">**Область применения**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="59de3-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="59de3-104">Кроме того, ADO позволяет использовать команды в качестве альтернатив встроенным свойствам и методам редактирования данных.</span><span class="sxs-lookup"><span data-stu-id="59de3-104">ADO also allows using commands as alternatives to its built-in properties and methods for editing data.</span></span> <span data-ttu-id="59de3-105">В зависимости от поставщика все операции, упомянутые в этой главе, можно также выполнить, передавая команды в источник данных.</span><span class="sxs-lookup"><span data-stu-id="59de3-105">Depending upon your provider, all operations mentioned in this chapter could also be accomplished by passing commands to your data source.</span></span> <span data-ttu-id="59de3-106">Например, операторы обновления SQL можно использовать для изменения данных без использования свойства **value** **поля**.</span><span class="sxs-lookup"><span data-stu-id="59de3-106">For example, SQL UPDATE statements can be used to modify data without using the **Value** property of a **Field**.</span></span> <span data-ttu-id="59de3-107">Инструкции SQL INSERT можно использовать для добавления новых записей к источнику данных, а не к методу **AddNew**для ADO.</span><span class="sxs-lookup"><span data-stu-id="59de3-107">SQL INSERT statements can be used to add new records to a data source, rather than the ADO method **AddNew**.</span></span> <span data-ttu-id="59de3-108">Дополнительные сведения о SQL или языке обработки данных поставщика можно найти в документации к источнику данных.</span><span class="sxs-lookup"><span data-stu-id="59de3-108">For more information about SQL or the data-manipulation language of your provider, see the documentation of your data source.</span></span>

<span data-ttu-id="59de3-109">Например, можно передать строку SQL, содержащую инструкцию DELETE, в базу данных, как показано в следующем коде:</span><span class="sxs-lookup"><span data-stu-id="59de3-109">For example, you can pass a SQL string containing a DELETE statement to a database, as shown in the following code:</span></span>

```vb 
'BeginSQLDelete 
strSQL = "DELETE FROM Shippers WHERE ShipperID = " & intId 
objConn.Execute strSQL, , adCmdText + adExecuteNoRecords 
'EndSQLDelete 
```

