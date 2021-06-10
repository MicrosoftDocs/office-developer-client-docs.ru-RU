---
title: Свойство Field2.SourceField (DAO)
TOCTitle: SourceField Property
ms:assetid: f89146c1-d4a4-1129-636a-c22cf7921a4e
ms:mtpsurl: https://msdn.microsoft.com/library/Ff836948(v=office.15)
ms:contentKeyID: 48548784
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: 1d0bedd3c1f9f2af6ccf156e1cf8c0192551f582
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32292680"
---
# <a name="field2sourcefield-property-dao"></a><span data-ttu-id="07477-102">Свойство Field2.SourceField (DAO)</span><span class="sxs-lookup"><span data-stu-id="07477-102">Field2.SourceField property (DAO)</span></span>


<span data-ttu-id="07477-103">**Область применения**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="07477-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="07477-104">Возвращает значение, которое указывает имя поля, которое является исходным источником данных для **объекта Field2.**</span><span class="sxs-lookup"><span data-stu-id="07477-104">Returns a value that indicates the name of the field that is the original source of the data for a **Field2** object.</span></span> <span data-ttu-id="07477-105">Только для чтения, **String**.</span><span class="sxs-lookup"><span data-stu-id="07477-105">Read-only **String**.</span></span>

## <a name="syntax"></a><span data-ttu-id="07477-106">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="07477-106">Syntax</span></span>

<span data-ttu-id="07477-107">*выражения* . SourceField</span><span class="sxs-lookup"><span data-stu-id="07477-107">*expression* .SourceField</span></span>

<span data-ttu-id="07477-108">*expression* — переменная, представляющая объект **Field2**.</span><span class="sxs-lookup"><span data-stu-id="07477-108">*expression* A variable that represents a **Field2** object.</span></span>

## <a name="remarks"></a><span data-ttu-id="07477-109">Примечания</span><span class="sxs-lookup"><span data-stu-id="07477-109">Remarks</span></span>

<span data-ttu-id="07477-110">Для объекта **Field2** использование свойств **SourceField** и  **SourceTable** зависит от объекта, который содержит коллекцию Полей, к которую примыкает объект **Field2,** как показано в следующей таблице.</span><span class="sxs-lookup"><span data-stu-id="07477-110">For a **Field2** object, use of the **SourceField** and **SourceTable** properties depends on the object that contains the **Fields** collection that the **Field2** object is appended to, as shown in the following table.</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="07477-111">Объект, приданный</span><span class="sxs-lookup"><span data-stu-id="07477-111">Object appended to</span></span></p></th>
<th><p><span data-ttu-id="07477-112">Usage</span><span class="sxs-lookup"><span data-stu-id="07477-112">Usage</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="07477-113"><strong>Index</strong></span><span class="sxs-lookup"><span data-stu-id="07477-113"><strong>Index</strong></span></span></p></td>
<td><p><span data-ttu-id="07477-114">Не поддерживается</span><span class="sxs-lookup"><span data-stu-id="07477-114">Not supported</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="07477-115"><strong>QueryDef</strong></span><span class="sxs-lookup"><span data-stu-id="07477-115"><strong>QueryDef</strong></span></span></p></td>
<td><p><span data-ttu-id="07477-116">Только для чтения</span><span class="sxs-lookup"><span data-stu-id="07477-116">Read-only</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="07477-117"><strong>Recordset</strong></span><span class="sxs-lookup"><span data-stu-id="07477-117"><strong>Recordset</strong></span></span></p></td>
<td><p><span data-ttu-id="07477-118">Только для чтения</span><span class="sxs-lookup"><span data-stu-id="07477-118">Read-only</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="07477-119"><strong>Relation</strong></span><span class="sxs-lookup"><span data-stu-id="07477-119"><strong>Relation</strong></span></span></p></td>
<td><p><span data-ttu-id="07477-120">Не поддерживается</span><span class="sxs-lookup"><span data-stu-id="07477-120">Not supported</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="07477-121"><strong>TableDef</strong></span><span class="sxs-lookup"><span data-stu-id="07477-121"><strong>TableDef</strong></span></span></p></td>
<td><p><span data-ttu-id="07477-122">Только для чтения</span><span class="sxs-lookup"><span data-stu-id="07477-122">Read-only</span></span></p></td>
</tr>
</tbody>
</table>


<span data-ttu-id="07477-123">Эти свойства указывают исходные имена полей и таблиц, связанных с **объектом Field2.**</span><span class="sxs-lookup"><span data-stu-id="07477-123">These properties indicate the original field and table names associated with a **Field2** object.</span></span> <span data-ttu-id="07477-124">Например, эти свойства можно использовать для определения исходного источника данных в поле запросов, имя которого не связано с именем поля в исходной таблице.</span><span class="sxs-lookup"><span data-stu-id="07477-124">For example, you could use these properties to determine the original source of the data in a query field whose name is unrelated to the name of the field in the underlying table.</span></span>

