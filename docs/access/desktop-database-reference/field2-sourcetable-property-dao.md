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
ms.sourcegitcommit: d6695c94415fa47952ee7961a69660abc0904434
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/17/2019
ms.locfileid: "28717946"
---
# <a name="field2sourcetable-property-dao"></a><span data-ttu-id="a4c29-102">Свойство Field2.SourceTable (DAO)</span><span class="sxs-lookup"><span data-stu-id="a4c29-102">Field2.SourceTable property (DAO)</span></span>


<span data-ttu-id="a4c29-103">**Применимо к**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="a4c29-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="a4c29-104">Возвращает значение, указывающее имя таблицы, который является оригинального источника данных для объекта **поле2** .</span><span class="sxs-lookup"><span data-stu-id="a4c29-104">Returns a value that indicates the name of the table that is the original source of the data for a **Field2** object.</span></span> <span data-ttu-id="a4c29-105">Только для чтения, **String**.</span><span class="sxs-lookup"><span data-stu-id="a4c29-105">Read-only **String**.</span></span>

## <a name="syntax"></a><span data-ttu-id="a4c29-106">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="a4c29-106">Syntax</span></span>

<span data-ttu-id="a4c29-107">*выражение* . Таблица</span><span class="sxs-lookup"><span data-stu-id="a4c29-107">*expression* .SourceTable</span></span>

<span data-ttu-id="a4c29-108">*выражение* Переменная, которая представляет собой объект- **поле2** .</span><span class="sxs-lookup"><span data-stu-id="a4c29-108">*expression* A variable that represents a **Field2** object.</span></span>

## <a name="remarks"></a><span data-ttu-id="a4c29-109">Замечания</span><span class="sxs-lookup"><span data-stu-id="a4c29-109">Remarks</span></span>

<span data-ttu-id="a4c29-110">Для объекта **поле2** использование свойств **SourceField** и **Таблица** зависит от объекта, который содержит коллекцию **полей** , добавляется объект **поле2** , как показано в следующей таблице.</span><span class="sxs-lookup"><span data-stu-id="a4c29-110">For a **Field2** object, use of the **SourceField** and **SourceTable** properties depends on the object that contains the **Fields** collection that the **Field2** object is appended to, as shown in the following table.</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="a4c29-111">Объект, добавляемый в конец</span><span class="sxs-lookup"><span data-stu-id="a4c29-111">Object appended to</span></span></p></th>
<th><p><span data-ttu-id="a4c29-112">Применение</span><span class="sxs-lookup"><span data-stu-id="a4c29-112">Usage</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="a4c29-113"><strong>Index</strong></span><span class="sxs-lookup"><span data-stu-id="a4c29-113"><strong>Index</strong></span></span></p></td>
<td><p><span data-ttu-id="a4c29-114">Не поддерживается</span><span class="sxs-lookup"><span data-stu-id="a4c29-114">Not supported</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="a4c29-115"><strong>QueryDef</strong></span><span class="sxs-lookup"><span data-stu-id="a4c29-115"><strong>QueryDef</strong></span></span></p></td>
<td><p><span data-ttu-id="a4c29-116">Только для чтения</span><span class="sxs-lookup"><span data-stu-id="a4c29-116">Read-only</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="a4c29-117"><strong>Recordset</strong></span><span class="sxs-lookup"><span data-stu-id="a4c29-117"><strong>Recordset</strong></span></span></p></td>
<td><p><span data-ttu-id="a4c29-118">Только для чтения</span><span class="sxs-lookup"><span data-stu-id="a4c29-118">Read-only</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="a4c29-119"><strong>Relation</strong></span><span class="sxs-lookup"><span data-stu-id="a4c29-119"><strong>Relation</strong></span></span></p></td>
<td><p><span data-ttu-id="a4c29-120">Не поддерживается</span><span class="sxs-lookup"><span data-stu-id="a4c29-120">Not supported</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="a4c29-121"><strong>TableDef</strong></span><span class="sxs-lookup"><span data-stu-id="a4c29-121"><strong>TableDef</strong></span></span></p></td>
<td><p><span data-ttu-id="a4c29-122">Только для чтения</span><span class="sxs-lookup"><span data-stu-id="a4c29-122">Read-only</span></span></p></td>
</tr>
</tbody>
</table>


<span data-ttu-id="a4c29-123">Эти свойства указывают исходные имена полей и таблиц, связанной с объектом **поле2** .</span><span class="sxs-lookup"><span data-stu-id="a4c29-123">These properties indicate the original field and table names associated with a **Field2** object.</span></span> <span data-ttu-id="a4c29-124">Например можно использовать эти свойства для определения исходного источника данных в поле запроса, имя которого не связано с имя поля в таблице.</span><span class="sxs-lookup"><span data-stu-id="a4c29-124">For example, you could use these properties to determine the original source of the data in a query field whose name is unrelated to the name of the field in the underlying table.</span></span>


> [!NOTE]
> <span data-ttu-id="a4c29-125">Свойство **Таблица** не возвращает имя удобной для восприятия таблицы при использовании объекта **поле2** в коллекции **полей** объекта **набора записей** в таблице тип.</span><span class="sxs-lookup"><span data-stu-id="a4c29-125">The **SourceTable** property will not return a meaningful table name if used on a **Field2** object in the **Fields** collection of a table-type **Recordset** object.</span></span>


