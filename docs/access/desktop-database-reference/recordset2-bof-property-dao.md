---
title: Recordset2.BOF Property (DAO)
TOCTitle: BOF Property
ms:assetid: d97d0507-0d5a-e3f1-fa30-40caec9f3ffa
ms:mtpsurl: https://msdn.microsoft.com/library/Ff835098(v=office.15)
ms:contentKeyID: 48548053
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 9e85b86d2ccfeaddd56f5373684e8790ee1ab0b2
ms.sourcegitcommit: c557bbcccf37a6011f89aae1ddd399dfe549d087
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/31/2018
ms.locfileid: "25876423"
---
# <a name="recordset2bof-property-dao"></a><span data-ttu-id="d1312-102">Recordset2.BOF Property (DAO)</span><span class="sxs-lookup"><span data-stu-id="d1312-102">Recordset2.BOF Property (DAO)</span></span>


<span data-ttu-id="d1312-103">**Применимо к**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="d1312-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="d1312-104">Возвращает значение, указывающее, является ли положение текущей записи перед первой записи в объекте **набора записей** .</span><span class="sxs-lookup"><span data-stu-id="d1312-104">Returns a value that indicates whether the current record position is before the first record in a **Recordset** object.</span></span> <span data-ttu-id="d1312-105">Только для чтения, **Boolean**.</span><span class="sxs-lookup"><span data-stu-id="d1312-105">Read-only **Boolean**.</span></span>

## <a name="syntax"></a><span data-ttu-id="d1312-106">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="d1312-106">Syntax</span></span>

<span data-ttu-id="d1312-107">*выражение* . BOF</span><span class="sxs-lookup"><span data-stu-id="d1312-107">*expression* .BOF</span></span>

<span data-ttu-id="d1312-108">*выражение* Переменная, которая представляет собой объект- **Recordset2** .</span><span class="sxs-lookup"><span data-stu-id="d1312-108">*expression* A variable that represents a **Recordset2** object.</span></span>

## <a name="remarks"></a><span data-ttu-id="d1312-109">Замечания</span><span class="sxs-lookup"><span data-stu-id="d1312-109">Remarks</span></span>

<span data-ttu-id="d1312-110">Свойства **BOF** и **EOF** можно использовать для определения того, содержит ли объект **набора записей** ли вы уменьшилось за пределы ограничения объекта **набора записей** , при перемещении по записям или записи.</span><span class="sxs-lookup"><span data-stu-id="d1312-110">You can use the **BOF** and **EOF** properties to determine whether a **Recordset** object contains records or whether you've gone beyond the limits of a **Recordset** object when you move from record to record.</span></span>

<span data-ttu-id="d1312-111">Определяет расположение указатель текущей записи **BOF** и **EOF** возвращаемые значения.</span><span class="sxs-lookup"><span data-stu-id="d1312-111">The location of the current record pointer determines the **BOF** and **EOF** return values.</span></span>

<span data-ttu-id="d1312-112">Если параметр **BOF** или **EOF** свойство имеет **значение True**, нет нет текущей записи.</span><span class="sxs-lookup"><span data-stu-id="d1312-112">If either the **BOF** or **EOF** property is **True**, there is no current record.</span></span>

<span data-ttu-id="d1312-113">При открытии объекта **набора записей** нет записей, содержащий **BOF** и **EOF** было задано значение **True**, и объекта **набора записей** **RecordCount** свойство имеет значение 0.</span><span class="sxs-lookup"><span data-stu-id="d1312-113">If you open a **Recordset** object containing no records, the **BOF** and **EOF** properties are set to **True**, and the **Recordset** object's **RecordCount** property setting is 0.</span></span> <span data-ttu-id="d1312-114">При открытии объекта **набора записей** , который содержит по крайней мере одна запись первой записи является текущей записи и свойства **BOF** и **EOF** — это **значение False**; они остаются **значение False** , пока не перемещать за пределы начала или окончания объекта **набора записей** с помощью **MovePrevious** или метод **MoveNext** , соответственно.</span><span class="sxs-lookup"><span data-stu-id="d1312-114">When you open a **Recordset** object that contains at least one record, the first record is the current record and the **BOF** and **EOF** properties are **False**; they remain **False** until you move beyond the beginning or end of the **Recordset** object by using the **MovePrevious** or **MoveNext** method, respectively.</span></span> <span data-ttu-id="d1312-115">При перемещении за пределы начале или конце набора записей нет текущей записи или запись не существует.</span><span class="sxs-lookup"><span data-stu-id="d1312-115">When you move beyond the beginning or end of the recordset, there is no current record or no record exists.</span></span>

<span data-ttu-id="d1312-116">При удалении последней оставшиеся записи в объекте **набора записей** , свойства **BOF** и **EOF** может оставаться **значение False,** пока вы пытаетесь изменить положение текущей записи.</span><span class="sxs-lookup"><span data-stu-id="d1312-116">If you delete the last remaining record in the **Recordset** object, the **BOF** and **EOF** properties may remain **False** until you attempt to reposition the current record.</span></span>

<span data-ttu-id="d1312-117">При использовании метода **MoveLast** на объект **набора записей** , содержащий записи Последняя запись становится текущей; При использовании метода **MoveNext** текущей записи становится недействительным и свойство **EOF** имеет значение **True**.</span><span class="sxs-lookup"><span data-stu-id="d1312-117">If you use the **MoveLast** method on a **Recordset** object containing records, the last record becomes the current record; if you then use the **MoveNext** method, the current record becomes invalid and the **EOF** property is set to **True**.</span></span> <span data-ttu-id="d1312-118">С другой стороны при использовании метода **MoveFirst** на объект **набора записей** , содержащий записи первая запись становится текущей; При использовании метода **MovePrevious** нет текущей записи и **BOF** задано значение **True**.</span><span class="sxs-lookup"><span data-stu-id="d1312-118">Conversely, if you use the **MoveFirst** method on a **Recordset** object containing records, the first record becomes the current record; if you then use the **MovePrevious** method, there is no current record and the **BOF** property is set to **True**.</span></span>

<span data-ttu-id="d1312-119">Как правило при работе с всех записей в объекте **набора записей** код перебирает записей с помощью метода **MoveNext** , пока свойство **EOF** имеет значение **True**.</span><span class="sxs-lookup"><span data-stu-id="d1312-119">Typically, when you work with all the records in a **Recordset** object, your code will loop through the records by using the **MoveNext** method until the **EOF** property is set to **True**.</span></span>

<span data-ttu-id="d1312-120">Если вы используете метод **MoveNext** , хотя свойство **EOF** установлено значение **True,** либо метод **MovePrevious** во время **BOF** задано значение **True**, возникает ошибка.</span><span class="sxs-lookup"><span data-stu-id="d1312-120">If you use the **MoveNext** method while the **EOF** property is set to **True** or the **MovePrevious** method while the **BOF** property is set to **True**, an error occurs.</span></span>

<span data-ttu-id="d1312-121">В этой таблице показано, какие методы могут с помощью комбинации свойств **BOF** и **EOF** перемещения.</span><span class="sxs-lookup"><span data-stu-id="d1312-121">This table shows which Move methods are allowed with different combinations of the **BOF** and **EOF** properties.</span></span>

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
<th><p><span data-ttu-id="d1312-122">MoveFirst</span><span class="sxs-lookup"><span data-stu-id="d1312-122">MoveFirst,</span></span><br />
<span data-ttu-id="d1312-123">MoveLast</span><span class="sxs-lookup"><span data-stu-id="d1312-123">MoveLast</span></span></p></th>
<th><p><span data-ttu-id="d1312-124">MovePrevious,</span><span class="sxs-lookup"><span data-stu-id="d1312-124">MovePrevious,</span></span><br />
<span data-ttu-id="d1312-125">Перемещение &lt; 0</span><span class="sxs-lookup"><span data-stu-id="d1312-125">Move &lt; 0</span></span></p></th>
<th><p><br />
<span data-ttu-id="d1312-126">Перемещение 0</span><span class="sxs-lookup"><span data-stu-id="d1312-126">Move 0</span></span></p></th>
<th><p><span data-ttu-id="d1312-127">MoveNext,</span><span class="sxs-lookup"><span data-stu-id="d1312-127">MoveNext,</span></span><br />
<span data-ttu-id="d1312-128">Перемещение &gt; 0</span><span class="sxs-lookup"><span data-stu-id="d1312-128">Move &gt; 0</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="d1312-129"><strong>BOF = True,</strong></span><span class="sxs-lookup"><span data-stu-id="d1312-129"><strong>BOF=True,</strong></span></span><br /><span data-ttu-id="d1312-130">
<strong>Функция EOF = False</strong></span><span class="sxs-lookup"><span data-stu-id="d1312-130">
<strong>EOF=False</strong></span></span></p></td>
<td><p><span data-ttu-id="d1312-131">Разрешено</span><span class="sxs-lookup"><span data-stu-id="d1312-131">Allowed</span></span></p></td>
<td><p><span data-ttu-id="d1312-132">Error</span><span class="sxs-lookup"><span data-stu-id="d1312-132">Error</span></span></p></td>
<td><p><span data-ttu-id="d1312-133">Error</span><span class="sxs-lookup"><span data-stu-id="d1312-133">Error</span></span></p></td>
<td><p><span data-ttu-id="d1312-134">Разрешено</span><span class="sxs-lookup"><span data-stu-id="d1312-134">Allowed</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="d1312-135"><strong>BOF = False,</strong></span><span class="sxs-lookup"><span data-stu-id="d1312-135"><strong>BOF=False,</strong></span></span><br /><span data-ttu-id="d1312-136">
<strong>Функция EOF = True</strong></span><span class="sxs-lookup"><span data-stu-id="d1312-136">
<strong>EOF=True</strong></span></span></p></td>
<td><p><span data-ttu-id="d1312-137">Разрешено</span><span class="sxs-lookup"><span data-stu-id="d1312-137">Allowed</span></span></p></td>
<td><p><span data-ttu-id="d1312-138">Разрешено</span><span class="sxs-lookup"><span data-stu-id="d1312-138">Allowed</span></span></p></td>
<td><p><span data-ttu-id="d1312-139">Error</span><span class="sxs-lookup"><span data-stu-id="d1312-139">Error</span></span></p></td>
<td><p><span data-ttu-id="d1312-140">Error</span><span class="sxs-lookup"><span data-stu-id="d1312-140">Error</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="d1312-141">Оба <strong>значение True</strong></span><span class="sxs-lookup"><span data-stu-id="d1312-141">Both <strong>True</strong></span></span></p></td>
<td><p><span data-ttu-id="d1312-142">Error</span><span class="sxs-lookup"><span data-stu-id="d1312-142">Error</span></span></p></td>
<td><p><span data-ttu-id="d1312-143">Error</span><span class="sxs-lookup"><span data-stu-id="d1312-143">Error</span></span></p></td>
<td><p><span data-ttu-id="d1312-144">Error</span><span class="sxs-lookup"><span data-stu-id="d1312-144">Error</span></span></p></td>
<td><p><span data-ttu-id="d1312-145">Error</span><span class="sxs-lookup"><span data-stu-id="d1312-145">Error</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="d1312-146">Оба <strong>False</strong></span><span class="sxs-lookup"><span data-stu-id="d1312-146">Both <strong>False</strong></span></span></p></td>
<td><p><span data-ttu-id="d1312-147">Разрешено</span><span class="sxs-lookup"><span data-stu-id="d1312-147">Allowed</span></span></p></td>
<td><p><span data-ttu-id="d1312-148">Разрешено</span><span class="sxs-lookup"><span data-stu-id="d1312-148">Allowed</span></span></p></td>
<td><p><span data-ttu-id="d1312-149">Разрешено</span><span class="sxs-lookup"><span data-stu-id="d1312-149">Allowed</span></span></p></td>
<td><p><span data-ttu-id="d1312-150">Разрешено</span><span class="sxs-lookup"><span data-stu-id="d1312-150">Allowed</span></span></p></td>
</tr>
</tbody>
</table>


<span data-ttu-id="d1312-151">Разрешение метода Move не означает, что метод будет успешно найдите запись.</span><span class="sxs-lookup"><span data-stu-id="d1312-151">Allowing a Move method doesn't mean that the method will successfully locate a record.</span></span> <span data-ttu-id="d1312-152">Просто указывается, что при попытке выполнения указанного метода Move может и не возникнет ошибка.</span><span class="sxs-lookup"><span data-stu-id="d1312-152">It merely indicates that an attempt to perform the specified Move method is allowed and won't generate an error.</span></span> <span data-ttu-id="d1312-153">Состояние свойства **BOF** и **EOF** может меняться, попытка переместить.</span><span class="sxs-lookup"><span data-stu-id="d1312-153">The state of the **BOF** and **EOF** properties may change as a result of the attempted Move.</span></span>

<span data-ttu-id="d1312-154">Метод **OpenRecordset** во внутренней сети вызывает метод **MoveFirst** .</span><span class="sxs-lookup"><span data-stu-id="d1312-154">An **OpenRecordset** method internally invokes a **MoveFirst** method.</span></span> <span data-ttu-id="d1312-155">Таким образом с помощью метода **OpenRecordset** на пустой набор записей задает свойства **EOF** и **BOF** значение **True**.</span><span class="sxs-lookup"><span data-stu-id="d1312-155">Therefore, using an **OpenRecordset** method on an empty set of records sets the **BOF** and **EOF** properties to **True**.</span></span> <span data-ttu-id="d1312-156">(См. в следующей таблице поведение неудачных метод **MoveFirst** .)</span><span class="sxs-lookup"><span data-stu-id="d1312-156">(See the following table for the behavior of a failed **MoveFirst** method.)</span></span>

<span data-ttu-id="d1312-157">Все методы перемещения, которые успешно найдите запись установите **BOF** и **EOF** значение **False**.</span><span class="sxs-lookup"><span data-stu-id="d1312-157">All Move methods that successfully locate a record will set both **BOF** and **EOF** to **False**.</span></span>

<span data-ttu-id="d1312-158">В рабочей области Microsoft Access при добавлении записи в пустой записей, **BOF** станут **значение False**, однако **EOF** останутся **значение True**, это означает, что текущей позиции находится в конце набора записей.</span><span class="sxs-lookup"><span data-stu-id="d1312-158">In a Microsoft Access workspace, if you add a record to an empty recordset, **BOF** will become **False**, but **EOF** will remain **True**, indicating that the current position is at the end of recordset.</span></span>

<span data-ttu-id="d1312-159">Любой метод **Delete** , даже в том случае, если он удаляется только оставшиеся записи из набора записей не будет изменить значение параметра свойство **BOF** или **EOF** .</span><span class="sxs-lookup"><span data-stu-id="d1312-159">Any **Delete** method, even if it removes the only remaining record from a recordset, won't change the setting of the **BOF** or **EOF** property.</span></span>

<span data-ttu-id="d1312-160">В следующей таблице показаны влияние перемещения методы, которые не найдите запись на параметры свойства **BOF** и **EOF** .</span><span class="sxs-lookup"><span data-stu-id="d1312-160">The following table shows how Move methods that don't locate a record affect the **BOF** and **EOF** property settings.</span></span>

<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th><p></p></th>
<th><p><span data-ttu-id="d1312-161">BOF</span><span class="sxs-lookup"><span data-stu-id="d1312-161">BOF</span></span></p></th>
<th><p><span data-ttu-id="d1312-162">ФУНКЦИЯ EOF</span><span class="sxs-lookup"><span data-stu-id="d1312-162">EOF</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="d1312-163"><strong>MoveFirst</strong> <strong>MoveLast</strong></span><span class="sxs-lookup"><span data-stu-id="d1312-163"><strong>MoveFirst</strong>, <strong>MoveLast</strong></span></span></p></td>
<td><p><span data-ttu-id="d1312-164"><strong>Значение true</strong></span><span class="sxs-lookup"><span data-stu-id="d1312-164"><strong>True</strong></span></span></p></td>
<td><p><span data-ttu-id="d1312-165"><strong>Значение true</strong></span><span class="sxs-lookup"><span data-stu-id="d1312-165"><strong>True</strong></span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="d1312-166"><strong>Перемещение</strong> 0</span><span class="sxs-lookup"><span data-stu-id="d1312-166"><strong>Move</strong> 0</span></span></p></td>
<td><p><span data-ttu-id="d1312-167">Без изменений</span><span class="sxs-lookup"><span data-stu-id="d1312-167">No change</span></span></p></td>
<td><p><span data-ttu-id="d1312-168">Без изменений</span><span class="sxs-lookup"><span data-stu-id="d1312-168">No change</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="d1312-169"><strong>MovePrevious</strong>, <strong>Переместите</strong> &lt; 0</span><span class="sxs-lookup"><span data-stu-id="d1312-169"><strong>MovePrevious</strong>, <strong>Move</strong> &lt; 0</span></span></p></td>
<td><p><span data-ttu-id="d1312-170"><strong>Значение true</strong></span><span class="sxs-lookup"><span data-stu-id="d1312-170"><strong>True</strong></span></span></p></td>
<td><p><span data-ttu-id="d1312-171">Без изменений</span><span class="sxs-lookup"><span data-stu-id="d1312-171">No change</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="d1312-172"><strong>MoveNext</strong>, <strong>Переместите</strong> &gt; 0</span><span class="sxs-lookup"><span data-stu-id="d1312-172"><strong>MoveNext</strong>, <strong>Move</strong> &gt; 0</span></span></p></td>
<td><p><span data-ttu-id="d1312-173">Без изменений</span><span class="sxs-lookup"><span data-stu-id="d1312-173">No change</span></span></p></td>
<td><p><span data-ttu-id="d1312-174"><strong>Значение true</strong></span><span class="sxs-lookup"><span data-stu-id="d1312-174"><strong>True</strong></span></span></p></td>
</tr>
</tbody>
</table>

