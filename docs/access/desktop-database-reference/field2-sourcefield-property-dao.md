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
# <a name="field2sourcefield-property-dao"></a><span data-ttu-id="1d656-102">Свойство Field2.SourceField (DAO)</span><span class="sxs-lookup"><span data-stu-id="1d656-102">Field2.SourceField property (DAO)</span></span>


<span data-ttu-id="1d656-103">**Область применения**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="1d656-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="1d656-104">Возвращает значение, которое указывает имя поля, которое является исходным источником данных для **объекта Field2.**</span><span class="sxs-lookup"><span data-stu-id="1d656-104">Returns a value that indicates the name of the field that is the original source of the data for a **Field2** object.</span></span> <span data-ttu-id="1d656-105">Только для чтения, **String**.</span><span class="sxs-lookup"><span data-stu-id="1d656-105">Read-only **String**.</span></span>

## <a name="syntax"></a><span data-ttu-id="1d656-106">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="1d656-106">Syntax</span></span>

<span data-ttu-id="1d656-107">*выражение .* SourceField</span><span class="sxs-lookup"><span data-stu-id="1d656-107">*expression* .SourceField</span></span>

<span data-ttu-id="1d656-108">*expression* — переменная, представляющая объект **Field2**.</span><span class="sxs-lookup"><span data-stu-id="1d656-108">*expression* A variable that represents a **Field2** object.</span></span>

## <a name="remarks"></a><span data-ttu-id="1d656-109">Заметки</span><span class="sxs-lookup"><span data-stu-id="1d656-109">Remarks</span></span>

<span data-ttu-id="1d656-110">Для объекта **Field2** использование свойств **SourceField** и **SourceTable** зависит от объекта, который содержит коллекцию **Fields,** к которую применит объект **Field2,** как показано в следующей таблице.</span><span class="sxs-lookup"><span data-stu-id="1d656-110">For a **Field2** object, use of the **SourceField** and **SourceTable** properties depends on the object that contains the **Fields** collection that the **Field2** object is appended to, as shown in the following table.</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="1d656-111">Объект, к</span><span class="sxs-lookup"><span data-stu-id="1d656-111">Object appended to</span></span></p></th>
<th><p><span data-ttu-id="1d656-112">Использование</span><span class="sxs-lookup"><span data-stu-id="1d656-112">Usage</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="1d656-113"><strong>Индекс</strong></span><span class="sxs-lookup"><span data-stu-id="1d656-113"><strong>Index</strong></span></span></p></td>
<td><p><span data-ttu-id="1d656-114">Не поддерживается</span><span class="sxs-lookup"><span data-stu-id="1d656-114">Not supported</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="1d656-115"><strong>QueryDef</strong></span><span class="sxs-lookup"><span data-stu-id="1d656-115"><strong>QueryDef</strong></span></span></p></td>
<td><p><span data-ttu-id="1d656-116">Только для чтения</span><span class="sxs-lookup"><span data-stu-id="1d656-116">Read-only</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="1d656-117"><strong>Recordset</strong></span><span class="sxs-lookup"><span data-stu-id="1d656-117"><strong>Recordset</strong></span></span></p></td>
<td><p><span data-ttu-id="1d656-118">Только для чтения</span><span class="sxs-lookup"><span data-stu-id="1d656-118">Read-only</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="1d656-119"><strong>Relation</strong></span><span class="sxs-lookup"><span data-stu-id="1d656-119"><strong>Relation</strong></span></span></p></td>
<td><p><span data-ttu-id="1d656-120">Не поддерживается</span><span class="sxs-lookup"><span data-stu-id="1d656-120">Not supported</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="1d656-121"><strong>TableDef</strong></span><span class="sxs-lookup"><span data-stu-id="1d656-121"><strong>TableDef</strong></span></span></p></td>
<td><p><span data-ttu-id="1d656-122">Только для чтения</span><span class="sxs-lookup"><span data-stu-id="1d656-122">Read-only</span></span></p></td>
</tr>
</tbody>
</table>


<span data-ttu-id="1d656-123">Эти свойства указывают исходные имена полей и таблиц, связанных с **объектом Field2.**</span><span class="sxs-lookup"><span data-stu-id="1d656-123">These properties indicate the original field and table names associated with a **Field2** object.</span></span> <span data-ttu-id="1d656-124">Например, эти свойства можно использовать для определения исходного источника данных в поле запроса, имя которого не связано с именем поля в таблице ниже.</span><span class="sxs-lookup"><span data-stu-id="1d656-124">For example, you could use these properties to determine the original source of the data in a query field whose name is unrelated to the name of the field in the underlying table.</span></span>

