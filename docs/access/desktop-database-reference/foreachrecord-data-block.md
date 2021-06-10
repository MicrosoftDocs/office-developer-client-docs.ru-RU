---
title: Блок данных ForEachRecord
TOCTitle: ForEachRecord data block
ms:assetid: be369196-230e-1f92-e36b-667048eef2be
ms:mtpsurl: https://msdn.microsoft.com/library/Ff822743(v=office.15)
ms:contentKeyID: 48547455
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: 84ab685b946e390645027790e5b1402561527ab6
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32292330"
---
# <a name="foreachrecord-data-block"></a><span data-ttu-id="46bf5-102">Блок данных ForEachRecord</span><span class="sxs-lookup"><span data-stu-id="46bf5-102">ForEachRecord data block</span></span>

<span data-ttu-id="46bf5-103">**Область применения**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="46bf5-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="46bf5-104">Блок **данных ForEachRecord** повторяет набор заявлений для каждой записи в домене.</span><span class="sxs-lookup"><span data-stu-id="46bf5-104">A **ForEachRecord** data block repeats a set of statements for each record in a domain.</span></span>

> [!NOTE]
> <span data-ttu-id="46bf5-105">Блок **данных ForEachRecord** доступен только в макросах данных.</span><span class="sxs-lookup"><span data-stu-id="46bf5-105">The **ForEachRecord** data block is available only in Data Macros.</span></span>

## <a name="setting"></a><span data-ttu-id="46bf5-106">Параметр</span><span class="sxs-lookup"><span data-stu-id="46bf5-106">Setting</span></span>

<span data-ttu-id="46bf5-107">Действие **ForEachRecord имеет** следующие аргументы.</span><span class="sxs-lookup"><span data-stu-id="46bf5-107">The **ForEachRecord** action has the following arguments.</span></span>

<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="46bf5-108">Аргумент</span><span class="sxs-lookup"><span data-stu-id="46bf5-108">Argument</span></span></p></th>
<th><p><span data-ttu-id="46bf5-109">Обязательный</span><span class="sxs-lookup"><span data-stu-id="46bf5-109">Required</span></span></p></th>
<th><p><span data-ttu-id="46bf5-110">Описание</span><span class="sxs-lookup"><span data-stu-id="46bf5-110">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="46bf5-111"><strong>В</strong></span><span class="sxs-lookup"><span data-stu-id="46bf5-111"><strong>In</strong></span></span></p></td>
<td><p><span data-ttu-id="46bf5-112">Да</span><span class="sxs-lookup"><span data-stu-id="46bf5-112">Yes</span></span></p></td>
<td><p><span data-ttu-id="46bf5-113">Строка, определяемая доменом записей для работы.</span><span class="sxs-lookup"><span data-stu-id="46bf5-113">A string that identifies the domain of records to operate on.</span></span> <span data-ttu-id="46bf5-114">Аргумент <em>In</em> может содержать имя таблицы, выбранный запрос или SQL.</span><span class="sxs-lookup"><span data-stu-id="46bf5-114">The <em>In</em> argument can contain the name of the table, a select query, or a SQL statement.</span></span></p><p><span data-ttu-id="46bf5-115"><strong>ПРИМЕЧАНИЕ.</strong>Указанный домен не может включать данные, хранимые в связанной таблице или источнике данных ODBC.</span><span class="sxs-lookup"><span data-stu-id="46bf5-115"><strong>NOTE</strong>: The specified domain cannot include data stored in a linked table or ODBC data source.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="46bf5-116"><strong>Где состояние</strong></span><span class="sxs-lookup"><span data-stu-id="46bf5-116"><strong>Where Condition</strong></span></span></p></td>
<td><p><span data-ttu-id="46bf5-117">Нет</span><span class="sxs-lookup"><span data-stu-id="46bf5-117">No</span></span></p></td>
<td><p><span data-ttu-id="46bf5-118">Строковая экспрессия, используемая для ограничения диапазона данных, на которых выполняется блок данных <strong>ForEachRecord.</strong></span><span class="sxs-lookup"><span data-stu-id="46bf5-118">A string expression used to restrict the range of data on which the <strong>ForEachRecord</strong> data block is performed.</span></span> <span data-ttu-id="46bf5-119">Например, критерии часто эквивалентны пункту WHERE в SQL, без слова WHERE.</span><span class="sxs-lookup"><span data-stu-id="46bf5-119">For example, criteria is often equivalent to the WHERE clause in an SQL expression, without the word WHERE.</span></span> <span data-ttu-id="46bf5-120">Если критерии не указаны, блок <strong>данных ForEachRecord</strong> работает на всем домене, указанном аргументом <em>In.</em></span><span class="sxs-lookup"><span data-stu-id="46bf5-120">If criteria is omitted, the <strong>ForEachRecord</strong> data block operates on the entire domain specified by the <em>In</em> argument.</span></span> <span data-ttu-id="46bf5-121">Любое поле, включенное в критерии, также должно быть полем <em>в In</em>.</span><span class="sxs-lookup"><span data-stu-id="46bf5-121">Any field that is included in criteria must also be a field in <em>In</em>.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="46bf5-122"><strong>Alias</strong></span><span class="sxs-lookup"><span data-stu-id="46bf5-122"><strong>Alias</strong></span></span></p></td>
<td><p><span data-ttu-id="46bf5-123">Нет</span><span class="sxs-lookup"><span data-stu-id="46bf5-123">No</span></span></p></td>
<td><p><span data-ttu-id="46bf5-124">Строка, которая предоставляет альтернативное имя для домена, указанного аргументом <em>In.</em></span><span class="sxs-lookup"><span data-stu-id="46bf5-124">A string that provides an alternative name for the domain specified by the <em>In</em> argument.</span></span> <span data-ttu-id="46bf5-125">Часто используется для сокращения имени таблицы для последующих ссылок, чтобы предотвратить возможные неоднозначные ссылки. Если <em>псевдоним не</em> указан, в качестве псевдонима будет использоваться таблица или имя запроса.</span><span class="sxs-lookup"><span data-stu-id="46bf5-125">Often used to shorten the table name for subsequent references to prevent possible ambiguous references.If <em>Alias</em> is not specified, the table or query name will be used as the alias.</span></span></p></td>
</tr>
</tbody>
</table>


## <a name="remarks"></a><span data-ttu-id="46bf5-126">Примечания</span><span class="sxs-lookup"><span data-stu-id="46bf5-126">Remarks</span></span>

<span data-ttu-id="46bf5-127">Чтобы немедленно выйти из блока данных **ForEachRecord, используйте действие ExitForEachRecord.** **[](exitforeachrecord-macro-action.md)**</span><span class="sxs-lookup"><span data-stu-id="46bf5-127">Use the **[ExitForEachRecord](exitforeachrecord-macro-action.md)** action to exit a **ForEachRecord** data block immediately.</span></span>

