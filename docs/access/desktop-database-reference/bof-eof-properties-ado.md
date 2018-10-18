---
<span data-ttu-id="3ac50-101"><<<<<<< Название HEAD: BOF, TOCTitle свойства EOF (ADO): BOF, свойства EOF (ADO) === название: BOF, свойства EOF (ADO) TOCTitle: BOF, свойства EOF (ADO)</span><span class="sxs-lookup"><span data-stu-id="3ac50-101"><<<<<<< HEAD title: BOF, EOF Properties (ADO) TOCTitle: BOF, EOF Properties (ADO) ======= title: BOF, EOF properties (ADO) TOCTitle: BOF, EOF properties (ADO)</span></span>
>>>>>>> <span data-ttu-id="3ac50-102">главные ms:assetid: f797e140-5572-1a4d-9afc-285f6a3868a8 ms:mtpsurl: https://msdn.microsoft.com/library/JJ250260(v=office.15) ms:contentKeyID: 48548768 ms.date: 09/18/2015 mtps_version: v=office.15</span><span class="sxs-lookup"><span data-stu-id="3ac50-102">master ms:assetid: f797e140-5572-1a4d-9afc-285f6a3868a8 ms:mtpsurl: https://msdn.microsoft.com/library/JJ250260(v=office.15) ms:contentKeyID: 48548768 ms.date: 09/18/2015 mtps_version: v=office.15</span></span>
---

<span data-ttu-id="3ac50-103"><<<<<<< HEAD</span><span class="sxs-lookup"><span data-stu-id="3ac50-103"><<<<<<< HEAD</span></span>
# <a name="bof-eof-properties-ado"></a><span data-ttu-id="3ac50-104">BOF, EOF Properties (ADO)</span><span class="sxs-lookup"><span data-stu-id="3ac50-104">BOF, EOF Properties (ADO)</span></span>
=======
# <a name="bof-eof-properties-ado"></a><span data-ttu-id="3ac50-105">BOF, свойства EOF (ADO)</span><span class="sxs-lookup"><span data-stu-id="3ac50-105">BOF, EOF properties (ADO)</span></span>
>>>>>>> <span data-ttu-id="3ac50-106">master</span><span class="sxs-lookup"><span data-stu-id="3ac50-106">master</span></span>


<span data-ttu-id="3ac50-107">**Применимо к**: Access 2013 | Office 2013</span><span class="sxs-lookup"><span data-stu-id="3ac50-107">**Applies to**: Access 2013 | Office 2013</span></span>

  - <span data-ttu-id="3ac50-108">**BOF** — указывает, что положение текущей записи — перед первой записи в объекте [набора записей](recordset-object-ado.md) .</span><span class="sxs-lookup"><span data-stu-id="3ac50-108">**BOF** — Indicates that the current record position is before the first record in a [Recordset](recordset-object-ado.md) object.</span></span>

  - <span data-ttu-id="3ac50-109">**Функция EOF** — указывает, что положение текущей записи после последней записи в объекте **набора записей** .</span><span class="sxs-lookup"><span data-stu-id="3ac50-109">**EOF** — Indicates that the current record position is after the last record in a **Recordset** object.</span></span>

<span data-ttu-id="3ac50-110"><<<<<<< HEAD</span><span class="sxs-lookup"><span data-stu-id="3ac50-110"><<<<<<< HEAD</span></span>
## <a name="return-value"></a><span data-ttu-id="3ac50-111">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="3ac50-111">Return Value</span></span>
=======
## <a name="return-value"></a><span data-ttu-id="3ac50-112">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="3ac50-112">Return value</span></span>
>>>>>>> <span data-ttu-id="3ac50-113">master</span><span class="sxs-lookup"><span data-stu-id="3ac50-113">master</span></span>

<span data-ttu-id="3ac50-114">**Логические** значения, возвращаемые свойства **BOF** и **EOF** .</span><span class="sxs-lookup"><span data-stu-id="3ac50-114">The **BOF** and **EOF** properties return **Boolean** values.</span></span>

## <a name="remarks"></a><span data-ttu-id="3ac50-115">Замечания</span><span class="sxs-lookup"><span data-stu-id="3ac50-115">Remarks</span></span>

<span data-ttu-id="3ac50-116">Используйте свойства **BOF** и **EOF** , чтобы определить, содержит ли объект **набора записей** записей или ли вы уменьшилось за пределы ограничения объекта **набора записей** , при перемещении между записями.</span><span class="sxs-lookup"><span data-stu-id="3ac50-116">Use the **BOF** and **EOF** properties to determine whether a **Recordset** object contains records or whether you've gone beyond the limits of a **Recordset** object when you move from record to record.</span></span>

<span data-ttu-id="3ac50-117">Свойство **BOF** возвращает **значение True** (значение -1) при текущей позиции записи перед первой записи и **значение False** (0) Если в настоящее время записи на или после первой записи.</span><span class="sxs-lookup"><span data-stu-id="3ac50-117">The **BOF** property returns **True** (-1) if the current record position is before the first record and **False** (0) if the current record position is on or after the first record.</span></span>

<span data-ttu-id="3ac50-118">Свойство **EOF** возвращает **значение True** , если в настоящее время записи после последней записи и **значение False** , если текущей позиции записи не позднее последней записи.</span><span class="sxs-lookup"><span data-stu-id="3ac50-118">The **EOF** property returns **True** if the current record position is after the last record and **False** if the current record position is on or before the last record.</span></span>

<span data-ttu-id="3ac50-119">Если параметр **BOF** или **EOF** свойство имеет **значение True**, нет нет текущей записи.</span><span class="sxs-lookup"><span data-stu-id="3ac50-119">If either the **BOF** or **EOF** property is **True**, there is no current record.</span></span>

<span data-ttu-id="3ac50-120">При открытии объекта **набора записей** , содержащий записи не **BOF** и **EOF** задано значение **True** (см. свойство [RecordCount](recordcount-property-ado.md) Дополнительные сведения об этом состоянии **набора записей**).</span><span class="sxs-lookup"><span data-stu-id="3ac50-120">If you open a **Recordset** object containing no records, the **BOF** and **EOF** properties are set to **True** (see the [RecordCount](recordcount-property-ado.md) property for more information about this state of a **Recordset**).</span></span> <span data-ttu-id="3ac50-121">При открытии объекта **набора записей** , который содержит по крайней мере одна запись первая запись является текущей записи и свойства **BOF** и **EOF** — **значение False**.</span><span class="sxs-lookup"><span data-stu-id="3ac50-121">When you open a **Recordset** object that contains at least one record, the first record is the current record and the **BOF** and **EOF** properties are **False**.</span></span>

<span data-ttu-id="3ac50-122">При удалении последней оставшиеся записи в объекте **набора записей** , свойства **BOF** и **EOF** может оставаться **значение False,** пока вы пытаетесь изменить положение текущей записи.</span><span class="sxs-lookup"><span data-stu-id="3ac50-122">If you delete the last remaining record in the **Recordset** object, the **BOF** and **EOF** properties may remain **False** until you attempt to reposition the current record.</span></span>

<span data-ttu-id="3ac50-123">Этой таблице показано, какие методы **перемещения** может использоваться с разные сочетания свойства **BOF** и **EOF** .</span><span class="sxs-lookup"><span data-stu-id="3ac50-123">This table shows which **Move** methods are allowed with different combinations of the **BOF** and **EOF** properties.</span></span>

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
<th><p><span data-ttu-id="3ac50-124">MoveFirst</span><span class="sxs-lookup"><span data-stu-id="3ac50-124">MoveFirst,</span></span><br />
<span data-ttu-id="3ac50-125">MoveLast</span><span class="sxs-lookup"><span data-stu-id="3ac50-125">MoveLast</span></span></p></th>
<th><p><span data-ttu-id="3ac50-126">MovePrevious,</span><span class="sxs-lookup"><span data-stu-id="3ac50-126">MovePrevious,</span></span><br />
<span data-ttu-id="3ac50-127">Перемещение &lt; 0</span><span class="sxs-lookup"><span data-stu-id="3ac50-127">Move &lt; 0</span></span></p></th>
<th><p><br />
<span data-ttu-id="3ac50-128">Перемещение 0</span><span class="sxs-lookup"><span data-stu-id="3ac50-128">Move 0</span></span></p></th>
<th><p><span data-ttu-id="3ac50-129">MoveNext,</span><span class="sxs-lookup"><span data-stu-id="3ac50-129">MoveNext,</span></span><br />
<span data-ttu-id="3ac50-130">Перемещение &gt; 0</span><span class="sxs-lookup"><span data-stu-id="3ac50-130">Move &gt; 0</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="3ac50-131"><strong>BOF = True,</strong></span><span class="sxs-lookup"><span data-stu-id="3ac50-131"><strong>BOF=True,</strong></span></span><br /><span data-ttu-id="3ac50-132">
<strong>Функция EOF = False</strong></span><span class="sxs-lookup"><span data-stu-id="3ac50-132">
<strong>EOF=False</strong></span></span></p></td>
<td><p><span data-ttu-id="3ac50-133">Разрешено</span><span class="sxs-lookup"><span data-stu-id="3ac50-133">Allowed</span></span></p></td>
<td><p><span data-ttu-id="3ac50-134">Error</span><span class="sxs-lookup"><span data-stu-id="3ac50-134">Error</span></span></p></td>
<td><p><span data-ttu-id="3ac50-135">Error</span><span class="sxs-lookup"><span data-stu-id="3ac50-135">Error</span></span></p></td>
<td><p><span data-ttu-id="3ac50-136">Разрешено</span><span class="sxs-lookup"><span data-stu-id="3ac50-136">Allowed</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="3ac50-137"><strong>BOF = False,</strong></span><span class="sxs-lookup"><span data-stu-id="3ac50-137"><strong>BOF=False,</strong></span></span><br /><span data-ttu-id="3ac50-138">
<strong>Функция EOF = True</strong></span><span class="sxs-lookup"><span data-stu-id="3ac50-138">
<strong>EOF=True</strong></span></span></p></td>
<td><p><span data-ttu-id="3ac50-139">Разрешено</span><span class="sxs-lookup"><span data-stu-id="3ac50-139">Allowed</span></span></p></td>
<td><p><span data-ttu-id="3ac50-140">Разрешено</span><span class="sxs-lookup"><span data-stu-id="3ac50-140">Allowed</span></span></p></td>
<td><p><span data-ttu-id="3ac50-141">Error</span><span class="sxs-lookup"><span data-stu-id="3ac50-141">Error</span></span></p></td>
<td><p><span data-ttu-id="3ac50-142">Error</span><span class="sxs-lookup"><span data-stu-id="3ac50-142">Error</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="3ac50-143">Оба <strong>значение True</strong></span><span class="sxs-lookup"><span data-stu-id="3ac50-143">Both <strong>True</strong></span></span></p></td>
<td><p><span data-ttu-id="3ac50-144">Error</span><span class="sxs-lookup"><span data-stu-id="3ac50-144">Error</span></span></p></td>
<td><p><span data-ttu-id="3ac50-145">Error</span><span class="sxs-lookup"><span data-stu-id="3ac50-145">Error</span></span></p></td>
<td><p><span data-ttu-id="3ac50-146">Error</span><span class="sxs-lookup"><span data-stu-id="3ac50-146">Error</span></span></p></td>
<td><p><span data-ttu-id="3ac50-147">Error</span><span class="sxs-lookup"><span data-stu-id="3ac50-147">Error</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="3ac50-148">Оба <strong>False</strong></span><span class="sxs-lookup"><span data-stu-id="3ac50-148">Both <strong>False</strong></span></span></p></td>
<td><p><span data-ttu-id="3ac50-149">Разрешено</span><span class="sxs-lookup"><span data-stu-id="3ac50-149">Allowed</span></span></p></td>
<td><p><span data-ttu-id="3ac50-150">Разрешено</span><span class="sxs-lookup"><span data-stu-id="3ac50-150">Allowed</span></span></p></td>
<td><p><span data-ttu-id="3ac50-151">Разрешено</span><span class="sxs-lookup"><span data-stu-id="3ac50-151">Allowed</span></span></p></td>
<td><p><span data-ttu-id="3ac50-152">Разрешено</span><span class="sxs-lookup"><span data-stu-id="3ac50-152">Allowed</span></span></p></td>
</tr>
</tbody>
</table>


<span data-ttu-id="3ac50-153">Позволяет **переместить** метод не гарантирует, что метод будет успешно найдите запись; только это означает, что вызов **Перемещение** указанный метод не возникнет ошибка.</span><span class="sxs-lookup"><span data-stu-id="3ac50-153">Allowing a **Move** method doesn't guarantee that the method will successfully locate a record; it only means that calling the specified **Move** method won't generate an error.</span></span>

<span data-ttu-id="3ac50-154">В следующей таблице показаны, что происходит с **BOF** или **EOF** параметров при вызове различные методы **перемещения** , но не удается найти запись успешно.</span><span class="sxs-lookup"><span data-stu-id="3ac50-154">The following table shows what happens to the **BOF** and **EOF** property settings when you call various **Move** methods but are unable to successfully locate a record.</span></span>

<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th><p></p></th>
<th><p><span data-ttu-id="3ac50-155">BOF</span><span class="sxs-lookup"><span data-stu-id="3ac50-155">BOF</span></span></p></th>
<th><p><span data-ttu-id="3ac50-156">ФУНКЦИЯ EOF</span><span class="sxs-lookup"><span data-stu-id="3ac50-156">EOF</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="3ac50-157"><strong>MoveFirst</strong> <strong>MoveLast</strong></span><span class="sxs-lookup"><span data-stu-id="3ac50-157"><strong>MoveFirst</strong>, <strong>MoveLast</strong></span></span></p></td>
<td><p><span data-ttu-id="3ac50-158">Значение <strong>True</strong></span><span class="sxs-lookup"><span data-stu-id="3ac50-158">Set to <strong>True</strong></span></span></p></td>
<td><p><span data-ttu-id="3ac50-159">Значение <strong>True</strong></span><span class="sxs-lookup"><span data-stu-id="3ac50-159">Set to <strong>True</strong></span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="3ac50-160"><strong>Перемещение</strong> 0</span><span class="sxs-lookup"><span data-stu-id="3ac50-160"><strong>Move</strong> 0</span></span></p></td>
<td><p><span data-ttu-id="3ac50-161">Без изменений</span><span class="sxs-lookup"><span data-stu-id="3ac50-161">No change</span></span></p></td>
<td><p><span data-ttu-id="3ac50-162">Без изменений</span><span class="sxs-lookup"><span data-stu-id="3ac50-162">No change</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="3ac50-163"><strong>MovePrevious</strong>, <strong>Переместите</strong> &lt; 0</span><span class="sxs-lookup"><span data-stu-id="3ac50-163"><strong>MovePrevious</strong>, <strong>Move</strong> &lt; 0</span></span></p></td>
<td><p><span data-ttu-id="3ac50-164">Значение <strong>True</strong></span><span class="sxs-lookup"><span data-stu-id="3ac50-164">Set to <strong>True</strong></span></span></p></td>
<td><p><span data-ttu-id="3ac50-165">Без изменений</span><span class="sxs-lookup"><span data-stu-id="3ac50-165">No change</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="3ac50-166"><strong>MoveNext</strong>, <strong>Переместите</strong> &gt; 0</span><span class="sxs-lookup"><span data-stu-id="3ac50-166"><strong>MoveNext</strong>, <strong>Move</strong> &gt; 0</span></span></p></td>
<td><p><span data-ttu-id="3ac50-167">Без изменений</span><span class="sxs-lookup"><span data-stu-id="3ac50-167">No change</span></span></p></td>
<td><p><span data-ttu-id="3ac50-168">Значение <strong>True</strong></span><span class="sxs-lookup"><span data-stu-id="3ac50-168">Set to <strong>True</strong></span></span></p></td>
</tr>
</tbody>
</table>

