---
title: Метод Recordset2.Move (DAO)
TOCTitle: Move Method
ms:assetid: df39c05e-c5f8-3b66-fa5f-c91b687c147d
ms:mtpsurl: https://msdn.microsoft.com/library/Ff835635(v=office.15)
ms:contentKeyID: 48548211
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: d2231e94703b49fd14fb89d7642c0144c1dda532
ms.sourcegitcommit: 1dd744993ecb4bed241ace874ad26edaef1778b8
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 11/06/2018
ms.locfileid: "25998597"
---
# <a name="recordset2move-method-dao"></a><span data-ttu-id="1c54d-102">Метод Recordset2.Move (DAO)</span><span class="sxs-lookup"><span data-stu-id="1c54d-102">Recordset2.Move method (DAO)</span></span>

<span data-ttu-id="1c54d-103">**Применимо к**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="1c54d-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="1c54d-104">Перемещает положение текущей записи в объекте **[набора записей](recordset-object-dao.md)** .</span><span class="sxs-lookup"><span data-stu-id="1c54d-104">Moves the position of the current record in a **[Recordset](recordset-object-dao.md)** object.</span></span>

## <a name="syntax"></a><span data-ttu-id="1c54d-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="1c54d-105">Syntax</span></span>

<span data-ttu-id="1c54d-106">*выражение* . Перемещение (***строк***, ***StartBookmark***)</span><span class="sxs-lookup"><span data-stu-id="1c54d-106">*expression* .Move(***Rows***, ***StartBookmark***)</span></span>

<span data-ttu-id="1c54d-107">*выражение* Переменная, которая представляет собой объект- **Recordset2** .</span><span class="sxs-lookup"><span data-stu-id="1c54d-107">*expression* A variable that represents a **Recordset2** object.</span></span>

## <a name="parameters"></a><span data-ttu-id="1c54d-108">Параметры</span><span class="sxs-lookup"><span data-stu-id="1c54d-108">Parameters</span></span>

<table>
<colgroup>
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="1c54d-109">Имя</span><span class="sxs-lookup"><span data-stu-id="1c54d-109">Name</span></span></p></th>
<th><p><span data-ttu-id="1c54d-110">Обязательный или необязательный</span><span class="sxs-lookup"><span data-stu-id="1c54d-110">Required/optional</span></span></p></th>
<th><p><span data-ttu-id="1c54d-111">Тип данных</span><span class="sxs-lookup"><span data-stu-id="1c54d-111">Data type</span></span></p></th>
<th><p><span data-ttu-id="1c54d-112">Описание</span><span class="sxs-lookup"><span data-stu-id="1c54d-112">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="1c54d-113"><em>Строк</em></span><span class="sxs-lookup"><span data-stu-id="1c54d-113"><em>Rows</em></span></span></p></td>
<td><p><span data-ttu-id="1c54d-114">Обязательный</span><span class="sxs-lookup"><span data-stu-id="1c54d-114">Required</span></span></p></td>
<td><p><span data-ttu-id="1c54d-115"><strong>Длинный</strong></span><span class="sxs-lookup"><span data-stu-id="1c54d-115"><strong>Long</strong></span></span></p></td>
<td><p><span data-ttu-id="1c54d-116">Количество строк, которые будут перемещаться положение.</span><span class="sxs-lookup"><span data-stu-id="1c54d-116">The number of rows the position will move.</span></span> <span data-ttu-id="1c54d-117">Если строк больше 0, положение перемещается вперед (ближе к концу файла).</span><span class="sxs-lookup"><span data-stu-id="1c54d-117">If rows is greater than 0, the position is moved forward (toward the end of the file).</span></span> <span data-ttu-id="1c54d-118">Если строк меньше 0, положение перемещается назад (к началу файла).</span><span class="sxs-lookup"><span data-stu-id="1c54d-118">If rows is less than 0, the position is moved backward (toward the beginning of the file).</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="1c54d-119"><em>StartBookmark</em></span><span class="sxs-lookup"><span data-stu-id="1c54d-119"><em>StartBookmark</em></span></span></p></td>
<td><p><span data-ttu-id="1c54d-120">Необязательный</span><span class="sxs-lookup"><span data-stu-id="1c54d-120">Optional</span></span></p></td>
<td><p><span data-ttu-id="1c54d-121"><strong>Variant</strong></span><span class="sxs-lookup"><span data-stu-id="1c54d-121"><strong>Variant</strong></span></span></p></td>
<td><p><span data-ttu-id="1c54d-122">Значение, идентифицирующее закладку.</span><span class="sxs-lookup"><span data-stu-id="1c54d-122">A value identifying a bookmark.</span></span> <span data-ttu-id="1c54d-123">При указании startbookmark move начинается относительно эту закладку.</span><span class="sxs-lookup"><span data-stu-id="1c54d-123">If you specify startbookmark, the move begins relative to this bookmark.</span></span> <span data-ttu-id="1c54d-124">В противном случае перемещение начинается с текущей записи.</span><span class="sxs-lookup"><span data-stu-id="1c54d-124">Otherwise, Move begins from the current record.</span></span></p></td>
</tr>
</tbody>
</table>


## <a name="remarks"></a><span data-ttu-id="1c54d-125">Примечания</span><span class="sxs-lookup"><span data-stu-id="1c54d-125">Remarks</span></span>

<span data-ttu-id="1c54d-126">Если вы используете **Перемещение** навести указатель текущей записи перед первой записи указатель текущей записи перемещает в начало файла.</span><span class="sxs-lookup"><span data-stu-id="1c54d-126">If you use **Move** to position the current record pointer before the first record, the current record pointer moves to the beginning of the file.</span></span> <span data-ttu-id="1c54d-127">Если **записей** не содержит записей и его свойство **[BOF](recordset2-bof-property-dao.md)** имеет **значение True**, с помощью этого метода для перемещения назад приводит к ошибке.</span><span class="sxs-lookup"><span data-stu-id="1c54d-127">If the **Recordset** contains no records and its **[BOF](recordset2-bof-property-dao.md)** property is **True**, using this method to move backward causes an error.</span></span>

<span data-ttu-id="1c54d-128">Если вы можете **переместить** наведите указатель текущей записи после последней записи, текущей позиции указателя записи перемещается в конец файла.</span><span class="sxs-lookup"><span data-stu-id="1c54d-128">If you use **Move** to position the current record pointer after the last record, the current record pointer position moves to the end of the file.</span></span> <span data-ttu-id="1c54d-129">Если **записей** не содержит записей и его свойство **[EOF](recordset2-eof-property-dao.md)** имеет **значение True**, затем перейти вперед, с помощью этого метода приводит к ошибке.</span><span class="sxs-lookup"><span data-stu-id="1c54d-129">If the **Recordset** contains no records and its **[EOF](recordset2-eof-property-dao.md)** property is **True**, then using this method to move forward causes an error.</span></span>

<span data-ttu-id="1c54d-130">Если параметр **BOF** или **EOF** свойство имеет **значение True** , и попытаться использовать метод **Move** без допустимого закладку, возникает ошибка времени выполнения.</span><span class="sxs-lookup"><span data-stu-id="1c54d-130">If either the **BOF** or **EOF** property is **True** and you attempt to use the **Move** method without a valid bookmark, a run-time error occurs.</span></span>

> [!NOTE]
> - <span data-ttu-id="1c54d-131">При использовании **Перемещение** на объект **набора записей** прямого только для типа аргумент строки должно быть положительное целое число, и закладки не разрешается.</span><span class="sxs-lookup"><span data-stu-id="1c54d-131">When you use **Move** on a forward-only-type **Recordset** object, the rows argument must be a positive integer and bookmarks aren't allowed.</span></span> <span data-ttu-id="1c54d-132">Это означает, что можно только Переместить вперед.</span><span class="sxs-lookup"><span data-stu-id="1c54d-132">This means you can only move forward.</span></span>
> - <span data-ttu-id="1c54d-133">Чтобы сделать первый, и, наконец, следующий или предыдущий записи в **набор записей** текущей записи метод **MoveFirst**, **MoveLast**, **MoveNext**или **MovePrevious** .</span><span class="sxs-lookup"><span data-stu-id="1c54d-133">To make the first, last, next, or previous record in a **Recordset** the current record, use either the **MoveFirst**, **MoveLast**, **MoveNext**, or **MovePrevious** method.</span></span>
> - <span data-ttu-id="1c54d-134">Использование **Перемещение** с строк равно 0 — это простой способ получения данных для текущей записи.</span><span class="sxs-lookup"><span data-stu-id="1c54d-134">Using **Move** with rows equal to 0 is an easy way to retrieve the underlying data for the current record.</span></span> <span data-ttu-id="1c54d-135">Эта функция особенно полезна, если вы хотите убедиться, что текущая запись имеет самых последних данных из базовых таблиц.</span><span class="sxs-lookup"><span data-stu-id="1c54d-135">This is useful if you want to make sure that the current record has the most recent data from the base tables.</span></span> <span data-ttu-id="1c54d-136">Он также будет отменить все ожидающие **[изменения](recordset2-edit-method-dao.md)** или **[AddNew](recordset-addnew-method-dao.md)** вызовы.</span><span class="sxs-lookup"><span data-stu-id="1c54d-136">It will also cancel any pending **[Edit](recordset2-edit-method-dao.md)** or **[AddNew](recordset-addnew-method-dao.md)** calls.</span></span>


## <a name="example"></a><span data-ttu-id="1c54d-137">Пример</span><span class="sxs-lookup"><span data-stu-id="1c54d-137">Example</span></span>

<span data-ttu-id="1c54d-138">В этом примере используется метод **Move** навести указатель записи, в зависимости от введенных пользователем.</span><span class="sxs-lookup"><span data-stu-id="1c54d-138">This example uses the **Move** method to position the record pointer based on user input.</span></span>

```vb
    Sub MoveX() 
     
       Dim dbsNorthwind As Database 
       Dim rstSuppliers As Recordset2 
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
