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
# <a name="alternatives-using-sql-statements"></a><span data-ttu-id="02ff5-102">Альтернативы: использование операторов SQL</span><span class="sxs-lookup"><span data-stu-id="02ff5-102">Alternatives: Using SQL statements</span></span>


<span data-ttu-id="02ff5-103">**Область применения**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="02ff5-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="02ff5-104">ADO также позволяет использовать команды в качестве альтернативы встроенным свойствам и методам редактирования данных.</span><span class="sxs-lookup"><span data-stu-id="02ff5-104">ADO also allows using commands as alternatives to its built-in properties and methods for editing data.</span></span> <span data-ttu-id="02ff5-105">В зависимости от поставщика все операции, упомянутые в этой главе, также можно выполнить, передав команды в источник данных.</span><span class="sxs-lookup"><span data-stu-id="02ff5-105">Depending upon your provider, all operations mentioned in this chapter could also be accomplished by passing commands to your data source.</span></span> <span data-ttu-id="02ff5-106">Например, SQL UPDATE можно использовать для изменения данных без использования свойства **Value** **поля.**</span><span class="sxs-lookup"><span data-stu-id="02ff5-106">For example, SQL UPDATE statements can be used to modify data without using the **Value** property of a **Field**.</span></span> <span data-ttu-id="02ff5-107">SQL INSERT можно использовать для добавления новых записей в источник данных, а не метод ADO **AddNew.**</span><span class="sxs-lookup"><span data-stu-id="02ff5-107">SQL INSERT statements can be used to add new records to a data source, rather than the ADO method **AddNew**.</span></span> <span data-ttu-id="02ff5-108">Дополнительные сведения о SQL или языке обработки данных поставщика см. в документации к источнику данных.</span><span class="sxs-lookup"><span data-stu-id="02ff5-108">For more information about SQL or the data-manipulation language of your provider, see the documentation of your data source.</span></span>

<span data-ttu-id="02ff5-109">Например, можно передать строку SQL, содержащую строку DELETE, в базу данных, как показано в следующем коде:</span><span class="sxs-lookup"><span data-stu-id="02ff5-109">For example, you can pass a SQL string containing a DELETE statement to a database, as shown in the following code:</span></span>

```vb 
'BeginSQLDelete 
strSQL = "DELETE FROM Shippers WHERE ShipperID = " & intId 
objConn.Execute strSQL, , adCmdText + adExecuteNoRecords 
'EndSQLDelete 
```

