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
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32296054"
---
# <a name="comparison-of-microsoft-access-sql-and-ansi-sql"></a><span data-ttu-id="63924-102">Сравнение Microsoft Access SQL и ANSI SQL</span><span class="sxs-lookup"><span data-stu-id="63924-102">Comparison of Microsoft Access SQL and ANSI SQL</span></span>

<span data-ttu-id="63924-103">**Область применения**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="63924-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="63924-104">SQL ядра СУБД Microsoft Access, как правило, соответствует СТАНДАРТу ANSI-89 Level 1.</span><span class="sxs-lookup"><span data-stu-id="63924-104">Microsoft Access database engine SQL is generally ANSI-89 Level 1 compliant.</span></span> <span data-ttu-id="63924-105">Однако некоторые функции ANSI SQL не реализованы в Microsoft Access SQL.</span><span class="sxs-lookup"><span data-stu-id="63924-105">However, certain ANSI SQL features are not implemented in Microsoft Access SQL.</span></span> <span data-ttu-id="63924-106">И наоборот, Microsoft Access SQL включает зарезервированные слова и функции, не поддерживаемые в ANSI SQL.</span><span class="sxs-lookup"><span data-stu-id="63924-106">Conversely, Microsoft Access SQL includes reserved words and features not supported in ANSI SQL.</span></span>

## <a name="major-differences"></a><span data-ttu-id="63924-107">Основные различия</span><span class="sxs-lookup"><span data-stu-id="63924-107">Major differences</span></span>

- <span data-ttu-id="63924-108">Microsoft Access SQL и ANSI SQL имеют различные зарезервированные слова и типы данных.</span><span class="sxs-lookup"><span data-stu-id="63924-108">Microsoft Access SQL and ANSI SQL each have different reserved words and data types.</span></span> <span data-ttu-id="63924-109">Для получения дополнительных сведений см [ЗарезервированНые слова SQL для ядра СУБД Microsoft Access](sql-reserved-words.md) и [эквивалентные типы данных ANSI SQL](equivalent-ansi-sql-data-types.md).</span><span class="sxs-lookup"><span data-stu-id="63924-109">For more information, see [Microsoft Access Database Engine SQL Reserved Words](sql-reserved-words.md) and [Equivalent ANSI SQL Data Types](equivalent-ansi-sql-data-types.md).</span></span> <span data-ttu-id="63924-110">Использование поставщика OLE DB для ядра СУБД Microsoft Access содержит дополнительные зарезервированные слова.</span><span class="sxs-lookup"><span data-stu-id="63924-110">Using the Microsoft Access Database Engine OLE DB Provider there are additional reserved words.</span></span>

- <span data-ttu-id="63924-111">**[Между... С](https://docs.microsoft.com/office/vba/access/concepts/miscellaneous/and-operator)**</span><span class="sxs-lookup"><span data-stu-id="63924-111">**[Between…And](https://docs.microsoft.com/office/vba/access/concepts/miscellaneous/and-operator)**</span></span>
    
  <span data-ttu-id="63924-112">*Выражение1* \[Не\] **между** *Значение1* **и** *value2*</span><span class="sxs-lookup"><span data-stu-id="63924-112">*expr1* \[NOT\] **Between** *value1* **And** *value2*</span></span>
    
  <span data-ttu-id="63924-113">В Microsoft Access SQL *Значение1* может быть больше, чем *value2*. в ANSI SQL *Значение1* должно быть равно или меньше *value2.*</span><span class="sxs-lookup"><span data-stu-id="63924-113">In Microsoft Access SQL, *value1* can be greater than *value2*; in ANSI SQL, *value1* must be equal to or less than *value2.*</span></span>

- <span data-ttu-id="63924-114">Microsoft Access SQL поддерживает как подстановочные знаки ANSI SQL, так и [подстановочные знаки](using-wildcard-characters-in-string-comparisons.md) , которые относятся к ядру СУБД Microsoft Access с помощью оператора **[Like](https://docs.microsoft.com/office/vba/access/Concepts/Structured-Query-Language/like-operator-microsoft-access-sql)** .</span><span class="sxs-lookup"><span data-stu-id="63924-114">Microsoft Access SQL supports both ANSI SQL wildcard characters and [wildcard characters](using-wildcard-characters-in-string-comparisons.md) that are specific to the Microsoft Access database engine to use with the **[Like](https://docs.microsoft.com/office/vba/access/Concepts/Structured-Query-Language/like-operator-microsoft-access-sql)** operator.</span></span> <span data-ttu-id="63924-115">Использование подстановочных знаков для механизма базы данных ANSI и Microsoft Access является взаимно исключающим.</span><span class="sxs-lookup"><span data-stu-id="63924-115">The use of the ANSI and Microsoft Access database engine wildcard characters is mutually exclusive.</span></span> <span data-ttu-id="63924-116">Вы должны использовать один набор или другой, и они не могут смешиваться.</span><span class="sxs-lookup"><span data-stu-id="63924-116">You must use one set or the other and cannot mix them.</span></span> <span data-ttu-id="63924-117">Подстановочные знаки ANSI SQL доступны только при использовании ядра СУБД Microsoft Access и поставщика OLE DB ядра СУБД Microsoft Access.</span><span class="sxs-lookup"><span data-stu-id="63924-117">The ANSI SQL wildcards are only available when using the Microsoft Access database engine and the Microsoft Access Database Engine OLE DB Provider.</span></span> <span data-ttu-id="63924-118">Если вы попытаетесь использовать подстановочные знаки ANSI SQL с помощью Microsoft Access или DAO, они будут интерпретироваться как литералы.</span><span class="sxs-lookup"><span data-stu-id="63924-118">If you try to use the ANSI SQL wildcards through Microsoft Access or DAO, then they will be interpreted as literals.</span></span> <span data-ttu-id="63924-119">Противоположным является true при использовании поставщика OLE DB для ядра СУБД Microsoft Access.</span><span class="sxs-lookup"><span data-stu-id="63924-119">The opposite is true when using the Microsoft Access Database Engine OLE DB Provider.</span></span>
    
    <table>
    <colgroup>
    <col style="width: 33%" />
    <col style="width: 33%" />
    <col style="width: 33%" />
    </colgroup>
    <thead>
    <tr class="header">
    <th><p><span data-ttu-id="63924-120">СоПоставленный символ</span><span class="sxs-lookup"><span data-stu-id="63924-120">Matching character</span></span></p></th>
    <th><p><span data-ttu-id="63924-121">Microsoft Access SQL</span><span class="sxs-lookup"><span data-stu-id="63924-121">Microsoft Access SQL</span></span></p></th>
    <th><p><span data-ttu-id="63924-122">ANSI SQL</span><span class="sxs-lookup"><span data-stu-id="63924-122">ANSI SQL</span></span></p></th>
    </tr>
    </thead>
    <tbody>
    <tr class="odd">
    <td><p><span data-ttu-id="63924-123">Любой знак</span><span class="sxs-lookup"><span data-stu-id="63924-123">Any single character</span></span></p></td>
    <td><p><span data-ttu-id="63924-124">?</span><span class="sxs-lookup"><span data-stu-id="63924-124"></span></span></p></td>
    <td><p><span data-ttu-id="63924-125">_ (знак подчеркивания)</span><span class="sxs-lookup"><span data-stu-id="63924-125">_ (underscore)</span></span></p></td>
    </tr>
    <tr class="even">
    <td><p><span data-ttu-id="63924-126">Ноль или более символов</span><span class="sxs-lookup"><span data-stu-id="63924-126">Zero or more characters</span></span></p></td>
    <td><p>*</p></td>
    <td><p>%</p></td>
    </tr>
    </tbody>
    </table>


- <span data-ttu-id="63924-127">Microsoft Access SQL, как правило, является менее ограниченным.</span><span class="sxs-lookup"><span data-stu-id="63924-127">Microsoft Access SQL is generally less restrictive.</span></span> <span data-ttu-id="63924-128">Например, Допускается группировка и упорядочивание выражений.</span><span class="sxs-lookup"><span data-stu-id="63924-128">For example, it permits grouping and ordering on expressions.</span></span>

- <span data-ttu-id="63924-129">Microsoft Access SQL поддерживает более эффективные выражения.</span><span class="sxs-lookup"><span data-stu-id="63924-129">Microsoft Access SQL supports more powerful expressions.</span></span>

## <a name="enhanced-features-of-microsoft-access-sql"></a><span data-ttu-id="63924-130">Расширенные функции Microsoft Access SQL</span><span class="sxs-lookup"><span data-stu-id="63924-130">Enhanced features of Microsoft Access SQL</span></span>

<span data-ttu-id="63924-131">Microsoft Access SQL предоставляет следующие расширенные возможности:</span><span class="sxs-lookup"><span data-stu-id="63924-131">Microsoft Access SQL provides the following enhanced features:</span></span>

- <span data-ttu-id="63924-132">Оператор [Transform](transform-statement-microsoft-access-sql.md) , который обеспечивает поддержку перекрестных запросов.</span><span class="sxs-lookup"><span data-stu-id="63924-132">The [TRANSFORM](transform-statement-microsoft-access-sql.md) statement, which provides support for crosstab queries.</span></span>

- <span data-ttu-id="63924-133">Дополнительные [статистические функции](sql-aggregate-functions-sql.md), такие как **STDEV** и **ДИСПР**.</span><span class="sxs-lookup"><span data-stu-id="63924-133">Additional [aggregate functions](sql-aggregate-functions-sql.md), such as **StDev** and **VarP**.</span></span>

- <span data-ttu-id="63924-134">Объявление [параметров](parameters-declaration-microsoft-access-sql.md) для определения запросов с параметрами.</span><span class="sxs-lookup"><span data-stu-id="63924-134">The [PARAMETERS](parameters-declaration-microsoft-access-sql.md) declaration for defining parameter queries.</span></span>

## <a name="ansi-sql-features-not-supported-in-microsoft-access-sql"></a><span data-ttu-id="63924-135">Функции ANSI SQL, не поддерживаемые в Microsoft Access SQL</span><span class="sxs-lookup"><span data-stu-id="63924-135">ANSI SQL features not supported in Microsoft Access SQL</span></span>

<span data-ttu-id="63924-136">Microsoft Access SQL не поддерживает следующие функции ANSI SQL:</span><span class="sxs-lookup"><span data-stu-id="63924-136">Microsoft Access SQL does not support the following ANSI SQL features:</span></span>

- <span data-ttu-id="63924-137">Ссылки на статистические функции DISTINCT.</span><span class="sxs-lookup"><span data-stu-id="63924-137">DISTINCT aggregate function references.</span></span> <span data-ttu-id="63924-138">Например, SQL Microsoft Access не позволяет использовать SUM (DISTINCT) \*\*.</span><span class="sxs-lookup"><span data-stu-id="63924-138">For example, Microsoft Access SQL does not allow SUM(DISTINCT *columnname*).</span></span>

- <span data-ttu-id="63924-139">Предложение LIMIT TO *nn* Rows, используемое для ограничения числа строк, возвращаемых запросом.</span><span class="sxs-lookup"><span data-stu-id="63924-139">The LIMIT TO *nn* ROWS clause used to limit the number of rows returned by a query.</span></span> <span data-ttu-id="63924-140">Для ограничения области запроса можно использовать только [предложение WHERE](https://docs.microsoft.com/office/vba/access/Concepts/Structured-Query-Language/where-clause-microsoft-access-sql) .</span><span class="sxs-lookup"><span data-stu-id="63924-140">You can use only the [WHERE clause](https://docs.microsoft.com/office/vba/access/Concepts/Structured-Query-Language/where-clause-microsoft-access-sql) to limit the scope of a query.</span></span>

