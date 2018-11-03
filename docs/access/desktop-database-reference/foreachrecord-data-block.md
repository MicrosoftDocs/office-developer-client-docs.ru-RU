---
title: Блок данных ДляКаждойЗаписи
TOCTitle: ForEachRecord data block
ms:assetid: be369196-230e-1f92-e36b-667048eef2be
ms:mtpsurl: https://msdn.microsoft.com/library/Ff822743(v=office.15)
ms:contentKeyID: 48547455
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 09a09a80773adecf760ae4610df30bbd5f36f3d6
ms.sourcegitcommit: 38d0db57580cc5f4a0231c27b1643f8db5431ca3
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 11/02/2018
ms.locfileid: "25937528"
---
# <a name="foreachrecord-data-block"></a><span data-ttu-id="0c64d-102">Блок данных ДляКаждойЗаписи</span><span class="sxs-lookup"><span data-stu-id="0c64d-102">ForEachRecord data block</span></span>


<span data-ttu-id="0c64d-103">**Применимо к**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="0c64d-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="0c64d-104">Блок данных **ДляКаждойЗаписи** повторяет набор инструкций для каждой записи в домене.</span><span class="sxs-lookup"><span data-stu-id="0c64d-104">A **ForEachRecord** data block repeats a set of statements for each record in a domain.</span></span>

> [!NOTE]
> <span data-ttu-id="0c64d-105">Блок данных **ДляКаждойЗаписи** доступна только в макросов данных.</span><span class="sxs-lookup"><span data-stu-id="0c64d-105">The **ForEachRecord** data block is available only in Data Macros.</span></span>

## <a name="setting"></a><span data-ttu-id="0c64d-106">Параметр</span><span class="sxs-lookup"><span data-stu-id="0c64d-106">Setting</span></span>

<span data-ttu-id="0c64d-107">Действие **ДляКаждойЗаписи** имеет следующие аргументы.</span><span class="sxs-lookup"><span data-stu-id="0c64d-107">The **ForEachRecord** action has the following arguments.</span></span>

<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="0c64d-108">Argument</span><span class="sxs-lookup"><span data-stu-id="0c64d-108">Argument</span></span></p></th>
<th><p><span data-ttu-id="0c64d-109">Обязательный</span><span class="sxs-lookup"><span data-stu-id="0c64d-109">Required</span></span></p></th>
<th><p><span data-ttu-id="0c64d-110">Описание</span><span class="sxs-lookup"><span data-stu-id="0c64d-110">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="0c64d-111"><strong>В</strong></span><span class="sxs-lookup"><span data-stu-id="0c64d-111"><strong>In</strong></span></span></p></td>
<td><p><span data-ttu-id="0c64d-112">Да</span><span class="sxs-lookup"><span data-stu-id="0c64d-112">Yes</span></span></p></td>
<td><p><span data-ttu-id="0c64d-113">Строка, идентифицирующая домена записей для работы с.</span><span class="sxs-lookup"><span data-stu-id="0c64d-113">A string that identifies the domain of records to operate on.</span></span> <span data-ttu-id="0c64d-114">Аргумент <em>в</em> может содержать имя таблицы, запроса или инструкции SQL.</span><span class="sxs-lookup"><span data-stu-id="0c64d-114">The <em>In</em> argument can contain the name of the table, a select query, or a SQL statement.</span></span></p>

> [!NOTE]
> <span data-ttu-id="0c64d-115">Указанный домен не может включать данные, хранящиеся в связанной таблице или источник данных ODBC.</span><span class="sxs-lookup"><span data-stu-id="0c64d-115">The specified domain cannot include data stored in a linked table or ODBC data source.</span></span>


<p></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="0c64d-116"><strong>Условие отбора</strong></span><span class="sxs-lookup"><span data-stu-id="0c64d-116"><strong>Where Condition</strong></span></span></p></td>
<td><p><span data-ttu-id="0c64d-117">Нет</span><span class="sxs-lookup"><span data-stu-id="0c64d-117">No</span></span></p></td>
<td><p><span data-ttu-id="0c64d-118">Строковое выражение, используемое для ограничения диапазона данных, на котором блок данных <strong>ДляКаждойЗаписи</strong> выполняется.</span><span class="sxs-lookup"><span data-stu-id="0c64d-118">A string expression used to restrict the range of data on which the <strong>ForEachRecord</strong> data block is performed.</span></span> <span data-ttu-id="0c64d-119">К примеру, критерии эквивалентен часто предложение WHERE в выражении SQL без слова ГДЕ.</span><span class="sxs-lookup"><span data-stu-id="0c64d-119">For example, criteria is often equivalent to the WHERE clause in an SQL expression, without the word WHERE.</span></span> <span data-ttu-id="0c64d-120">Если критерии опущен, блок данных <strong>ДляКаждойЗаписи</strong> действует на весь домен, указанный в аргументе <em>в</em> .</span><span class="sxs-lookup"><span data-stu-id="0c64d-120">If criteria is omitted, the <strong>ForEachRecord</strong> data block operates on the entire domain specified by the <em>In</em> argument.</span></span> <span data-ttu-id="0c64d-121">Поля, который включен в условия также должны входить в <em>в</em>поле.</span><span class="sxs-lookup"><span data-stu-id="0c64d-121">Any field that is included in criteria must also be a field in <em>In</em>.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="0c64d-122"><strong>псевдоним;</strong></span><span class="sxs-lookup"><span data-stu-id="0c64d-122"><strong>Alias</strong></span></span></p></td>
<td><p><span data-ttu-id="0c64d-123">Нет</span><span class="sxs-lookup"><span data-stu-id="0c64d-123">No</span></span></p></td>
<td><p><span data-ttu-id="0c64d-124">Строка, которая предоставляет альтернативное имя для домена, указанный в аргументе <em>в</em> .</span><span class="sxs-lookup"><span data-stu-id="0c64d-124">A string that provides an alternative name for the domain specified by the <em>In</em> argument.</span></span> <span data-ttu-id="0c64d-125">Позволяет сократить имя таблицы для последующих ссылок избежать возможных неоднозначных ссылок. Если <em>псевдоним</em> не указан, будут использовать имя таблицы или запроса в качестве псевдоним.</span><span class="sxs-lookup"><span data-stu-id="0c64d-125">Often used to shorten the table name for subsequent references to prevent possible ambiguous references.If <em>Alias</em> is not specified, the table or query name will be used as the alias.</span></span></p></td>
</tr>
</tbody>
</table>


## <a name="remarks"></a><span data-ttu-id="0c64d-126">Примечания</span><span class="sxs-lookup"><span data-stu-id="0c64d-126">Remarks</span></span>

<span data-ttu-id="0c64d-127">Действие **[ExitForEachRecord](exitforeachrecord-macro-action.md)** используется для выхода из блока **ДляКаждойЗаписи** данных немедленно.</span><span class="sxs-lookup"><span data-stu-id="0c64d-127">Use the **[ExitForEachRecord](exitforeachrecord-macro-action.md)** action to exit a **ForEachRecord** data block immediately.</span></span>

