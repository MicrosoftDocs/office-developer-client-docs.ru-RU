---
title: Свойство Field. Саурцетабле (DAO)
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
# <a name="fieldsourcetable-property-dao"></a><span data-ttu-id="b42a9-102">Свойство Field. Саурцетабле (DAO)</span><span class="sxs-lookup"><span data-stu-id="b42a9-102">Field.SourceTable property (DAO)</span></span>


<span data-ttu-id="b42a9-103">**Область применения**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="b42a9-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="b42a9-104">Возвращает значение, которое указывает имя таблицы, которая является исходным источником данных для объекта **field** .</span><span class="sxs-lookup"><span data-stu-id="b42a9-104">Returns a value that indicates the name of the table that is the original source of the data for a **Field** object.</span></span> <span data-ttu-id="b42a9-105">Только для чтения, **String**.</span><span class="sxs-lookup"><span data-stu-id="b42a9-105">Read-only **String**.</span></span>

## <a name="syntax"></a><span data-ttu-id="b42a9-106">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="b42a9-106">Syntax</span></span>

<span data-ttu-id="b42a9-107">*Expression* . Саурцетабле</span><span class="sxs-lookup"><span data-stu-id="b42a9-107">*expression* .SourceTable</span></span>

<span data-ttu-id="b42a9-108">*выражение*: переменная, представляющая объект **Field**.</span><span class="sxs-lookup"><span data-stu-id="b42a9-108">*expression* A variable that represents a **Field** object.</span></span>

## <a name="remarks"></a><span data-ttu-id="b42a9-109">Комментарии</span><span class="sxs-lookup"><span data-stu-id="b42a9-109">Remarks</span></span>

<span data-ttu-id="b42a9-110">Для объекта **field** использование свойств **саурцефиелд** и **саурцетабле** зависит от объекта, содержащего коллекцию Fields, в которую \*\*\*\* добавляется объект **field** , как показано в следующей таблице.</span><span class="sxs-lookup"><span data-stu-id="b42a9-110">For a **Field** object, use of the **SourceField** and **SourceTable** properties depends on the object that contains the **Fields** collection that the **Field** object is appended to, as shown in the following table.</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="b42a9-111">Объект, добавленный в</span><span class="sxs-lookup"><span data-stu-id="b42a9-111">Object appended to</span></span></p></th>
<th><p><span data-ttu-id="b42a9-112">Использование</span><span class="sxs-lookup"><span data-stu-id="b42a9-112">Usage</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="b42a9-113"><strong>Index</strong></span><span class="sxs-lookup"><span data-stu-id="b42a9-113"><strong>Index</strong></span></span></p></td>
<td><p><span data-ttu-id="b42a9-114">Не поддерживается</span><span class="sxs-lookup"><span data-stu-id="b42a9-114">Not supported</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="b42a9-115"><strong>QueryDef</strong></span><span class="sxs-lookup"><span data-stu-id="b42a9-115"><strong>QueryDef</strong></span></span></p></td>
<td><p><span data-ttu-id="b42a9-116">Только для чтения</span><span class="sxs-lookup"><span data-stu-id="b42a9-116">Read-only</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="b42a9-117"><strong>Recordset</strong></span><span class="sxs-lookup"><span data-stu-id="b42a9-117"><strong>Recordset</strong></span></span></p></td>
<td><p><span data-ttu-id="b42a9-118">Только для чтения</span><span class="sxs-lookup"><span data-stu-id="b42a9-118">Read-only</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="b42a9-119"><strong>Relation</strong></span><span class="sxs-lookup"><span data-stu-id="b42a9-119"><strong>Relation</strong></span></span></p></td>
<td><p><span data-ttu-id="b42a9-120">Не поддерживается</span><span class="sxs-lookup"><span data-stu-id="b42a9-120">Not supported</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="b42a9-121"><strong>TableDef</strong></span><span class="sxs-lookup"><span data-stu-id="b42a9-121"><strong>TableDef</strong></span></span></p></td>
<td><p><span data-ttu-id="b42a9-122">Только для чтения</span><span class="sxs-lookup"><span data-stu-id="b42a9-122">Read-only</span></span></p></td>
</tr>
</tbody>
</table>


<span data-ttu-id="b42a9-123">Эти свойства указывают исходное имя поля и таблицы, связанные с объектом **field** .</span><span class="sxs-lookup"><span data-stu-id="b42a9-123">These properties indicate the original field and table names associated with a **Field** object.</span></span> <span data-ttu-id="b42a9-124">Например, эти свойства можно использовать для определения исходного источника данных в поле запроса с именем, не связанным с именем поля в базовой таблице.</span><span class="sxs-lookup"><span data-stu-id="b42a9-124">For example, you could use these properties to determine the original source of the data in a query field whose name is unrelated to the name of the field in the underlying table.</span></span>


> [!NOTE]
> <span data-ttu-id="b42a9-125">Свойство **саурцетабле** не будет возвращать осмысленное имя таблицы, если оно используется для объекта **field** в \*\*\*\* коллекции Fields объекта **Recordset** табличного типа.</span><span class="sxs-lookup"><span data-stu-id="b42a9-125">The **SourceTable** property will not return a meaningful table name if used on a **Field** object in the **Fields** collection of a table-type **Recordset** object.</span></span>


