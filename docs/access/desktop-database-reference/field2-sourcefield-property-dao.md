---
title: Field2.SourceField Property (DAO)
TOCTitle: SourceField Property
ms:assetid: f89146c1-d4a4-1129-636a-c22cf7921a4e
ms:mtpsurl: https://msdn.microsoft.com/library/Ff836948(v=office.15)
ms:contentKeyID: 48548784
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 09351acfea263c41bd9cb7f857139dfacf359421
ms.sourcegitcommit: 19aca09c5812cfb98b68b5d4604dcaa814479df7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/09/2018
ms.locfileid: "25481418"
---
# <a name="field2sourcefield-property-dao"></a><span data-ttu-id="1e6d6-102">Field2.SourceField Property (DAO)</span><span class="sxs-lookup"><span data-stu-id="1e6d6-102">Field2.SourceField Property (DAO)</span></span>


<span data-ttu-id="1e6d6-103">**Применимо к**: Access 2013 | Office 2013</span><span class="sxs-lookup"><span data-stu-id="1e6d6-103">**Applies to**: Access 2013 | Office 2013</span></span>

<span data-ttu-id="1e6d6-104">Возвращает значение, указывающее имя поля, который является оригинального источника данных для объекта **поле2** .</span><span class="sxs-lookup"><span data-stu-id="1e6d6-104">Returns a value that indicates the name of the field that is the original source of the data for a **Field2** object.</span></span> <span data-ttu-id="1e6d6-105">Только для чтения, **String**.</span><span class="sxs-lookup"><span data-stu-id="1e6d6-105">Read-only **String**.</span></span>

## <a name="syntax"></a><span data-ttu-id="1e6d6-106">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="1e6d6-106">Syntax</span></span>

<span data-ttu-id="1e6d6-107">*выражение* . SourceField</span><span class="sxs-lookup"><span data-stu-id="1e6d6-107">*expression* .SourceField</span></span>

<span data-ttu-id="1e6d6-108">*выражение* Переменная, которая представляет собой объект- **поле2** .</span><span class="sxs-lookup"><span data-stu-id="1e6d6-108">*expression* A variable that represents a **Field2** object.</span></span>

## <a name="remarks"></a><span data-ttu-id="1e6d6-109">Замечания</span><span class="sxs-lookup"><span data-stu-id="1e6d6-109">Remarks</span></span>

<span data-ttu-id="1e6d6-110">Для объекта **поле2** использование свойств **SourceField** и **Таблица** зависит от объекта, который содержит коллекцию **полей** , добавляется объект **поле2** , как показано в следующей таблице.</span><span class="sxs-lookup"><span data-stu-id="1e6d6-110">For a **Field2** object, use of the **SourceField** and **SourceTable** properties depends on the object that contains the **Fields** collection that the **Field2** object is appended to, as shown in the following table.</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="1e6d6-111">Объект, добавляемый в конец</span><span class="sxs-lookup"><span data-stu-id="1e6d6-111">Object appended to</span></span></p></th>
<th><p><span data-ttu-id="1e6d6-112">Применение</span><span class="sxs-lookup"><span data-stu-id="1e6d6-112">Usage</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="1e6d6-113"><strong>Индекс</strong></span><span class="sxs-lookup"><span data-stu-id="1e6d6-113"><strong>Index</strong></span></span></p></td>
<td><p><span data-ttu-id="1e6d6-114">Не поддерживается</span><span class="sxs-lookup"><span data-stu-id="1e6d6-114">Not supported</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="1e6d6-115"><strong>QueryDef</strong></span><span class="sxs-lookup"><span data-stu-id="1e6d6-115"><strong>QueryDef</strong></span></span></p></td>
<td><p><span data-ttu-id="1e6d6-116">Только для чтения</span><span class="sxs-lookup"><span data-stu-id="1e6d6-116">Read-only</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="1e6d6-117"><strong>Набор записей</strong></span><span class="sxs-lookup"><span data-stu-id="1e6d6-117"><strong>Recordset</strong></span></span></p></td>
<td><p><span data-ttu-id="1e6d6-118">Только для чтения</span><span class="sxs-lookup"><span data-stu-id="1e6d6-118">Read-only</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="1e6d6-119"><strong>Связь</strong></span><span class="sxs-lookup"><span data-stu-id="1e6d6-119"><strong>Relation</strong></span></span></p></td>
<td><p><span data-ttu-id="1e6d6-120">Не поддерживается</span><span class="sxs-lookup"><span data-stu-id="1e6d6-120">Not supported</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="1e6d6-121"><strong>TableDef</strong></span><span class="sxs-lookup"><span data-stu-id="1e6d6-121"><strong>TableDef</strong></span></span></p></td>
<td><p><span data-ttu-id="1e6d6-122">Только для чтения</span><span class="sxs-lookup"><span data-stu-id="1e6d6-122">Read-only</span></span></p></td>
</tr>
</tbody>
</table>


<span data-ttu-id="1e6d6-123">Эти свойства указывают исходные имена полей и таблиц, связанной с объектом **поле2** .</span><span class="sxs-lookup"><span data-stu-id="1e6d6-123">These properties indicate the original field and table names associated with a **Field2** object.</span></span> <span data-ttu-id="1e6d6-124">Например можно использовать эти свойства для определения исходного источника данных в поле запроса, имя которого не связано с имя поля в таблице.</span><span class="sxs-lookup"><span data-stu-id="1e6d6-124">For example, you could use these properties to determine the original source of the data in a query field whose name is unrelated to the name of the field in the underlying table.</span></span>

