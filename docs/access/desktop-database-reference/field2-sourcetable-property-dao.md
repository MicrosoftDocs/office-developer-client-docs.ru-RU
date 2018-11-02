---
title: Свойство Field2.SourceTable (DAO)
TOCTitle: SourceTable Property
ms:assetid: 24d2fdda-d924-d95e-8458-063dd1d36d5d
ms:mtpsurl: https://msdn.microsoft.com/library/Ff191839(v=office.15)
ms:contentKeyID: 48543768
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: fbde7aa9785e4e875f96569884e7f6e45743f2bb
ms.sourcegitcommit: d7248f803002b31cf7fc561b03530199a9b0a8fd
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 11/02/2018
ms.locfileid: "25925585"
---
# <a name="field2sourcetable-property-dao"></a><span data-ttu-id="5b591-102">Свойство Field2.SourceTable (DAO)</span><span class="sxs-lookup"><span data-stu-id="5b591-102">Field2.SourceTable property (DAO)</span></span>


<span data-ttu-id="5b591-103">**Применимо к**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="5b591-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="5b591-104">Возвращает значение, указывающее имя таблицы, который является оригинального источника данных для объекта **поле2** .</span><span class="sxs-lookup"><span data-stu-id="5b591-104">Returns a value that indicates the name of the table that is the original source of the data for a **Field2** object.</span></span> <span data-ttu-id="5b591-105">Только для чтения, **String**.</span><span class="sxs-lookup"><span data-stu-id="5b591-105">Read-only **String**.</span></span>

## <a name="syntax"></a><span data-ttu-id="5b591-106">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="5b591-106">Syntax</span></span>

<span data-ttu-id="5b591-107">*выражение* . Таблица</span><span class="sxs-lookup"><span data-stu-id="5b591-107">*expression* .SourceTable</span></span>

<span data-ttu-id="5b591-108">*выражение* Переменная, которая представляет собой объект- **поле2** .</span><span class="sxs-lookup"><span data-stu-id="5b591-108">*expression* A variable that represents a **Field2** object.</span></span>

## <a name="remarks"></a><span data-ttu-id="5b591-109">Примечания</span><span class="sxs-lookup"><span data-stu-id="5b591-109">Remarks</span></span>

<span data-ttu-id="5b591-110">Для объекта **поле2** использование свойств **SourceField** и **Таблица** зависит от объекта, который содержит коллекцию **полей** , добавляется объект **поле2** , как показано в следующей таблице.</span><span class="sxs-lookup"><span data-stu-id="5b591-110">For a **Field2** object, use of the **SourceField** and **SourceTable** properties depends on the object that contains the **Fields** collection that the **Field2** object is appended to, as shown in the following table.</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="5b591-111">Объект, добавляемый в конец</span><span class="sxs-lookup"><span data-stu-id="5b591-111">Object appended to</span></span></p></th>
<th><p><span data-ttu-id="5b591-112">Применение</span><span class="sxs-lookup"><span data-stu-id="5b591-112">Usage</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="5b591-113"><strong>Индекс</strong></span><span class="sxs-lookup"><span data-stu-id="5b591-113"><strong>Index</strong></span></span></p></td>
<td><p><span data-ttu-id="5b591-114">Не поддерживается</span><span class="sxs-lookup"><span data-stu-id="5b591-114">Not supported</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="5b591-115"><strong>QueryDef</strong></span><span class="sxs-lookup"><span data-stu-id="5b591-115"><strong>QueryDef</strong></span></span></p></td>
<td><p><span data-ttu-id="5b591-116">Только для чтения</span><span class="sxs-lookup"><span data-stu-id="5b591-116">Read-only</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="5b591-117"><strong>Набор записей</strong></span><span class="sxs-lookup"><span data-stu-id="5b591-117"><strong>Recordset</strong></span></span></p></td>
<td><p><span data-ttu-id="5b591-118">Только для чтения</span><span class="sxs-lookup"><span data-stu-id="5b591-118">Read-only</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="5b591-119"><strong>Связь</strong></span><span class="sxs-lookup"><span data-stu-id="5b591-119"><strong>Relation</strong></span></span></p></td>
<td><p><span data-ttu-id="5b591-120">Не поддерживается</span><span class="sxs-lookup"><span data-stu-id="5b591-120">Not supported</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="5b591-121"><strong>TableDef</strong></span><span class="sxs-lookup"><span data-stu-id="5b591-121"><strong>TableDef</strong></span></span></p></td>
<td><p><span data-ttu-id="5b591-122">Только для чтения</span><span class="sxs-lookup"><span data-stu-id="5b591-122">Read-only</span></span></p></td>
</tr>
</tbody>
</table>


<span data-ttu-id="5b591-123">Эти свойства указывают исходные имена полей и таблиц, связанной с объектом **поле2** .</span><span class="sxs-lookup"><span data-stu-id="5b591-123">These properties indicate the original field and table names associated with a **Field2** object.</span></span> <span data-ttu-id="5b591-124">Например можно использовать эти свойства для определения исходного источника данных в поле запроса, имя которого не связано с имя поля в таблице.</span><span class="sxs-lookup"><span data-stu-id="5b591-124">For example, you could use these properties to determine the original source of the data in a query field whose name is unrelated to the name of the field in the underlying table.</span></span>


> [!NOTE]
> <P><span data-ttu-id="5b591-125">Свойство <STRONG>Таблица</STRONG> не возвращает имя удобной для восприятия таблицы при использовании объекта <STRONG>поле2</STRONG> в коллекции <STRONG>полей</STRONG> объекта <STRONG>набора записей</STRONG> в таблице тип.</span><span class="sxs-lookup"><span data-stu-id="5b591-125">The <STRONG>SourceTable</STRONG> property will not return a meaningful table name if used on a <STRONG>Field2</STRONG> object in the <STRONG>Fields</STRONG> collection of a table-type <STRONG>Recordset</STRONG> object.</span></span></P>


