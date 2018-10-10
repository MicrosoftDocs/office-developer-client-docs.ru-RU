---
title: Field2.SourceTable Property (DAO)
TOCTitle: SourceTable Property
ms:assetid: 24d2fdda-d924-d95e-8458-063dd1d36d5d
ms:mtpsurl: https://msdn.microsoft.com/library/Ff191839(v=office.15)
ms:contentKeyID: 48543768
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: af404f3b741445ef434c4f3266f89aa318e13ad2
ms.sourcegitcommit: 19aca09c5812cfb98b68b5d4604dcaa814479df7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/09/2018
ms.locfileid: "25481313"
---
# <a name="field2sourcetable-property-dao"></a><span data-ttu-id="07c81-102">Field2.SourceTable Property (DAO)</span><span class="sxs-lookup"><span data-stu-id="07c81-102">Field2.SourceTable Property (DAO)</span></span>


<span data-ttu-id="07c81-103">**Применимо к**: Access 2013 | Office 2013</span><span class="sxs-lookup"><span data-stu-id="07c81-103">**Applies to**: Access 2013 | Office 2013</span></span>

<span data-ttu-id="07c81-104">Возвращает значение, указывающее имя таблицы, который является оригинального источника данных для объекта **поле2** .</span><span class="sxs-lookup"><span data-stu-id="07c81-104">Returns a value that indicates the name of the table that is the original source of the data for a **Field2** object.</span></span> <span data-ttu-id="07c81-105">Только для чтения, **String**.</span><span class="sxs-lookup"><span data-stu-id="07c81-105">Read-only **String**.</span></span>

## <a name="syntax"></a><span data-ttu-id="07c81-106">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="07c81-106">Syntax</span></span>

<span data-ttu-id="07c81-107">*выражение* . Таблица</span><span class="sxs-lookup"><span data-stu-id="07c81-107">*expression* .SourceTable</span></span>

<span data-ttu-id="07c81-108">*выражение* Переменная, которая представляет собой объект- **поле2** .</span><span class="sxs-lookup"><span data-stu-id="07c81-108">*expression* A variable that represents a **Field2** object.</span></span>

## <a name="remarks"></a><span data-ttu-id="07c81-109">Замечания</span><span class="sxs-lookup"><span data-stu-id="07c81-109">Remarks</span></span>

<span data-ttu-id="07c81-110">Для объекта **поле2** использование свойств **SourceField** и **Таблица** зависит от объекта, который содержит коллекцию **полей** , добавляется объект **поле2** , как показано в следующей таблице.</span><span class="sxs-lookup"><span data-stu-id="07c81-110">For a **Field2** object, use of the **SourceField** and **SourceTable** properties depends on the object that contains the **Fields** collection that the **Field2** object is appended to, as shown in the following table.</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="07c81-111">Объект, добавляемый в конец</span><span class="sxs-lookup"><span data-stu-id="07c81-111">Object appended to</span></span></p></th>
<th><p><span data-ttu-id="07c81-112">Применение</span><span class="sxs-lookup"><span data-stu-id="07c81-112">Usage</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="07c81-113"><strong>Индекс</strong></span><span class="sxs-lookup"><span data-stu-id="07c81-113"><strong>Index</strong></span></span></p></td>
<td><p><span data-ttu-id="07c81-114">Не поддерживается</span><span class="sxs-lookup"><span data-stu-id="07c81-114">Not supported</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="07c81-115"><strong>QueryDef</strong></span><span class="sxs-lookup"><span data-stu-id="07c81-115"><strong>QueryDef</strong></span></span></p></td>
<td><p><span data-ttu-id="07c81-116">Только для чтения</span><span class="sxs-lookup"><span data-stu-id="07c81-116">Read-only</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="07c81-117"><strong>Набор записей</strong></span><span class="sxs-lookup"><span data-stu-id="07c81-117"><strong>Recordset</strong></span></span></p></td>
<td><p><span data-ttu-id="07c81-118">Только для чтения</span><span class="sxs-lookup"><span data-stu-id="07c81-118">Read-only</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="07c81-119"><strong>Связь</strong></span><span class="sxs-lookup"><span data-stu-id="07c81-119"><strong>Relation</strong></span></span></p></td>
<td><p><span data-ttu-id="07c81-120">Не поддерживается</span><span class="sxs-lookup"><span data-stu-id="07c81-120">Not supported</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="07c81-121"><strong>TableDef</strong></span><span class="sxs-lookup"><span data-stu-id="07c81-121"><strong>TableDef</strong></span></span></p></td>
<td><p><span data-ttu-id="07c81-122">Только для чтения</span><span class="sxs-lookup"><span data-stu-id="07c81-122">Read-only</span></span></p></td>
</tr>
</tbody>
</table>


<span data-ttu-id="07c81-123">Эти свойства указывают исходные имена полей и таблиц, связанной с объектом **поле2** .</span><span class="sxs-lookup"><span data-stu-id="07c81-123">These properties indicate the original field and table names associated with a **Field2** object.</span></span> <span data-ttu-id="07c81-124">Например можно использовать эти свойства для определения исходного источника данных в поле запроса, имя которого не связано с имя поля в таблице.</span><span class="sxs-lookup"><span data-stu-id="07c81-124">For example, you could use these properties to determine the original source of the data in a query field whose name is unrelated to the name of the field in the underlying table.</span></span>


> [!NOTE]
> <P><span data-ttu-id="07c81-125">Свойство <STRONG>Таблица</STRONG> не возвращает имя удобной для восприятия таблицы при использовании объекта <STRONG>поле2</STRONG> в коллекции <STRONG>полей</STRONG> объекта <STRONG>набора записей</STRONG> в таблице тип.</span><span class="sxs-lookup"><span data-stu-id="07c81-125">The <STRONG>SourceTable</STRONG> property will not return a meaningful table name if used on a <STRONG>Field2</STRONG> object in the <STRONG>Fields</STRONG> collection of a table-type <STRONG>Recordset</STRONG> object.</span></span></P>


