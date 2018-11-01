---
title: Field.SourceTable Property (DAO)
TOCTitle: SourceTable Property
ms:assetid: 9564ea1c-eafd-0b72-fd68-d88fcc3ea189
ms:mtpsurl: https://msdn.microsoft.com/library/Ff197694(v=office.15)
ms:contentKeyID: 48546429
ms.date: 09/18/2015
mtps_version: v=office.15
f1_keywords:
- dao360.chm1052900
f1_categories:
- Office.Version=v15
ms.openlocfilehash: 1a11544808cfb897a359a5e170332ba23e25ceae
ms.sourcegitcommit: c557bbcccf37a6011f89aae1ddd399dfe549d087
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/31/2018
ms.locfileid: "25888043"
---
# <a name="fieldsourcetable-property-dao"></a><span data-ttu-id="90493-102">Field.SourceTable Property (DAO)</span><span class="sxs-lookup"><span data-stu-id="90493-102">Field.SourceTable Property (DAO)</span></span>


<span data-ttu-id="90493-103">**Применимо к**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="90493-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="90493-104">Возвращает значение, указывающее имя таблицы, который является оригинального источника данных для объекта **поля** .</span><span class="sxs-lookup"><span data-stu-id="90493-104">Returns a value that indicates the name of the table that is the original source of the data for a **Field** object.</span></span> <span data-ttu-id="90493-105">Только для чтения, **String**.</span><span class="sxs-lookup"><span data-stu-id="90493-105">Read-only **String**.</span></span>

## <a name="syntax"></a><span data-ttu-id="90493-106">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="90493-106">Syntax</span></span>

<span data-ttu-id="90493-107">*выражение* . Таблица</span><span class="sxs-lookup"><span data-stu-id="90493-107">*expression* .SourceTable</span></span>

<span data-ttu-id="90493-108">*выражение* Переменная, которая представляет собой объект- **поля** .</span><span class="sxs-lookup"><span data-stu-id="90493-108">*expression* A variable that represents a **Field** object.</span></span>

## <a name="remarks"></a><span data-ttu-id="90493-109">Замечания</span><span class="sxs-lookup"><span data-stu-id="90493-109">Remarks</span></span>

<span data-ttu-id="90493-110">Для объекта **поля** использование свойств **SourceField** и **Таблица** зависит от объекта, который содержит коллекцию **полей** , используется в качестве объекта **поля** "Кому", как показано в следующей таблице.</span><span class="sxs-lookup"><span data-stu-id="90493-110">For a **Field** object, use of the **SourceField** and **SourceTable** properties depends on the object that contains the **Fields** collection that the **Field** object is appended to, as shown in the following table.</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="90493-111">Объект, добавляемый в конец</span><span class="sxs-lookup"><span data-stu-id="90493-111">Object appended to</span></span></p></th>
<th><p><span data-ttu-id="90493-112">Применение</span><span class="sxs-lookup"><span data-stu-id="90493-112">Usage</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="90493-113"><strong>Индекс</strong></span><span class="sxs-lookup"><span data-stu-id="90493-113"><strong>Index</strong></span></span></p></td>
<td><p><span data-ttu-id="90493-114">Не поддерживается</span><span class="sxs-lookup"><span data-stu-id="90493-114">Not supported</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="90493-115"><strong>QueryDef</strong></span><span class="sxs-lookup"><span data-stu-id="90493-115"><strong>QueryDef</strong></span></span></p></td>
<td><p><span data-ttu-id="90493-116">Только для чтения</span><span class="sxs-lookup"><span data-stu-id="90493-116">Read-only</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="90493-117"><strong>Набор записей</strong></span><span class="sxs-lookup"><span data-stu-id="90493-117"><strong>Recordset</strong></span></span></p></td>
<td><p><span data-ttu-id="90493-118">Только для чтения</span><span class="sxs-lookup"><span data-stu-id="90493-118">Read-only</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="90493-119"><strong>Связь</strong></span><span class="sxs-lookup"><span data-stu-id="90493-119"><strong>Relation</strong></span></span></p></td>
<td><p><span data-ttu-id="90493-120">Не поддерживается</span><span class="sxs-lookup"><span data-stu-id="90493-120">Not supported</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="90493-121"><strong>TableDef</strong></span><span class="sxs-lookup"><span data-stu-id="90493-121"><strong>TableDef</strong></span></span></p></td>
<td><p><span data-ttu-id="90493-122">Только для чтения</span><span class="sxs-lookup"><span data-stu-id="90493-122">Read-only</span></span></p></td>
</tr>
</tbody>
</table>


<span data-ttu-id="90493-123">Эти свойства указывают исходные имена полей и таблиц, связанной с объектом **поля** .</span><span class="sxs-lookup"><span data-stu-id="90493-123">These properties indicate the original field and table names associated with a **Field** object.</span></span> <span data-ttu-id="90493-124">Например можно использовать эти свойства для определения исходного источника данных в поле запроса, имя которого не связано с имя поля в таблице.</span><span class="sxs-lookup"><span data-stu-id="90493-124">For example, you could use these properties to determine the original source of the data in a query field whose name is unrelated to the name of the field in the underlying table.</span></span>


> [!NOTE]
> <P><span data-ttu-id="90493-125">Свойство <STRONG>Таблица</STRONG> не возвращает имя удобной для восприятия таблицы при использовании объекта <STRONG>поля</STRONG> в коллекции <STRONG>полей</STRONG> объекта <STRONG>набора записей</STRONG> в таблице тип.</span><span class="sxs-lookup"><span data-stu-id="90493-125">The <STRONG>SourceTable</STRONG> property will not return a meaningful table name if used on a <STRONG>Field</STRONG> object in the <STRONG>Fields</STRONG> collection of a table-type <STRONG>Recordset</STRONG> object.</span></span></P>


