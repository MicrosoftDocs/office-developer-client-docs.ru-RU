---
title: Метод Recordset.Move (DAO)
TOCTitle: Move Method
ms:assetid: 21ca5ab5-ff71-1ae8-21b3-8991d5f795cf
ms:mtpsurl: https://msdn.microsoft.com/library/Ff191697(v=office.15)
ms:contentKeyID: 48543689
ms.date: 09/18/2015
mtps_version: v=office.15
f1_keywords:
- dao360.chm1052941
f1_categories:
- Office.Version=v15
localization_priority: Priority
ms.openlocfilehash: 1f10b5b779141189f114e420b3f7d4827e701161
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32284801"
---
# <a name="recordsetmove-method-dao"></a><span data-ttu-id="7ee56-102">Метод Recordset.Move (DAO)</span><span class="sxs-lookup"><span data-stu-id="7ee56-102">Recordset.Move method (DAO)</span></span>

<span data-ttu-id="7ee56-103">**Область применения**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="7ee56-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="7ee56-104">Перемещает положение текущей записи в объекте **[Recordset](recordset-object-dao.md)**.</span><span class="sxs-lookup"><span data-stu-id="7ee56-104">Moves the position of the current record in a **[Recordset](recordset-object-dao.md)** object.</span></span>

## <a name="syntax"></a><span data-ttu-id="7ee56-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="7ee56-105">Syntax</span></span>

<span data-ttu-id="7ee56-106">*expression* .Move(***Rows***, ***StartBookmark***)</span><span class="sxs-lookup"><span data-stu-id="7ee56-106">*expression* .Move(***Rows***, ***StartBookmark***)</span></span>

<span data-ttu-id="7ee56-107">*expression*: переменная, представляющая объект **Recordset**.</span><span class="sxs-lookup"><span data-stu-id="7ee56-107">*expression* A variable that represents a **Recordset** object.</span></span>

## <a name="parameters"></a><span data-ttu-id="7ee56-108">Параметры</span><span class="sxs-lookup"><span data-stu-id="7ee56-108">Parameters</span></span>

<table>
<colgroup>
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="7ee56-109">Имя</span><span class="sxs-lookup"><span data-stu-id="7ee56-109">Name</span></span></p></th>
<th><p><span data-ttu-id="7ee56-110">Обязательный/необязательный</span><span class="sxs-lookup"><span data-stu-id="7ee56-110">Required/optional</span></span></p></th>
<th><p><span data-ttu-id="7ee56-111">Тип данных</span><span class="sxs-lookup"><span data-stu-id="7ee56-111">Data type</span></span></p></th>
<th><p><span data-ttu-id="7ee56-112">Описание</span><span class="sxs-lookup"><span data-stu-id="7ee56-112">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="7ee56-113"><em>Rows</em></span><span class="sxs-lookup"><span data-stu-id="7ee56-113"><em>Rows</em></span></span></p></td>
<td><p><span data-ttu-id="7ee56-114">Обязательный</span><span class="sxs-lookup"><span data-stu-id="7ee56-114">Required</span></span></p></td>
<td><p><span data-ttu-id="7ee56-115"><strong>Long</strong></span><span class="sxs-lookup"><span data-stu-id="7ee56-115"><strong>Long</strong></span></span></p></td>
<td><p><span data-ttu-id="7ee56-116">Количество строк, на которое сдвинется положение.</span><span class="sxs-lookup"><span data-stu-id="7ee56-116">The number of rows the position will move.</span></span> <span data-ttu-id="7ee56-117">Если значение rows больше 0, то положение смещается вперед (к концу файла).</span><span class="sxs-lookup"><span data-stu-id="7ee56-117">If rows is greater than 0, the position is moved forward (toward the end of the file).</span></span> <span data-ttu-id="7ee56-118">Если оно меньше 0, то положение смещается назад (к началу файла).</span><span class="sxs-lookup"><span data-stu-id="7ee56-118">If rows is less than 0, the position is moved backward (toward the beginning of the file).</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="7ee56-119"><em>StartBookmark</em></span><span class="sxs-lookup"><span data-stu-id="7ee56-119"><em>StartBookmark</em></span></span></p></td>
<td><p><span data-ttu-id="7ee56-120">Необязательный</span><span class="sxs-lookup"><span data-stu-id="7ee56-120">Optional</span></span></p></td>
<td><p><span data-ttu-id="7ee56-121"><strong>Variant</strong></span><span class="sxs-lookup"><span data-stu-id="7ee56-121"><strong>Variant</strong></span></span></p></td>
<td><p><span data-ttu-id="7ee56-122">Значение, определяющее закладку.</span><span class="sxs-lookup"><span data-stu-id="7ee56-122">A value identifying a bookmark.</span></span> <span data-ttu-id="7ee56-123">Если указать значение startbookmark, смещение начнется относительно закладки.</span><span class="sxs-lookup"><span data-stu-id="7ee56-123">If you specify startbookmark, the move begins relative to this bookmark.</span></span> <span data-ttu-id="7ee56-124">В противном случае оно начнется с текущей записи.</span><span class="sxs-lookup"><span data-stu-id="7ee56-124">Otherwise, Move begins from the current record.</span></span></p></td>
</tr>
</tbody>
</table>


## <a name="remarks"></a><span data-ttu-id="7ee56-125">Примечания</span><span class="sxs-lookup"><span data-stu-id="7ee56-125">Remarks</span></span>

<span data-ttu-id="7ee56-126">Если с помощью метода **Move** поместить указатель текущей записи перед первой записью, то указатель текущей записи переместится в начало файла.</span><span class="sxs-lookup"><span data-stu-id="7ee56-126">If you use **Move** to position the current record pointer before the first record, the current record pointer moves to the beginning of the file.</span></span> <span data-ttu-id="7ee56-127">Если объект **Recordset** не содержит записей, а для его свойства **[BOF](recordset-bof-property-dao.md)** задано значение **True**, то при попытке использовать этот метод для перемещения назад возникнет ошибка.</span><span class="sxs-lookup"><span data-stu-id="7ee56-127">If the **Recordset** contains no records and its **[BOF](recordset-bof-property-dao.md)** property is **True**, using this method to move backward causes an error.</span></span>

<span data-ttu-id="7ee56-128">Если с помощью метода **Move** поместить указатель текущей записи после последней записи, то указатель текущей записи переместится в конец файла.</span><span class="sxs-lookup"><span data-stu-id="7ee56-128">If you use **Move** to position the current record pointer after the last record, the current record pointer position moves to the end of the file.</span></span> <span data-ttu-id="7ee56-129">Если объект **Recordset** не содержит записей, а для его свойства **[EOF](recordset-eof-property-dao.md)** задано значение **True**, то при попытке использовать этот метод для перемещения вперед возникнет ошибка.</span><span class="sxs-lookup"><span data-stu-id="7ee56-129">If the **Recordset** contains no records and its **[EOF](recordset-eof-property-dao.md)** property is **True**, then using this method to move forward causes an error.</span></span>

<span data-ttu-id="7ee56-130">Если для свойства **BOF** или **EOF** задано значение **True**, а вы попытаетесь использовать метод **Move** без действительной закладки, возникнет ошибка во время выполнения.</span><span class="sxs-lookup"><span data-stu-id="7ee56-130">If either the **BOF** or **EOF** property is **True** and you attempt to use the **Move** method without a valid bookmark, a run-time error occurs.</span></span>

> [!NOTE]
> - <span data-ttu-id="7ee56-131">Если использовать метод **Move** для однонаправленного объекта **Recordset**, значение аргумента rows должно быть положительным целым числом, а использование закладок не допускается.</span><span class="sxs-lookup"><span data-stu-id="7ee56-131">When you use **Move** on a forward-only-type **Recordset** object, the rows argument must be a positive integer and bookmarks aren't allowed.</span></span> <span data-ttu-id="7ee56-132">Это означает, что перемещать запись можно только вперед.</span><span class="sxs-lookup"><span data-stu-id="7ee56-132">This means you can only move forward.</span></span>
> - <span data-ttu-id="7ee56-133">Чтобы сделать первую, последнюю, следующую или предыдущую запись в объекте **Recordset** текущей, используйте метод **MoveFirst**, **MoveLast**, **MoveNext** или **MovePrevious**.</span><span class="sxs-lookup"><span data-stu-id="7ee56-133">To make the first, last, next, or previous record in a **Recordset** the current record, use either the **MoveFirst**, **MoveLast**, **MoveNext**, or **MovePrevious** method.</span></span>
> - <span data-ttu-id="7ee56-134">Используя метод **Move** и задав для аргумента rows значение 0, можно легко получить базовые данные для текущей записи.</span><span class="sxs-lookup"><span data-stu-id="7ee56-134">Using **Move** with rows equal to 0 is an easy way to retrieve the underlying data for the current record.</span></span> <span data-ttu-id="7ee56-135">Это полезно, если вы хотите убедиться, что текущая запись содержит наиболее актуальные данные из базовых таблиц.</span><span class="sxs-lookup"><span data-stu-id="7ee56-135">This is useful if you want to make sure that the current record has the most recent data from the base tables.</span></span> <span data-ttu-id="7ee56-136">При этом также будут отменены все ожидающие обработки вызовы методов **[Edit](recordset2-edit-method-dao.md)** и **[AddNew](recordset-addnew-method-dao.md)**.</span><span class="sxs-lookup"><span data-stu-id="7ee56-136">It will also cancel any pending **[Edit](recordset2-edit-method-dao.md)** or **[AddNew](recordset-addnew-method-dao.md)** calls.</span></span>


## <a name="example"></a><span data-ttu-id="7ee56-137">Пример</span><span class="sxs-lookup"><span data-stu-id="7ee56-137">Example</span></span>

<span data-ttu-id="7ee56-138">В этом примере с помощью метода **Move** указатель перемещается в соответствии с вводимыми пользователем данными.</span><span class="sxs-lookup"><span data-stu-id="7ee56-138">This example uses the **Move** method to position the record pointer based on user input.</span></span>

```vb
    Sub MoveX() 
     
       Dim dbsNorthwind As Database 
       Dim rstSuppliers As Recordset 
       Dim varBookmark As Variant 
       Dim strCommand As String 
       Dim lngMove As Long 
     
       Set dbsNorthwind = OpenDatabase("Northwind.mdb") 
       Set rstSuppliers = _ 
          dbsNorthwind.OpenRecordset("SELECT CompanyName, " & _ 
          "City, Country FROM Suppliers ORDER BY CompanyName", _ 
          dbOpenDynaset) 
     
       With rstSuppliers 
          ' Populate recordset. 
          .MoveLast 
          .MoveFirst 
     
          Do While True 
             ' Display information about current record and ask  
             ' how many records to move. 
             strCommand = InputBox( _ 
                "Record " & (.AbsolutePosition + 1) & " of " & _ 
                .RecordCount & vbCr & "Company: " & _ 
                !CompanyName & vbCr & "Location: " & !City & _ 
                ", " & !Country & vbCr & vbCr & _ 
                "Enter number of records to Move " & _ 
                "(positive or negative).") 
     
             If strCommand = "" Then Exit Do 
     
             ' Store bookmark in case the Move doesn't work. 
             varBookmark = .Bookmark 
     
             ' Move method requires parameter of data type Long. 
             lngMove = CLng(strCommand) 
             .Move lngMove 
     
             ' Trap for BOF or EOF. 
             If .BOF Then 
                MsgBox "Too far backward! " & _ 
                   "Returning to current record." 
                .Bookmark = varBookmark 
             End If 
             If .EOF Then 
                MsgBox "Too far forward! " & _ 
                   "Returning to current record." 
                .Bookmark = varBookmark 
             End If 
          Loop 
          .Close 
       End With 
     
       dbsNorthwind.Close 
     
    End Sub
```
