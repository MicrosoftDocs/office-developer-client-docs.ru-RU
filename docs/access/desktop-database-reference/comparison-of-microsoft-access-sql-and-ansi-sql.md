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
# <a name="comparison-of-microsoft-access-sql-and-ansi-sql"></a><span data-ttu-id="a3a31-102">Сравнение Microsoft Access SQL и ANSI SQL</span><span class="sxs-lookup"><span data-stu-id="a3a31-102">Comparison of Microsoft Access SQL and ANSI SQL</span></span>

<span data-ttu-id="a3a31-103">**Область применения**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="a3a31-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="a3a31-104">Яд баз SQL Microsoft Access, как правило, соответствует стандарту ANSI-89 уровня 1.</span><span class="sxs-lookup"><span data-stu-id="a3a31-104">Microsoft Access database engine SQL is generally ANSI-89 Level 1 compliant.</span></span> <span data-ttu-id="a3a31-105">Однако некоторые функции SQL ANSI не реализованы в Microsoft Access SQL.</span><span class="sxs-lookup"><span data-stu-id="a3a31-105">However, certain ANSI SQL features are not implemented in Microsoft Access SQL.</span></span> <span data-ttu-id="a3a31-106">И наоборот, microsoft Access SQL зарезервированные слова и функции, не поддерживаемые в anSI SQL.</span><span class="sxs-lookup"><span data-stu-id="a3a31-106">Conversely, Microsoft Access SQL includes reserved words and features not supported in ANSI SQL.</span></span>

## <a name="major-differences"></a><span data-ttu-id="a3a31-107">Основные различия</span><span class="sxs-lookup"><span data-stu-id="a3a31-107">Major differences</span></span>

- <span data-ttu-id="a3a31-108">Microsoft Access SQL и ANSI SQL имеют разные зарезервированные слова и типы данных.</span><span class="sxs-lookup"><span data-stu-id="a3a31-108">Microsoft Access SQL and ANSI SQL each have different reserved words and data types.</span></span> <span data-ttu-id="a3a31-109">Дополнительные сведения см. в SQL microsoft [Access Database Engine reserved Words](sql-reserved-words.md) and Equivalent [ANSI SQL Data Types.](equivalent-ansi-sql-data-types.md)</span><span class="sxs-lookup"><span data-stu-id="a3a31-109">For more information, see [Microsoft Access Database Engine SQL Reserved Words](sql-reserved-words.md) and [Equivalent ANSI SQL Data Types](equivalent-ansi-sql-data-types.md).</span></span> <span data-ttu-id="a3a31-110">При использовании поставщика OLE DB для ядоработки Microsoft Access существуют дополнительные зарезервированные слова.</span><span class="sxs-lookup"><span data-stu-id="a3a31-110">Using the Microsoft Access Database Engine OLE DB Provider there are additional reserved words.</span></span>

- <span data-ttu-id="a3a31-111">**[Между... И](https://docs.microsoft.com/office/vba/access/concepts/miscellaneous/between-and-operator)**</span><span class="sxs-lookup"><span data-stu-id="a3a31-111">**[Between…And](https://docs.microsoft.com/office/vba/access/concepts/miscellaneous/between-and-operator)**</span></span>
    
  <span data-ttu-id="a3a31-112">*expr1* \[ NOT \] **Between** *value1* **And** *value2*</span><span class="sxs-lookup"><span data-stu-id="a3a31-112">*expr1* \[NOT\] **Between** *value1* **And** *value2*</span></span>
    
  <span data-ttu-id="a3a31-113">В Microsoft Access SQL *значение 1* может быть больше *значения 2;* в anSI SQL *значение 1* должно быть равно или меньше *значения 2.*</span><span class="sxs-lookup"><span data-stu-id="a3a31-113">In Microsoft Access SQL, *value1* can be greater than *value2*; in ANSI SQL, *value1* must be equal to or less than *value2.*</span></span>

- <span data-ttu-id="a3a31-114">Microsoft Access SQL поддерживает как поддиансовые знаки [](using-wildcard-characters-in-string-comparisons.md) anSI SQL, так и поддиафидные знаки, которые используются в ядере баз данных Microsoft Access с оператором **[Like.](https://docs.microsoft.com/office/vba/access/Concepts/Structured-Query-Language/like-operator-microsoft-access-sql)**</span><span class="sxs-lookup"><span data-stu-id="a3a31-114">Microsoft Access SQL supports both ANSI SQL wildcard characters and [wildcard characters](using-wildcard-characters-in-string-comparisons.md) that are specific to the Microsoft Access database engine to use with the **[Like](https://docs.microsoft.com/office/vba/access/Concepts/Structured-Query-Language/like-operator-microsoft-access-sql)** operator.</span></span> <span data-ttu-id="a3a31-115">Использование поддиапозитных знаков ANSI и ядер базы данных Microsoft Access является взаимоисключающими.</span><span class="sxs-lookup"><span data-stu-id="a3a31-115">The use of the ANSI and Microsoft Access database engine wildcard characters is mutually exclusive.</span></span> <span data-ttu-id="a3a31-116">Необходимо использовать один набор или другой набор и не может их смешивать.</span><span class="sxs-lookup"><span data-stu-id="a3a31-116">You must use one set or the other and cannot mix them.</span></span> <span data-ttu-id="a3a31-117">Поддиапные SQL ANSI доступны только при использовании ядер базы данных Microsoft Access и поставщика OLE DB ядер баз данных Microsoft Access.</span><span class="sxs-lookup"><span data-stu-id="a3a31-117">The ANSI SQL wildcards are only available when using the Microsoft Access database engine and the Microsoft Access Database Engine OLE DB Provider.</span></span> <span data-ttu-id="a3a31-118">Если вы попытались использовать под SQL ANSI через Microsoft Access или DAO, они будут интерпретируются как литералы.</span><span class="sxs-lookup"><span data-stu-id="a3a31-118">If you try to use the ANSI SQL wildcards through Microsoft Access or DAO, then they will be interpreted as literals.</span></span> <span data-ttu-id="a3a31-119">При использовании поставщика OLE DB для ядоработки OLE DB для ядоработки Microsoft Access используется обратное.</span><span class="sxs-lookup"><span data-stu-id="a3a31-119">The opposite is true when using the Microsoft Access Database Engine OLE DB Provider.</span></span>
    
    <table>
    <colgroup>
    <col style="width: 33%" />
    <col style="width: 33%" />
    <col style="width: 33%" />
    </colgroup>
    <thead>
    <tr class="header">
    <th><p><span data-ttu-id="a3a31-120">Совпадающий символ</span><span class="sxs-lookup"><span data-stu-id="a3a31-120">Matching character</span></span></p></th>
    <th><p><span data-ttu-id="a3a31-121">Microsoft Access SQL</span><span class="sxs-lookup"><span data-stu-id="a3a31-121">Microsoft Access SQL</span></span></p></th>
    <th><p><span data-ttu-id="a3a31-122">ANSI SQL</span><span class="sxs-lookup"><span data-stu-id="a3a31-122">ANSI SQL</span></span></p></th>
    </tr>
    </thead>
    <tbody>
    <tr class="odd">
    <td><p><span data-ttu-id="a3a31-123">Любой знак</span><span class="sxs-lookup"><span data-stu-id="a3a31-123">Any single character</span></span></p></td>
    <td><p><span data-ttu-id="a3a31-124">?</span><span class="sxs-lookup"><span data-stu-id="a3a31-124">?</span></span></p></td>
    <td><p><span data-ttu-id="a3a31-125">_ (знак подчеркивания)</span><span class="sxs-lookup"><span data-stu-id="a3a31-125">_ (underscore)</span></span></p></td>
    </tr>
    <tr class="even">
    <td><p><span data-ttu-id="a3a31-126">Ноль или более символов</span><span class="sxs-lookup"><span data-stu-id="a3a31-126">Zero or more characters</span></span></p></td>
    <td><p>*</p></td>
    <td><p>%</p></td>
    </tr>
    </tbody>
    </table>


- <span data-ttu-id="a3a31-127">Как правило SQL Microsoft Access менее строгий.</span><span class="sxs-lookup"><span data-stu-id="a3a31-127">Microsoft Access SQL is generally less restrictive.</span></span> <span data-ttu-id="a3a31-128">Например, он разрешает группировку и порядок выражений.</span><span class="sxs-lookup"><span data-stu-id="a3a31-128">For example, it permits grouping and ordering on expressions.</span></span>

- <span data-ttu-id="a3a31-129">Microsoft Access SQL поддерживает более мощные выражения.</span><span class="sxs-lookup"><span data-stu-id="a3a31-129">Microsoft Access SQL supports more powerful expressions.</span></span>

## <a name="enhanced-features-of-microsoft-access-sql"></a><span data-ttu-id="a3a31-130">Расширенные функции microsoft Access SQL</span><span class="sxs-lookup"><span data-stu-id="a3a31-130">Enhanced features of Microsoft Access SQL</span></span>

<span data-ttu-id="a3a31-131">Microsoft Access SQL предоставляет следующие расширенные функции:</span><span class="sxs-lookup"><span data-stu-id="a3a31-131">Microsoft Access SQL provides the following enhanced features:</span></span>

- <span data-ttu-id="a3a31-132">Заявление [TRANSFORM,](transform-statement-microsoft-access-sql.md) которое поддерживает перекрестные запросы.</span><span class="sxs-lookup"><span data-stu-id="a3a31-132">The [TRANSFORM](transform-statement-microsoft-access-sql.md) statement, which provides support for crosstab queries.</span></span>

- <span data-ttu-id="a3a31-133">Дополнительные [агрегатные функции,](sql-aggregate-functions-sql.md)такие как **StDev** и **VarP.**</span><span class="sxs-lookup"><span data-stu-id="a3a31-133">Additional [aggregate functions](sql-aggregate-functions-sql.md), such as **StDev** and **VarP**.</span></span>

- <span data-ttu-id="a3a31-134">Объявление [PARAMETERS](parameters-declaration-microsoft-access-sql.md) для определения запросов параметров.</span><span class="sxs-lookup"><span data-stu-id="a3a31-134">The [PARAMETERS](parameters-declaration-microsoft-access-sql.md) declaration for defining parameter queries.</span></span>

## <a name="ansi-sql-features-not-supported-in-microsoft-access-sql"></a><span data-ttu-id="a3a31-135">Функции SQL ANSI не поддерживаются в Microsoft Access SQL</span><span class="sxs-lookup"><span data-stu-id="a3a31-135">ANSI SQL features not supported in Microsoft Access SQL</span></span>

<span data-ttu-id="a3a31-136">Microsoft Access SQL не поддерживает следующие функции SQL ANSI:</span><span class="sxs-lookup"><span data-stu-id="a3a31-136">Microsoft Access SQL does not support the following ANSI SQL features:</span></span>

- <span data-ttu-id="a3a31-137">ОТДЕЛЬНЫЕ сводные ссылки на функции.</span><span class="sxs-lookup"><span data-stu-id="a3a31-137">DISTINCT aggregate function references.</span></span> <span data-ttu-id="a3a31-138">Например, microsoft Access SQL не разрешает СУММ(DISTINCT *columnname).*</span><span class="sxs-lookup"><span data-stu-id="a3a31-138">For example, Microsoft Access SQL does not allow SUM(DISTINCT *columnname*).</span></span>

- <span data-ttu-id="a3a31-139">Предложение LIMIT TO *nn* ROWS, используемого для ограничения количества строк, возвращаемого запросом.</span><span class="sxs-lookup"><span data-stu-id="a3a31-139">The LIMIT TO *nn* ROWS clause used to limit the number of rows returned by a query.</span></span> <span data-ttu-id="a3a31-140">Для ограничения области [запроса можно](https://docs.microsoft.com/office/vba/access/Concepts/Structured-Query-Language/where-clause-microsoft-access-sql) использовать только предложение WHERE.</span><span class="sxs-lookup"><span data-stu-id="a3a31-140">You can use only the [WHERE clause](https://docs.microsoft.com/office/vba/access/Concepts/Structured-Query-Language/where-clause-microsoft-access-sql) to limit the scope of a query.</span></span>

