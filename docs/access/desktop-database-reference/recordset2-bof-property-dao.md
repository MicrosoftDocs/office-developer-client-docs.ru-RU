---
title: Свойство Recordset2.BOF (DAO)
TOCTitle: BOF Property
ms:assetid: d97d0507-0d5a-e3f1-fa30-40caec9f3ffa
ms:mtpsurl: https://msdn.microsoft.com/library/Ff835098(v=office.15)
ms:contentKeyID: 48548053
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: 5ffe9c679da3f11666799caa070f51f384729cc1
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32307464"
---
# <a name="recordset2bof-property-dao"></a><span data-ttu-id="3b5a5-102">Свойство Recordset2.BOF (DAO)</span><span class="sxs-lookup"><span data-stu-id="3b5a5-102">Recordset2.BOF property (DAO)</span></span>


<span data-ttu-id="3b5a5-103">**Область применения**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="3b5a5-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="3b5a5-104">Возвращает значение, которое показывает, находится ли текущее положение записи курсора перед первой записью объекта **Recordset**.</span><span class="sxs-lookup"><span data-stu-id="3b5a5-104">Returns a value that indicates whether the current record position is before the first record in a **Recordset** object.</span></span> <span data-ttu-id="3b5a5-105">Только для чтения, **Boolean**.</span><span class="sxs-lookup"><span data-stu-id="3b5a5-105">Read-only **Boolean**.</span></span>

## <a name="syntax"></a><span data-ttu-id="3b5a5-106">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="3b5a5-106">Syntax</span></span>

<span data-ttu-id="3b5a5-107">*выражение .* BOF</span><span class="sxs-lookup"><span data-stu-id="3b5a5-107">*expression* .BOF</span></span>

<span data-ttu-id="3b5a5-108">*выражение* Переменная, представляюная объект **Recordset2.**</span><span class="sxs-lookup"><span data-stu-id="3b5a5-108">*expression* A variable that represents a **Recordset2** object.</span></span>

## <a name="remarks"></a><span data-ttu-id="3b5a5-109">Комментарии</span><span class="sxs-lookup"><span data-stu-id="3b5a5-109">Remarks</span></span>

<span data-ttu-id="3b5a5-110">С помощью свойств **BOF** и **EOF** можно определить, содержит ли объект **Recordset** записи и не вышли ли вы за пределы объекта **Recordset** при переходе от записи к записи.</span><span class="sxs-lookup"><span data-stu-id="3b5a5-110">You can use the **BOF** and **EOF** properties to determine whether a **Recordset** object contains records or whether you've gone beyond the limits of a **Recordset** object when you move from record to record.</span></span>

<span data-ttu-id="3b5a5-111">Значения, возвращаемые свойствами **BOF** и **EOF**, определяются расположением указателя текущей записи.</span><span class="sxs-lookup"><span data-stu-id="3b5a5-111">The location of the current record pointer determines the **BOF** and **EOF** return values.</span></span>

<span data-ttu-id="3b5a5-112">Если любое из свойств **BOF** или **EOF** имеет значение **True**, то текущей записи нет.</span><span class="sxs-lookup"><span data-stu-id="3b5a5-112">If either the **BOF** or **EOF** property is **True**, there is no current record.</span></span>

<span data-ttu-id="3b5a5-113">Если открыть объект **Recordset**, не содержащий записей, свойства **BOF** и **EOF** будут иметь значение **True**, а свойство **RecordCount** объекта **Recordset** — значение 0.</span><span class="sxs-lookup"><span data-stu-id="3b5a5-113">If you open a **Recordset** object containing no records, the **BOF** and **EOF** properties are set to **True**, and the **Recordset** object's **RecordCount** property setting is 0.</span></span> <span data-ttu-id="3b5a5-114">Если открыть объект **Recordset**, содержащий хотя бы одну запись, первая запись будет текущей записью, а свойства **BOF** и **EOF** будут иметь значение **False**; они будут иметь значение **False** до тех пор, пока вы не переместитесь за начало или конец объекта **Recordset** с помощью метода **MovePrevious** или **MoveNext** соответственно.</span><span class="sxs-lookup"><span data-stu-id="3b5a5-114">When you open a **Recordset** object that contains at least one record, the first record is the current record and the **BOF** and **EOF** properties are **False**; they remain **False** until you move beyond the beginning or end of the **Recordset** object by using the **MovePrevious** or **MoveNext** method, respectively.</span></span> <span data-ttu-id="3b5a5-115">При переходе за пределы начала или конца наборов записей текущая запись или запись не существует.</span><span class="sxs-lookup"><span data-stu-id="3b5a5-115">When you move beyond the beginning or end of the recordset, there is no current record or no record exists.</span></span>

<span data-ttu-id="3b5a5-116">Если удалить последнюю оставшуюся запись в объекте **Recordset**, свойства **BOF** и **EOF** могут по-прежнему иметь значение **False**, пока вы не попытаетесь изменить позицию текущей записи.</span><span class="sxs-lookup"><span data-stu-id="3b5a5-116">If you delete the last remaining record in the **Recordset** object, the **BOF** and **EOF** properties may remain **False** until you attempt to reposition the current record.</span></span>

<span data-ttu-id="3b5a5-117">Если использовать метод **MoveLast** для объекта **Recordset**, содержащего записи, последняя запись станет текущей записью; если затем воспользоваться методом **MoveNext**, текущая запись станет недопустимой, и свойству **EOF** будет присвоено значение **True**.</span><span class="sxs-lookup"><span data-stu-id="3b5a5-117">If you use the **MoveLast** method on a **Recordset** object containing records, the last record becomes the current record; if you then use the **MoveNext** method, the current record becomes invalid and the **EOF** property is set to **True**.</span></span> <span data-ttu-id="3b5a5-118">И наоборот, если использовать метод **MoveFirst** для объекта **Recordset**, содержащего записи, первая запись станет текущей записью; если затем воспользоваться методом **MovePrevious**, текущей записи не будет, и свойству **BOF** будет присвоено значение **True**.</span><span class="sxs-lookup"><span data-stu-id="3b5a5-118">Conversely, if you use the **MoveFirst** method on a **Recordset** object containing records, the first record becomes the current record; if you then use the **MovePrevious** method, there is no current record and the **BOF** property is set to **True**.</span></span>

<span data-ttu-id="3b5a5-119">Обычно при работе со всеми записями в объекте **Recordset** код проходит через все записи с помощью метода **MoveNext**, пока значение свойства **EOF** не станет равно **True**.</span><span class="sxs-lookup"><span data-stu-id="3b5a5-119">Typically, when you work with all the records in a **Recordset** object, your code will loop through the records by using the **MoveNext** method until the **EOF** property is set to **True**.</span></span>

<span data-ttu-id="3b5a5-120">Если вы воспользуетесь методом **MoveNext**, когда свойство **EOF** имеет значение **True**, или методом **MovePrevious**, когда свойство **BOF** имеет значение **True**, возникнет ошибка.</span><span class="sxs-lookup"><span data-stu-id="3b5a5-120">If you use the **MoveNext** method while the **EOF** property is set to **True** or the **MovePrevious** method while the **BOF** property is set to **True**, an error occurs.</span></span>

<span data-ttu-id="3b5a5-121">В этой таблице показано, какие методы Move разрешено использовать при различных сочетаниях свойств **BOF** и **EOF**.</span><span class="sxs-lookup"><span data-stu-id="3b5a5-121">This table shows which Move methods are allowed with different combinations of the **BOF** and **EOF** properties.</span></span>

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
<th><p><span data-ttu-id="3b5a5-122">MoveFirst,</span><span class="sxs-lookup"><span data-stu-id="3b5a5-122">MoveFirst,</span></span><br />
<span data-ttu-id="3b5a5-123">MoveLast</span><span class="sxs-lookup"><span data-stu-id="3b5a5-123">MoveLast</span></span></p></th>
<th><p><span data-ttu-id="3b5a5-124">MovePrevious,</span><span class="sxs-lookup"><span data-stu-id="3b5a5-124">MovePrevious,</span></span><br />
<span data-ttu-id="3b5a5-125">Move &lt; 0</span><span class="sxs-lookup"><span data-stu-id="3b5a5-125">Move &lt; 0</span></span></p></th>
<th><p><br />
<span data-ttu-id="3b5a5-126">Move 0</span><span class="sxs-lookup"><span data-stu-id="3b5a5-126">Move 0</span></span></p></th>
<th><p><span data-ttu-id="3b5a5-127">MoveNext,</span><span class="sxs-lookup"><span data-stu-id="3b5a5-127">MoveNext,</span></span><br />
<span data-ttu-id="3b5a5-128">Move &gt; 0</span><span class="sxs-lookup"><span data-stu-id="3b5a5-128">Move &gt; 0</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="3b5a5-129"><strong>BOF=True,</strong></span><span class="sxs-lookup"><span data-stu-id="3b5a5-129"><strong>BOF=True,</strong></span></span><br /><span data-ttu-id="3b5a5-130">
<strong>EOF=False</strong></span><span class="sxs-lookup"><span data-stu-id="3b5a5-130">
<strong>EOF=False</strong></span></span></p></td>
<td><p><span data-ttu-id="3b5a5-131">Разрешено</span><span class="sxs-lookup"><span data-stu-id="3b5a5-131">Allowed</span></span></p></td>
<td><p><span data-ttu-id="3b5a5-132">Ошибка</span><span class="sxs-lookup"><span data-stu-id="3b5a5-132">Error</span></span></p></td>
<td><p><span data-ttu-id="3b5a5-133">Ошибка</span><span class="sxs-lookup"><span data-stu-id="3b5a5-133">Error</span></span></p></td>
<td><p><span data-ttu-id="3b5a5-134">Разрешено</span><span class="sxs-lookup"><span data-stu-id="3b5a5-134">Allowed</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="3b5a5-135"><strong>BOF=False,</strong></span><span class="sxs-lookup"><span data-stu-id="3b5a5-135"><strong>BOF=False,</strong></span></span><br /><span data-ttu-id="3b5a5-136">
<strong>EOF=True</strong></span><span class="sxs-lookup"><span data-stu-id="3b5a5-136">
<strong>EOF=True</strong></span></span></p></td>
<td><p><span data-ttu-id="3b5a5-137">Разрешено</span><span class="sxs-lookup"><span data-stu-id="3b5a5-137">Allowed</span></span></p></td>
<td><p><span data-ttu-id="3b5a5-138">Разрешено</span><span class="sxs-lookup"><span data-stu-id="3b5a5-138">Allowed</span></span></p></td>
<td><p><span data-ttu-id="3b5a5-139">Ошибка</span><span class="sxs-lookup"><span data-stu-id="3b5a5-139">Error</span></span></p></td>
<td><p><span data-ttu-id="3b5a5-140">Ошибка</span><span class="sxs-lookup"><span data-stu-id="3b5a5-140">Error</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="3b5a5-141">Оба свойства имеют значение <strong>True</strong></span><span class="sxs-lookup"><span data-stu-id="3b5a5-141">Both <strong>True</strong></span></span></p></td>
<td><p><span data-ttu-id="3b5a5-142">Ошибка</span><span class="sxs-lookup"><span data-stu-id="3b5a5-142">Error</span></span></p></td>
<td><p><span data-ttu-id="3b5a5-143">Ошибка</span><span class="sxs-lookup"><span data-stu-id="3b5a5-143">Error</span></span></p></td>
<td><p><span data-ttu-id="3b5a5-144">Ошибка</span><span class="sxs-lookup"><span data-stu-id="3b5a5-144">Error</span></span></p></td>
<td><p><span data-ttu-id="3b5a5-145">Ошибка</span><span class="sxs-lookup"><span data-stu-id="3b5a5-145">Error</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="3b5a5-146">Оба свойства имеют значение <strong>False</strong></span><span class="sxs-lookup"><span data-stu-id="3b5a5-146">Both <strong>False</strong></span></span></p></td>
<td><p><span data-ttu-id="3b5a5-147">Разрешено</span><span class="sxs-lookup"><span data-stu-id="3b5a5-147">Allowed</span></span></p></td>
<td><p><span data-ttu-id="3b5a5-148">Разрешено</span><span class="sxs-lookup"><span data-stu-id="3b5a5-148">Allowed</span></span></p></td>
<td><p><span data-ttu-id="3b5a5-149">Разрешено</span><span class="sxs-lookup"><span data-stu-id="3b5a5-149">Allowed</span></span></p></td>
<td><p><span data-ttu-id="3b5a5-150">Разрешено</span><span class="sxs-lookup"><span data-stu-id="3b5a5-150">Allowed</span></span></p></td>
</tr>
</tbody>
</table>


<span data-ttu-id="3b5a5-151">Разрешение использовать метод Move не означает, что этот метод успешно найдет запись.</span><span class="sxs-lookup"><span data-stu-id="3b5a5-151">Allowing a Move method doesn't mean that the method will successfully locate a record.</span></span> <span data-ttu-id="3b5a5-152">Это всего лишь значит, что попытки выполнить указанный метод Move разрешены и не приведут к возникновению ошибки.</span><span class="sxs-lookup"><span data-stu-id="3b5a5-152">It merely indicates that an attempt to perform the specified Move method is allowed and won't generate an error.</span></span> <span data-ttu-id="3b5a5-153">В результате выполнения методов Move состояние свойств **BOF** и **EOF** может изменяться.</span><span class="sxs-lookup"><span data-stu-id="3b5a5-153">The state of the **BOF** and **EOF** properties may change as a result of the attempted Move.</span></span>

<span data-ttu-id="3b5a5-154">Метод **OpenRecordset** внутренним образом вызывает метод **MoveFirst**.</span><span class="sxs-lookup"><span data-stu-id="3b5a5-154">An **OpenRecordset** method internally invokes a **MoveFirst** method.</span></span> <span data-ttu-id="3b5a5-155">Таким образом, при использовании метода **OpenRecordset** для пустого набора записей свойствам **BOF** и **EOF** будет присвоено значение **True**.</span><span class="sxs-lookup"><span data-stu-id="3b5a5-155">Therefore, using an **OpenRecordset** method on an empty set of records sets the **BOF** and **EOF** properties to **True**.</span></span> <span data-ttu-id="3b5a5-156">(Сведения о том, как ведет себя метод **MoveFirst** при его неудачном выполнении, см. в приведенной ниже таблице.)</span><span class="sxs-lookup"><span data-stu-id="3b5a5-156">(See the following table for the behavior of a failed **MoveFirst** method.)</span></span>

<span data-ttu-id="3b5a5-157">Если любой метод Move успешно находит запись, свойствам **BOF** и **EOF** присваивается значение **False**.</span><span class="sxs-lookup"><span data-stu-id="3b5a5-157">All Move methods that successfully locate a record will set both **BOF** and **EOF** to **False**.</span></span>

<span data-ttu-id="3b5a5-158">В рабочей области Microsoft Access, если добавить запись в пустой набор записей, **BOF** станет **False,** но **EOF** останется **True,** что означает, что текущая позиция находится в конце набор записей.</span><span class="sxs-lookup"><span data-stu-id="3b5a5-158">In a Microsoft Access workspace, if you add a record to an empty recordset, **BOF** will become **False**, but **EOF** will remain **True**, indicating that the current position is at the end of recordset.</span></span>

<span data-ttu-id="3b5a5-159">Любой **метод Delete,** даже если он удаляет единственную оставшиеся записи из объекта recordset, не меняет параметры свойства **BOF** или **EOF.**</span><span class="sxs-lookup"><span data-stu-id="3b5a5-159">Any **Delete** method, even if it removes the only remaining record from a recordset, won't change the setting of the **BOF** or **EOF** property.</span></span>

<span data-ttu-id="3b5a5-160">В приведенной ниже таблице показано, как методы Move, которым не удалось найти запись, влияют на значения свойств **BOF** и **EOF**.</span><span class="sxs-lookup"><span data-stu-id="3b5a5-160">The following table shows how Move methods that don't locate a record affect the **BOF** and **EOF** property settings.</span></span>

<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th><p></p></th>
<th><p><span data-ttu-id="3b5a5-161">BOF</span><span class="sxs-lookup"><span data-stu-id="3b5a5-161">BOF</span></span></p></th>
<th><p><span data-ttu-id="3b5a5-162">EOF</span><span class="sxs-lookup"><span data-stu-id="3b5a5-162">EOF</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="3b5a5-163"><strong>MoveFirst</strong>, <strong>MoveLast</strong></span><span class="sxs-lookup"><span data-stu-id="3b5a5-163"><strong>MoveFirst</strong>, <strong>MoveLast</strong></span></span></p></td>
<td><p><span data-ttu-id="3b5a5-164"><strong>True</strong></span><span class="sxs-lookup"><span data-stu-id="3b5a5-164"><strong>True</strong></span></span></p></td>
<td><p><span data-ttu-id="3b5a5-165"><strong>True</strong></span><span class="sxs-lookup"><span data-stu-id="3b5a5-165"><strong>True</strong></span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="3b5a5-166"><strong>Move</strong> 0</span><span class="sxs-lookup"><span data-stu-id="3b5a5-166"><strong>Move</strong> 0</span></span></p></td>
<td><p><span data-ttu-id="3b5a5-167">Без изменений</span><span class="sxs-lookup"><span data-stu-id="3b5a5-167">No change</span></span></p></td>
<td><p><span data-ttu-id="3b5a5-168">Без изменений</span><span class="sxs-lookup"><span data-stu-id="3b5a5-168">No change</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="3b5a5-169"><strong>MovePrevious</strong>, <strong>Move</strong> &lt; 0</span><span class="sxs-lookup"><span data-stu-id="3b5a5-169"><strong>MovePrevious</strong>, <strong>Move</strong> &lt; 0</span></span></p></td>
<td><p><span data-ttu-id="3b5a5-170"><strong>True</strong></span><span class="sxs-lookup"><span data-stu-id="3b5a5-170"><strong>True</strong></span></span></p></td>
<td><p><span data-ttu-id="3b5a5-171">Без изменений</span><span class="sxs-lookup"><span data-stu-id="3b5a5-171">No change</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="3b5a5-172"><strong>MoveNext</strong>, <strong>Move</strong> &gt; 0</span><span class="sxs-lookup"><span data-stu-id="3b5a5-172"><strong>MoveNext</strong>, <strong>Move</strong> &gt; 0</span></span></p></td>
<td><p><span data-ttu-id="3b5a5-173">Без изменений</span><span class="sxs-lookup"><span data-stu-id="3b5a5-173">No change</span></span></p></td>
<td><p><span data-ttu-id="3b5a5-174"><strong>True</strong></span><span class="sxs-lookup"><span data-stu-id="3b5a5-174"><strong>True</strong></span></span></p></td>
</tr>
</tbody>
</table>

