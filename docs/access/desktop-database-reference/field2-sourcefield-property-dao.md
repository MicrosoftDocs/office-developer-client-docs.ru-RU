---
title: Свойство field2. Саурцефиелд (DAO)
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
# <a name="field2sourcefield-property-dao"></a><span data-ttu-id="ceb93-102">Свойство field2. Саурцефиелд (DAO)</span><span class="sxs-lookup"><span data-stu-id="ceb93-102">Field2.SourceField property (DAO)</span></span>


<span data-ttu-id="ceb93-103">**Область применения**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="ceb93-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="ceb93-104">Возвращает значение, которое указывает имя поля, которое является исходным источником данных для объекта **field2** .</span><span class="sxs-lookup"><span data-stu-id="ceb93-104">Returns a value that indicates the name of the field that is the original source of the data for a **Field2** object.</span></span> <span data-ttu-id="ceb93-105">Только для чтения, **String**.</span><span class="sxs-lookup"><span data-stu-id="ceb93-105">Read-only **String**.</span></span>

## <a name="syntax"></a><span data-ttu-id="ceb93-106">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="ceb93-106">Syntax</span></span>

<span data-ttu-id="ceb93-107">*Expression* . Саурцефиелд</span><span class="sxs-lookup"><span data-stu-id="ceb93-107">*expression* .SourceField</span></span>

<span data-ttu-id="ceb93-108">*expression* — переменная, представляющая объект **Field2**.</span><span class="sxs-lookup"><span data-stu-id="ceb93-108">*expression* A variable that represents a **Field2** object.</span></span>

## <a name="remarks"></a><span data-ttu-id="ceb93-109">Замечания</span><span class="sxs-lookup"><span data-stu-id="ceb93-109">Remarks</span></span>

<span data-ttu-id="ceb93-110">Для объекта **field2** использование свойств **саурцефиелд** и **саурцетабле** зависит от объекта, содержащего коллекцию Fields, в которую \*\*\*\* добавляется объект **field2** , как показано в следующей таблице.</span><span class="sxs-lookup"><span data-stu-id="ceb93-110">For a **Field2** object, use of the **SourceField** and **SourceTable** properties depends on the object that contains the **Fields** collection that the **Field2** object is appended to, as shown in the following table.</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="ceb93-111">Объект, добавленный в</span><span class="sxs-lookup"><span data-stu-id="ceb93-111">Object appended to</span></span></p></th>
<th><p><span data-ttu-id="ceb93-112">Использование</span><span class="sxs-lookup"><span data-stu-id="ceb93-112">Usage</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="ceb93-113"><strong>Index</strong></span><span class="sxs-lookup"><span data-stu-id="ceb93-113"><strong>Index</strong></span></span></p></td>
<td><p><span data-ttu-id="ceb93-114">Не поддерживается</span><span class="sxs-lookup"><span data-stu-id="ceb93-114">Not supported</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="ceb93-115"><strong>QueryDef</strong></span><span class="sxs-lookup"><span data-stu-id="ceb93-115"><strong>QueryDef</strong></span></span></p></td>
<td><p><span data-ttu-id="ceb93-116">Только для чтения</span><span class="sxs-lookup"><span data-stu-id="ceb93-116">Read-only</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="ceb93-117"><strong>Recordset</strong></span><span class="sxs-lookup"><span data-stu-id="ceb93-117"><strong>Recordset</strong></span></span></p></td>
<td><p><span data-ttu-id="ceb93-118">Только для чтения</span><span class="sxs-lookup"><span data-stu-id="ceb93-118">Read-only</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="ceb93-119"><strong>Relation</strong></span><span class="sxs-lookup"><span data-stu-id="ceb93-119"><strong>Relation</strong></span></span></p></td>
<td><p><span data-ttu-id="ceb93-120">Не поддерживается</span><span class="sxs-lookup"><span data-stu-id="ceb93-120">Not supported</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="ceb93-121"><strong>TableDef</strong></span><span class="sxs-lookup"><span data-stu-id="ceb93-121"><strong>TableDef</strong></span></span></p></td>
<td><p><span data-ttu-id="ceb93-122">Только для чтения</span><span class="sxs-lookup"><span data-stu-id="ceb93-122">Read-only</span></span></p></td>
</tr>
</tbody>
</table>


<span data-ttu-id="ceb93-123">Эти свойства указывают исходное имя поля и таблицы, связанные с объектом **field2** .</span><span class="sxs-lookup"><span data-stu-id="ceb93-123">These properties indicate the original field and table names associated with a **Field2** object.</span></span> <span data-ttu-id="ceb93-124">Например, эти свойства можно использовать для определения исходного источника данных в поле запроса с именем, не связанным с именем поля в базовой таблице.</span><span class="sxs-lookup"><span data-stu-id="ceb93-124">For example, you could use these properties to determine the original source of the data in a query field whose name is unrelated to the name of the field in the underlying table.</span></span>

