---
title: The Limits of a Recordset
TOCTitle: The Limits of a Recordset
ms:assetid: 51e27c95-e0c3-7fdc-ac11-891553620376
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249266(v=office.15)
ms:contentKeyID: 48544833
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: 0d0da48080b64e43cc39b9567275e1a8755a8881
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32314115"
---
# <a name="limits-of-a-recordset"></a><span data-ttu-id="23fb3-102">Ограничения набора записей</span><span class="sxs-lookup"><span data-stu-id="23fb3-102">Limits of a Recordset</span></span>


<span data-ttu-id="23fb3-103">**Область применения**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="23fb3-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="23fb3-104">Используйте свойства **BOF** и **EOF,** чтобы определить, содержит ли объект **Recordset** записи или выходите за пределы объекта **Recordset** при переходе от записи к записи.</span><span class="sxs-lookup"><span data-stu-id="23fb3-104">Use the **BOF** and **EOF** properties to determine whether a **Recordset** object contains records or whether you've gone beyond the limits of a **Recordset** object when you move from record to record.</span></span> <span data-ttu-id="23fb3-105">Думайте **о BOF** и **EOF** как "дозорные" записи, которые находятся в начале и конце **recordset**.</span><span class="sxs-lookup"><span data-stu-id="23fb3-105">Think of **BOF** and **EOF** as "phantom" records that are positioned at the beginning and end of the **Recordset**.</span></span> <span data-ttu-id="23fb3-106">На основе примера **recordset** из [изучения данных](chapter-3-examining-data.md)он будет выглядеть так:</span><span class="sxs-lookup"><span data-stu-id="23fb3-106">Building on the sample **Recordset** from [Examining Data](chapter-3-examining-data.md), it would now look like this:</span></span>

<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="23fb3-107">ProductID</span><span class="sxs-lookup"><span data-stu-id="23fb3-107">ProductID</span></span></p></th>
<th><p><span data-ttu-id="23fb3-108">ProductName</span><span class="sxs-lookup"><span data-stu-id="23fb3-108">ProductName</span></span></p></th>
<th><p><span data-ttu-id="23fb3-109">UnitPrice</span><span class="sxs-lookup"><span data-stu-id="23fb3-109">UnitPrice</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="23fb3-110">BOF</span><span class="sxs-lookup"><span data-stu-id="23fb3-110">BOF</span></span></p></td>
<td><p><br />
</p></td>
<td><p><br />
</p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="23fb3-111">7 </span><span class="sxs-lookup"><span data-stu-id="23fb3-111">7</span></span></p></td>
<td><p><span data-ttu-id="23fb3-112">Органичное замеченное "По-разное" Боба</span><span class="sxs-lookup"><span data-stu-id="23fb3-112">Uncle Bob's Organic Dried Pears</span></span></p></td>
<td><p><span data-ttu-id="23fb3-113">30.0000</span><span class="sxs-lookup"><span data-stu-id="23fb3-113">30.0000</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="23fb3-114">14 </span><span class="sxs-lookup"><span data-stu-id="23fb3-114">14</span></span></p></td>
<td><p><span data-ttu-id="23fb3-115">Тофу</span><span class="sxs-lookup"><span data-stu-id="23fb3-115">Tofu</span></span></p></td>
<td><p><span data-ttu-id="23fb3-116">23.2500</span><span class="sxs-lookup"><span data-stu-id="23fb3-116">23.2500</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="23fb3-117">28</span><span class="sxs-lookup"><span data-stu-id="23fb3-117">28</span></span></p></td>
<td><p><span data-ttu-id="23fb3-118">Rssle Sauerkraut</span><span class="sxs-lookup"><span data-stu-id="23fb3-118">Rssle Sauerkraut</span></span></p></td>
<td><p><span data-ttu-id="23fb3-119">45.6000</span><span class="sxs-lookup"><span data-stu-id="23fb3-119">45.6000</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="23fb3-120">51</span><span class="sxs-lookup"><span data-stu-id="23fb3-120">51</span></span></p></td>
<td><p><span data-ttu-id="23fb3-121">Manjimup : Apples</span><span class="sxs-lookup"><span data-stu-id="23fb3-121">Manjimup Dried Apples</span></span></p></td>
<td><p><span data-ttu-id="23fb3-122">53.0000</span><span class="sxs-lookup"><span data-stu-id="23fb3-122">53.0000</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="23fb3-123">74</span><span class="sxs-lookup"><span data-stu-id="23fb3-123">74</span></span></p></td>
<td><p><span data-ttu-id="23fb3-124">Longlife Tofu</span><span class="sxs-lookup"><span data-stu-id="23fb3-124">Longlife Tofu</span></span></p></td>
<td><p><span data-ttu-id="23fb3-125">10.0000</span><span class="sxs-lookup"><span data-stu-id="23fb3-125">10.0000</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="23fb3-126">EOF</span><span class="sxs-lookup"><span data-stu-id="23fb3-126">EOF</span></span></p></td>
<td><p><br />
</p></td>
<td><p><br />
</p></td>
</tr>
</tbody>
</table>


<span data-ttu-id="23fb3-127">Свойство **BOF** возвращает true (-1), если текущая позиция записи находится перед первой записью, и **False** (0), если текущая запись находится в первой записи или после нее. </span><span class="sxs-lookup"><span data-stu-id="23fb3-127">The **BOF** property returns **True** (-1) if the current record position is before the first record and **False** (0) if the current record position is on or after the first record.</span></span>

<span data-ttu-id="23fb3-128">Свойство **EOF** возвращает  true, если текущая позиция записи находится после последней записи, и **False,** если текущая запись находится в последней записи или до нее.</span><span class="sxs-lookup"><span data-stu-id="23fb3-128">The **EOF** property returns **True** if the current record position is after the last record and **False** if the current record position is on or before the last record.</span></span>

<span data-ttu-id="23fb3-129">Если свойство **BOF или** **EOF** имеет **true,** текущая запись не существует, как показано в следующем коде:</span><span class="sxs-lookup"><span data-stu-id="23fb3-129">If either the **BOF** or **EOF** property is **True**, there is no current record, as shown in the following code:</span></span>

```vb 
 
If oRs.BOF And oRs.EOF Then 
 ' Command returned no records. 
End If 
```

<span data-ttu-id="23fb3-130">Если открыть объект **Recordset** без записей, свойства **BOF** и **EOF** будут одновременно заданы как true, так и значение свойства  **RecordCount** объекта **Recordset** зависит от типа курсора.</span><span class="sxs-lookup"><span data-stu-id="23fb3-130">If you open a **Recordset** object containing no records, the **BOF** and **EOF** properties are both set to **True** and the value of the **Recordset** object's **RecordCount** property setting depends on the cursor type.</span></span> <span data-ttu-id="23fb3-131">Для динамических курсоров возвращается -1 **(CursorType**  =  **adOpenDynamic),** а для других — 0.</span><span class="sxs-lookup"><span data-stu-id="23fb3-131">-1 will be returned for dynamic cursors (**CursorType** = **adOpenDynamic**) and 0 will be returned for other cursors.</span></span>

<span data-ttu-id="23fb3-132">Когда вы открываете объект **Recordset,** содержащий хотя бы одну запись, первая запись является текущей записью, а свойства **BOF** и **EOF** — **False.**</span><span class="sxs-lookup"><span data-stu-id="23fb3-132">When you open a **Recordset** object that contains at least one record, the first record is the current record and the **BOF** and **EOF** properties are **False**.</span></span>

<span data-ttu-id="23fb3-133">При удалении последней оставшейся записи в **объекте Recordset** курсор остается в неустановленном состоянии.</span><span class="sxs-lookup"><span data-stu-id="23fb3-133">If you delete the last remaining record in the **Recordset** object, the cursor is left in an indeterminate state.</span></span> <span data-ttu-id="23fb3-134">Свойства **BOF** и **EOF** могут оставаться **false,** пока вы не попытались изменить положение текущей записи в зависимости от поставщика.</span><span class="sxs-lookup"><span data-stu-id="23fb3-134">The **BOF** and **EOF** properties may remain **False** until you attempt to reposition the current record, depending upon the provider.</span></span>

