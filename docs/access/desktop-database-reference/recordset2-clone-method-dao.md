---
title: Метод Recordset2. Clone (DAO)
TOCTitle: Clone Method
ms:assetid: f0d32cb1-03f6-395d-2509-b2139a5fdc68
ms:mtpsurl: https://msdn.microsoft.com/library/Ff836567(v=office.15)
ms:contentKeyID: 48548614
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: 6780a27d573f5ff7ff41060074fb8abb9f8e2b80
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32307394"
---
# <a name="recordset2clone-method-dao"></a><span data-ttu-id="d7d53-102">Метод Recordset2. Clone (DAO)</span><span class="sxs-lookup"><span data-stu-id="d7d53-102">Recordset2.Clone method (DAO)</span></span>

<span data-ttu-id="d7d53-103">**Область применения**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="d7d53-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="d7d53-104">Создает дубликат объекта **[Recordset](recordset-object-dao.md)** , ссылающегося на исходный объект **Recordset2** .</span><span class="sxs-lookup"><span data-stu-id="d7d53-104">Creates a duplicate **[Recordset](recordset-object-dao.md)** object that refers to the original **Recordset2** object.</span></span>

## <a name="syntax"></a><span data-ttu-id="d7d53-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="d7d53-105">Syntax</span></span>

<span data-ttu-id="d7d53-106">*Expression* . Копирует</span><span class="sxs-lookup"><span data-stu-id="d7d53-106">*expression* .Clone</span></span>

<span data-ttu-id="d7d53-107">*Expression (выражение* ) Переменная, представляющая объект **Recordset2** .</span><span class="sxs-lookup"><span data-stu-id="d7d53-107">*expression* A variable that represents a **Recordset2** object.</span></span>

## <a name="return-value"></a><span data-ttu-id="d7d53-108">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="d7d53-108">Return value</span></span>

<span data-ttu-id="d7d53-109">Recordset</span><span class="sxs-lookup"><span data-stu-id="d7d53-109">Recordset</span></span>

## <a name="remarks"></a><span data-ttu-id="d7d53-110">Комментарии</span><span class="sxs-lookup"><span data-stu-id="d7d53-110">Remarks</span></span>

<span data-ttu-id="d7d53-111">Используйте метод **clone** для создания нескольких дубликатов объектов **Recordset** .</span><span class="sxs-lookup"><span data-stu-id="d7d53-111">Use the **Clone** method to create multiple, duplicate **Recordset** objects.</span></span> <span data-ttu-id="d7d53-112">Каждый набор записей может иметь собственную текущую запись.</span><span class="sxs-lookup"><span data-stu-id="d7d53-112">Each recordset can have its own current record.</span></span> <span data-ttu-id="d7d53-113">При \*\*\*\* использовании клона сам по себе данные не изменяются в объектах или в базовых структурах.</span><span class="sxs-lookup"><span data-stu-id="d7d53-113">Using **Clone** by itself doesn't change the data in the objects or in their underlying structures.</span></span> <span data-ttu-id="d7d53-114">При использовании метода **clone** можно предоставить общий доступ к закладкам между двумя или более объектами **Recordset2** , так как их закладки являются взаимозаменяемыми.</span><span class="sxs-lookup"><span data-stu-id="d7d53-114">When you use the **Clone** method, you can share bookmarks between two or more **Recordset2** objects because their bookmarks are interchangeable.</span></span>

<span data-ttu-id="d7d53-115">Метод **clone** можно использовать, если требуется выполнить операцию с набором записей, для которого требуется несколько текущих записей.</span><span class="sxs-lookup"><span data-stu-id="d7d53-115">You can use the **Clone** method when you want to perform an operation on a recordset that requires multiple current records.</span></span> <span data-ttu-id="d7d53-116">Это быстрее и эффективнее, чем открыть второй набор записей.</span><span class="sxs-lookup"><span data-stu-id="d7d53-116">This is faster and more efficient than opening a second recordset.</span></span> <span data-ttu-id="d7d53-117">Когда вы создаете объект Recordset с помощью метода **clone** , он изначально не имеет текущей записи.</span><span class="sxs-lookup"><span data-stu-id="d7d53-117">When you create a recordset with the **Clone** method, it initially lacks a current record.</span></span> <span data-ttu-id="d7d53-118">Чтобы сделать запись текущей, прежде чем использовать клон набора записей, необходимо задать свойство **[Bookmark](recordset2-bookmark-property-dao.md)** или использовать один из методов Find, **[](recordset-movefirst-method-dao.md)** один из методов **[Find](recordset2-findfirst-method-dao.md)** или метод **[Seek](recordset2-seek-method-dao.md)** .</span><span class="sxs-lookup"><span data-stu-id="d7d53-118">To make a record current before you use the recordset clone, you must set the **[Bookmark](recordset2-bookmark-property-dao.md)** property or use one of the **[Move](recordset-movefirst-method-dao.md)** methods, one of the **[Find](recordset2-findfirst-method-dao.md)** methods, or the **[Seek](recordset2-seek-method-dao.md)** method.</span></span>

<span data-ttu-id="d7d53-119">Использование метода **[Close](connection-close-method-dao.md)** для исходного или повторяющегося объекта не влияет на другой объект.</span><span class="sxs-lookup"><span data-stu-id="d7d53-119">Using the **[Close](connection-close-method-dao.md)** method on either the original or duplicate object doesn't affect the other object.</span></span> <span data-ttu-id="d7d53-120">Например, использование **Close** для исходного объекта Recordset не приводит к закрытию клона.</span><span class="sxs-lookup"><span data-stu-id="d7d53-120">For example, using **Close** on the original recordset doesn't close the clone.</span></span>

> [!NOTE]
> - <span data-ttu-id="d7d53-121">Закрытие набора записей клонирования в ожидающей транзакции приводит к неявной операции **отката** .</span><span class="sxs-lookup"><span data-stu-id="d7d53-121">Closing a clone recordset within a pending transaction will cause an implicit **Rollback** operation.</span></span>
> - <span data-ttu-id="d7d53-122">При клонировании объекта **Recordset** табличного типа в рабочей области Microsoft Access параметр свойства **[index](recordset2-index-property-dao.md)** не клонируется в новой копии набора записей.</span><span class="sxs-lookup"><span data-stu-id="d7d53-122">When you clone a table-type **Recordset** object in a Microsoft Access workspace, the **[Index](recordset2-index-property-dao.md)** property setting is not cloned on the new copy of the recordset.</span></span> <span data-ttu-id="d7d53-123">Значение свойства **index** необходимо скопировать вручную.</span><span class="sxs-lookup"><span data-stu-id="d7d53-123">You must copy the **Index** property setting manually.</span></span>

## <a name="example"></a><span data-ttu-id="d7d53-124">Пример</span><span class="sxs-lookup"><span data-stu-id="d7d53-124">Example</span></span>

<span data-ttu-id="d7d53-125">В этом примере используется метод **clone** для создания копий объекта Recordset, а затем пользователю разрешается располагать указатель записи каждой копии независимо друг от друга.</span><span class="sxs-lookup"><span data-stu-id="d7d53-125">This example uses the **Clone** method to create copies of a recordset and then lets the user position the record pointer of each copy independently.</span></span>

```vb
    Sub CloneX() 
     
       Dim dbsNorthwind As Database 
       Dim arstProducts(1 To 3) As Recordset2 
       Dim intLoop As Integer 
       Dim strMessage As String 
       Dim strFind As String 
     
       Set dbsNorthwind = OpenDatabase("Northwind.mdb") 
     
       ' If the following SQL statement will be used often,  
       ' creating a permanent QueryDef will result in better 
       ' performance. 
       Set arstProducts(1) = dbsNorthwind.OpenRecordset( _ 
          "SELECT ProductName FROM Products " & _ 
          "ORDER BY ProductName", dbOpenSnapshot) 
     
       ' Create two clones of the original Recordset. 
       Set arstProducts(2) = arstProducts(1).Clone 
       Set arstProducts(3) = arstProducts(1).Clone 
     
       Do While True 
     
          ' Loop through the array so that on each pass, the  
          ' user is searching a different copy of the same  
          ' Recordset. 
          For intLoop = 1 To 3 
     
             ' Ask for search string while showing where the 
             ' current record pointer is for each Recordset. 
             strMessage = _ 
                "Recordsets from Products table:" & vbCr & _ 
                "  1 - Original - Record pointer at " & _ 
                arstProducts(1)!ProductName & vbCr & _ 
                "  2 - Clone - Record pointer at " & _ 
                arstProducts(2)!ProductName & vbCr & _ 
                "  3 - Clone - Record pointer at " & _ 
                arstProducts(3)!ProductName & vbCr & _ 
                "Enter search string for #" & intLoop & ":" 
             strFind = Trim(InputBox(strMessage)) 
             If strFind = "" Then Exit Do 
     
             ' Find the search string; if there's no match, jump 
             ' to the last record. 
             With arstProducts(intLoop) 
                .FindFirst "ProductName >= '" & strFind & "'" 
                If .NoMatch Then .MoveLast 
             End With 
     
          Next intLoop 
     
       Loop 
     
       arstProducts(1).Close 
       arstProducts(2).Close 
       arstProducts(3).Close 
       dbsNorthwind.Close 
     
    End Sub
```
