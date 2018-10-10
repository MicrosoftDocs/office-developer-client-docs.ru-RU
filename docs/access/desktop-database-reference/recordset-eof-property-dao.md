---
title: Recordset.EOF Property (DAO)
TOCTitle: EOF Property
ms:assetid: aa82c6f9-89da-1061-437c-8ffb000744b6
ms:mtpsurl: https://msdn.microsoft.com/library/Ff821459(v=office.15)
ms:contentKeyID: 48546950
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: e800ce42b5ada2380dcb895814787ab4a9db6573
ms.sourcegitcommit: 19aca09c5812cfb98b68b5d4604dcaa814479df7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/09/2018
ms.locfileid: "25481133"
---
# <a name="recordseteof-property-dao"></a><span data-ttu-id="510f6-102">Recordset.EOF Property (DAO)</span><span class="sxs-lookup"><span data-stu-id="510f6-102">Recordset.EOF Property (DAO)</span></span>


<span data-ttu-id="510f6-103">**Применимо к**: Access 2013 | Office 2013</span><span class="sxs-lookup"><span data-stu-id="510f6-103">**Applies to**: Access 2013 | Office 2013</span></span>

<span data-ttu-id="510f6-104">Возвращает значение, указывающее, является ли положение текущей записи после последней записи в объекте **набора записей** .</span><span class="sxs-lookup"><span data-stu-id="510f6-104">Returns a value that indicates whether the current record position is after the last record in a **Recordset** object.</span></span> <span data-ttu-id="510f6-105">Только для чтения, **Boolean**.</span><span class="sxs-lookup"><span data-stu-id="510f6-105">Read-only **Boolean**.</span></span>

## <a name="syntax"></a><span data-ttu-id="510f6-106">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="510f6-106">Syntax</span></span>

<span data-ttu-id="510f6-107">*выражение* . ФУНКЦИЯ EOF</span><span class="sxs-lookup"><span data-stu-id="510f6-107">*expression* .EOF</span></span>

<span data-ttu-id="510f6-108">*выражение* Переменная, которая представляет собой объект **набора записей** .</span><span class="sxs-lookup"><span data-stu-id="510f6-108">*expression* A variable that represents a **Recordset** object.</span></span>

## <a name="remarks"></a><span data-ttu-id="510f6-109">Замечания</span><span class="sxs-lookup"><span data-stu-id="510f6-109">Remarks</span></span>

<span data-ttu-id="510f6-110">Свойства **BOF** и **EOF** можно использовать для определения того, содержит ли объект **набора записей** ли вы уменьшилось за пределы ограничения объекта **набора записей** , при перемещении по записям или записи.</span><span class="sxs-lookup"><span data-stu-id="510f6-110">You can use the **BOF** and **EOF** properties to determine whether a **Recordset** object contains records or whether you've gone beyond the limits of a **Recordset** object when you move from record to record.</span></span>

<span data-ttu-id="510f6-111">Определяет расположение указатель текущей записи **BOF** и **EOF** возвращаемые значения.</span><span class="sxs-lookup"><span data-stu-id="510f6-111">The location of the current record pointer determines the **BOF** and **EOF** return values.</span></span>

<span data-ttu-id="510f6-112">Если параметр **BOF** или **EOF** свойство имеет **значение True**, нет нет текущей записи.</span><span class="sxs-lookup"><span data-stu-id="510f6-112">If either the **BOF** or **EOF** property is **True**, there is no current record.</span></span>

<span data-ttu-id="510f6-113">При открытии объекта **набора записей** нет записей, содержащий **BOF** и **EOF** было задано значение **True**, и объекта **набора записей** **RecordCount** свойство имеет значение 0.</span><span class="sxs-lookup"><span data-stu-id="510f6-113">If you open a **Recordset** object containing no records, the **BOF** and **EOF** properties are set to **True**, and the **Recordset** object's **RecordCount** property setting is 0.</span></span> <span data-ttu-id="510f6-114">При открытии объекта **набора записей** , который содержит по крайней мере одна запись первой записи является текущей записи и свойства **BOF** и **EOF** — это **значение False**; они остаются **значение False** , пока не перемещать за пределы начала или окончания объекта **набора записей** с помощью **MovePrevious** или метод **MoveNext** , соответственно.</span><span class="sxs-lookup"><span data-stu-id="510f6-114">When you open a **Recordset** object that contains at least one record, the first record is the current record and the **BOF** and **EOF** properties are **False**; they remain **False** until you move beyond the beginning or end of the **Recordset** object by using the **MovePrevious** or **MoveNext** method, respectively.</span></span> <span data-ttu-id="510f6-115">При перемещении за пределы начале или конце **записей**нет текущей записи или запись не существует.</span><span class="sxs-lookup"><span data-stu-id="510f6-115">When you move beyond the beginning or end of the **Recordset**, there is no current record or no record exists.</span></span>

<span data-ttu-id="510f6-116">При удалении последней оставшиеся записи в объекте **набора записей** , свойства **BOF** и **EOF** может оставаться **значение False,** пока вы пытаетесь изменить положение текущей записи.</span><span class="sxs-lookup"><span data-stu-id="510f6-116">If you delete the last remaining record in the **Recordset** object, the **BOF** and **EOF** properties may remain **False** until you attempt to reposition the current record.</span></span>

<span data-ttu-id="510f6-117">При использовании метода **MoveLast** на объект **набора записей** , содержащий записи Последняя запись становится текущей; При использовании метода **MoveNext** текущей записи становится недействительным и свойство **EOF** имеет значение **True**.</span><span class="sxs-lookup"><span data-stu-id="510f6-117">If you use the **MoveLast** method on a **Recordset** object containing records, the last record becomes the current record; if you then use the **MoveNext** method, the current record becomes invalid and the **EOF** property is set to **True**.</span></span> <span data-ttu-id="510f6-118">С другой стороны при использовании метода **MoveFirst** на объект **набора записей** , содержащий записи первая запись становится текущей; При использовании метода **MovePrevious** нет текущей записи и **BOF** задано значение **True**.</span><span class="sxs-lookup"><span data-stu-id="510f6-118">Conversely, if you use the **MoveFirst** method on a **Recordset** object containing records, the first record becomes the current record; if you then use the **MovePrevious** method, there is no current record and the **BOF** property is set to **True**.</span></span>

<span data-ttu-id="510f6-119">Как правило при работе с всех записей в объекте **набора записей** код перебирает записей с помощью метода **MoveNext** , пока свойство **EOF** имеет значение **True**.</span><span class="sxs-lookup"><span data-stu-id="510f6-119">Typically, when you work with all the records in a **Recordset** object, your code will loop through the records by using the **MoveNext** method until the **EOF** property is set to **True**.</span></span>

<span data-ttu-id="510f6-120">Если вы используете метод **MoveNext** , хотя свойство **EOF** установлено значение **True,** либо метод **MovePrevious** во время **BOF** задано значение **True**, возникает ошибка.</span><span class="sxs-lookup"><span data-stu-id="510f6-120">If you use the **MoveNext** method while the **EOF** property is set to **True** or the **MovePrevious** method while the **BOF** property is set to **True**, an error occurs.</span></span>

<span data-ttu-id="510f6-121">В этой таблице показано, какие методы могут с помощью комбинации свойств **BOF** и **EOF** перемещения.</span><span class="sxs-lookup"><span data-stu-id="510f6-121">This table shows which Move methods are allowed with different combinations of the **BOF** and **EOF** properties.</span></span>

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
<th><p><span data-ttu-id="510f6-122">MoveFirst</span><span class="sxs-lookup"><span data-stu-id="510f6-122">MoveFirst,</span></span><br />
<span data-ttu-id="510f6-123">MoveLast</span><span class="sxs-lookup"><span data-stu-id="510f6-123">MoveLast</span></span></p></th>
<th><p><span data-ttu-id="510f6-124">MovePrevious,</span><span class="sxs-lookup"><span data-stu-id="510f6-124">MovePrevious,</span></span><br />
<span data-ttu-id="510f6-125">Перемещение &lt; 0</span><span class="sxs-lookup"><span data-stu-id="510f6-125">Move &lt; 0</span></span></p></th>
<th><p><br />
<span data-ttu-id="510f6-126">Перемещение 0</span><span class="sxs-lookup"><span data-stu-id="510f6-126">Move 0</span></span></p></th>
<th><p><span data-ttu-id="510f6-127">MoveNext,</span><span class="sxs-lookup"><span data-stu-id="510f6-127">MoveNext,</span></span><br />
<span data-ttu-id="510f6-128">Перемещение &gt; 0</span><span class="sxs-lookup"><span data-stu-id="510f6-128">Move &gt; 0</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="510f6-129"><strong>BOF = True,</strong></span><span class="sxs-lookup"><span data-stu-id="510f6-129"><strong>BOF=True,</strong></span></span><br /><span data-ttu-id="510f6-130">
<strong>Функция EOF = False</strong></span><span class="sxs-lookup"><span data-stu-id="510f6-130">
<strong>EOF=False</strong></span></span></p></td>
<td><p><span data-ttu-id="510f6-131">Разрешено</span><span class="sxs-lookup"><span data-stu-id="510f6-131">Allowed</span></span></p></td>
<td><p><span data-ttu-id="510f6-132">Error</span><span class="sxs-lookup"><span data-stu-id="510f6-132">Error</span></span></p></td>
<td><p><span data-ttu-id="510f6-133">Error</span><span class="sxs-lookup"><span data-stu-id="510f6-133">Error</span></span></p></td>
<td><p><span data-ttu-id="510f6-134">Разрешено</span><span class="sxs-lookup"><span data-stu-id="510f6-134">Allowed</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="510f6-135"><strong>BOF = False,</strong></span><span class="sxs-lookup"><span data-stu-id="510f6-135"><strong>BOF=False,</strong></span></span><br /><span data-ttu-id="510f6-136">
<strong>Функция EOF = True</strong></span><span class="sxs-lookup"><span data-stu-id="510f6-136">
<strong>EOF=True</strong></span></span></p></td>
<td><p><span data-ttu-id="510f6-137">Разрешено</span><span class="sxs-lookup"><span data-stu-id="510f6-137">Allowed</span></span></p></td>
<td><p><span data-ttu-id="510f6-138">Разрешено</span><span class="sxs-lookup"><span data-stu-id="510f6-138">Allowed</span></span></p></td>
<td><p><span data-ttu-id="510f6-139">Error</span><span class="sxs-lookup"><span data-stu-id="510f6-139">Error</span></span></p></td>
<td><p><span data-ttu-id="510f6-140">Error</span><span class="sxs-lookup"><span data-stu-id="510f6-140">Error</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="510f6-141">Оба <strong>значение True</strong></span><span class="sxs-lookup"><span data-stu-id="510f6-141">Both <strong>True</strong></span></span></p></td>
<td><p><span data-ttu-id="510f6-142">Error</span><span class="sxs-lookup"><span data-stu-id="510f6-142">Error</span></span></p></td>
<td><p><span data-ttu-id="510f6-143">Error</span><span class="sxs-lookup"><span data-stu-id="510f6-143">Error</span></span></p></td>
<td><p><span data-ttu-id="510f6-144">Error</span><span class="sxs-lookup"><span data-stu-id="510f6-144">Error</span></span></p></td>
<td><p><span data-ttu-id="510f6-145">Error</span><span class="sxs-lookup"><span data-stu-id="510f6-145">Error</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="510f6-146">Оба <strong>False</strong></span><span class="sxs-lookup"><span data-stu-id="510f6-146">Both <strong>False</strong></span></span></p></td>
<td><p><span data-ttu-id="510f6-147">Разрешено</span><span class="sxs-lookup"><span data-stu-id="510f6-147">Allowed</span></span></p></td>
<td><p><span data-ttu-id="510f6-148">Разрешено</span><span class="sxs-lookup"><span data-stu-id="510f6-148">Allowed</span></span></p></td>
<td><p><span data-ttu-id="510f6-149">Разрешено</span><span class="sxs-lookup"><span data-stu-id="510f6-149">Allowed</span></span></p></td>
<td><p><span data-ttu-id="510f6-150">Разрешено</span><span class="sxs-lookup"><span data-stu-id="510f6-150">Allowed</span></span></p></td>
</tr>
</tbody>
</table>


<span data-ttu-id="510f6-151">Разрешение метода Move не означает, что метод будет успешно найдите запись.</span><span class="sxs-lookup"><span data-stu-id="510f6-151">Allowing a Move method doesn't mean that the method will successfully locate a record.</span></span> <span data-ttu-id="510f6-152">Просто указывается, что при попытке выполнения указанного метода Move может и не возникнет ошибка.</span><span class="sxs-lookup"><span data-stu-id="510f6-152">It merely indicates that an attempt to perform the specified Move method is allowed and won't generate an error.</span></span> <span data-ttu-id="510f6-153">Состояние свойства **BOF** и **EOF** может меняться, попытка переместить.</span><span class="sxs-lookup"><span data-stu-id="510f6-153">The state of the **BOF** and **EOF** properties may change as a result of the attempted Move.</span></span>

<span data-ttu-id="510f6-154">Метод **OpenRecordset** во внутренней сети вызывает метод **MoveFirst** .</span><span class="sxs-lookup"><span data-stu-id="510f6-154">An **OpenRecordset** method internally invokes a **MoveFirst** method.</span></span> <span data-ttu-id="510f6-155">Таким образом с помощью метода **OpenRecordset** на пустой набор записей задает свойства **EOF** и **BOF** значение **True**.</span><span class="sxs-lookup"><span data-stu-id="510f6-155">Therefore, using an **OpenRecordset** method on an empty set of records sets the **BOF** and **EOF** properties to **True**.</span></span> <span data-ttu-id="510f6-156">(См. в следующей таблице поведение неудачных метод **MoveFirst** .)</span><span class="sxs-lookup"><span data-stu-id="510f6-156">(See the following table for the behavior of a failed **MoveFirst** method.)</span></span>

<span data-ttu-id="510f6-157">Все методы перемещения, которые успешно найдите запись установите **BOF** и **EOF** значение **False**.</span><span class="sxs-lookup"><span data-stu-id="510f6-157">All Move methods that successfully locate a record will set both **BOF** and **EOF** to **False**.</span></span>

<span data-ttu-id="510f6-158">В рабочей области Microsoft Access при добавлении записи в пустой **набор записей**, **BOF** станут **значение False**, однако **EOF** останутся **значение True**, это означает, что текущей позиции находится в конце **набора записей**.</span><span class="sxs-lookup"><span data-stu-id="510f6-158">In a Microsoft Access workspace, if you add a record to an empty **Recordset**, **BOF** will become **False**, but **EOF** will remain **True**, indicating that the current position is at the end of **Recordset**.</span></span>

<span data-ttu-id="510f6-159">Любой метод **Delete** , даже в том случае, если он удаляется только оставшиеся записи из **набора записей**не будет изменить значение параметра свойство **BOF** или **EOF** .</span><span class="sxs-lookup"><span data-stu-id="510f6-159">Any **Delete** method, even if it removes the only remaining record from a **Recordset**, won't change the setting of the **BOF** or **EOF** property.</span></span>

<span data-ttu-id="510f6-160">В следующей таблице показаны влияние перемещения методы, которые не найдите запись на параметры свойства **BOF** и **EOF** .</span><span class="sxs-lookup"><span data-stu-id="510f6-160">The following table shows how Move methods that don't locate a record affect the **BOF** and **EOF** property settings.</span></span>

<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th><p></p></th>
<th><p><span data-ttu-id="510f6-161">BOF</span><span class="sxs-lookup"><span data-stu-id="510f6-161">BOF</span></span></p></th>
<th><p><span data-ttu-id="510f6-162">ФУНКЦИЯ EOF</span><span class="sxs-lookup"><span data-stu-id="510f6-162">EOF</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="510f6-163"><strong>MoveFirst</strong> <strong>MoveLast</strong></span><span class="sxs-lookup"><span data-stu-id="510f6-163"><strong>MoveFirst</strong>, <strong>MoveLast</strong></span></span></p></td>
<td><p><span data-ttu-id="510f6-164"><strong>Значение true</strong></span><span class="sxs-lookup"><span data-stu-id="510f6-164"><strong>True</strong></span></span></p></td>
<td><p><span data-ttu-id="510f6-165"><strong>Значение true</strong></span><span class="sxs-lookup"><span data-stu-id="510f6-165"><strong>True</strong></span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="510f6-166"><strong>Перемещение</strong> 0</span><span class="sxs-lookup"><span data-stu-id="510f6-166"><strong>Move</strong> 0</span></span></p></td>
<td><p><span data-ttu-id="510f6-167">Без изменений</span><span class="sxs-lookup"><span data-stu-id="510f6-167">No change</span></span></p></td>
<td><p><span data-ttu-id="510f6-168">Без изменений</span><span class="sxs-lookup"><span data-stu-id="510f6-168">No change</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="510f6-169"><strong>MovePrevious</strong>, <strong>Переместите</strong> &lt; 0</span><span class="sxs-lookup"><span data-stu-id="510f6-169"><strong>MovePrevious</strong>, <strong>Move</strong> &lt; 0</span></span></p></td>
<td><p><span data-ttu-id="510f6-170"><strong>Значение true</strong></span><span class="sxs-lookup"><span data-stu-id="510f6-170"><strong>True</strong></span></span></p></td>
<td><p><span data-ttu-id="510f6-171">Без изменений</span><span class="sxs-lookup"><span data-stu-id="510f6-171">No change</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="510f6-172"><strong>MoveNext</strong>, <strong>Переместите</strong> &gt; 0</span><span class="sxs-lookup"><span data-stu-id="510f6-172"><strong>MoveNext</strong>, <strong>Move</strong> &gt; 0</span></span></p></td>
<td><p><span data-ttu-id="510f6-173">Без изменений</span><span class="sxs-lookup"><span data-stu-id="510f6-173">No change</span></span></p></td>
<td><p><span data-ttu-id="510f6-174"><strong>Значение true</strong></span><span class="sxs-lookup"><span data-stu-id="510f6-174"><strong>True</strong></span></span></p></td>
</tr>
</tbody>
</table>

