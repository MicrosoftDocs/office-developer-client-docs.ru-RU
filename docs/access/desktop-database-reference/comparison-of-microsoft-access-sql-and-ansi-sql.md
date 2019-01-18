---
title: Сравнение Microsoft Access SQL и ANSI SQL
TOCTitle: Comparison of Microsoft Access SQL and ANSI SQL
ms:assetid: 0686f98f-10fe-0e02-e9d1-84ff3e755b57
ms:mtpsurl: https://msdn.microsoft.com/library/Ff844937(v=office.15)
ms:contentKeyID: 48543052
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: 195d9f5d882fd252b1b10e937fe851c4830c52d3
ms.sourcegitcommit: d6695c94415fa47952ee7961a69660abc0904434
ms.translationtype: Auto
ms.contentlocale: ru-RU
ms.lasthandoff: 01/17/2019
ms.locfileid: "28713081"
---
# <a name="comparison-of-microsoft-access-sql-and-ansi-sql"></a><span data-ttu-id="e4457-102">Сравнение Microsoft Access SQL и ANSI SQL</span><span class="sxs-lookup"><span data-stu-id="e4457-102">Comparison of Microsoft Access SQL and ANSI SQL</span></span>

<span data-ttu-id="e4457-103">**Применимо к**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="e4457-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="e4457-104">Ядро СУБД Microsoft Access SQL обычно является совместимым с ANSI-89 уровня 1.</span><span class="sxs-lookup"><span data-stu-id="e4457-104">Microsoft Access database engine SQL is generally ANSI-89 Level 1 compliant.</span></span> <span data-ttu-id="e4457-105">Тем не менее некоторые функции ANSI SQL не реализованы в Microsoft Access SQL.</span><span class="sxs-lookup"><span data-stu-id="e4457-105">However, certain ANSI SQL features are not implemented in Microsoft Access SQL.</span></span> <span data-ttu-id="e4457-106">С другой стороны Microsoft Access SQL включает в себя зарезервированные слова и функции, не поддерживаемые в формате ANSI SQL.</span><span class="sxs-lookup"><span data-stu-id="e4457-106">Conversely, Microsoft Access SQL includes reserved words and features not supported in ANSI SQL.</span></span>

## <a name="major-differences"></a><span data-ttu-id="e4457-107">Основные различия</span><span class="sxs-lookup"><span data-stu-id="e4457-107">Major differences</span></span>

- <span data-ttu-id="e4457-108">Microsoft Access SQL и ANSI SQL иметь разные зарезервированные слова и типы данных.</span><span class="sxs-lookup"><span data-stu-id="e4457-108">Microsoft Access SQL and ANSI SQL each have different reserved words and data types.</span></span> <span data-ttu-id="e4457-109">Для получения дополнительных сведений см [Microsoft Access базы данных модуля SQL зарезервированные слова](sql-reserved-words.md) и [Эквивалентные типы данных ANSI SQL](equivalent-ansi-sql-data-types.md).</span><span class="sxs-lookup"><span data-stu-id="e4457-109">For more information, see [Microsoft Access Database Engine SQL Reserved Words](sql-reserved-words.md) and [Equivalent ANSI SQL Data Types](equivalent-ansi-sql-data-types.md).</span></span> <span data-ttu-id="e4457-110">С помощью Microsoft Access базы данных модуля поставщика OLE DB существуют дополнительные зарезервированные слова.</span><span class="sxs-lookup"><span data-stu-id="e4457-110">Using the Microsoft Access Database Engine OLE DB Provider there are additional reserved words.</span></span>

- <span data-ttu-id="e4457-111">**[Между... И](https://docs.microsoft.com/office/vba/access/concepts/miscellaneous/and-operator)**</span><span class="sxs-lookup"><span data-stu-id="e4457-111">**[Between…And](https://docs.microsoft.com/office/vba/access/concepts/miscellaneous/and-operator)**</span></span>
    
  <span data-ttu-id="e4457-112">*Expr1* \[Не\] **между** *значение1* **и** *значение2*</span><span class="sxs-lookup"><span data-stu-id="e4457-112">*expr1* \[NOT\] **Between** *value1* **And** *value2*</span></span>
    
  <span data-ttu-id="e4457-113">В Microsoft Access SQL *значение1* может быть больше, чем *значение2*; в формате ANSI SQL *значение1* должно быть не более чем *значение2.*</span><span class="sxs-lookup"><span data-stu-id="e4457-113">In Microsoft Access SQL, *value1* can be greater than *value2*; in ANSI SQL, *value1* must be equal to or less than *value2.*</span></span>

- <span data-ttu-id="e4457-114">Microsoft Access SQL поддерживает подстановочные знаки ANSI SQL и [подстановочные знаки](using-wildcard-characters-in-string-comparisons.md) , относящиеся к ядру базы данных Microsoft Access для использования с оператор **[Like](https://docs.microsoft.com/office/vba/access/Concepts/Structured-Query-Language/like-operator-microsoft-access-sql)** .</span><span class="sxs-lookup"><span data-stu-id="e4457-114">Microsoft Access SQL supports both ANSI SQL wildcard characters and [wildcard characters](using-wildcard-characters-in-string-comparisons.md) that are specific to the Microsoft Access database engine to use with the **[Like](https://docs.microsoft.com/office/vba/access/Concepts/Structured-Query-Language/like-operator-microsoft-access-sql)** operator.</span></span> <span data-ttu-id="e4457-115">Использование ANSI и Microsoft Access базы данных модуля подстановочные знаки являются взаимоисключающими.</span><span class="sxs-lookup"><span data-stu-id="e4457-115">The use of the ANSI and Microsoft Access database engine wildcard characters is mutually exclusive.</span></span> <span data-ttu-id="e4457-116">Необходимо использовать один набор знаков, их нельзя смешивать.</span><span class="sxs-lookup"><span data-stu-id="e4457-116">You must use one set or the other and cannot mix them.</span></span> <span data-ttu-id="e4457-117">Подстановочные знаки доступны только при использовании ядро базы данных Microsoft Access и Microsoft Access базы данных модуля поставщика OLE DB.</span><span class="sxs-lookup"><span data-stu-id="e4457-117">The ANSI SQL wildcards are only available when using the Microsoft Access database engine and the Microsoft Access Database Engine OLE DB Provider.</span></span> <span data-ttu-id="e4457-118">При попытке использовать подстановочные знаки ANSI SQL через Microsoft Access или DAO, они будут интерпретируются как литералы.</span><span class="sxs-lookup"><span data-stu-id="e4457-118">If you try to use the ANSI SQL wildcards through Microsoft Access or DAO, then they will be interpreted as literals.</span></span> <span data-ttu-id="e4457-119">При использовании Microsoft Access базы данных модуля поставщика OLE DB верно обратное.</span><span class="sxs-lookup"><span data-stu-id="e4457-119">The opposite is true when using the Microsoft Access Database Engine OLE DB Provider.</span></span>
    
    <table>
    <colgroup>
    <col style="width: 33%" />
    <col style="width: 33%" />
    <col style="width: 33%" />
    </colgroup>
    <thead>
    <tr class="header">
    <th><p><span data-ttu-id="e4457-120">Символ соответствия</span><span class="sxs-lookup"><span data-stu-id="e4457-120">Matching character</span></span></p></th>
    <th><p><span data-ttu-id="e4457-121">Microsoft Access SQL</span><span class="sxs-lookup"><span data-stu-id="e4457-121">Microsoft Access SQL</span></span></p></th>
    <th><p><span data-ttu-id="e4457-122">ANSI SQL</span><span class="sxs-lookup"><span data-stu-id="e4457-122">ANSI SQL</span></span></p></th>
    </tr>
    </thead>
    <tbody>
    <tr class="odd">
    <td><p><span data-ttu-id="e4457-123">Любой знак</span><span class="sxs-lookup"><span data-stu-id="e4457-123">Any single character</span></span></p></td>
    <td><p><span data-ttu-id="e4457-124">?</span><span class="sxs-lookup"><span data-stu-id="e4457-124"></span></span></p></td>
    <td><p><span data-ttu-id="e4457-125">_ (знак подчеркивания)</span><span class="sxs-lookup"><span data-stu-id="e4457-125">_ (underscore)</span></span></p></td>
    </tr>
    <tr class="even">
    <td><p><span data-ttu-id="e4457-126">Ноль или более символов</span><span class="sxs-lookup"><span data-stu-id="e4457-126">Zero or more characters</span></span></p></td>
    <td><p>*</p></td>
    <td><p>%</p></td>
    </tr>
    </tbody>
    </table>


- <span data-ttu-id="e4457-127">Microsoft Access SQL обычно меньше ограничений.</span><span class="sxs-lookup"><span data-stu-id="e4457-127">Microsoft Access SQL is generally less restrictive.</span></span> <span data-ttu-id="e4457-128">Например уменьшение Группировка и порядок выражений.</span><span class="sxs-lookup"><span data-stu-id="e4457-128">For example, it permits grouping and ordering on expressions.</span></span>

- <span data-ttu-id="e4457-129">Microsoft Access SQL поддерживает более мощного выражения.</span><span class="sxs-lookup"><span data-stu-id="e4457-129">Microsoft Access SQL supports more powerful expressions.</span></span>

## <a name="enhanced-features-of-microsoft-access-sql"></a><span data-ttu-id="e4457-130">Расширенные возможности Microsoft Access SQL</span><span class="sxs-lookup"><span data-stu-id="e4457-130">Enhanced features of Microsoft Access SQL</span></span>

<span data-ttu-id="e4457-131">Microsoft Access SQL предоставляет следующие расширенные возможности:</span><span class="sxs-lookup"><span data-stu-id="e4457-131">Microsoft Access SQL provides the following enhanced features:</span></span>

- <span data-ttu-id="e4457-132">Оператор [ПРЕОБРАЗОВАНИЯ](transform-statement-microsoft-access-sql.md) , который обеспечивает поддержку перекрестных запросов.</span><span class="sxs-lookup"><span data-stu-id="e4457-132">The [TRANSFORM](transform-statement-microsoft-access-sql.md) statement, which provides support for crosstab queries.</span></span>

- <span data-ttu-id="e4457-133">Дополнительные [агрегатных функций](sql-aggregate-functions-sql.md), таких как **StDev** и **VarP**.</span><span class="sxs-lookup"><span data-stu-id="e4457-133">Additional [aggregate functions](sql-aggregate-functions-sql.md), such as **StDev** and **VarP**.</span></span>

- <span data-ttu-id="e4457-134">Объявление [параметров](parameters-declaration-microsoft-access-sql.md) для определения параметров запроса.</span><span class="sxs-lookup"><span data-stu-id="e4457-134">The [PARAMETERS](parameters-declaration-microsoft-access-sql.md) declaration for defining parameter queries.</span></span>

## <a name="ansi-sql-features-not-supported-in-microsoft-access-sql"></a><span data-ttu-id="e4457-135">Функции ANSI SQL, не поддерживаемые в Microsoft Access SQL</span><span class="sxs-lookup"><span data-stu-id="e4457-135">ANSI SQL features not supported in Microsoft Access SQL</span></span>

<span data-ttu-id="e4457-136">Microsoft Access SQL не поддерживает следующие функции ANSI SQL:</span><span class="sxs-lookup"><span data-stu-id="e4457-136">Microsoft Access SQL does not support the following ANSI SQL features:</span></span>

- <span data-ttu-id="e4457-137">Ссылки на РАЗЛИЧНЫЕ статистические функции.</span><span class="sxs-lookup"><span data-stu-id="e4457-137">DISTINCT aggregate function references.</span></span> <span data-ttu-id="e4457-138">К примеру Microsoft Access SQL не разрешает сумм (ЧЕТКИЕ *columnname*).</span><span class="sxs-lookup"><span data-stu-id="e4457-138">For example, Microsoft Access SQL does not allow SUM(DISTINCT *columnname*).</span></span>

- <span data-ttu-id="e4457-139">Предложения LIMIT TO *nn* СТРОК используется, чтобы ограничить число строк, возвращаемых запросом.</span><span class="sxs-lookup"><span data-stu-id="e4457-139">The LIMIT TO *nn* ROWS clause used to limit the number of rows returned by a query.</span></span> <span data-ttu-id="e4457-140">[Предложение WHERE](https://docs.microsoft.com/office/vba/access/Concepts/Structured-Query-Language/where-clause-microsoft-access-sql) можно использовать для ограничения области запроса.</span><span class="sxs-lookup"><span data-stu-id="e4457-140">You can use only the [WHERE clause](https://docs.microsoft.com/office/vba/access/Concepts/Structured-Query-Language/where-clause-microsoft-access-sql) to limit the scope of a query.</span></span>

