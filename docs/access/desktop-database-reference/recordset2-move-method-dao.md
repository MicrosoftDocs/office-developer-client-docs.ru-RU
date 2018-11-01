---
title: Recordset2.Move Method (DAO)
TOCTitle: Move Method
ms:assetid: df39c05e-c5f8-3b66-fa5f-c91b687c147d
ms:mtpsurl: https://msdn.microsoft.com/library/Ff835635(v=office.15)
ms:contentKeyID: 48548211
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 0ee1bf654df8cebbb936111d633262fd7418f58a
ms.sourcegitcommit: c557bbcccf37a6011f89aae1ddd399dfe549d087
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/31/2018
ms.locfileid: "25875345"
---
# <a name="recordset2move-method-dao"></a><span data-ttu-id="09ddd-102">Recordset2.Move Method (DAO)</span><span class="sxs-lookup"><span data-stu-id="09ddd-102">Recordset2.Move Method (DAO)</span></span>


<span data-ttu-id="09ddd-103">**Применимо к**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="09ddd-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="09ddd-104">Перемещает положение текущей записи в объекте **[набора записей](recordset-object-dao.md)** .</span><span class="sxs-lookup"><span data-stu-id="09ddd-104">Moves the position of the current record in a **[Recordset](recordset-object-dao.md)** object.</span></span>

## <a name="syntax"></a><span data-ttu-id="09ddd-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="09ddd-105">Syntax</span></span>

<span data-ttu-id="09ddd-106">*выражение* . Перемещение (***строк***, ***StartBookmark***)</span><span class="sxs-lookup"><span data-stu-id="09ddd-106">*expression* .Move(***Rows***, ***StartBookmark***)</span></span>

<span data-ttu-id="09ddd-107">*выражение* Переменная, которая представляет собой объект- **Recordset2** .</span><span class="sxs-lookup"><span data-stu-id="09ddd-107">*expression* A variable that represents a **Recordset2** object.</span></span>

### <a name="parameters"></a><span data-ttu-id="09ddd-108">Параметры</span><span class="sxs-lookup"><span data-stu-id="09ddd-108">Parameters</span></span>

<table>
<colgroup>
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="09ddd-109">Имя</span><span class="sxs-lookup"><span data-stu-id="09ddd-109">Name</span></span></p></th>
<th><p><span data-ttu-id="09ddd-110">Обязательный или необязательный</span><span class="sxs-lookup"><span data-stu-id="09ddd-110">Required/Optional</span></span></p></th>
<th><p><span data-ttu-id="09ddd-111">Тип данных</span><span class="sxs-lookup"><span data-stu-id="09ddd-111">Data Type</span></span></p></th>
<th><p><span data-ttu-id="09ddd-112">Описание</span><span class="sxs-lookup"><span data-stu-id="09ddd-112">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="09ddd-113">Строки</span><span class="sxs-lookup"><span data-stu-id="09ddd-113">Rows</span></span></p></td>
<td><p><span data-ttu-id="09ddd-114">Обязательный</span><span class="sxs-lookup"><span data-stu-id="09ddd-114">Required</span></span></p></td>
<td><p><span data-ttu-id="09ddd-115"><strong>Длинный</strong></span><span class="sxs-lookup"><span data-stu-id="09ddd-115"><strong>Long</strong></span></span></p></td>
<td><p><span data-ttu-id="09ddd-116">Количество строк, которые будут перемещаться положение.</span><span class="sxs-lookup"><span data-stu-id="09ddd-116">The number of rows the position will move.</span></span> <span data-ttu-id="09ddd-117">Если строк больше 0, положение перемещается вперед (ближе к концу файла).</span><span class="sxs-lookup"><span data-stu-id="09ddd-117">If rows is greater than 0, the position is moved forward (toward the end of the file).</span></span> <span data-ttu-id="09ddd-118">Если строк меньше 0, положение перемещается назад (к началу файла).</span><span class="sxs-lookup"><span data-stu-id="09ddd-118">If rows is less than 0, the position is moved backward (toward the beginning of the file).</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="09ddd-119">StartBookmark</span><span class="sxs-lookup"><span data-stu-id="09ddd-119">StartBookmark</span></span></p></td>
<td><p><span data-ttu-id="09ddd-120">Необязательный</span><span class="sxs-lookup"><span data-stu-id="09ddd-120">Optional</span></span></p></td>
<td><p><span data-ttu-id="09ddd-121"><strong>Variant</strong></span><span class="sxs-lookup"><span data-stu-id="09ddd-121"><strong>Variant</strong></span></span></p></td>
<td><p><span data-ttu-id="09ddd-122">Значение, идентифицирующее закладку.</span><span class="sxs-lookup"><span data-stu-id="09ddd-122">A value identifying a bookmark.</span></span> <span data-ttu-id="09ddd-123">При указании startbookmark move начинается относительно эту закладку.</span><span class="sxs-lookup"><span data-stu-id="09ddd-123">If you specify startbookmark, the move begins relative to this bookmark.</span></span> <span data-ttu-id="09ddd-124">В противном случае перемещение начинается с текущей записи.</span><span class="sxs-lookup"><span data-stu-id="09ddd-124">Otherwise, Move begins from the current record.</span></span></p></td>
</tr>
</tbody>
</table>


## <a name="remarks"></a><span data-ttu-id="09ddd-125">Замечания</span><span class="sxs-lookup"><span data-stu-id="09ddd-125">Remarks</span></span>

<span data-ttu-id="09ddd-126">Если вы используете **Перемещение** навести указатель текущей записи перед первой записи указатель текущей записи перемещает в начало файла.</span><span class="sxs-lookup"><span data-stu-id="09ddd-126">If you use **Move** to position the current record pointer before the first record, the current record pointer moves to the beginning of the file.</span></span> <span data-ttu-id="09ddd-127">Если **записей** не содержит записей и его свойство **[BOF](recordset2-bof-property-dao.md)** имеет **значение True**, с помощью этого метода для перемещения назад приводит к ошибке.</span><span class="sxs-lookup"><span data-stu-id="09ddd-127">If the **Recordset** contains no records and its **[BOF](recordset2-bof-property-dao.md)** property is **True**, using this method to move backward causes an error.</span></span>

<span data-ttu-id="09ddd-128">Если вы можете **переместить** наведите указатель текущей записи после последней записи, текущей позиции указателя записи перемещается в конец файла.</span><span class="sxs-lookup"><span data-stu-id="09ddd-128">If you use **Move** to position the current record pointer after the last record, the current record pointer position moves to the end of the file.</span></span> <span data-ttu-id="09ddd-129">Если **записей** не содержит записей и его свойство **[EOF](recordset2-eof-property-dao.md)** имеет **значение True**, затем перейти вперед, с помощью этого метода приводит к ошибке.</span><span class="sxs-lookup"><span data-stu-id="09ddd-129">If the **Recordset** contains no records and its **[EOF](recordset2-eof-property-dao.md)** property is **True**, then using this method to move forward causes an error.</span></span>

<span data-ttu-id="09ddd-130">Если параметр **BOF** или **EOF** свойство имеет **значение True** , и попытаться использовать метод **Move** без допустимого закладку, возникает ошибка времени выполнения.</span><span class="sxs-lookup"><span data-stu-id="09ddd-130">If either the **BOF** or **EOF** property is **True** and you attempt to use the **Move** method without a valid bookmark, a run-time error occurs.</span></span>


> [!NOTE]
> <UL>
> <LI>
> <P><span data-ttu-id="09ddd-131">При использовании <STRONG>Перемещение</STRONG> на объект <STRONG>набора записей</STRONG> прямого только для типа аргумент строки должно быть положительное целое число, и закладки не разрешается.</span><span class="sxs-lookup"><span data-stu-id="09ddd-131">When you use <STRONG>Move</STRONG> on a forward-only-type <STRONG>Recordset</STRONG> object, the rows argument must be a positive integer and bookmarks aren't allowed.</span></span> <span data-ttu-id="09ddd-132">Это означает, что можно только Переместить вперед.</span><span class="sxs-lookup"><span data-stu-id="09ddd-132">This means you can only move forward.</span></span></P>
> <LI>
> <P><span data-ttu-id="09ddd-133">Чтобы сделать первый, и, наконец, следующий или предыдущий записи в <STRONG>набор записей</STRONG> текущей записи метод <STRONG>MoveFirst</STRONG>, <STRONG>MoveLast</STRONG>, <STRONG>MoveNext</STRONG>или <STRONG>MovePrevious</STRONG> .</span><span class="sxs-lookup"><span data-stu-id="09ddd-133">To make the first, last, next, or previous record in a <STRONG>Recordset</STRONG> the current record, use either the <STRONG>MoveFirst</STRONG>, <STRONG>MoveLast</STRONG>, <STRONG>MoveNext</STRONG>, or <STRONG>MovePrevious</STRONG> method.</span></span></P>
> <LI>
> <P><span data-ttu-id="09ddd-134">Использование <STRONG>Перемещение</STRONG> с строк равно 0 — это простой способ получения данных для текущей записи.</span><span class="sxs-lookup"><span data-stu-id="09ddd-134">Using <STRONG>Move</STRONG> with rows equal to 0 is an easy way to retrieve the underlying data for the current record.</span></span> <span data-ttu-id="09ddd-135">Эта функция особенно полезна, если вы хотите убедиться, что текущая запись имеет самых последних данных из базовых таблиц.</span><span class="sxs-lookup"><span data-stu-id="09ddd-135">This is useful if you want to make sure that the current record has the most recent data from the base tables.</span></span> <span data-ttu-id="09ddd-136">Он также будет отменить все ожидающие <STRONG><A href="recordset2-edit-method-dao.md">изменения</A></STRONG> или <STRONG><A href="recordset-addnew-method-dao.md">AddNew</A></STRONG> вызовы.</span><span class="sxs-lookup"><span data-stu-id="09ddd-136">It will also cancel any pending <STRONG><A href="recordset2-edit-method-dao.md">Edit</A></STRONG> or <STRONG><A href="recordset-addnew-method-dao.md">AddNew</A></STRONG> calls.</span></span></P></LI></UL>



## <a name="example"></a><span data-ttu-id="09ddd-137">Пример</span><span class="sxs-lookup"><span data-stu-id="09ddd-137">Example</span></span>

<span data-ttu-id="09ddd-138">В этом примере используется метод **Move** навести указатель записи, в зависимости от введенных пользователем.</span><span class="sxs-lookup"><span data-stu-id="09ddd-138">This example uses the **Move** method to position the record pointer based on user input.</span></span>

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
