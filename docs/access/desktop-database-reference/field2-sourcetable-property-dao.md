---
title: Свойство Field2.SourceTable (DAO)
TOCTitle: SourceTable Property
ms:assetid: 24d2fdda-d924-d95e-8458-063dd1d36d5d
ms:mtpsurl: https://msdn.microsoft.com/library/Ff191839(v=office.15)
ms:contentKeyID: 48543768
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: a3ecf8b6655bb9f1dd2b25d264708112834e8a90
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32292673"
---
# <a name="field2sourcetable-property-dao"></a><span data-ttu-id="993ff-102">Свойство Field2.SourceTable (DAO)</span><span class="sxs-lookup"><span data-stu-id="993ff-102">Field2.SourceTable property (DAO)</span></span>


<span data-ttu-id="993ff-103">**Область применения**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="993ff-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="993ff-104">Возвращает значение, которое указывает имя таблицы, которая является исходным источником данных для **объекта Field2.**</span><span class="sxs-lookup"><span data-stu-id="993ff-104">Returns a value that indicates the name of the table that is the original source of the data for a **Field2** object.</span></span> <span data-ttu-id="993ff-105">Только для чтения, **String**.</span><span class="sxs-lookup"><span data-stu-id="993ff-105">Read-only **String**.</span></span>

## <a name="syntax"></a><span data-ttu-id="993ff-106">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="993ff-106">Syntax</span></span>

<span data-ttu-id="993ff-107">*выражения* . SourceTable</span><span class="sxs-lookup"><span data-stu-id="993ff-107">*expression* .SourceTable</span></span>

<span data-ttu-id="993ff-108">*expression* — переменная, представляющая объект **Field2**.</span><span class="sxs-lookup"><span data-stu-id="993ff-108">*expression* A variable that represents a **Field2** object.</span></span>

## <a name="remarks"></a><span data-ttu-id="993ff-109">Примечания</span><span class="sxs-lookup"><span data-stu-id="993ff-109">Remarks</span></span>

<span data-ttu-id="993ff-110">Для объекта **Field2** использование свойств **SourceField** и  **SourceTable** зависит от объекта, который содержит коллекцию Полей, к которую примыкает объект **Field2,** как показано в следующей таблице.</span><span class="sxs-lookup"><span data-stu-id="993ff-110">For a **Field2** object, use of the **SourceField** and **SourceTable** properties depends on the object that contains the **Fields** collection that the **Field2** object is appended to, as shown in the following table.</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="993ff-111">Объект, приданный</span><span class="sxs-lookup"><span data-stu-id="993ff-111">Object appended to</span></span></p></th>
<th><p><span data-ttu-id="993ff-112">Usage</span><span class="sxs-lookup"><span data-stu-id="993ff-112">Usage</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="993ff-113"><strong>Index</strong></span><span class="sxs-lookup"><span data-stu-id="993ff-113"><strong>Index</strong></span></span></p></td>
<td><p><span data-ttu-id="993ff-114">Не поддерживается</span><span class="sxs-lookup"><span data-stu-id="993ff-114">Not supported</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="993ff-115"><strong>QueryDef</strong></span><span class="sxs-lookup"><span data-stu-id="993ff-115"><strong>QueryDef</strong></span></span></p></td>
<td><p><span data-ttu-id="993ff-116">Только для чтения</span><span class="sxs-lookup"><span data-stu-id="993ff-116">Read-only</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="993ff-117"><strong>Recordset</strong></span><span class="sxs-lookup"><span data-stu-id="993ff-117"><strong>Recordset</strong></span></span></p></td>
<td><p><span data-ttu-id="993ff-118">Только для чтения</span><span class="sxs-lookup"><span data-stu-id="993ff-118">Read-only</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="993ff-119"><strong>Relation</strong></span><span class="sxs-lookup"><span data-stu-id="993ff-119"><strong>Relation</strong></span></span></p></td>
<td><p><span data-ttu-id="993ff-120">Не поддерживается</span><span class="sxs-lookup"><span data-stu-id="993ff-120">Not supported</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="993ff-121"><strong>TableDef</strong></span><span class="sxs-lookup"><span data-stu-id="993ff-121"><strong>TableDef</strong></span></span></p></td>
<td><p><span data-ttu-id="993ff-122">Только для чтения</span><span class="sxs-lookup"><span data-stu-id="993ff-122">Read-only</span></span></p></td>
</tr>
</tbody>
</table>


<span data-ttu-id="993ff-123">Эти свойства указывают исходные имена полей и таблиц, связанных с **объектом Field2.**</span><span class="sxs-lookup"><span data-stu-id="993ff-123">These properties indicate the original field and table names associated with a **Field2** object.</span></span> <span data-ttu-id="993ff-124">Например, эти свойства можно использовать для определения исходного источника данных в поле запросов, имя которого не связано с именем поля в исходной таблице.</span><span class="sxs-lookup"><span data-stu-id="993ff-124">For example, you could use these properties to determine the original source of the data in a query field whose name is unrelated to the name of the field in the underlying table.</span></span>


> [!NOTE]
> <span data-ttu-id="993ff-125">Свойство **SourceTable** не возвращает содержательное имя таблицы, если используется на **объекте Field2** в коллекции **Fields** объекта **Recordset типа** таблицы.</span><span class="sxs-lookup"><span data-stu-id="993ff-125">The **SourceTable** property will not return a meaningful table name if used on a **Field2** object in the **Fields** collection of a table-type **Recordset** object.</span></span>


