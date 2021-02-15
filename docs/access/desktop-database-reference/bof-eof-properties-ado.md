---
title: BoF, EOF properties (ADO)
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
# <a name="bof-eof-properties-ado"></a><span data-ttu-id="49971-102">BoF, EOF properties (ADO)</span><span class="sxs-lookup"><span data-stu-id="49971-102">BOF, EOF properties (ADO)</span></span>


<span data-ttu-id="49971-103">**Область применения**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="49971-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="49971-104">**BOF** — указывает, что текущая позиция записи находится перед первой записью в [объекте Recordset.](recordset-object-ado.md)</span><span class="sxs-lookup"><span data-stu-id="49971-104">**BOF** — Indicates that the current record position is before the first record in a [Recordset](recordset-object-ado.md) object.</span></span>

<span data-ttu-id="49971-105">**EOF** — указывает, что текущая позиция записи находится после последней записи в **объекте Recordset.**</span><span class="sxs-lookup"><span data-stu-id="49971-105">**EOF** — Indicates that the current record position is after the last record in a **Recordset** object.</span></span>

## <a name="return-value"></a><span data-ttu-id="49971-106">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="49971-106">Return value</span></span>

<span data-ttu-id="49971-107">Свойства **BOF** и **EOF** возвращают **boolean** значения.</span><span class="sxs-lookup"><span data-stu-id="49971-107">The **BOF** and **EOF** properties return **Boolean** values.</span></span>

## <a name="remarks"></a><span data-ttu-id="49971-108">Заметки</span><span class="sxs-lookup"><span data-stu-id="49971-108">Remarks</span></span>

<span data-ttu-id="49971-109">Используйте свойства **BOF** и **EOF,** чтобы определить, содержит ли объект **Recordset** записи или выходите за пределы объекта **Recordset** при переходе от записи к записи.</span><span class="sxs-lookup"><span data-stu-id="49971-109">Use the **BOF** and **EOF** properties to determine whether a **Recordset** object contains records or whether you've gone beyond the limits of a **Recordset** object when you move from record to record.</span></span>

<span data-ttu-id="49971-110">Свойство **BOF** возвращает true (-1), если текущая позиция записи находится перед первой записью, и **False** (0), если текущая запись находится в первой записи или после нее. </span><span class="sxs-lookup"><span data-stu-id="49971-110">The **BOF** property returns **True** (-1) if the current record position is before the first record and **False** (0) if the current record position is on or after the first record.</span></span>

<span data-ttu-id="49971-111">Свойство **EOF** возвращает  true, если текущая позиция записи находится после последней записи, и **False,** если текущая запись находится в последней записи или до нее.</span><span class="sxs-lookup"><span data-stu-id="49971-111">The **EOF** property returns **True** if the current record position is after the last record and **False** if the current record position is on or before the last record.</span></span>

<span data-ttu-id="49971-112">Если любое из свойств **BOF** или **EOF** имеет значение **True**, то текущей записи нет.</span><span class="sxs-lookup"><span data-stu-id="49971-112">If either the **BOF** or **EOF** property is **True**, there is no current record.</span></span>

<span data-ttu-id="49971-113">Если открыть объект  **Recordset** без записей, свойства **BOF** и **EOF** будут заданы как **True** (дополнительные сведения об этом состоянии набора записей см. в свойстве [RecordCount).](recordcount-property-ado.md)</span><span class="sxs-lookup"><span data-stu-id="49971-113">If you open a **Recordset** object containing no records, the **BOF** and **EOF** properties are set to **True** (see the [RecordCount](recordcount-property-ado.md) property for more information about this state of a **Recordset**).</span></span> <span data-ttu-id="49971-114">Когда вы открываете объект **Recordset,** содержащий хотя бы одну запись, первая запись является текущей записью, а свойства **BOF** и **EOF** — **False.**</span><span class="sxs-lookup"><span data-stu-id="49971-114">When you open a **Recordset** object that contains at least one record, the first record is the current record and the **BOF** and **EOF** properties are **False**.</span></span>

<span data-ttu-id="49971-115">Если удалить последнюю оставшуюся запись в объекте **Recordset**, свойства **BOF** и **EOF** могут по-прежнему иметь значение **False**, пока вы не попытаетесь изменить позицию текущей записи.</span><span class="sxs-lookup"><span data-stu-id="49971-115">If you delete the last remaining record in the **Recordset** object, the **BOF** and **EOF** properties may remain **False** until you attempt to reposition the current record.</span></span>

<span data-ttu-id="49971-116">В этой таблице показано, какие методы **Move** разрешены с различными сочетаниями свойств **BOF** и **EOF.**</span><span class="sxs-lookup"><span data-stu-id="49971-116">This table shows which **Move** methods are allowed with different combinations of the **BOF** and **EOF** properties.</span></span>

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
<th><p><span data-ttu-id="49971-117">MoveFirst,</span><span class="sxs-lookup"><span data-stu-id="49971-117">MoveFirst,</span></span><br />
<span data-ttu-id="49971-118">MoveLast</span><span class="sxs-lookup"><span data-stu-id="49971-118">MoveLast</span></span></p></th>
<th><p><span data-ttu-id="49971-119">MovePrevious,</span><span class="sxs-lookup"><span data-stu-id="49971-119">MovePrevious,</span></span><br />
<span data-ttu-id="49971-120">Move &lt; 0</span><span class="sxs-lookup"><span data-stu-id="49971-120">Move &lt; 0</span></span></p></th>
<th><p><br />
<span data-ttu-id="49971-121">Move 0</span><span class="sxs-lookup"><span data-stu-id="49971-121">Move 0</span></span></p></th>
<th><p><span data-ttu-id="49971-122">MoveNext,</span><span class="sxs-lookup"><span data-stu-id="49971-122">MoveNext,</span></span><br />
<span data-ttu-id="49971-123">Move &gt; 0</span><span class="sxs-lookup"><span data-stu-id="49971-123">Move &gt; 0</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="49971-124"><strong>BOF=True,</strong></span><span class="sxs-lookup"><span data-stu-id="49971-124"><strong>BOF=True,</strong></span></span><br /><span data-ttu-id="49971-125">
<strong>EOF=False</strong></span><span class="sxs-lookup"><span data-stu-id="49971-125">
<strong>EOF=False</strong></span></span></p></td>
<td><p><span data-ttu-id="49971-126">Разрешено</span><span class="sxs-lookup"><span data-stu-id="49971-126">Allowed</span></span></p></td>
<td><p><span data-ttu-id="49971-127">Ошибка</span><span class="sxs-lookup"><span data-stu-id="49971-127">Error</span></span></p></td>
<td><p><span data-ttu-id="49971-128">Ошибка</span><span class="sxs-lookup"><span data-stu-id="49971-128">Error</span></span></p></td>
<td><p><span data-ttu-id="49971-129">Разрешено</span><span class="sxs-lookup"><span data-stu-id="49971-129">Allowed</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="49971-130"><strong>BOF=False,</strong></span><span class="sxs-lookup"><span data-stu-id="49971-130"><strong>BOF=False,</strong></span></span><br /><span data-ttu-id="49971-131">
<strong>EOF=True</strong></span><span class="sxs-lookup"><span data-stu-id="49971-131">
<strong>EOF=True</strong></span></span></p></td>
<td><p><span data-ttu-id="49971-132">Разрешено</span><span class="sxs-lookup"><span data-stu-id="49971-132">Allowed</span></span></p></td>
<td><p><span data-ttu-id="49971-133">Разрешено</span><span class="sxs-lookup"><span data-stu-id="49971-133">Allowed</span></span></p></td>
<td><p><span data-ttu-id="49971-134">Ошибка</span><span class="sxs-lookup"><span data-stu-id="49971-134">Error</span></span></p></td>
<td><p><span data-ttu-id="49971-135">Ошибка</span><span class="sxs-lookup"><span data-stu-id="49971-135">Error</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="49971-136">Оба свойства имеют значение <strong>True</strong></span><span class="sxs-lookup"><span data-stu-id="49971-136">Both <strong>True</strong></span></span></p></td>
<td><p><span data-ttu-id="49971-137">Ошибка</span><span class="sxs-lookup"><span data-stu-id="49971-137">Error</span></span></p></td>
<td><p><span data-ttu-id="49971-138">Ошибка</span><span class="sxs-lookup"><span data-stu-id="49971-138">Error</span></span></p></td>
<td><p><span data-ttu-id="49971-139">Ошибка</span><span class="sxs-lookup"><span data-stu-id="49971-139">Error</span></span></p></td>
<td><p><span data-ttu-id="49971-140">Ошибка</span><span class="sxs-lookup"><span data-stu-id="49971-140">Error</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="49971-141">Оба свойства имеют значение <strong>False</strong></span><span class="sxs-lookup"><span data-stu-id="49971-141">Both <strong>False</strong></span></span></p></td>
<td><p><span data-ttu-id="49971-142">Разрешено</span><span class="sxs-lookup"><span data-stu-id="49971-142">Allowed</span></span></p></td>
<td><p><span data-ttu-id="49971-143">Разрешено</span><span class="sxs-lookup"><span data-stu-id="49971-143">Allowed</span></span></p></td>
<td><p><span data-ttu-id="49971-144">Разрешено</span><span class="sxs-lookup"><span data-stu-id="49971-144">Allowed</span></span></p></td>
<td><p><span data-ttu-id="49971-145">Разрешено</span><span class="sxs-lookup"><span data-stu-id="49971-145">Allowed</span></span></p></td>
</tr>
</tbody>
</table>


<span data-ttu-id="49971-146">Разрешение метода **Move** не гарантирует, что метод успешно наймет запись; Это означает, что вызов указанного метода **Move** не будет создавать ошибку.</span><span class="sxs-lookup"><span data-stu-id="49971-146">Allowing a **Move** method doesn't guarantee that the method will successfully locate a record; it only means that calling the specified **Move** method won't generate an error.</span></span>

<span data-ttu-id="49971-147">В следующей таблице показано, что происходит с настройками свойств **BOF** и **EOF** при вызове различных методов **Move,** но не удается найти запись.</span><span class="sxs-lookup"><span data-stu-id="49971-147">The following table shows what happens to the **BOF** and **EOF** property settings when you call various **Move** methods but are unable to successfully locate a record.</span></span>

<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th><p></p></th>
<th><p><span data-ttu-id="49971-148">BOF</span><span class="sxs-lookup"><span data-stu-id="49971-148">BOF</span></span></p></th>
<th><p><span data-ttu-id="49971-149">EOF</span><span class="sxs-lookup"><span data-stu-id="49971-149">EOF</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="49971-150"><strong>MoveFirst</strong>, <strong>MoveLast</strong></span><span class="sxs-lookup"><span data-stu-id="49971-150"><strong>MoveFirst</strong>, <strong>MoveLast</strong></span></span></p></td>
<td><p><span data-ttu-id="49971-151">Установите <strong>true</strong></span><span class="sxs-lookup"><span data-stu-id="49971-151">Set to <strong>True</strong></span></span></p></td>
<td><p><span data-ttu-id="49971-152">Установите <strong>true</strong></span><span class="sxs-lookup"><span data-stu-id="49971-152">Set to <strong>True</strong></span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="49971-153"><strong>Move</strong> 0</span><span class="sxs-lookup"><span data-stu-id="49971-153"><strong>Move</strong> 0</span></span></p></td>
<td><p><span data-ttu-id="49971-154">Без изменений</span><span class="sxs-lookup"><span data-stu-id="49971-154">No change</span></span></p></td>
<td><p><span data-ttu-id="49971-155">Без изменений</span><span class="sxs-lookup"><span data-stu-id="49971-155">No change</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="49971-156"><strong>MovePrevious</strong>, <strong>Move</strong> &lt; 0</span><span class="sxs-lookup"><span data-stu-id="49971-156"><strong>MovePrevious</strong>, <strong>Move</strong> &lt; 0</span></span></p></td>
<td><p><span data-ttu-id="49971-157">Установите <strong>true</strong></span><span class="sxs-lookup"><span data-stu-id="49971-157">Set to <strong>True</strong></span></span></p></td>
<td><p><span data-ttu-id="49971-158">Без изменений</span><span class="sxs-lookup"><span data-stu-id="49971-158">No change</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="49971-159"><strong>MoveNext</strong>, <strong>Move</strong> &gt; 0</span><span class="sxs-lookup"><span data-stu-id="49971-159"><strong>MoveNext</strong>, <strong>Move</strong> &gt; 0</span></span></p></td>
<td><p><span data-ttu-id="49971-160">Без изменений</span><span class="sxs-lookup"><span data-stu-id="49971-160">No change</span></span></p></td>
<td><p><span data-ttu-id="49971-161">Установите <strong>true</strong></span><span class="sxs-lookup"><span data-stu-id="49971-161">Set to <strong>True</strong></span></span></p></td>
</tr>
</tbody>
</table>

