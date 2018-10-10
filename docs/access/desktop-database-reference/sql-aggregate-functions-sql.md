---
title: SQL Aggregate Functions (SQL)
TOCTitle: SQL Aggregate Functions (SQL)
ms:assetid: 8866cd71-0216-25b4-6a6a-02cb7acad9a2
ms:mtpsurl: https://msdn.microsoft.com/library/Ff197054(v=office.15)
ms:contentKeyID: 48546136
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 6c95c29a5864bd07590a494d10556b3f537c14b2
ms.sourcegitcommit: 19aca09c5812cfb98b68b5d4604dcaa814479df7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/09/2018
ms.locfileid: "25481826"
---
# <a name="sql-aggregate-functions-sql"></a><span data-ttu-id="ecadf-102">SQL Aggregate Functions (SQL)</span><span class="sxs-lookup"><span data-stu-id="ecadf-102">SQL Aggregate Functions (SQL)</span></span>


<span data-ttu-id="ecadf-103">**Применимо к**: Access 2013 | Office 2013</span><span class="sxs-lookup"><span data-stu-id="ecadf-103">**Applies to**: Access 2013 | Office 2013</span></span>

<span data-ttu-id="ecadf-104">Использование агрегатных функций SQL, можно определить различные статистики на наборы значений.</span><span class="sxs-lookup"><span data-stu-id="ecadf-104">Using the SQL aggregate functions, you can determine various statistics on sets of values.</span></span> <span data-ttu-id="ecadf-105">Можно использовать эти функции в запросе и статистические выражения в свойстве **SQL** объекта **QueryDef** или при создании объекта **набора записей** на основе запроса SQL.</span><span class="sxs-lookup"><span data-stu-id="ecadf-105">You can use these functions in a query and aggregate expressions in the **SQL** property of a **QueryDef** object or when creating a **Recordset** object based on an SQL query.</span></span>

<span data-ttu-id="ecadf-106">**[Функция AVG](https://msdn.microsoft.com/library/ff822755\(v=office.15\))**</span><span class="sxs-lookup"><span data-stu-id="ecadf-106">**[Avg Function](https://msdn.microsoft.com/library/ff822755\(v=office.15\))**</span></span>

<span data-ttu-id="ecadf-107">**[Функция Count](https://msdn.microsoft.com/library/ff844748\(v=office.15\))**</span><span class="sxs-lookup"><span data-stu-id="ecadf-107">**[Count Function](https://msdn.microsoft.com/library/ff844748\(v=office.15\))**</span></span>

<span data-ttu-id="ecadf-108">**[Имя, Фамилия функции](https://msdn.microsoft.com/library/ff197381\(v=office.15\))**</span><span class="sxs-lookup"><span data-stu-id="ecadf-108">**[First, Last Functions](https://msdn.microsoft.com/library/ff197381\(v=office.15\))**</span></span>

<span data-ttu-id="ecadf-109">**[Функции Max, MIN,](https://msdn.microsoft.com/library/ff194490\(v=office.15\))**</span><span class="sxs-lookup"><span data-stu-id="ecadf-109">**[Min, Max Functions](https://msdn.microsoft.com/library/ff194490\(v=office.15\))**</span></span>

<span data-ttu-id="ecadf-110">**[StDev, StDevP функции](https://msdn.microsoft.com/library/ff197043\(v=office.15\))**</span><span class="sxs-lookup"><span data-stu-id="ecadf-110">**[StDev, StDevP Functions](https://msdn.microsoft.com/library/ff197043\(v=office.15\))**</span></span>

<span data-ttu-id="ecadf-111">**[Функция сумм](https://msdn.microsoft.com/library/ff844764\(v=office.15\))**</span><span class="sxs-lookup"><span data-stu-id="ecadf-111">**[Sum Function](https://msdn.microsoft.com/library/ff844764\(v=office.15\))**</span></span>

<span data-ttu-id="ecadf-112">**[Var, VarP функции](https://msdn.microsoft.com/library/ff192105\(v=office.15\))**</span><span class="sxs-lookup"><span data-stu-id="ecadf-112">**[Var, VarP Functions](https://msdn.microsoft.com/library/ff192105\(v=office.15\))**</span></span>

