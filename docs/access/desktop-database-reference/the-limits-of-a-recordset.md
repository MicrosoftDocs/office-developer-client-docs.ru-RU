---
title: The Limits of a Recordset
TOCTitle: The Limits of a Recordset
ms:assetid: 51e27c95-e0c3-7fdc-ac11-891553620376
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249266(v=office.15)
ms:contentKeyID: 48544833
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: c5b0f03e135f4e00b3ca9d6be7417bfe0e5047e6
ms.sourcegitcommit: 558d09fad81f8d80b5ad0edd21934fc09c098f2c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 11/03/2018
ms.locfileid: "25946582"
---
# <a name="limits-of-a-recordset"></a><span data-ttu-id="37231-102">Ограничения набора записей</span><span class="sxs-lookup"><span data-stu-id="37231-102">Limits of a Recordset</span></span>


<span data-ttu-id="37231-103">**Применимо к**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="37231-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="37231-104">Используйте свойства **BOF** и **EOF** , чтобы определить, содержит ли объект **набора записей** записей или ли вы уменьшилось за пределы ограничения объекта **набора записей** , при перемещении между записями.</span><span class="sxs-lookup"><span data-stu-id="37231-104">Use the **BOF** and **EOF** properties to determine whether a **Recordset** object contains records or whether you've gone beyond the limits of a **Recordset** object when you move from record to record.</span></span> <span data-ttu-id="37231-105">Считайте **BOF** и **EOF** «фантомных» записей, размещенный в начало и конец **набора записей**.</span><span class="sxs-lookup"><span data-stu-id="37231-105">Think of **BOF** and **EOF** as "phantom" records that are positioned at the beginning and end of the **Recordset**.</span></span> <span data-ttu-id="37231-106">Основываясь на пример **набора записей** на основе [Данных проверки](chapter-3-examining-data.md), она теперь выглядит следующим образом:</span><span class="sxs-lookup"><span data-stu-id="37231-106">Building on the sample **Recordset** from [Examining Data](chapter-3-examining-data.md), it would now look like this:</span></span>

<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="37231-107">ProductID</span><span class="sxs-lookup"><span data-stu-id="37231-107">ProductID</span></span></p></th>
<th><p><span data-ttu-id="37231-108">Имя продукта</span><span class="sxs-lookup"><span data-stu-id="37231-108">ProductName</span></span></p></th>
<th><p><span data-ttu-id="37231-109">Цена</span><span class="sxs-lookup"><span data-stu-id="37231-109">UnitPrice</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="37231-110">BOF</span><span class="sxs-lookup"><span data-stu-id="37231-110">BOF</span></span></p></td>
<td><p><br />
</p></td>
<td><p><br />
</p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="37231-111">7</span><span class="sxs-lookup"><span data-stu-id="37231-111">7</span></span></p></td>
<td><p><span data-ttu-id="37231-112">Боб ячейку органических высохла Груши</span><span class="sxs-lookup"><span data-stu-id="37231-112">Uncle Bob's Organic Dried Pears</span></span></p></td>
<td><p><span data-ttu-id="37231-113">30.0000</span><span class="sxs-lookup"><span data-stu-id="37231-113">30.0000</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="37231-114">14</span><span class="sxs-lookup"><span data-stu-id="37231-114">14</span></span></p></td>
<td><p><span data-ttu-id="37231-115">Диаграмме</span><span class="sxs-lookup"><span data-stu-id="37231-115">Tofu</span></span></p></td>
<td><p><span data-ttu-id="37231-116">23.2500</span><span class="sxs-lookup"><span data-stu-id="37231-116">23.2500</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="37231-117">28</span><span class="sxs-lookup"><span data-stu-id="37231-117">28</span></span></p></td>
<td><p><span data-ttu-id="37231-118">Квашеная капуста Rssle</span><span class="sxs-lookup"><span data-stu-id="37231-118">Rssle Sauerkraut</span></span></p></td>
<td><p><span data-ttu-id="37231-119">45.6000</span><span class="sxs-lookup"><span data-stu-id="37231-119">45.6000</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="37231-120">51</span><span class="sxs-lookup"><span data-stu-id="37231-120">51</span></span></p></td>
<td><p><span data-ttu-id="37231-121">Сушеные "apples"</span><span class="sxs-lookup"><span data-stu-id="37231-121">Manjimup Dried Apples</span></span></p></td>
<td><p><span data-ttu-id="37231-122">53.0000</span><span class="sxs-lookup"><span data-stu-id="37231-122">53.0000</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="37231-123">74</span><span class="sxs-lookup"><span data-stu-id="37231-123">74</span></span></p></td>
<td><p><span data-ttu-id="37231-124">Longlife диаграмме</span><span class="sxs-lookup"><span data-stu-id="37231-124">Longlife Tofu</span></span></p></td>
<td><p><span data-ttu-id="37231-125">10.0000</span><span class="sxs-lookup"><span data-stu-id="37231-125">10.0000</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="37231-126">ФУНКЦИЯ EOF</span><span class="sxs-lookup"><span data-stu-id="37231-126">EOF</span></span></p></td>
<td><p><br />
</p></td>
<td><p><br />
</p></td>
</tr>
</tbody>
</table>


<span data-ttu-id="37231-127">Свойство **BOF** возвращает **значение True** (значение -1) при текущей позиции записи перед первой записи и **значение False** (0) Если в настоящее время записи на или после первой записи.</span><span class="sxs-lookup"><span data-stu-id="37231-127">The **BOF** property returns **True** (-1) if the current record position is before the first record and **False** (0) if the current record position is on or after the first record.</span></span>

<span data-ttu-id="37231-128">Свойство **EOF** возвращает **значение True** , если в настоящее время записи после последней записи и **значение False** , если текущей позиции записи не позднее последней записи.</span><span class="sxs-lookup"><span data-stu-id="37231-128">The **EOF** property returns **True** if the current record position is after the last record and **False** if the current record position is on or before the last record.</span></span>

<span data-ttu-id="37231-129">Если свойство **BOF** или **EOF** имеет **значение True**, отсутствует текущий запись, как показано в следующем коде:</span><span class="sxs-lookup"><span data-stu-id="37231-129">If either the **BOF** or **EOF** property is **True**, there is no current record, as shown in the following code:</span></span>

```vb 
 
If oRs.BOF And oRs.EOF Then 
 ' Command returned no records. 
End If 
```

<span data-ttu-id="37231-130">При открытии объекта **набора записей** , содержащий записи не **BOF** и **EOF** свойства, как значение **True** , так и значения параметра свойства **RecordCount** объекта **набора записей** зависит от типа курсора.</span><span class="sxs-lookup"><span data-stu-id="37231-130">If you open a **Recordset** object containing no records, the **BOF** and **EOF** properties are both set to **True** and the value of the **Recordset** object's **RecordCount** property setting depends on the cursor type.</span></span> <span data-ttu-id="37231-131">-1, будут возвращены для динамических курсоров (**CursorType** = **adOpenDynamic**) и 0 для других курсоров возвращается.</span><span class="sxs-lookup"><span data-stu-id="37231-131">-1 will be returned for dynamic cursors (**CursorType** = **adOpenDynamic**) and 0 will be returned for other cursors.</span></span>

<span data-ttu-id="37231-132">При открытии объекта **набора записей** , который содержит по крайней мере одна запись первая запись является текущей записи и свойства **BOF** и **EOF** — **значение False**.</span><span class="sxs-lookup"><span data-stu-id="37231-132">When you open a **Recordset** object that contains at least one record, the first record is the current record and the **BOF** and **EOF** properties are **False**.</span></span>

<span data-ttu-id="37231-133">При удалении последней оставшиеся записи в объекте **набора записей** , курсор остается в неопределенное состояние.</span><span class="sxs-lookup"><span data-stu-id="37231-133">If you delete the last remaining record in the **Recordset** object, the cursor is left in an indeterminate state.</span></span> <span data-ttu-id="37231-134">Свойства **BOF** и **EOF** может оставаться **значение False** , пока вы пытаетесь изменить положение текущей записи в зависимости от поставщика.</span><span class="sxs-lookup"><span data-stu-id="37231-134">The **BOF** and **EOF** properties may remain **False** until you attempt to reposition the current record, depending upon the provider.</span></span>

