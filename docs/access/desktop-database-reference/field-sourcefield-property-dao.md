---
title: Свойство Field.SourceField (DAO)
TOCTitle: SourceField Property
ms:assetid: e5750d6c-4078-7bbb-9356-f9207c4e8028
ms:mtpsurl: https://msdn.microsoft.com/library/Ff835953(v=office.15)
ms:contentKeyID: 48548360
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: 249dabfa13bac6973cea4bd69e0867292c4a6967
ms.sourcegitcommit: d6695c94415fa47952ee7961a69660abc0904434
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/17/2019
ms.locfileid: "28718212"
---
# <a name="fieldsourcefield-property-dao"></a><span data-ttu-id="0708f-102">Свойство Field.SourceField (DAO)</span><span class="sxs-lookup"><span data-stu-id="0708f-102">Field.SourceField property (DAO)</span></span>


<span data-ttu-id="0708f-103">**Применимо к**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="0708f-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="0708f-104">Возвращает значение, указывающее имя поля, который является оригинального источника данных для объекта **поля** .</span><span class="sxs-lookup"><span data-stu-id="0708f-104">Returns a value that indicates the name of the field that is the original source of the data for a **Field** object.</span></span> <span data-ttu-id="0708f-105">Только для чтения, **String**.</span><span class="sxs-lookup"><span data-stu-id="0708f-105">Read-only **String**.</span></span>

## <a name="syntax"></a><span data-ttu-id="0708f-106">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="0708f-106">Syntax</span></span>

<span data-ttu-id="0708f-107">*выражение* . SourceField</span><span class="sxs-lookup"><span data-stu-id="0708f-107">*expression* .SourceField</span></span>

<span data-ttu-id="0708f-108">*выражение* Переменная, которая представляет собой объект- **поля** .</span><span class="sxs-lookup"><span data-stu-id="0708f-108">*expression* A variable that represents a **Field** object.</span></span>

## <a name="remarks"></a><span data-ttu-id="0708f-109">Замечания</span><span class="sxs-lookup"><span data-stu-id="0708f-109">Remarks</span></span>

<span data-ttu-id="0708f-110">Для объекта **поля** использование свойств **SourceField** и **Таблица** зависит от объекта, который содержит коллекцию **полей** , используется в качестве объекта **поля** "Кому", как показано в следующей таблице.</span><span class="sxs-lookup"><span data-stu-id="0708f-110">For a **Field** object, use of the **SourceField** and **SourceTable** properties depends on the object that contains the **Fields** collection that the **Field** object is appended to, as shown in the following table.</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="0708f-111">Объект, добавляемый в конец</span><span class="sxs-lookup"><span data-stu-id="0708f-111">Object appended to</span></span></p></th>
<th><p><span data-ttu-id="0708f-112">Применение</span><span class="sxs-lookup"><span data-stu-id="0708f-112">Usage</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="0708f-113"><strong>Index</strong></span><span class="sxs-lookup"><span data-stu-id="0708f-113"><strong>Index</strong></span></span></p></td>
<td><p><span data-ttu-id="0708f-114">Не поддерживается</span><span class="sxs-lookup"><span data-stu-id="0708f-114">Not supported</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="0708f-115"><strong>QueryDef</strong></span><span class="sxs-lookup"><span data-stu-id="0708f-115"><strong>QueryDef</strong></span></span></p></td>
<td><p><span data-ttu-id="0708f-116">Только для чтения</span><span class="sxs-lookup"><span data-stu-id="0708f-116">Read-only</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="0708f-117"><strong>Recordset</strong></span><span class="sxs-lookup"><span data-stu-id="0708f-117"><strong>Recordset</strong></span></span></p></td>
<td><p><span data-ttu-id="0708f-118">Только для чтения</span><span class="sxs-lookup"><span data-stu-id="0708f-118">Read-only</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="0708f-119"><strong>Relation</strong></span><span class="sxs-lookup"><span data-stu-id="0708f-119"><strong>Relation</strong></span></span></p></td>
<td><p><span data-ttu-id="0708f-120">Не поддерживается</span><span class="sxs-lookup"><span data-stu-id="0708f-120">Not supported</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="0708f-121"><strong>TableDef</strong></span><span class="sxs-lookup"><span data-stu-id="0708f-121"><strong>TableDef</strong></span></span></p></td>
<td><p><span data-ttu-id="0708f-122">Только для чтения</span><span class="sxs-lookup"><span data-stu-id="0708f-122">Read-only</span></span></p></td>
</tr>
</tbody>
</table>


<span data-ttu-id="0708f-123">Эти свойства указывают исходные имена полей и таблиц, связанной с объектом **поля** .</span><span class="sxs-lookup"><span data-stu-id="0708f-123">These properties indicate the original field and table names associated with a **Field** object.</span></span> <span data-ttu-id="0708f-124">Например можно использовать эти свойства для определения исходного источника данных в поле запроса, имя которого не связано с имя поля в таблице.</span><span class="sxs-lookup"><span data-stu-id="0708f-124">For example, you could use these properties to determine the original source of the data in a query field whose name is unrelated to the name of the field in the underlying table.</span></span>

