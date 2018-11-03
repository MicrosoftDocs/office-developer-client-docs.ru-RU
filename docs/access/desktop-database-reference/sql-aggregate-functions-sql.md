---
title: Статистические функции SQL (SQL)
TOCTitle: SQL aggregate functions (SQL)
ms:assetid: 8866cd71-0216-25b4-6a6a-02cb7acad9a2
ms:mtpsurl: https://msdn.microsoft.com/library/Ff197054(v=office.15)
ms:contentKeyID: 48546136
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 946afd4ad9c1a2976e4833b59fa8467911ac1c56
ms.sourcegitcommit: 558d09fad81f8d80b5ad0edd21934fc09c098f2c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 11/03/2018
ms.locfileid: "25945980"
---
# <a name="sql-aggregate-functions-sql"></a><span data-ttu-id="1638e-102">Статистические функции SQL (SQL)</span><span class="sxs-lookup"><span data-stu-id="1638e-102">SQL aggregate functions (SQL)</span></span>


<span data-ttu-id="1638e-103">**Применимо к**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="1638e-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="1638e-104">Использование агрегатных функций SQL, можно определить различные статистики на наборы значений.</span><span class="sxs-lookup"><span data-stu-id="1638e-104">Using the SQL aggregate functions, you can determine various statistics on sets of values.</span></span> <span data-ttu-id="1638e-105">Можно использовать эти функции в запросе и статистические выражения в свойстве **SQL** объекта **QueryDef** или при создании объекта **набора записей** на основе запроса SQL.</span><span class="sxs-lookup"><span data-stu-id="1638e-105">You can use these functions in a query and aggregate expressions in the **SQL** property of a **QueryDef** object or when creating a **Recordset** object based on an SQL query.</span></span>

- <span data-ttu-id="1638e-106">[Функция AVG](https://msdn.microsoft.com/library/ff822755\(v=office.15\))</span><span class="sxs-lookup"><span data-stu-id="1638e-106">[Avg function](https://msdn.microsoft.com/library/ff822755\(v=office.15\))</span></span>

- <span data-ttu-id="1638e-107">[Функция Count](https://msdn.microsoft.com/library/ff844748\(v=office.15\))</span><span class="sxs-lookup"><span data-stu-id="1638e-107">[Count function](https://msdn.microsoft.com/library/ff844748\(v=office.15\))</span></span>

- <span data-ttu-id="1638e-108">[Имя Фамилия функции](https://msdn.microsoft.com/library/ff197381\(v=office.15\))</span><span class="sxs-lookup"><span data-stu-id="1638e-108">[First, Last functions](https://msdn.microsoft.com/library/ff197381\(v=office.15\))</span></span>

- <span data-ttu-id="1638e-109">[Минимальное, максимальное число функций](https://msdn.microsoft.com/library/ff194490\(v=office.15\))</span><span class="sxs-lookup"><span data-stu-id="1638e-109">[Min, Max functions](https://msdn.microsoft.com/library/ff194490\(v=office.15\))</span></span>

- <span data-ttu-id="1638e-110">[StDev, StDevP функции](https://msdn.microsoft.com/library/ff197043\(v=office.15\))</span><span class="sxs-lookup"><span data-stu-id="1638e-110">[StDev, StDevP functions](https://msdn.microsoft.com/library/ff197043\(v=office.15\))</span></span>

- <span data-ttu-id="1638e-111">[Функция сумм](https://msdn.microsoft.com/library/ff844764\(v=office.15\))</span><span class="sxs-lookup"><span data-stu-id="1638e-111">[Sum function](https://msdn.microsoft.com/library/ff844764\(v=office.15\))</span></span>

- <span data-ttu-id="1638e-112">[Var, VarP функции](https://msdn.microsoft.com/library/ff192105\(v=office.15\))</span><span class="sxs-lookup"><span data-stu-id="1638e-112">[Var, VarP functions](https://msdn.microsoft.com/library/ff192105\(v=office.15\))</span></span>

