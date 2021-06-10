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
# <a name="comparison-of-microsoft-access-sql-and-ansi-sql"></a><span data-ttu-id="4a479-102">Сравнение Microsoft Access SQL и ANSI SQL</span><span class="sxs-lookup"><span data-stu-id="4a479-102">Comparison of Microsoft Access SQL and ANSI SQL</span></span>

<span data-ttu-id="4a479-103">**Область применения**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="4a479-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="4a479-104">Движок базы данных Microsoft Access SQL, как правило, является совместимым с ANSI-89 Level 1.</span><span class="sxs-lookup"><span data-stu-id="4a479-104">Microsoft Access database engine SQL is generally ANSI-89 Level 1 compliant.</span></span> <span data-ttu-id="4a479-105">Однако некоторые функции SQL anSI не реализованы в Microsoft Access SQL.</span><span class="sxs-lookup"><span data-stu-id="4a479-105">However, certain ANSI SQL features are not implemented in Microsoft Access SQL.</span></span> <span data-ttu-id="4a479-106">И наоборот, microsoft Access SQL содержит зарезервированные слова и функции, не поддерживаемые в ansi SQL.</span><span class="sxs-lookup"><span data-stu-id="4a479-106">Conversely, Microsoft Access SQL includes reserved words and features not supported in ANSI SQL.</span></span>

## <a name="major-differences"></a><span data-ttu-id="4a479-107">Основные различия</span><span class="sxs-lookup"><span data-stu-id="4a479-107">Major differences</span></span>

- <span data-ttu-id="4a479-108">Microsoft Access SQL и ANSI SQL имеют разные зарезервированные слова и типы данных.</span><span class="sxs-lookup"><span data-stu-id="4a479-108">Microsoft Access SQL and ANSI SQL each have different reserved words and data types.</span></span> <span data-ttu-id="4a479-109">Дополнительные сведения см. в ядро СУБД SQL Microsoft [Access ядро СУБД SQL](sql-reserved-words.md) и [эквивалентных SQL anSI.](equivalent-ansi-sql-data-types.md)</span><span class="sxs-lookup"><span data-stu-id="4a479-109">For more information, see [Microsoft Access Database Engine SQL Reserved Words](sql-reserved-words.md) and [Equivalent ANSI SQL Data Types](equivalent-ansi-sql-data-types.md).</span></span> <span data-ttu-id="4a479-110">С помощью поставщика ядро СУБД OLE DB есть дополнительные зарезервированные слова.</span><span class="sxs-lookup"><span data-stu-id="4a479-110">Using the Microsoft Access Database Engine OLE DB Provider there are additional reserved words.</span></span>

- <span data-ttu-id="4a479-111">**[Между... И](https://docs.microsoft.com/office/vba/access/concepts/miscellaneous/between-and-operator)**</span><span class="sxs-lookup"><span data-stu-id="4a479-111">**[Between…And](https://docs.microsoft.com/office/vba/access/concepts/miscellaneous/between-and-operator)**</span></span>
    
  <span data-ttu-id="4a479-112">*expr1* \[ NOT \] **Between** *value1* **And** *value2*</span><span class="sxs-lookup"><span data-stu-id="4a479-112">*expr1* \[NOT\] **Between** *value1* **And** *value2*</span></span>
    
  <span data-ttu-id="4a479-113">В microsoft Access SQL *значение1* может быть больше *значения 2;* в SQL *anSI значение1 должно* быть равно или меньше *значения2.*</span><span class="sxs-lookup"><span data-stu-id="4a479-113">In Microsoft Access SQL, *value1* can be greater than *value2*; in ANSI SQL, *value1* must be equal to or less than *value2.*</span></span>

- <span data-ttu-id="4a479-114">Microsoft Access SQL поддерживает как символы SQL ansi, [](using-wildcard-characters-in-string-comparisons.md) так и символы подмайки, которые являются специфическими для двигателя базы данных Microsoft Access для использования с оператором **[Like.](https://docs.microsoft.com/office/vba/access/Concepts/Structured-Query-Language/like-operator-microsoft-access-sql)**</span><span class="sxs-lookup"><span data-stu-id="4a479-114">Microsoft Access SQL supports both ANSI SQL wildcard characters and [wildcard characters](using-wildcard-characters-in-string-comparisons.md) that are specific to the Microsoft Access database engine to use with the **[Like](https://docs.microsoft.com/office/vba/access/Concepts/Structured-Query-Language/like-operator-microsoft-access-sql)** operator.</span></span> <span data-ttu-id="4a479-115">Использование символов подкардных знаков базы данных anSI и Microsoft Access является взаимоисключающими.</span><span class="sxs-lookup"><span data-stu-id="4a479-115">The use of the ANSI and Microsoft Access database engine wildcard characters is mutually exclusive.</span></span> <span data-ttu-id="4a479-116">Необходимо использовать один набор или другой набор и не смешивать их.</span><span class="sxs-lookup"><span data-stu-id="4a479-116">You must use one set or the other and cannot mix them.</span></span> <span data-ttu-id="4a479-117">Подкарды SQL anSI доступны только при использовании двигателя базы данных Microsoft Access и поставщика ядро СУБД OLE DB.</span><span class="sxs-lookup"><span data-stu-id="4a479-117">The ANSI SQL wildcards are only available when using the Microsoft Access database engine and the Microsoft Access Database Engine OLE DB Provider.</span></span> <span data-ttu-id="4a479-118">Если вы попробуете использовать SQL anSI через Microsoft Access или DAO, они будут интерпретируются как буквальные.</span><span class="sxs-lookup"><span data-stu-id="4a479-118">If you try to use the ANSI SQL wildcards through Microsoft Access or DAO, then they will be interpreted as literals.</span></span> <span data-ttu-id="4a479-119">При использовании поставщика OLE DB ядро СУБД Microsoft Access ядро СУБД обратное.</span><span class="sxs-lookup"><span data-stu-id="4a479-119">The opposite is true when using the Microsoft Access Database Engine OLE DB Provider.</span></span>
    
    <table>
    <colgroup>
    <col style="width: 33%" />
    <col style="width: 33%" />
    <col style="width: 33%" />
    </colgroup>
    <thead>
    <tr class="header">
    <th><p><span data-ttu-id="4a479-120">Соответствие символу</span><span class="sxs-lookup"><span data-stu-id="4a479-120">Matching character</span></span></p></th>
    <th><p><span data-ttu-id="4a479-121">Microsoft Access SQL</span><span class="sxs-lookup"><span data-stu-id="4a479-121">Microsoft Access SQL</span></span></p></th>
    <th><p><span data-ttu-id="4a479-122">ANSI SQL</span><span class="sxs-lookup"><span data-stu-id="4a479-122">ANSI SQL</span></span></p></th>
    </tr>
    </thead>
    <tbody>
    <tr class="odd">
    <td><p><span data-ttu-id="4a479-123">Любой знак</span><span class="sxs-lookup"><span data-stu-id="4a479-123">Any single character</span></span></p></td>
    <td><p><span data-ttu-id="4a479-124">?</span><span class="sxs-lookup"><span data-stu-id="4a479-124">?</span></span></p></td>
    <td><p><span data-ttu-id="4a479-125">_ (знак подчеркивания)</span><span class="sxs-lookup"><span data-stu-id="4a479-125">_ (underscore)</span></span></p></td>
    </tr>
    <tr class="even">
    <td><p><span data-ttu-id="4a479-126">Ноль или более символов</span><span class="sxs-lookup"><span data-stu-id="4a479-126">Zero or more characters</span></span></p></td>
    <td><p>*</p></td>
    <td><p>%</p></td>
    </tr>
    </tbody>
    </table>


- <span data-ttu-id="4a479-127">Microsoft Access SQL, как правило, менее строгим.</span><span class="sxs-lookup"><span data-stu-id="4a479-127">Microsoft Access SQL is generally less restrictive.</span></span> <span data-ttu-id="4a479-128">Например, позволяет группить и заказывать выражения.</span><span class="sxs-lookup"><span data-stu-id="4a479-128">For example, it permits grouping and ordering on expressions.</span></span>

- <span data-ttu-id="4a479-129">Microsoft Access SQL поддерживает более мощные выражения.</span><span class="sxs-lookup"><span data-stu-id="4a479-129">Microsoft Access SQL supports more powerful expressions.</span></span>

## <a name="enhanced-features-of-microsoft-access-sql"></a><span data-ttu-id="4a479-130">Расширенные возможности microsoft Access SQL</span><span class="sxs-lookup"><span data-stu-id="4a479-130">Enhanced features of Microsoft Access SQL</span></span>

<span data-ttu-id="4a479-131">Microsoft Access SQL предоставляет следующие расширенные функции:</span><span class="sxs-lookup"><span data-stu-id="4a479-131">Microsoft Access SQL provides the following enhanced features:</span></span>

- <span data-ttu-id="4a479-132">Заявление [TRANSFORM,](transform-statement-microsoft-access-sql.md) которое обеспечивает поддержку запросов на перекрестие.</span><span class="sxs-lookup"><span data-stu-id="4a479-132">The [TRANSFORM](transform-statement-microsoft-access-sql.md) statement, which provides support for crosstab queries.</span></span>

- <span data-ttu-id="4a479-133">Дополнительные [агрегированные](sql-aggregate-functions-sql.md)функции, такие как **StDev** и **VarP.**</span><span class="sxs-lookup"><span data-stu-id="4a479-133">Additional [aggregate functions](sql-aggregate-functions-sql.md), such as **StDev** and **VarP**.</span></span>

- <span data-ttu-id="4a479-134">Объявление [PARAMETERS](parameters-declaration-microsoft-access-sql.md) для определения запросов параметров.</span><span class="sxs-lookup"><span data-stu-id="4a479-134">The [PARAMETERS](parameters-declaration-microsoft-access-sql.md) declaration for defining parameter queries.</span></span>

## <a name="ansi-sql-features-not-supported-in-microsoft-access-sql"></a><span data-ttu-id="4a479-135">Функции SQL anSI, не поддерживаемые в Microsoft Access SQL</span><span class="sxs-lookup"><span data-stu-id="4a479-135">ANSI SQL features not supported in Microsoft Access SQL</span></span>

<span data-ttu-id="4a479-136">Microsoft Access SQL не поддерживает следующие функции SQL ANSI:</span><span class="sxs-lookup"><span data-stu-id="4a479-136">Microsoft Access SQL does not support the following ANSI SQL features:</span></span>

- <span data-ttu-id="4a479-137">Ссылки на отдельные совокупные функции.</span><span class="sxs-lookup"><span data-stu-id="4a479-137">DISTINCT aggregate function references.</span></span> <span data-ttu-id="4a479-138">Например, microsoft Access SQL не позволяет sum (DISTINCT *columnname).*</span><span class="sxs-lookup"><span data-stu-id="4a479-138">For example, Microsoft Access SQL does not allow SUM(DISTINCT *columnname*).</span></span>

- <span data-ttu-id="4a479-139">Пункт LIMIT TO *nn* ROWS, используемый для ограничения количества строк, возвращаемого запросом.</span><span class="sxs-lookup"><span data-stu-id="4a479-139">The LIMIT TO *nn* ROWS clause used to limit the number of rows returned by a query.</span></span> <span data-ttu-id="4a479-140">Чтобы ограничить область запроса, можно использовать только пункт [WHERE.](https://docs.microsoft.com/office/vba/access/Concepts/Structured-Query-Language/where-clause-microsoft-access-sql)</span><span class="sxs-lookup"><span data-stu-id="4a479-140">You can use only the [WHERE clause](https://docs.microsoft.com/office/vba/access/Concepts/Structured-Query-Language/where-clause-microsoft-access-sql) to limit the scope of a query.</span></span>

