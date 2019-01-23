---
title: Перечисление RecordsetOptionEnum (DAO)
TOCTitle: RecordsetOptionEnum Enumeration
ms:assetid: 3a9d8664-dcb6-cb60-7cf6-e229eb699ef1
ms:mtpsurl: https://msdn.microsoft.com/library/Ff192649(v=office.15)
ms:contentKeyID: 48544266
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Priority
ms.openlocfilehash: b9e2a69f6952feb892de736e7ff3c3ca94e9da64
ms.sourcegitcommit: d6695c94415fa47952ee7961a69660abc0904434
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/17/2019
ms.locfileid: "28717281"
---
# <a name="recordsetoptionenum-enumeration-dao"></a><span data-ttu-id="6e9dc-102">Перечисление RecordsetOptionEnum (DAO)</span><span class="sxs-lookup"><span data-stu-id="6e9dc-102">RecordsetOptionEnum Enumeration (DAO)</span></span>


<span data-ttu-id="6e9dc-103">**Область применения**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="6e9dc-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="6e9dc-104">Используется с методом **OpenRecordset** для указания характеристик нового объекта **Recordset**.</span><span class="sxs-lookup"><span data-stu-id="6e9dc-104">Used with the **OpenRecordset** method to specify characteristics of a new **Recordset** object.</span></span>

<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="6e9dc-105">Имя</span><span class="sxs-lookup"><span data-stu-id="6e9dc-105">Name</span></span></p></th>
<th><p><span data-ttu-id="6e9dc-106">Значение</span><span class="sxs-lookup"><span data-stu-id="6e9dc-106">Value</span></span></p></th>
<th><p><span data-ttu-id="6e9dc-107">Описание</span><span class="sxs-lookup"><span data-stu-id="6e9dc-107">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="6e9dc-108">dbAppendOnly</span><span class="sxs-lookup"><span data-stu-id="6e9dc-108">dbAppendOnly</span></span></p></td>
<td><p><span data-ttu-id="6e9dc-109">8</span><span class="sxs-lookup"><span data-stu-id="6e9dc-109"> :=8</span></span></p></td>
<td><p><span data-ttu-id="6e9dc-110">Дает пользователю возможность добавлять новые записи в динамическое подмножество данных, но запрещает ему чтение существующих записей.</span><span class="sxs-lookup"><span data-stu-id="6e9dc-110">Allows user to add new records to the dynaset, but prevents user from reading existing records.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="6e9dc-111">dbConsistent</span><span class="sxs-lookup"><span data-stu-id="6e9dc-111">dbConsistent</span></span></p></td>
<td><p><span data-ttu-id="6e9dc-112">32</span><span class="sxs-lookup"><span data-stu-id="6e9dc-112">3.2</span></span></p></td>
<td><p><span data-ttu-id="6e9dc-113">Применяет обновления только к тем полям, которые не окажут влияния на другие записи в динамическом подмножестве данных (только для типов "динамическое подмножество данных" и "моментальный снимок").</span><span class="sxs-lookup"><span data-stu-id="6e9dc-113">Applies updates only to those fields that will not affect other records in the dynaset (dynaset- and snapshot-type only).</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="6e9dc-114">dbDenyRead</span><span class="sxs-lookup"><span data-stu-id="6e9dc-114">dbDenyRead</span></span></p></td>
<td><p><span data-ttu-id="6e9dc-115">2</span><span class="sxs-lookup"><span data-stu-id="6e9dc-115">-2</span></span></p></td>
<td><p><span data-ttu-id="6e9dc-116">Запрещает другим пользователям чтение записей объекта Recordset (только для табличного типа).</span><span class="sxs-lookup"><span data-stu-id="6e9dc-116">Prevents other users from reading Recordset records (table-type only).</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="6e9dc-117">dbDenyWrite</span><span class="sxs-lookup"><span data-stu-id="6e9dc-117">dbDenyWrite</span></span></p></td>
<td><p><span data-ttu-id="6e9dc-118">1</span><span class="sxs-lookup"><span data-stu-id="6e9dc-118">-1</span></span></p></td>
<td><p><span data-ttu-id="6e9dc-119">Запрещает другим пользователям изменять записи объекта Recordset.</span><span class="sxs-lookup"><span data-stu-id="6e9dc-119">Prevents other users from changing Recordset records.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="6e9dc-120">dbExecDirect</span><span class="sxs-lookup"><span data-stu-id="6e9dc-120">dbExecDirect</span></span></p></td>
<td><p><span data-ttu-id="6e9dc-121">2048</span><span class="sxs-lookup"><span data-stu-id="6e9dc-121">2048 characters</span></span></p></td>
<td><p><span data-ttu-id="6e9dc-122">Выполняет запрос, не вызывая перед этим функцию ODBC SQLPrepare.</span><span class="sxs-lookup"><span data-stu-id="6e9dc-122">Executes the query without first calling the SQLPrepare ODBC function.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="6e9dc-123">dbFailOnError</span><span class="sxs-lookup"><span data-stu-id="6e9dc-123">dbFailOnError</span></span></p></td>
<td><p><span data-ttu-id="6e9dc-124">128</span><span class="sxs-lookup"><span data-stu-id="6e9dc-124">128</span></span></p></td>
<td><p><span data-ttu-id="6e9dc-125">Откатывает обновления при возникновении ошибки.</span><span class="sxs-lookup"><span data-stu-id="6e9dc-125">Rolls back updates if an error occurs.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="6e9dc-126">dbForwardOnly</span><span class="sxs-lookup"><span data-stu-id="6e9dc-126">dbForwardOnly</span></span></p></td>
<td><p><span data-ttu-id="6e9dc-127">256</span><span class="sxs-lookup"><span data-stu-id="6e9dc-127">256</span></span></p></td>
<td><p><span data-ttu-id="6e9dc-128">Создает объект Recordset типа "моментальный снимок" с прокруткой только вперед (только для типа "моментальный снимок").</span><span class="sxs-lookup"><span data-stu-id="6e9dc-128">Creates a forward-only scrolling snapshot-type Recordset (snapshot-type only).</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="6e9dc-129">dbInconsistent</span><span class="sxs-lookup"><span data-stu-id="6e9dc-129">dbInconsistent</span></span></p></td>
<td><p><span data-ttu-id="6e9dc-130">16</span><span class="sxs-lookup"><span data-stu-id="6e9dc-130">1.6</span></span></p></td>
<td><p><span data-ttu-id="6e9dc-131">Применяет обновления ко всем полям динамического подмножества данных, даже если это повлияет на другие записи (только для типов "динамическое подмножество данных" и "моментальный снимок").</span><span class="sxs-lookup"><span data-stu-id="6e9dc-131">Applies updates to all dynaset fields, even if other records are affected (dynaset- and snapshot-type only).</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="6e9dc-132">dbReadOnly</span><span class="sxs-lookup"><span data-stu-id="6e9dc-132">dbReadOnly</span></span></p></td>
<td><p><span data-ttu-id="6e9dc-133">4</span><span class="sxs-lookup"><span data-stu-id="6e9dc-133">4</span></span></p></td>
<td><p><span data-ttu-id="6e9dc-134">Открывает объект Recordset только для чтения.</span><span class="sxs-lookup"><span data-stu-id="6e9dc-134">Opens the Recordset as read-only.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="6e9dc-135">dbRunAsync</span><span class="sxs-lookup"><span data-stu-id="6e9dc-135">dbRunAsync</span></span></p></td>
<td><p><span data-ttu-id="6e9dc-136">1024</span><span class="sxs-lookup"><span data-stu-id="6e9dc-136">1024 px</span></span></p></td>
<td><p><span data-ttu-id="6e9dc-137">Выполняет запрос асинхронно.</span><span class="sxs-lookup"><span data-stu-id="6e9dc-137">Executes the SQL query.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="6e9dc-138">dbSeeChanges</span><span class="sxs-lookup"><span data-stu-id="6e9dc-138">dbSeeChanges</span></span></p></td>
<td><p><span data-ttu-id="6e9dc-139">512</span><span class="sxs-lookup"><span data-stu-id="6e9dc-139">5.12</span></span></p></td>
<td><p><span data-ttu-id="6e9dc-140">Создает ошибку во время выполнения, если другой пользователь пытается изменить данные, которые вы редактируете (только для типа "динамическое подмножество данных").</span><span class="sxs-lookup"><span data-stu-id="6e9dc-140">Generates a run-time error if another user is changing data you are editing (dynaset-type only).</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="6e9dc-141">dbSQLPassThrough</span><span class="sxs-lookup"><span data-stu-id="6e9dc-141">dbSQLPassThrough</span></span></p></td>
<td><p><span data-ttu-id="6e9dc-142">64</span><span class="sxs-lookup"><span data-stu-id="6e9dc-142">6.4</span></span></p></td>
<td><p><span data-ttu-id="6e9dc-143">Отправляет инструкцию SQL в базу данных ODBC (только для типа "моментальный снимок").</span><span class="sxs-lookup"><span data-stu-id="6e9dc-143">Sends an SQL statement to an ODBC database (snapshot-type only).</span></span></p></td>
</tr>
</tbody>
</table>

