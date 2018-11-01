---
title: Свойства BOF, EOF (ADO)
TOCTitle: BOF, EOF properties (ADO)
ms:assetid: f797e140-5572-1a4d-9afc-285f6a3868a8
ms:mtpsurl: https://msdn.microsoft.com/library/JJ250260(v=office.15)
ms:contentKeyID: 48548768
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 5b71e48f3fe0b596f085f02d371b0775695ffd5c
ms.sourcegitcommit: c557bbcccf37a6011f89aae1ddd399dfe549d087
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/31/2018
ms.locfileid: "25874246"
---
# <a name="bof-eof-properties-ado"></a><span data-ttu-id="0a585-102">Свойства BOF, EOF (ADO)</span><span class="sxs-lookup"><span data-stu-id="0a585-102">BOF, EOF properties (ADO)</span></span>


<span data-ttu-id="0a585-103">**Применимо к**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="0a585-103">**Applies to**: Access 2013, Office 2013</span></span>

  - <span data-ttu-id="0a585-104">**BOF** — указывает, что положение текущей записи — перед первой записи в объекте [набора записей](recordset-object-ado.md) .</span><span class="sxs-lookup"><span data-stu-id="0a585-104">**BOF** — Indicates that the current record position is before the first record in a [Recordset](recordset-object-ado.md) object.</span></span>

  - <span data-ttu-id="0a585-105">**Функция EOF** — указывает, что положение текущей записи после последней записи в объекте **набора записей** .</span><span class="sxs-lookup"><span data-stu-id="0a585-105">**EOF** — Indicates that the current record position is after the last record in a **Recordset** object.</span></span>

## <a name="return-value"></a><span data-ttu-id="0a585-106">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="0a585-106">Return value</span></span>

<span data-ttu-id="0a585-107">**Логические** значения, возвращаемые свойства **BOF** и **EOF** .</span><span class="sxs-lookup"><span data-stu-id="0a585-107">The **BOF** and **EOF** properties return **Boolean** values.</span></span>

## <a name="remarks"></a><span data-ttu-id="0a585-108">Замечания</span><span class="sxs-lookup"><span data-stu-id="0a585-108">Remarks</span></span>

<span data-ttu-id="0a585-109">Используйте свойства **BOF** и **EOF** , чтобы определить, содержит ли объект **набора записей** записей или ли вы уменьшилось за пределы ограничения объекта **набора записей** , при перемещении между записями.</span><span class="sxs-lookup"><span data-stu-id="0a585-109">Use the **BOF** and **EOF** properties to determine whether a **Recordset** object contains records or whether you've gone beyond the limits of a **Recordset** object when you move from record to record.</span></span>

<span data-ttu-id="0a585-110">Свойство **BOF** возвращает **значение True** (значение -1) при текущей позиции записи перед первой записи и **значение False** (0) Если в настоящее время записи на или после первой записи.</span><span class="sxs-lookup"><span data-stu-id="0a585-110">The **BOF** property returns **True** (-1) if the current record position is before the first record and **False** (0) if the current record position is on or after the first record.</span></span>

<span data-ttu-id="0a585-111">Свойство **EOF** возвращает **значение True** , если в настоящее время записи после последней записи и **значение False** , если текущей позиции записи не позднее последней записи.</span><span class="sxs-lookup"><span data-stu-id="0a585-111">The **EOF** property returns **True** if the current record position is after the last record and **False** if the current record position is on or before the last record.</span></span>

<span data-ttu-id="0a585-112">Если параметр **BOF** или **EOF** свойство имеет **значение True**, нет нет текущей записи.</span><span class="sxs-lookup"><span data-stu-id="0a585-112">If either the **BOF** or **EOF** property is **True**, there is no current record.</span></span>

<span data-ttu-id="0a585-113">При открытии объекта **набора записей** , содержащий записи не **BOF** и **EOF** задано значение **True** (см. свойство [RecordCount](recordcount-property-ado.md) Дополнительные сведения об этом состоянии **набора записей**).</span><span class="sxs-lookup"><span data-stu-id="0a585-113">If you open a **Recordset** object containing no records, the **BOF** and **EOF** properties are set to **True** (see the [RecordCount](recordcount-property-ado.md) property for more information about this state of a **Recordset**).</span></span> <span data-ttu-id="0a585-114">При открытии объекта **набора записей** , который содержит по крайней мере одна запись первая запись является текущей записи и свойства **BOF** и **EOF** — **значение False**.</span><span class="sxs-lookup"><span data-stu-id="0a585-114">When you open a **Recordset** object that contains at least one record, the first record is the current record and the **BOF** and **EOF** properties are **False**.</span></span>

<span data-ttu-id="0a585-115">При удалении последней оставшиеся записи в объекте **набора записей** , свойства **BOF** и **EOF** может оставаться **значение False,** пока вы пытаетесь изменить положение текущей записи.</span><span class="sxs-lookup"><span data-stu-id="0a585-115">If you delete the last remaining record in the **Recordset** object, the **BOF** and **EOF** properties may remain **False** until you attempt to reposition the current record.</span></span>

<span data-ttu-id="0a585-116">Этой таблице показано, какие методы **перемещения** может использоваться с разные сочетания свойства **BOF** и **EOF** .</span><span class="sxs-lookup"><span data-stu-id="0a585-116">This table shows which **Move** methods are allowed with different combinations of the **BOF** and **EOF** properties.</span></span>

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
<th><p><span data-ttu-id="0a585-117">MoveFirst</span><span class="sxs-lookup"><span data-stu-id="0a585-117">MoveFirst,</span></span><br />
<span data-ttu-id="0a585-118">MoveLast</span><span class="sxs-lookup"><span data-stu-id="0a585-118">MoveLast</span></span></p></th>
<th><p><span data-ttu-id="0a585-119">MovePrevious,</span><span class="sxs-lookup"><span data-stu-id="0a585-119">MovePrevious,</span></span><br />
<span data-ttu-id="0a585-120">Перемещение &lt; 0</span><span class="sxs-lookup"><span data-stu-id="0a585-120">Move &lt; 0</span></span></p></th>
<th><p><br />
<span data-ttu-id="0a585-121">Перемещение 0</span><span class="sxs-lookup"><span data-stu-id="0a585-121">Move 0</span></span></p></th>
<th><p><span data-ttu-id="0a585-122">MoveNext,</span><span class="sxs-lookup"><span data-stu-id="0a585-122">MoveNext,</span></span><br />
<span data-ttu-id="0a585-123">Перемещение &gt; 0</span><span class="sxs-lookup"><span data-stu-id="0a585-123">Move &gt; 0</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="0a585-124"><strong>BOF = True,</strong></span><span class="sxs-lookup"><span data-stu-id="0a585-124"><strong>BOF=True,</strong></span></span><br /><span data-ttu-id="0a585-125">
<strong>Функция EOF = False</strong></span><span class="sxs-lookup"><span data-stu-id="0a585-125">
<strong>EOF=False</strong></span></span></p></td>
<td><p><span data-ttu-id="0a585-126">Разрешено</span><span class="sxs-lookup"><span data-stu-id="0a585-126">Allowed</span></span></p></td>
<td><p><span data-ttu-id="0a585-127">Error</span><span class="sxs-lookup"><span data-stu-id="0a585-127">Error</span></span></p></td>
<td><p><span data-ttu-id="0a585-128">Error</span><span class="sxs-lookup"><span data-stu-id="0a585-128">Error</span></span></p></td>
<td><p><span data-ttu-id="0a585-129">Разрешено</span><span class="sxs-lookup"><span data-stu-id="0a585-129">Allowed</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="0a585-130"><strong>BOF = False,</strong></span><span class="sxs-lookup"><span data-stu-id="0a585-130"><strong>BOF=False,</strong></span></span><br /><span data-ttu-id="0a585-131">
<strong>Функция EOF = True</strong></span><span class="sxs-lookup"><span data-stu-id="0a585-131">
<strong>EOF=True</strong></span></span></p></td>
<td><p><span data-ttu-id="0a585-132">Разрешено</span><span class="sxs-lookup"><span data-stu-id="0a585-132">Allowed</span></span></p></td>
<td><p><span data-ttu-id="0a585-133">Разрешено</span><span class="sxs-lookup"><span data-stu-id="0a585-133">Allowed</span></span></p></td>
<td><p><span data-ttu-id="0a585-134">Error</span><span class="sxs-lookup"><span data-stu-id="0a585-134">Error</span></span></p></td>
<td><p><span data-ttu-id="0a585-135">Error</span><span class="sxs-lookup"><span data-stu-id="0a585-135">Error</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="0a585-136">Оба <strong>значение True</strong></span><span class="sxs-lookup"><span data-stu-id="0a585-136">Both <strong>True</strong></span></span></p></td>
<td><p><span data-ttu-id="0a585-137">Error</span><span class="sxs-lookup"><span data-stu-id="0a585-137">Error</span></span></p></td>
<td><p><span data-ttu-id="0a585-138">Error</span><span class="sxs-lookup"><span data-stu-id="0a585-138">Error</span></span></p></td>
<td><p><span data-ttu-id="0a585-139">Error</span><span class="sxs-lookup"><span data-stu-id="0a585-139">Error</span></span></p></td>
<td><p><span data-ttu-id="0a585-140">Error</span><span class="sxs-lookup"><span data-stu-id="0a585-140">Error</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="0a585-141">Оба <strong>False</strong></span><span class="sxs-lookup"><span data-stu-id="0a585-141">Both <strong>False</strong></span></span></p></td>
<td><p><span data-ttu-id="0a585-142">Разрешено</span><span class="sxs-lookup"><span data-stu-id="0a585-142">Allowed</span></span></p></td>
<td><p><span data-ttu-id="0a585-143">Разрешено</span><span class="sxs-lookup"><span data-stu-id="0a585-143">Allowed</span></span></p></td>
<td><p><span data-ttu-id="0a585-144">Разрешено</span><span class="sxs-lookup"><span data-stu-id="0a585-144">Allowed</span></span></p></td>
<td><p><span data-ttu-id="0a585-145">Разрешено</span><span class="sxs-lookup"><span data-stu-id="0a585-145">Allowed</span></span></p></td>
</tr>
</tbody>
</table>


<span data-ttu-id="0a585-146">Позволяет **переместить** метод не гарантирует, что метод будет успешно найдите запись; только это означает, что вызов **Перемещение** указанный метод не возникнет ошибка.</span><span class="sxs-lookup"><span data-stu-id="0a585-146">Allowing a **Move** method doesn't guarantee that the method will successfully locate a record; it only means that calling the specified **Move** method won't generate an error.</span></span>

<span data-ttu-id="0a585-147">В следующей таблице показаны, что происходит с **BOF** или **EOF** параметров при вызове различные методы **перемещения** , но не удается найти запись успешно.</span><span class="sxs-lookup"><span data-stu-id="0a585-147">The following table shows what happens to the **BOF** and **EOF** property settings when you call various **Move** methods but are unable to successfully locate a record.</span></span>

<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th><p></p></th>
<th><p><span data-ttu-id="0a585-148">BOF</span><span class="sxs-lookup"><span data-stu-id="0a585-148">BOF</span></span></p></th>
<th><p><span data-ttu-id="0a585-149">ФУНКЦИЯ EOF</span><span class="sxs-lookup"><span data-stu-id="0a585-149">EOF</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="0a585-150"><strong>MoveFirst</strong> <strong>MoveLast</strong></span><span class="sxs-lookup"><span data-stu-id="0a585-150"><strong>MoveFirst</strong>, <strong>MoveLast</strong></span></span></p></td>
<td><p><span data-ttu-id="0a585-151">Значение <strong>True</strong></span><span class="sxs-lookup"><span data-stu-id="0a585-151">Set to <strong>True</strong></span></span></p></td>
<td><p><span data-ttu-id="0a585-152">Значение <strong>True</strong></span><span class="sxs-lookup"><span data-stu-id="0a585-152">Set to <strong>True</strong></span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="0a585-153"><strong>Перемещение</strong> 0</span><span class="sxs-lookup"><span data-stu-id="0a585-153"><strong>Move</strong> 0</span></span></p></td>
<td><p><span data-ttu-id="0a585-154">Без изменений</span><span class="sxs-lookup"><span data-stu-id="0a585-154">No change</span></span></p></td>
<td><p><span data-ttu-id="0a585-155">Без изменений</span><span class="sxs-lookup"><span data-stu-id="0a585-155">No change</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="0a585-156"><strong>MovePrevious</strong>, <strong>Переместите</strong> &lt; 0</span><span class="sxs-lookup"><span data-stu-id="0a585-156"><strong>MovePrevious</strong>, <strong>Move</strong> &lt; 0</span></span></p></td>
<td><p><span data-ttu-id="0a585-157">Значение <strong>True</strong></span><span class="sxs-lookup"><span data-stu-id="0a585-157">Set to <strong>True</strong></span></span></p></td>
<td><p><span data-ttu-id="0a585-158">Без изменений</span><span class="sxs-lookup"><span data-stu-id="0a585-158">No change</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="0a585-159"><strong>MoveNext</strong>, <strong>Переместите</strong> &gt; 0</span><span class="sxs-lookup"><span data-stu-id="0a585-159"><strong>MoveNext</strong>, <strong>Move</strong> &gt; 0</span></span></p></td>
<td><p><span data-ttu-id="0a585-160">Без изменений</span><span class="sxs-lookup"><span data-stu-id="0a585-160">No change</span></span></p></td>
<td><p><span data-ttu-id="0a585-161">Значение <strong>True</strong></span><span class="sxs-lookup"><span data-stu-id="0a585-161">Set to <strong>True</strong></span></span></p></td>
</tr>
</tbody>
</table>

