---
title: Свойство Field2.SourceField (DAO)
TOCTitle: SourceField Property
ms:assetid: f89146c1-d4a4-1129-636a-c22cf7921a4e
ms:mtpsurl: https://msdn.microsoft.com/library/Ff836948(v=office.15)
ms:contentKeyID: 48548784
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 587214a5fddc5774423d2eb5af7c2a8926ee1622
ms.sourcegitcommit: d7248f803002b31cf7fc561b03530199a9b0a8fd
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 11/02/2018
ms.locfileid: "25926271"
---
# <a name="field2sourcefield-property-dao"></a><span data-ttu-id="a9b41-102">Свойство Field2.SourceField (DAO)</span><span class="sxs-lookup"><span data-stu-id="a9b41-102">Field2.SourceField property (DAO)</span></span>


<span data-ttu-id="a9b41-103">**Применимо к**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="a9b41-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="a9b41-104">Возвращает значение, указывающее имя поля, который является оригинального источника данных для объекта **поле2** .</span><span class="sxs-lookup"><span data-stu-id="a9b41-104">Returns a value that indicates the name of the field that is the original source of the data for a **Field2** object.</span></span> <span data-ttu-id="a9b41-105">Только для чтения, **String**.</span><span class="sxs-lookup"><span data-stu-id="a9b41-105">Read-only **String**.</span></span>

## <a name="syntax"></a><span data-ttu-id="a9b41-106">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="a9b41-106">Syntax</span></span>

<span data-ttu-id="a9b41-107">*выражение* . SourceField</span><span class="sxs-lookup"><span data-stu-id="a9b41-107">*expression* .SourceField</span></span>

<span data-ttu-id="a9b41-108">*выражение* Переменная, которая представляет собой объект- **поле2** .</span><span class="sxs-lookup"><span data-stu-id="a9b41-108">*expression* A variable that represents a **Field2** object.</span></span>

## <a name="remarks"></a><span data-ttu-id="a9b41-109">Примечания</span><span class="sxs-lookup"><span data-stu-id="a9b41-109">Remarks</span></span>

<span data-ttu-id="a9b41-110">Для объекта **поле2** использование свойств **SourceField** и **Таблица** зависит от объекта, который содержит коллекцию **полей** , добавляется объект **поле2** , как показано в следующей таблице.</span><span class="sxs-lookup"><span data-stu-id="a9b41-110">For a **Field2** object, use of the **SourceField** and **SourceTable** properties depends on the object that contains the **Fields** collection that the **Field2** object is appended to, as shown in the following table.</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="a9b41-111">Объект, добавляемый в конец</span><span class="sxs-lookup"><span data-stu-id="a9b41-111">Object appended to</span></span></p></th>
<th><p><span data-ttu-id="a9b41-112">Применение</span><span class="sxs-lookup"><span data-stu-id="a9b41-112">Usage</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="a9b41-113"><strong>Индекс</strong></span><span class="sxs-lookup"><span data-stu-id="a9b41-113"><strong>Index</strong></span></span></p></td>
<td><p><span data-ttu-id="a9b41-114">Не поддерживается</span><span class="sxs-lookup"><span data-stu-id="a9b41-114">Not supported</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="a9b41-115"><strong>QueryDef</strong></span><span class="sxs-lookup"><span data-stu-id="a9b41-115"><strong>QueryDef</strong></span></span></p></td>
<td><p><span data-ttu-id="a9b41-116">Только для чтения</span><span class="sxs-lookup"><span data-stu-id="a9b41-116">Read-only</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="a9b41-117"><strong>Набор записей</strong></span><span class="sxs-lookup"><span data-stu-id="a9b41-117"><strong>Recordset</strong></span></span></p></td>
<td><p><span data-ttu-id="a9b41-118">Только для чтения</span><span class="sxs-lookup"><span data-stu-id="a9b41-118">Read-only</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="a9b41-119"><strong>Связь</strong></span><span class="sxs-lookup"><span data-stu-id="a9b41-119"><strong>Relation</strong></span></span></p></td>
<td><p><span data-ttu-id="a9b41-120">Не поддерживается</span><span class="sxs-lookup"><span data-stu-id="a9b41-120">Not supported</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="a9b41-121"><strong>TableDef</strong></span><span class="sxs-lookup"><span data-stu-id="a9b41-121"><strong>TableDef</strong></span></span></p></td>
<td><p><span data-ttu-id="a9b41-122">Только для чтения</span><span class="sxs-lookup"><span data-stu-id="a9b41-122">Read-only</span></span></p></td>
</tr>
</tbody>
</table>


<span data-ttu-id="a9b41-123">Эти свойства указывают исходные имена полей и таблиц, связанной с объектом **поле2** .</span><span class="sxs-lookup"><span data-stu-id="a9b41-123">These properties indicate the original field and table names associated with a **Field2** object.</span></span> <span data-ttu-id="a9b41-124">Например можно использовать эти свойства для определения исходного источника данных в поле запроса, имя которого не связано с имя поля в таблице.</span><span class="sxs-lookup"><span data-stu-id="a9b41-124">For example, you could use these properties to determine the original source of the data in a query field whose name is unrelated to the name of the field in the underlying table.</span></span>

