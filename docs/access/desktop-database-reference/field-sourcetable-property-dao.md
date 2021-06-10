---
title: Свойство Field.SourceTable (DAO)
TOCTitle: SourceTable Property
ms:assetid: 9564ea1c-eafd-0b72-fd68-d88fcc3ea189
ms:mtpsurl: https://msdn.microsoft.com/library/Ff197694(v=office.15)
ms:contentKeyID: 48546429
ms.date: 09/18/2015
mtps_version: v=office.15
f1_keywords:
- dao360.chm1052900
f1_categories:
- Office.Version=v15
localization_priority: Normal
ms.openlocfilehash: a557a4941f5b4aa511489c5d057871df5fa72c08
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32292988"
---
# <a name="fieldsourcetable-property-dao"></a><span data-ttu-id="e0f5c-102">Свойство Field.SourceTable (DAO)</span><span class="sxs-lookup"><span data-stu-id="e0f5c-102">Field.SourceTable property (DAO)</span></span>


<span data-ttu-id="e0f5c-103">**Область применения**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="e0f5c-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="e0f5c-104">Возвращает значение, которое указывает имя таблицы, которая является исходным источником данных для **объекта Field.**</span><span class="sxs-lookup"><span data-stu-id="e0f5c-104">Returns a value that indicates the name of the table that is the original source of the data for a **Field** object.</span></span> <span data-ttu-id="e0f5c-105">Только для чтения, **String**.</span><span class="sxs-lookup"><span data-stu-id="e0f5c-105">Read-only **String**.</span></span>

## <a name="syntax"></a><span data-ttu-id="e0f5c-106">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="e0f5c-106">Syntax</span></span>

<span data-ttu-id="e0f5c-107">*выражения* . SourceTable</span><span class="sxs-lookup"><span data-stu-id="e0f5c-107">*expression* .SourceTable</span></span>

<span data-ttu-id="e0f5c-108">*выражение*: переменная, представляющая объект **Field**.</span><span class="sxs-lookup"><span data-stu-id="e0f5c-108">*expression* A variable that represents a **Field** object.</span></span>

## <a name="remarks"></a><span data-ttu-id="e0f5c-109">Примечания</span><span class="sxs-lookup"><span data-stu-id="e0f5c-109">Remarks</span></span>

<span data-ttu-id="e0f5c-110">Для  объекта **Field** использование свойств SourceField и **SourceTable** зависит от объекта, который содержит коллекцию Полей, к которую примыкает объект **Field,** как показано в следующей таблице. </span><span class="sxs-lookup"><span data-stu-id="e0f5c-110">For a **Field** object, use of the **SourceField** and **SourceTable** properties depends on the object that contains the **Fields** collection that the **Field** object is appended to, as shown in the following table.</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="e0f5c-111">Объект, приданный</span><span class="sxs-lookup"><span data-stu-id="e0f5c-111">Object appended to</span></span></p></th>
<th><p><span data-ttu-id="e0f5c-112">Usage</span><span class="sxs-lookup"><span data-stu-id="e0f5c-112">Usage</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="e0f5c-113"><strong>Index</strong></span><span class="sxs-lookup"><span data-stu-id="e0f5c-113"><strong>Index</strong></span></span></p></td>
<td><p><span data-ttu-id="e0f5c-114">Не поддерживается</span><span class="sxs-lookup"><span data-stu-id="e0f5c-114">Not supported</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="e0f5c-115"><strong>QueryDef</strong></span><span class="sxs-lookup"><span data-stu-id="e0f5c-115"><strong>QueryDef</strong></span></span></p></td>
<td><p><span data-ttu-id="e0f5c-116">Только для чтения</span><span class="sxs-lookup"><span data-stu-id="e0f5c-116">Read-only</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="e0f5c-117"><strong>Recordset</strong></span><span class="sxs-lookup"><span data-stu-id="e0f5c-117"><strong>Recordset</strong></span></span></p></td>
<td><p><span data-ttu-id="e0f5c-118">Только для чтения</span><span class="sxs-lookup"><span data-stu-id="e0f5c-118">Read-only</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="e0f5c-119"><strong>Relation</strong></span><span class="sxs-lookup"><span data-stu-id="e0f5c-119"><strong>Relation</strong></span></span></p></td>
<td><p><span data-ttu-id="e0f5c-120">Не поддерживается</span><span class="sxs-lookup"><span data-stu-id="e0f5c-120">Not supported</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="e0f5c-121"><strong>TableDef</strong></span><span class="sxs-lookup"><span data-stu-id="e0f5c-121"><strong>TableDef</strong></span></span></p></td>
<td><p><span data-ttu-id="e0f5c-122">Только для чтения</span><span class="sxs-lookup"><span data-stu-id="e0f5c-122">Read-only</span></span></p></td>
</tr>
</tbody>
</table>


<span data-ttu-id="e0f5c-123">Эти свойства указывают исходные имена полей и таблиц, связанных с **объектом Field.**</span><span class="sxs-lookup"><span data-stu-id="e0f5c-123">These properties indicate the original field and table names associated with a **Field** object.</span></span> <span data-ttu-id="e0f5c-124">Например, эти свойства можно использовать для определения исходного источника данных в поле запросов, имя которого не связано с именем поля в исходной таблице.</span><span class="sxs-lookup"><span data-stu-id="e0f5c-124">For example, you could use these properties to determine the original source of the data in a query field whose name is unrelated to the name of the field in the underlying table.</span></span>


> [!NOTE]
> <span data-ttu-id="e0f5c-125">Свойство **SourceTable** не возвращает содержательное имя таблицы, если используется на **объекте Field** в коллекции **Fields** объекта **Recordset типа** таблицы.</span><span class="sxs-lookup"><span data-stu-id="e0f5c-125">The **SourceTable** property will not return a meaningful table name if used on a **Field** object in the **Fields** collection of a table-type **Recordset** object.</span></span>


