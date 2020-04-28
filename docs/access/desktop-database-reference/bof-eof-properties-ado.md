---
title: BOF, свойства EOF (ADO)
TOCTitle: BOF, EOF properties (ADO)
ms:assetid: f797e140-5572-1a4d-9afc-285f6a3868a8
ms:mtpsurl: https://msdn.microsoft.com/library/JJ250260(v=office.15)
ms:contentKeyID: 48548768
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: d36a65ce8a6808f2128749bd7fbc6e468acbd279
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32296789"
---
# <a name="bof-eof-properties-ado"></a><span data-ttu-id="94667-102">BOF, свойства EOF (ADO)</span><span class="sxs-lookup"><span data-stu-id="94667-102">BOF, EOF properties (ADO)</span></span>


<span data-ttu-id="94667-103">**Область применения**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="94667-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="94667-104">**BOF** — указывает, что положение текущей записи находится перед первой записью в объекте [Recordset](recordset-object-ado.md) .</span><span class="sxs-lookup"><span data-stu-id="94667-104">**BOF** — Indicates that the current record position is before the first record in a [Recordset](recordset-object-ado.md) object.</span></span>

<span data-ttu-id="94667-105">**EOF** — указывает, что положение текущей записи находится после последней записи в объекте **Recordset** .</span><span class="sxs-lookup"><span data-stu-id="94667-105">**EOF** — Indicates that the current record position is after the last record in a **Recordset** object.</span></span>

## <a name="return-value"></a><span data-ttu-id="94667-106">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="94667-106">Return value</span></span>

<span data-ttu-id="94667-107">Свойства **BOF** и **EOF** возвращают **логические** значения.</span><span class="sxs-lookup"><span data-stu-id="94667-107">The **BOF** and **EOF** properties return **Boolean** values.</span></span>

## <a name="remarks"></a><span data-ttu-id="94667-108">Примечания</span><span class="sxs-lookup"><span data-stu-id="94667-108">Remarks</span></span>

<span data-ttu-id="94667-109">Используйте свойства **BOF** и **EOF** , чтобы определить, содержит ли объект **Recordset** записи или вы не превысили ограничения объекта **Recordset** при переходе с записи на запись.</span><span class="sxs-lookup"><span data-stu-id="94667-109">Use the **BOF** and **EOF** properties to determine whether a **Recordset** object contains records or whether you've gone beyond the limits of a **Recordset** object when you move from record to record.</span></span>

<span data-ttu-id="94667-110">Свойство **BOF** возвращает **значение true** (-1), если положение текущей записи находится перед первой записью, и **false** (0), если текущая позиция записи находится в или после первой записи.</span><span class="sxs-lookup"><span data-stu-id="94667-110">The **BOF** property returns **True** (-1) if the current record position is before the first record and **False** (0) if the current record position is on or after the first record.</span></span>

<span data-ttu-id="94667-111">Свойство **EOF** возвращает **значение true** , если текущая позиция записи находится после последней записи, и **значение false** , если текущая позиция записи находится в или до последней записи.</span><span class="sxs-lookup"><span data-stu-id="94667-111">The **EOF** property returns **True** if the current record position is after the last record and **False** if the current record position is on or before the last record.</span></span>

<span data-ttu-id="94667-112">Если любое из свойств **BOF** или **EOF** имеет значение **True**, то текущей записи нет.</span><span class="sxs-lookup"><span data-stu-id="94667-112">If either the **BOF** or **EOF** property is **True**, there is no current record.</span></span>

<span data-ttu-id="94667-113">При открытии объекта **Recordset** , не содержащего записей, свойству **BOF** и **EOF** присваивается **значение true** (для получения дополнительных сведений об этом состоянии объекта **Recordset**см. свойство [RecordCount](recordcount-property-ado.md) ).</span><span class="sxs-lookup"><span data-stu-id="94667-113">If you open a **Recordset** object containing no records, the **BOF** and **EOF** properties are set to **True** (see the [RecordCount](recordcount-property-ado.md) property for more information about this state of a **Recordset**).</span></span> <span data-ttu-id="94667-114">При открытии объекта **Recordset** , содержащего по крайней мере одну запись, первая запись является текущей, а свойство **BOF** и **EOF** имеет **значение false**.</span><span class="sxs-lookup"><span data-stu-id="94667-114">When you open a **Recordset** object that contains at least one record, the first record is the current record and the **BOF** and **EOF** properties are **False**.</span></span>

<span data-ttu-id="94667-115">Если удалить последнюю оставшуюся запись в объекте **Recordset**, свойства **BOF** и **EOF** могут по-прежнему иметь значение **False**, пока вы не попытаетесь изменить позицию текущей записи.</span><span class="sxs-lookup"><span data-stu-id="94667-115">If you delete the last remaining record in the **Recordset** object, the **BOF** and **EOF** properties may remain **False** until you attempt to reposition the current record.</span></span>

<span data-ttu-id="94667-116">В этой таблице показано, какие методы **Move** разрешены с различными сочетаниями свойств **BOF** и **EOF** .</span><span class="sxs-lookup"><span data-stu-id="94667-116">This table shows which **Move** methods are allowed with different combinations of the **BOF** and **EOF** properties.</span></span>

<table>
<colgroup>
<col style="width: 20%" />
<col style="width: 20%" />
<col style="width: 20%" />
<col style="width: 20%" />
<col style="width: 20%" />
</colgroup>
<thead>
<tr class="header">
<th><p></p></th>
<th><p><span data-ttu-id="94667-117">MoveFirst,</span><span class="sxs-lookup"><span data-stu-id="94667-117">MoveFirst,</span></span><br />
<span data-ttu-id="94667-118">MoveLast</span><span class="sxs-lookup"><span data-stu-id="94667-118">MoveLast</span></span></p></th>
<th><p><span data-ttu-id="94667-119">MovePrevious,</span><span class="sxs-lookup"><span data-stu-id="94667-119">MovePrevious,</span></span><br />
<span data-ttu-id="94667-120">Move &lt; 0</span><span class="sxs-lookup"><span data-stu-id="94667-120">Move &lt; 0</span></span></p></th>
<th><p><br />
<span data-ttu-id="94667-121">Move 0</span><span class="sxs-lookup"><span data-stu-id="94667-121">Move 0</span></span></p></th>
<th><p><span data-ttu-id="94667-122">MoveNext,</span><span class="sxs-lookup"><span data-stu-id="94667-122">MoveNext,</span></span><br />
<span data-ttu-id="94667-123">Move &gt; 0</span><span class="sxs-lookup"><span data-stu-id="94667-123">Move &gt; 0</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="94667-124"><strong>BOF=True,</strong></span><span class="sxs-lookup"><span data-stu-id="94667-124"><strong>BOF=True,</strong></span></span><br /><span data-ttu-id="94667-125">
<strong>EOF=False</strong></span><span class="sxs-lookup"><span data-stu-id="94667-125">
<strong>EOF=False</strong></span></span></p></td>
<td><p><span data-ttu-id="94667-126">Разрешено</span><span class="sxs-lookup"><span data-stu-id="94667-126">Allowed</span></span></p></td>
<td><p><span data-ttu-id="94667-127">Ошибка</span><span class="sxs-lookup"><span data-stu-id="94667-127">Error</span></span></p></td>
<td><p><span data-ttu-id="94667-128">Ошибка</span><span class="sxs-lookup"><span data-stu-id="94667-128">Error</span></span></p></td>
<td><p><span data-ttu-id="94667-129">Разрешено</span><span class="sxs-lookup"><span data-stu-id="94667-129">Allowed</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="94667-130"><strong>BOF=False,</strong></span><span class="sxs-lookup"><span data-stu-id="94667-130"><strong>BOF=False,</strong></span></span><br /><span data-ttu-id="94667-131">
<strong>EOF=True</strong></span><span class="sxs-lookup"><span data-stu-id="94667-131">
<strong>EOF=True</strong></span></span></p></td>
<td><p><span data-ttu-id="94667-132">Разрешено</span><span class="sxs-lookup"><span data-stu-id="94667-132">Allowed</span></span></p></td>
<td><p><span data-ttu-id="94667-133">Разрешено</span><span class="sxs-lookup"><span data-stu-id="94667-133">Allowed</span></span></p></td>
<td><p><span data-ttu-id="94667-134">Ошибка</span><span class="sxs-lookup"><span data-stu-id="94667-134">Error</span></span></p></td>
<td><p><span data-ttu-id="94667-135">Ошибка</span><span class="sxs-lookup"><span data-stu-id="94667-135">Error</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="94667-136">Оба свойства имеют значение <strong>True</strong></span><span class="sxs-lookup"><span data-stu-id="94667-136">Both <strong>True</strong></span></span></p></td>
<td><p><span data-ttu-id="94667-137">Ошибка</span><span class="sxs-lookup"><span data-stu-id="94667-137">Error</span></span></p></td>
<td><p><span data-ttu-id="94667-138">Ошибка</span><span class="sxs-lookup"><span data-stu-id="94667-138">Error</span></span></p></td>
<td><p><span data-ttu-id="94667-139">Ошибка</span><span class="sxs-lookup"><span data-stu-id="94667-139">Error</span></span></p></td>
<td><p><span data-ttu-id="94667-140">Ошибка</span><span class="sxs-lookup"><span data-stu-id="94667-140">Error</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="94667-141">Оба свойства имеют значение <strong>False</strong></span><span class="sxs-lookup"><span data-stu-id="94667-141">Both <strong>False</strong></span></span></p></td>
<td><p><span data-ttu-id="94667-142">Разрешено</span><span class="sxs-lookup"><span data-stu-id="94667-142">Allowed</span></span></p></td>
<td><p><span data-ttu-id="94667-143">Разрешено</span><span class="sxs-lookup"><span data-stu-id="94667-143">Allowed</span></span></p></td>
<td><p><span data-ttu-id="94667-144">Разрешено</span><span class="sxs-lookup"><span data-stu-id="94667-144">Allowed</span></span></p></td>
<td><p><span data-ttu-id="94667-145">Разрешено</span><span class="sxs-lookup"><span data-stu-id="94667-145">Allowed</span></span></p></td>
</tr>
</tbody>
</table>


<span data-ttu-id="94667-146">Разрешение метода **Move** не гарантирует, что метод будет успешно искать запись; Это означает, что вызов указанного метода **Move** не приводит к возникновению ошибки.</span><span class="sxs-lookup"><span data-stu-id="94667-146">Allowing a **Move** method doesn't guarantee that the method will successfully locate a record; it only means that calling the specified **Move** method won't generate an error.</span></span>

<span data-ttu-id="94667-147">В приведенной ниже таблице показано, что происходит с параметрами свойств **BOF** и **EOF** при вызове различных методов **Move** , но которые не могут успешно найти запись.</span><span class="sxs-lookup"><span data-stu-id="94667-147">The following table shows what happens to the **BOF** and **EOF** property settings when you call various **Move** methods but are unable to successfully locate a record.</span></span>

<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th><p></p></th>
<th><p><span data-ttu-id="94667-148">BOF</span><span class="sxs-lookup"><span data-stu-id="94667-148">BOF</span></span></p></th>
<th><p><span data-ttu-id="94667-149">EOF</span><span class="sxs-lookup"><span data-stu-id="94667-149">EOF</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="94667-150"><strong>MoveFirst</strong>, <strong>MoveLast</strong></span><span class="sxs-lookup"><span data-stu-id="94667-150"><strong>MoveFirst</strong>, <strong>MoveLast</strong></span></span></p></td>
<td><p><span data-ttu-id="94667-151">Задано <strong>значение true</strong></span><span class="sxs-lookup"><span data-stu-id="94667-151">Set to <strong>True</strong></span></span></p></td>
<td><p><span data-ttu-id="94667-152">Задано <strong>значение true</strong></span><span class="sxs-lookup"><span data-stu-id="94667-152">Set to <strong>True</strong></span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="94667-153"><strong>Move</strong> 0</span><span class="sxs-lookup"><span data-stu-id="94667-153"><strong>Move</strong> 0</span></span></p></td>
<td><p><span data-ttu-id="94667-154">Без изменений</span><span class="sxs-lookup"><span data-stu-id="94667-154">No change</span></span></p></td>
<td><p><span data-ttu-id="94667-155">Без изменений</span><span class="sxs-lookup"><span data-stu-id="94667-155">No change</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="94667-156"><strong>MovePrevious</strong>, <strong>Move</strong> &lt; 0</span><span class="sxs-lookup"><span data-stu-id="94667-156"><strong>MovePrevious</strong>, <strong>Move</strong> &lt; 0</span></span></p></td>
<td><p><span data-ttu-id="94667-157">Задано <strong>значение true</strong></span><span class="sxs-lookup"><span data-stu-id="94667-157">Set to <strong>True</strong></span></span></p></td>
<td><p><span data-ttu-id="94667-158">Без изменений</span><span class="sxs-lookup"><span data-stu-id="94667-158">No change</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="94667-159"><strong>MoveNext</strong>, <strong>Move</strong> &gt; 0</span><span class="sxs-lookup"><span data-stu-id="94667-159"><strong>MoveNext</strong>, <strong>Move</strong> &gt; 0</span></span></p></td>
<td><p><span data-ttu-id="94667-160">Без изменений</span><span class="sxs-lookup"><span data-stu-id="94667-160">No change</span></span></p></td>
<td><p><span data-ttu-id="94667-161">Задано <strong>значение true</strong></span><span class="sxs-lookup"><span data-stu-id="94667-161">Set to <strong>True</strong></span></span></p></td>
</tr>
</tbody>
</table>

