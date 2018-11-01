---
title: Field.SourceField Property (DAO)
TOCTitle: SourceField Property
ms:assetid: e5750d6c-4078-7bbb-9356-f9207c4e8028
ms:mtpsurl: https://msdn.microsoft.com/library/Ff835953(v=office.15)
ms:contentKeyID: 48548360
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 0a769cd242064ae9f1fef91c787e614610aab48a
ms.sourcegitcommit: c557bbcccf37a6011f89aae1ddd399dfe549d087
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/31/2018
ms.locfileid: "25869374"
---
# <a name="fieldsourcefield-property-dao"></a><span data-ttu-id="192ec-102">Field.SourceField Property (DAO)</span><span class="sxs-lookup"><span data-stu-id="192ec-102">Field.SourceField Property (DAO)</span></span>


<span data-ttu-id="192ec-103">**Применимо к**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="192ec-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="192ec-104">Возвращает значение, указывающее имя поля, который является оригинального источника данных для объекта **поля** .</span><span class="sxs-lookup"><span data-stu-id="192ec-104">Returns a value that indicates the name of the field that is the original source of the data for a **Field** object.</span></span> <span data-ttu-id="192ec-105">Только для чтения, **String**.</span><span class="sxs-lookup"><span data-stu-id="192ec-105">Read-only **String**.</span></span>

## <a name="syntax"></a><span data-ttu-id="192ec-106">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="192ec-106">Syntax</span></span>

<span data-ttu-id="192ec-107">*выражение* . SourceField</span><span class="sxs-lookup"><span data-stu-id="192ec-107">*expression* .SourceField</span></span>

<span data-ttu-id="192ec-108">*выражение* Переменная, которая представляет собой объект- **поля** .</span><span class="sxs-lookup"><span data-stu-id="192ec-108">*expression* A variable that represents a **Field** object.</span></span>

## <a name="remarks"></a><span data-ttu-id="192ec-109">Замечания</span><span class="sxs-lookup"><span data-stu-id="192ec-109">Remarks</span></span>

<span data-ttu-id="192ec-110">Для объекта **поля** использование свойств **SourceField** и **Таблица** зависит от объекта, который содержит коллекцию **полей** , используется в качестве объекта **поля** "Кому", как показано в следующей таблице.</span><span class="sxs-lookup"><span data-stu-id="192ec-110">For a **Field** object, use of the **SourceField** and **SourceTable** properties depends on the object that contains the **Fields** collection that the **Field** object is appended to, as shown in the following table.</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="192ec-111">Объект, добавляемый в конец</span><span class="sxs-lookup"><span data-stu-id="192ec-111">Object appended to</span></span></p></th>
<th><p><span data-ttu-id="192ec-112">Применение</span><span class="sxs-lookup"><span data-stu-id="192ec-112">Usage</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="192ec-113"><strong>Индекс</strong></span><span class="sxs-lookup"><span data-stu-id="192ec-113"><strong>Index</strong></span></span></p></td>
<td><p><span data-ttu-id="192ec-114">Не поддерживается</span><span class="sxs-lookup"><span data-stu-id="192ec-114">Not supported</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="192ec-115"><strong>QueryDef</strong></span><span class="sxs-lookup"><span data-stu-id="192ec-115"><strong>QueryDef</strong></span></span></p></td>
<td><p><span data-ttu-id="192ec-116">Только для чтения</span><span class="sxs-lookup"><span data-stu-id="192ec-116">Read-only</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="192ec-117"><strong>Набор записей</strong></span><span class="sxs-lookup"><span data-stu-id="192ec-117"><strong>Recordset</strong></span></span></p></td>
<td><p><span data-ttu-id="192ec-118">Только для чтения</span><span class="sxs-lookup"><span data-stu-id="192ec-118">Read-only</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="192ec-119"><strong>Связь</strong></span><span class="sxs-lookup"><span data-stu-id="192ec-119"><strong>Relation</strong></span></span></p></td>
<td><p><span data-ttu-id="192ec-120">Не поддерживается</span><span class="sxs-lookup"><span data-stu-id="192ec-120">Not supported</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="192ec-121"><strong>TableDef</strong></span><span class="sxs-lookup"><span data-stu-id="192ec-121"><strong>TableDef</strong></span></span></p></td>
<td><p><span data-ttu-id="192ec-122">Только для чтения</span><span class="sxs-lookup"><span data-stu-id="192ec-122">Read-only</span></span></p></td>
</tr>
</tbody>
</table>


<span data-ttu-id="192ec-123">Эти свойства указывают исходные имена полей и таблиц, связанной с объектом **поля** .</span><span class="sxs-lookup"><span data-stu-id="192ec-123">These properties indicate the original field and table names associated with a **Field** object.</span></span> <span data-ttu-id="192ec-124">Например можно использовать эти свойства для определения исходного источника данных в поле запроса, имя которого не связано с имя поля в таблице.</span><span class="sxs-lookup"><span data-stu-id="192ec-124">For example, you could use these properties to determine the original source of the data in a query field whose name is unrelated to the name of the field in the underlying table.</span></span>

