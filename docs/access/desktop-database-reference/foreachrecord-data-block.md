---
title: Блок данных ДляКаждойЗаписи
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
# <a name="foreachrecord-data-block"></a><span data-ttu-id="f9474-102">Блок данных ДляКаждойЗаписи</span><span class="sxs-lookup"><span data-stu-id="f9474-102">ForEachRecord data block</span></span>

<span data-ttu-id="f9474-103">**Область применения**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="f9474-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="f9474-104">Блок данных **ДляКаждойЗаписи** повторяет набор операторов для каждой записи в домене.</span><span class="sxs-lookup"><span data-stu-id="f9474-104">A **ForEachRecord** data block repeats a set of statements for each record in a domain.</span></span>

> [!NOTE]
> <span data-ttu-id="f9474-105">Блок данных **ДляКаждойЗаписи** доступен только в макросах данных.</span><span class="sxs-lookup"><span data-stu-id="f9474-105">The **ForEachRecord** data block is available only in Data Macros.</span></span>

## <a name="setting"></a><span data-ttu-id="f9474-106">Параметр</span><span class="sxs-lookup"><span data-stu-id="f9474-106">Setting</span></span>

<span data-ttu-id="f9474-107">Макрокоманда **ДляКаждойЗаписи** имеет следующие аргументы.</span><span class="sxs-lookup"><span data-stu-id="f9474-107">The **ForEachRecord** action has the following arguments.</span></span>

<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="f9474-108">Аргумент</span><span class="sxs-lookup"><span data-stu-id="f9474-108">Argument</span></span></p></th>
<th><p><span data-ttu-id="f9474-109">Обязательный</span><span class="sxs-lookup"><span data-stu-id="f9474-109">Required</span></span></p></th>
<th><p><span data-ttu-id="f9474-110">Описание</span><span class="sxs-lookup"><span data-stu-id="f9474-110">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="f9474-111"><strong>Возврата</strong></span><span class="sxs-lookup"><span data-stu-id="f9474-111"><strong>In</strong></span></span></p></td>
<td><p><span data-ttu-id="f9474-112">Да</span><span class="sxs-lookup"><span data-stu-id="f9474-112">Yes</span></span></p></td>
<td><p><span data-ttu-id="f9474-113">Строка, определяющая домен записей, с которыми выполняется работа.</span><span class="sxs-lookup"><span data-stu-id="f9474-113">A string that identifies the domain of records to operate on.</span></span> <span data-ttu-id="f9474-114">Аргумент <em>in</em> может содержать имя таблицы, запрос на выборку или инструкцию SQL.</span><span class="sxs-lookup"><span data-stu-id="f9474-114">The <em>In</em> argument can contain the name of the table, a select query, or a SQL statement.</span></span></p><p><span data-ttu-id="f9474-115"><strong>Note</strong>: указанный домен не может содержать данные, хранящиеся в связанной таблице или источнике данных ODBC.</span><span class="sxs-lookup"><span data-stu-id="f9474-115"><strong>NOTE</strong>: The specified domain cannot include data stored in a linked table or ODBC data source.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="f9474-116"><strong>Условие отбора</strong></span><span class="sxs-lookup"><span data-stu-id="f9474-116"><strong>Where Condition</strong></span></span></p></td>
<td><p><span data-ttu-id="f9474-117">Нет</span><span class="sxs-lookup"><span data-stu-id="f9474-117">No</span></span></p></td>
<td><p><span data-ttu-id="f9474-118">Строковое выражение, используемое для ограничения диапазона данных, в котором выполняется блок данных блока <strong>ДляКаждойЗаписи</strong> .</span><span class="sxs-lookup"><span data-stu-id="f9474-118">A string expression used to restrict the range of data on which the <strong>ForEachRecord</strong> data block is performed.</span></span> <span data-ttu-id="f9474-119">Например, критерии часто эквивалентны предложению WHERE в выражении SQL без слова WHERE.</span><span class="sxs-lookup"><span data-stu-id="f9474-119">For example, criteria is often equivalent to the WHERE clause in an SQL expression, without the word WHERE.</span></span> <span data-ttu-id="f9474-120">Если критерии опущены, блок данных <strong>ДляКаждойЗаписи</strong> работает на всем домене, указанном аргументом <em>in</em> .</span><span class="sxs-lookup"><span data-stu-id="f9474-120">If criteria is omitted, the <strong>ForEachRecord</strong> data block operates on the entire domain specified by the <em>In</em> argument.</span></span> <span data-ttu-id="f9474-121">Все поля, включенные в <em>критерии, также</em>должны быть полями в.</span><span class="sxs-lookup"><span data-stu-id="f9474-121">Any field that is included in criteria must also be a field in <em>In</em>.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="f9474-122"><strong>Alias</strong></span><span class="sxs-lookup"><span data-stu-id="f9474-122"><strong>Alias</strong></span></span></p></td>
<td><p><span data-ttu-id="f9474-123">Нет</span><span class="sxs-lookup"><span data-stu-id="f9474-123">No</span></span></p></td>
<td><p><span data-ttu-id="f9474-124">Строка, предоставляющая альтернативное имя для домена, указанного аргументом <em>in</em> .</span><span class="sxs-lookup"><span data-stu-id="f9474-124">A string that provides an alternative name for the domain specified by the <em>In</em> argument.</span></span> <span data-ttu-id="f9474-125">Часто используется для сокращения имени таблицы для последующих ссылок, чтобы предотвратить возможные неоднозначные ссылки. Если параметр <em>Alias</em> не указан, имя таблицы или запроса будет использоваться в качестве псевдонима.</span><span class="sxs-lookup"><span data-stu-id="f9474-125">Often used to shorten the table name for subsequent references to prevent possible ambiguous references.If <em>Alias</em> is not specified, the table or query name will be used as the alias.</span></span></p></td>
</tr>
</tbody>
</table>


## <a name="remarks"></a><span data-ttu-id="f9474-126">Примечания</span><span class="sxs-lookup"><span data-stu-id="f9474-126">Remarks</span></span>

<span data-ttu-id="f9474-127">Используйте действие **[екситфореачрекорд](exitforeachrecord-macro-action.md)** для немедленного выхода из блока данных **ДляКаждойЗаписи** .</span><span class="sxs-lookup"><span data-stu-id="f9474-127">Use the **[ExitForEachRecord](exitforeachrecord-macro-action.md)** action to exit a **ForEachRecord** data block immediately.</span></span>

