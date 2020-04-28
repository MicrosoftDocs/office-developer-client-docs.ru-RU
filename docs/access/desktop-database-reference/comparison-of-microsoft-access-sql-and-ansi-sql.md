---
title: Сравнение Microsoft Access SQL и ANSI SQL
TOCTitle: Comparison of Microsoft Access SQL and ANSI SQL
ms:assetid: 0686f98f-10fe-0e02-e9d1-84ff3e755b57
ms:mtpsurl: https://msdn.microsoft.com/library/Ff844937(v=office.15)
ms:contentKeyID: 48543052
ms.date: 06/13/2019
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: 4e9f30401891452970fdbe80123fc373e26f26c6
ms.sourcegitcommit: d0e1ce095a478d90411abb8c147eb9efe19ffa5f
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/12/2019
ms.locfileid: "34870859"
---
# <a name="comparison-of-microsoft-access-sql-and-ansi-sql"></a><span data-ttu-id="f755e-102">Сравнение Microsoft Access SQL и ANSI SQL</span><span class="sxs-lookup"><span data-stu-id="f755e-102">Comparison of Microsoft Access SQL and ANSI SQL</span></span>

<span data-ttu-id="f755e-103">**Область применения**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="f755e-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="f755e-104">SQL ядра СУБД Microsoft Access, как правило, соответствует стандарту ANSI-89 Level 1.</span><span class="sxs-lookup"><span data-stu-id="f755e-104">Microsoft Access database engine SQL is generally ANSI-89 Level 1 compliant.</span></span> <span data-ttu-id="f755e-105">Однако некоторые функции ANSI SQL не реализованы в Microsoft Access SQL.</span><span class="sxs-lookup"><span data-stu-id="f755e-105">However, certain ANSI SQL features are not implemented in Microsoft Access SQL.</span></span> <span data-ttu-id="f755e-106">И наоборот, Microsoft Access SQL включает зарезервированные слова и функции, не поддерживаемые в ANSI SQL.</span><span class="sxs-lookup"><span data-stu-id="f755e-106">Conversely, Microsoft Access SQL includes reserved words and features not supported in ANSI SQL.</span></span>

## <a name="major-differences"></a><span data-ttu-id="f755e-107">Основные различия</span><span class="sxs-lookup"><span data-stu-id="f755e-107">Major differences</span></span>

- <span data-ttu-id="f755e-108">Microsoft Access SQL и ANSI SQL имеют различные зарезервированные слова и типы данных.</span><span class="sxs-lookup"><span data-stu-id="f755e-108">Microsoft Access SQL and ANSI SQL each have different reserved words and data types.</span></span> <span data-ttu-id="f755e-109">Для получения дополнительных сведений см [зарезервированные слова SQL для ядра СУБД Microsoft Access](sql-reserved-words.md) и [эквивалентные типы данных ANSI SQL](equivalent-ansi-sql-data-types.md).</span><span class="sxs-lookup"><span data-stu-id="f755e-109">For more information, see [Microsoft Access Database Engine SQL Reserved Words](sql-reserved-words.md) and [Equivalent ANSI SQL Data Types](equivalent-ansi-sql-data-types.md).</span></span> <span data-ttu-id="f755e-110">Использование поставщика OLE DB для ядра СУБД Microsoft Access содержит дополнительные зарезервированные слова.</span><span class="sxs-lookup"><span data-stu-id="f755e-110">Using the Microsoft Access Database Engine OLE DB Provider there are additional reserved words.</span></span>

- <span data-ttu-id="f755e-111">**[Между... С](https://docs.microsoft.com/office/vba/access/concepts/miscellaneous/between-and-operator)**</span><span class="sxs-lookup"><span data-stu-id="f755e-111">**[Between…And](https://docs.microsoft.com/office/vba/access/concepts/miscellaneous/between-and-operator)**</span></span>
    
  <span data-ttu-id="f755e-112">*Выражение1* \[— не\] **между** *Значение1* **и** *value2*</span><span class="sxs-lookup"><span data-stu-id="f755e-112">*expr1* \[NOT\] **Between** *value1* **And** *value2*</span></span>
    
  <span data-ttu-id="f755e-113">В Microsoft Access SQL *Значение1* может быть больше, чем *value2*. в ANSI SQL *Значение1* должно быть равно или меньше *value2.*</span><span class="sxs-lookup"><span data-stu-id="f755e-113">In Microsoft Access SQL, *value1* can be greater than *value2*; in ANSI SQL, *value1* must be equal to or less than *value2.*</span></span>

- <span data-ttu-id="f755e-114">Microsoft Access SQL поддерживает как подстановочные знаки ANSI SQL, так и [подстановочные знаки](using-wildcard-characters-in-string-comparisons.md) , которые относятся к ядру СУБД Microsoft Access с помощью оператора **[Like](https://docs.microsoft.com/office/vba/access/Concepts/Structured-Query-Language/like-operator-microsoft-access-sql)** .</span><span class="sxs-lookup"><span data-stu-id="f755e-114">Microsoft Access SQL supports both ANSI SQL wildcard characters and [wildcard characters](using-wildcard-characters-in-string-comparisons.md) that are specific to the Microsoft Access database engine to use with the **[Like](https://docs.microsoft.com/office/vba/access/Concepts/Structured-Query-Language/like-operator-microsoft-access-sql)** operator.</span></span> <span data-ttu-id="f755e-115">Использование подстановочных знаков для механизма базы данных ANSI и Microsoft Access является взаимно исключающим.</span><span class="sxs-lookup"><span data-stu-id="f755e-115">The use of the ANSI and Microsoft Access database engine wildcard characters is mutually exclusive.</span></span> <span data-ttu-id="f755e-116">Вы должны использовать один набор или другой, и они не могут смешиваться.</span><span class="sxs-lookup"><span data-stu-id="f755e-116">You must use one set or the other and cannot mix them.</span></span> <span data-ttu-id="f755e-117">Подстановочные знаки ANSI SQL доступны только при использовании ядра СУБД Microsoft Access и поставщика OLE DB ядра СУБД Microsoft Access.</span><span class="sxs-lookup"><span data-stu-id="f755e-117">The ANSI SQL wildcards are only available when using the Microsoft Access database engine and the Microsoft Access Database Engine OLE DB Provider.</span></span> <span data-ttu-id="f755e-118">Если вы попытаетесь использовать подстановочные знаки ANSI SQL с помощью Microsoft Access или DAO, они будут интерпретироваться как литералы.</span><span class="sxs-lookup"><span data-stu-id="f755e-118">If you try to use the ANSI SQL wildcards through Microsoft Access or DAO, then they will be interpreted as literals.</span></span> <span data-ttu-id="f755e-119">Противоположным является true при использовании поставщика OLE DB для ядра СУБД Microsoft Access.</span><span class="sxs-lookup"><span data-stu-id="f755e-119">The opposite is true when using the Microsoft Access Database Engine OLE DB Provider.</span></span>
    
    <table>
    <colgroup>
    <col style="width: 33%" />
    <col style="width: 33%" />
    <col style="width: 33%" />
    </colgroup>
    <thead>
    <tr class="header">
    <th><p><span data-ttu-id="f755e-120">Сопоставленный символ</span><span class="sxs-lookup"><span data-stu-id="f755e-120">Matching character</span></span></p></th>
    <th><p><span data-ttu-id="f755e-121">Microsoft Access SQL</span><span class="sxs-lookup"><span data-stu-id="f755e-121">Microsoft Access SQL</span></span></p></th>
    <th><p><span data-ttu-id="f755e-122">ANSI SQL</span><span class="sxs-lookup"><span data-stu-id="f755e-122">ANSI SQL</span></span></p></th>
    </tr>
    </thead>
    <tbody>
    <tr class="odd">
    <td><p><span data-ttu-id="f755e-123">Любой знак</span><span class="sxs-lookup"><span data-stu-id="f755e-123">Any single character</span></span></p></td>
    <td><p><span data-ttu-id="f755e-124">?</span><span class="sxs-lookup"><span data-stu-id="f755e-124">?</span></span></p></td>
    <td><p><span data-ttu-id="f755e-125">_ (знак подчеркивания)</span><span class="sxs-lookup"><span data-stu-id="f755e-125">_ (underscore)</span></span></p></td>
    </tr>
    <tr class="even">
    <td><p><span data-ttu-id="f755e-126">Ноль или более символов</span><span class="sxs-lookup"><span data-stu-id="f755e-126">Zero or more characters</span></span></p></td>
    <td><p>*</p></td>
    <td><p>%</p></td>
    </tr>
    </tbody>
    </table>


- <span data-ttu-id="f755e-127">Microsoft Access SQL, как правило, является менее ограниченным.</span><span class="sxs-lookup"><span data-stu-id="f755e-127">Microsoft Access SQL is generally less restrictive.</span></span> <span data-ttu-id="f755e-128">Например, Допускается группировка и упорядочивание выражений.</span><span class="sxs-lookup"><span data-stu-id="f755e-128">For example, it permits grouping and ordering on expressions.</span></span>

- <span data-ttu-id="f755e-129">Microsoft Access SQL поддерживает более эффективные выражения.</span><span class="sxs-lookup"><span data-stu-id="f755e-129">Microsoft Access SQL supports more powerful expressions.</span></span>

## <a name="enhanced-features-of-microsoft-access-sql"></a><span data-ttu-id="f755e-130">Расширенные функции Microsoft Access SQL</span><span class="sxs-lookup"><span data-stu-id="f755e-130">Enhanced features of Microsoft Access SQL</span></span>

<span data-ttu-id="f755e-131">Microsoft Access SQL предоставляет следующие расширенные возможности:</span><span class="sxs-lookup"><span data-stu-id="f755e-131">Microsoft Access SQL provides the following enhanced features:</span></span>

- <span data-ttu-id="f755e-132">Оператор [Transform](transform-statement-microsoft-access-sql.md) , который обеспечивает поддержку перекрестных запросов.</span><span class="sxs-lookup"><span data-stu-id="f755e-132">The [TRANSFORM](transform-statement-microsoft-access-sql.md) statement, which provides support for crosstab queries.</span></span>

- <span data-ttu-id="f755e-133">Дополнительные [статистические функции](sql-aggregate-functions-sql.md), такие как **STDEV** и **ДИСПР**.</span><span class="sxs-lookup"><span data-stu-id="f755e-133">Additional [aggregate functions](sql-aggregate-functions-sql.md), such as **StDev** and **VarP**.</span></span>

- <span data-ttu-id="f755e-134">Объявление [параметров](parameters-declaration-microsoft-access-sql.md) для определения запросов с параметрами.</span><span class="sxs-lookup"><span data-stu-id="f755e-134">The [PARAMETERS](parameters-declaration-microsoft-access-sql.md) declaration for defining parameter queries.</span></span>

## <a name="ansi-sql-features-not-supported-in-microsoft-access-sql"></a><span data-ttu-id="f755e-135">Функции ANSI SQL, не поддерживаемые в Microsoft Access SQL</span><span class="sxs-lookup"><span data-stu-id="f755e-135">ANSI SQL features not supported in Microsoft Access SQL</span></span>

<span data-ttu-id="f755e-136">Microsoft Access SQL не поддерживает следующие функции ANSI SQL:</span><span class="sxs-lookup"><span data-stu-id="f755e-136">Microsoft Access SQL does not support the following ANSI SQL features:</span></span>

- <span data-ttu-id="f755e-137">Ссылки на статистические функции DISTINCT.</span><span class="sxs-lookup"><span data-stu-id="f755e-137">DISTINCT aggregate function references.</span></span> <span data-ttu-id="f755e-138">Например, SQL Microsoft Access не позволяет использовать SUM *(DISTINCT)*.</span><span class="sxs-lookup"><span data-stu-id="f755e-138">For example, Microsoft Access SQL does not allow SUM(DISTINCT *columnname*).</span></span>

- <span data-ttu-id="f755e-139">Предложение LIMIT TO *nn* Rows, используемое для ограничения числа строк, возвращаемых запросом.</span><span class="sxs-lookup"><span data-stu-id="f755e-139">The LIMIT TO *nn* ROWS clause used to limit the number of rows returned by a query.</span></span> <span data-ttu-id="f755e-140">Для ограничения области запроса можно использовать только [предложение WHERE](https://docs.microsoft.com/office/vba/access/Concepts/Structured-Query-Language/where-clause-microsoft-access-sql) .</span><span class="sxs-lookup"><span data-stu-id="f755e-140">You can use only the [WHERE clause](https://docs.microsoft.com/office/vba/access/Concepts/Structured-Query-Language/where-clause-microsoft-access-sql) to limit the scope of a query.</span></span>

