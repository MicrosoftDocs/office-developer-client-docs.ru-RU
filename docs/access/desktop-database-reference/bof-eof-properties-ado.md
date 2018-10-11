---
title: BOF, EOF Properties (ADO)
TOCTitle: BOF, EOF Properties (ADO)
ms:assetid: f797e140-5572-1a4d-9afc-285f6a3868a8
ms:mtpsurl: https://msdn.microsoft.com/library/JJ250260(v=office.15)
ms:contentKeyID: 48548768
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 14cd61f6bd2985d71321d848a6426c06c4c7a94d
ms.sourcegitcommit: 19aca09c5812cfb98b68b5d4604dcaa814479df7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/09/2018
ms.locfileid: "25480483"
---
# <a name="bof-eof-properties-ado"></a><span data-ttu-id="3e9cb-102">BOF, EOF Properties (ADO)</span><span class="sxs-lookup"><span data-stu-id="3e9cb-102">BOF, EOF Properties (ADO)</span></span>


<span data-ttu-id="3e9cb-103">**Применимо к**: Access 2013 | Office 2013</span><span class="sxs-lookup"><span data-stu-id="3e9cb-103">**Applies to**: Access 2013 | Office 2013</span></span>

  - <span data-ttu-id="3e9cb-104">**BOF** — указывает, что положение текущей записи — перед первой записи в объекте [набора записей](recordset-object-ado.md) .</span><span class="sxs-lookup"><span data-stu-id="3e9cb-104">**BOF** — Indicates that the current record position is before the first record in a [Recordset](recordset-object-ado.md) object.</span></span>

  - <span data-ttu-id="3e9cb-105">**Функция EOF** — указывает, что положение текущей записи после последней записи в объекте **набора записей** .</span><span class="sxs-lookup"><span data-stu-id="3e9cb-105">**EOF** — Indicates that the current record position is after the last record in a **Recordset** object.</span></span>

## <a name="return-value"></a><span data-ttu-id="3e9cb-106">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="3e9cb-106">Return Value</span></span>

<span data-ttu-id="3e9cb-107">**Логические** значения, возвращаемые свойства **BOF** и **EOF** .</span><span class="sxs-lookup"><span data-stu-id="3e9cb-107">The **BOF** and **EOF** properties return **Boolean** values.</span></span>

## <a name="remarks"></a><span data-ttu-id="3e9cb-108">Замечания</span><span class="sxs-lookup"><span data-stu-id="3e9cb-108">Remarks</span></span>

<span data-ttu-id="3e9cb-109">Используйте свойства **BOF** и **EOF** , чтобы определить, содержит ли объект **набора записей** записей или ли вы уменьшилось за пределы ограничения объекта **набора записей** , при перемещении между записями.</span><span class="sxs-lookup"><span data-stu-id="3e9cb-109">Use the **BOF** and **EOF** properties to determine whether a **Recordset** object contains records or whether you've gone beyond the limits of a **Recordset** object when you move from record to record.</span></span>

<span data-ttu-id="3e9cb-110">Свойство **BOF** возвращает **значение True** (значение -1) при текущей позиции записи перед первой записи и **значение False** (0) Если в настоящее время записи на или после первой записи.</span><span class="sxs-lookup"><span data-stu-id="3e9cb-110">The **BOF** property returns **True** (-1) if the current record position is before the first record and **False** (0) if the current record position is on or after the first record.</span></span>

<span data-ttu-id="3e9cb-111">Свойство **EOF** возвращает **значение True** , если в настоящее время записи после последней записи и **значение False** , если текущей позиции записи не позднее последней записи.</span><span class="sxs-lookup"><span data-stu-id="3e9cb-111">The **EOF** property returns **True** if the current record position is after the last record and **False** if the current record position is on or before the last record.</span></span>

<span data-ttu-id="3e9cb-112">Если параметр **BOF** или **EOF** свойство имеет **значение True**, нет нет текущей записи.</span><span class="sxs-lookup"><span data-stu-id="3e9cb-112">If either the **BOF** or **EOF** property is **True**, there is no current record.</span></span>

<span data-ttu-id="3e9cb-113">При открытии объекта **набора записей** , содержащий записи не **BOF** и **EOF** задано значение **True** (см. свойство [RecordCount](recordcount-property-ado.md) Дополнительные сведения об этом состоянии **набора записей**).</span><span class="sxs-lookup"><span data-stu-id="3e9cb-113">If you open a **Recordset** object containing no records, the **BOF** and **EOF** properties are set to **True** (see the [RecordCount](recordcount-property-ado.md) property for more information about this state of a **Recordset**).</span></span> <span data-ttu-id="3e9cb-114">При открытии объекта **набора записей** , который содержит по крайней мере одна запись первая запись является текущей записи и свойства **BOF** и **EOF** — **значение False**.</span><span class="sxs-lookup"><span data-stu-id="3e9cb-114">When you open a **Recordset** object that contains at least one record, the first record is the current record and the **BOF** and **EOF** properties are **False**.</span></span>

<span data-ttu-id="3e9cb-115">При удалении последней оставшиеся записи в объекте **набора записей** , свойства **BOF** и **EOF** может оставаться **значение False,** пока вы пытаетесь изменить положение текущей записи.</span><span class="sxs-lookup"><span data-stu-id="3e9cb-115">If you delete the last remaining record in the **Recordset** object, the **BOF** and **EOF** properties may remain **False** until you attempt to reposition the current record.</span></span>

<span data-ttu-id="3e9cb-116">Этой таблице показано, какие методы **перемещения** может использоваться с разные сочетания свойства **BOF** и **EOF** .</span><span class="sxs-lookup"><span data-stu-id="3e9cb-116">This table shows which **Move** methods are allowed with different combinations of the **BOF** and **EOF** properties.</span></span>

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
<th><p><span data-ttu-id="3e9cb-117">MoveFirst</span><span class="sxs-lookup"><span data-stu-id="3e9cb-117">MoveFirst,</span></span><br />
<span data-ttu-id="3e9cb-118">MoveLast</span><span class="sxs-lookup"><span data-stu-id="3e9cb-118">MoveLast</span></span></p></th>
<th><p><span data-ttu-id="3e9cb-119">MovePrevious,</span><span class="sxs-lookup"><span data-stu-id="3e9cb-119">MovePrevious,</span></span><br />
<span data-ttu-id="3e9cb-120">Перемещение &lt; 0</span><span class="sxs-lookup"><span data-stu-id="3e9cb-120">Move &lt; 0</span></span></p></th>
<th><p><br />
<span data-ttu-id="3e9cb-121">Перемещение 0</span><span class="sxs-lookup"><span data-stu-id="3e9cb-121">Move 0</span></span></p></th>
<th><p><span data-ttu-id="3e9cb-122">MoveNext,</span><span class="sxs-lookup"><span data-stu-id="3e9cb-122">MoveNext,</span></span><br />
<span data-ttu-id="3e9cb-123">Перемещение &gt; 0</span><span class="sxs-lookup"><span data-stu-id="3e9cb-123">Move &gt; 0</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="3e9cb-124"><strong>BOF = True,</strong></span><span class="sxs-lookup"><span data-stu-id="3e9cb-124"><strong>BOF=True,</strong></span></span><br /><span data-ttu-id="3e9cb-125">
<strong>Функция EOF = False</strong></span><span class="sxs-lookup"><span data-stu-id="3e9cb-125">
<strong>EOF=False</strong></span></span></p></td>
<td><p><span data-ttu-id="3e9cb-126">Разрешено</span><span class="sxs-lookup"><span data-stu-id="3e9cb-126">Allowed</span></span></p></td>
<td><p><span data-ttu-id="3e9cb-127">Error</span><span class="sxs-lookup"><span data-stu-id="3e9cb-127">Error</span></span></p></td>
<td><p><span data-ttu-id="3e9cb-128">Error</span><span class="sxs-lookup"><span data-stu-id="3e9cb-128">Error</span></span></p></td>
<td><p><span data-ttu-id="3e9cb-129">Разрешено</span><span class="sxs-lookup"><span data-stu-id="3e9cb-129">Allowed</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="3e9cb-130"><strong>BOF = False,</strong></span><span class="sxs-lookup"><span data-stu-id="3e9cb-130"><strong>BOF=False,</strong></span></span><br /><span data-ttu-id="3e9cb-131">
<strong>Функция EOF = True</strong></span><span class="sxs-lookup"><span data-stu-id="3e9cb-131">
<strong>EOF=True</strong></span></span></p></td>
<td><p><span data-ttu-id="3e9cb-132">Разрешено</span><span class="sxs-lookup"><span data-stu-id="3e9cb-132">Allowed</span></span></p></td>
<td><p><span data-ttu-id="3e9cb-133">Разрешено</span><span class="sxs-lookup"><span data-stu-id="3e9cb-133">Allowed</span></span></p></td>
<td><p><span data-ttu-id="3e9cb-134">Error</span><span class="sxs-lookup"><span data-stu-id="3e9cb-134">Error</span></span></p></td>
<td><p><span data-ttu-id="3e9cb-135">Error</span><span class="sxs-lookup"><span data-stu-id="3e9cb-135">Error</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="3e9cb-136">Оба <strong>значение True</strong></span><span class="sxs-lookup"><span data-stu-id="3e9cb-136">Both <strong>True</strong></span></span></p></td>
<td><p><span data-ttu-id="3e9cb-137">Error</span><span class="sxs-lookup"><span data-stu-id="3e9cb-137">Error</span></span></p></td>
<td><p><span data-ttu-id="3e9cb-138">Error</span><span class="sxs-lookup"><span data-stu-id="3e9cb-138">Error</span></span></p></td>
<td><p><span data-ttu-id="3e9cb-139">Error</span><span class="sxs-lookup"><span data-stu-id="3e9cb-139">Error</span></span></p></td>
<td><p><span data-ttu-id="3e9cb-140">Error</span><span class="sxs-lookup"><span data-stu-id="3e9cb-140">Error</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="3e9cb-141">Оба <strong>False</strong></span><span class="sxs-lookup"><span data-stu-id="3e9cb-141">Both <strong>False</strong></span></span></p></td>
<td><p><span data-ttu-id="3e9cb-142">Разрешено</span><span class="sxs-lookup"><span data-stu-id="3e9cb-142">Allowed</span></span></p></td>
<td><p><span data-ttu-id="3e9cb-143">Разрешено</span><span class="sxs-lookup"><span data-stu-id="3e9cb-143">Allowed</span></span></p></td>
<td><p><span data-ttu-id="3e9cb-144">Разрешено</span><span class="sxs-lookup"><span data-stu-id="3e9cb-144">Allowed</span></span></p></td>
<td><p><span data-ttu-id="3e9cb-145">Разрешено</span><span class="sxs-lookup"><span data-stu-id="3e9cb-145">Allowed</span></span></p></td>
</tr>
</tbody>
</table>


<span data-ttu-id="3e9cb-146">Позволяет **переместить** метод не гарантирует, что метод будет успешно найдите запись; только это означает, что вызов **Перемещение** указанный метод не возникнет ошибка.</span><span class="sxs-lookup"><span data-stu-id="3e9cb-146">Allowing a **Move** method doesn't guarantee that the method will successfully locate a record; it only means that calling the specified **Move** method won't generate an error.</span></span>

<span data-ttu-id="3e9cb-147">В следующей таблице показаны, что происходит с **BOF** или **EOF** параметров при вызове различные методы **перемещения** , но не удается найти запись успешно.</span><span class="sxs-lookup"><span data-stu-id="3e9cb-147">The following table shows what happens to the **BOF** and **EOF** property settings when you call various **Move** methods but are unable to successfully locate a record.</span></span>

<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th><p></p></th>
<th><p><span data-ttu-id="3e9cb-148">BOF</span><span class="sxs-lookup"><span data-stu-id="3e9cb-148">BOF</span></span></p></th>
<th><p><span data-ttu-id="3e9cb-149">ФУНКЦИЯ EOF</span><span class="sxs-lookup"><span data-stu-id="3e9cb-149">EOF</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="3e9cb-150"><strong>MoveFirst</strong> <strong>MoveLast</strong></span><span class="sxs-lookup"><span data-stu-id="3e9cb-150"><strong>MoveFirst</strong>, <strong>MoveLast</strong></span></span></p></td>
<td><p><span data-ttu-id="3e9cb-151">Значение <strong>True</strong></span><span class="sxs-lookup"><span data-stu-id="3e9cb-151">Set to <strong>True</strong></span></span></p></td>
<td><p><span data-ttu-id="3e9cb-152">Значение <strong>True</strong></span><span class="sxs-lookup"><span data-stu-id="3e9cb-152">Set to <strong>True</strong></span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="3e9cb-153"><strong>Перемещение</strong> 0</span><span class="sxs-lookup"><span data-stu-id="3e9cb-153"><strong>Move</strong> 0</span></span></p></td>
<td><p><span data-ttu-id="3e9cb-154">Без изменений</span><span class="sxs-lookup"><span data-stu-id="3e9cb-154">No change</span></span></p></td>
<td><p><span data-ttu-id="3e9cb-155">Без изменений</span><span class="sxs-lookup"><span data-stu-id="3e9cb-155">No change</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="3e9cb-156"><strong>MovePrevious</strong>, <strong>Переместите</strong> &lt; 0</span><span class="sxs-lookup"><span data-stu-id="3e9cb-156"><strong>MovePrevious</strong>, <strong>Move</strong> &lt; 0</span></span></p></td>
<td><p><span data-ttu-id="3e9cb-157">Значение <strong>True</strong></span><span class="sxs-lookup"><span data-stu-id="3e9cb-157">Set to <strong>True</strong></span></span></p></td>
<td><p><span data-ttu-id="3e9cb-158">Без изменений</span><span class="sxs-lookup"><span data-stu-id="3e9cb-158">No change</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="3e9cb-159"><strong>MoveNext</strong>, <strong>Переместите</strong> &gt; 0</span><span class="sxs-lookup"><span data-stu-id="3e9cb-159"><strong>MoveNext</strong>, <strong>Move</strong> &gt; 0</span></span></p></td>
<td><p><span data-ttu-id="3e9cb-160">Без изменений</span><span class="sxs-lookup"><span data-stu-id="3e9cb-160">No change</span></span></p></td>
<td><p><span data-ttu-id="3e9cb-161">Значение <strong>True</strong></span><span class="sxs-lookup"><span data-stu-id="3e9cb-161">Set to <strong>True</strong></span></span></p></td>
</tr>
</tbody>
</table>

