---
title: Recordset2.Clone Method (DAO)
TOCTitle: Clone Method
ms:assetid: f0d32cb1-03f6-395d-2509-b2139a5fdc68
ms:mtpsurl: https://msdn.microsoft.com/library/Ff836567(v=office.15)
ms:contentKeyID: 48548614
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 47aa31bf6b32b674d7701b6572cc411eb88cc301
ms.sourcegitcommit: a49b77f4c8cec69f90656a86f0872cf34c35968e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/17/2018
ms.locfileid: "25603289"
---
# <a name="recordset2clone-method-dao"></a><span data-ttu-id="7cb44-102">Recordset2.Clone Method (DAO)</span><span class="sxs-lookup"><span data-stu-id="7cb44-102">Recordset2.Clone Method (DAO)</span></span>


<span data-ttu-id="7cb44-103">**Применимо к**: Access 2013 | Office 2013</span><span class="sxs-lookup"><span data-stu-id="7cb44-103">**Applies to**: Access 2013 | Office 2013</span></span>

<span data-ttu-id="7cb44-104">Создает объект повторяющихся **[записей](recordset-object-dao.md)** , на который ссылается на исходный объект **Recordset2** .</span><span class="sxs-lookup"><span data-stu-id="7cb44-104">Creates a duplicate **[Recordset](recordset-object-dao.md)** object that refers to the original **Recordset2** object.</span></span>

## <a name="syntax"></a><span data-ttu-id="7cb44-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="7cb44-105">Syntax</span></span>

<span data-ttu-id="7cb44-106">*выражение* . Копия</span><span class="sxs-lookup"><span data-stu-id="7cb44-106">*expression* .Clone</span></span>

<span data-ttu-id="7cb44-107">*выражение* Переменная, которая представляет собой объект- **Recordset2** .</span><span class="sxs-lookup"><span data-stu-id="7cb44-107">*expression* A variable that represents a **Recordset2** object.</span></span>

<span data-ttu-id="7cb44-108"><<<<<<< HEAD</span><span class="sxs-lookup"><span data-stu-id="7cb44-108"><<<<<<< HEAD</span></span>
### <a name="return-value"></a><span data-ttu-id="7cb44-109">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="7cb44-109">Return Value</span></span>
=======
### <a name="return-value"></a><span data-ttu-id="7cb44-110">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="7cb44-110">Return value</span></span>
>>>>>>> <span data-ttu-id="7cb44-111">master</span><span class="sxs-lookup"><span data-stu-id="7cb44-111">master</span></span>

<span data-ttu-id="7cb44-112">Набор записей</span><span class="sxs-lookup"><span data-stu-id="7cb44-112">Recordset</span></span>

## <a name="remarks"></a><span data-ttu-id="7cb44-113">Замечания</span><span class="sxs-lookup"><span data-stu-id="7cb44-113">Remarks</span></span>

<span data-ttu-id="7cb44-114">Используйте метод **клонированной** для создания нескольких дубликатов объектов **набора записей** .</span><span class="sxs-lookup"><span data-stu-id="7cb44-114">Use the **Clone** method to create multiple, duplicate **Recordset** objects.</span></span> <span data-ttu-id="7cb44-115">Каждый набор записей может иметь собственный текущей записи.</span><span class="sxs-lookup"><span data-stu-id="7cb44-115">Each recordset can have its own current record.</span></span> <span data-ttu-id="7cb44-116">С помощью **клонированной** сам по себе не изменяет данные в объектах или в их базовые структуры.</span><span class="sxs-lookup"><span data-stu-id="7cb44-116">Using **Clone** by itself doesn't change the data in the objects or in their underlying structures.</span></span> <span data-ttu-id="7cb44-117">При использовании метода **клонирования** могут совместно использовать закладки между двумя или более объектов **Recordset2** , так как их закладки являются взаимозаменяемыми.</span><span class="sxs-lookup"><span data-stu-id="7cb44-117">When you use the **Clone** method, you can share bookmarks between two or more **Recordset2** objects because their bookmarks are interchangeable.</span></span>

<span data-ttu-id="7cb44-118">Можно использовать метод **клонированной** , если необходимо использовать для выполнения операции наборов записей, требует нескольких записей текущей.</span><span class="sxs-lookup"><span data-stu-id="7cb44-118">You can use the **Clone** method when you want to perform an operation on a recordset that requires multiple current records.</span></span> <span data-ttu-id="7cb44-119">Это быстрее и эффективнее, чем при открытии второго набора записей.</span><span class="sxs-lookup"><span data-stu-id="7cb44-119">This is faster and more efficient than opening a second recordset.</span></span> <span data-ttu-id="7cb44-120">При создании набора записей с помощью метода **клонированной** его изначально не имеет текущей записи.</span><span class="sxs-lookup"><span data-stu-id="7cb44-120">When you create a recordset with the **Clone** method, it initially lacks a current record.</span></span> <span data-ttu-id="7cb44-121">Чтобы сделать запись текущей, прежде чем использовать клонированной записей, необходимо задать свойство **[закладку](recordset2-bookmark-property-dao.md)** или используйте один из методов **[перемещения](recordset-movefirst-method-dao.md)** , один из методов **[поиска](recordset2-findfirst-method-dao.md)** , либо метод **[Seek](recordset2-seek-method-dao.md)** .</span><span class="sxs-lookup"><span data-stu-id="7cb44-121">To make a record current before you use the recordset clone, you must set the **[Bookmark](recordset2-bookmark-property-dao.md)** property or use one of the **[Move](recordset-movefirst-method-dao.md)** methods, one of the **[Find](recordset2-findfirst-method-dao.md)** methods, or the **[Seek](recordset2-seek-method-dao.md)** method.</span></span>

<span data-ttu-id="7cb44-122">С помощью метода **[Close](connection-close-method-dao.md)** исходной или повторяющихся объекта не влияет на другой объект.</span><span class="sxs-lookup"><span data-stu-id="7cb44-122">Using the **[Close](connection-close-method-dao.md)** method on either the original or duplicate object doesn't affect the other object.</span></span> <span data-ttu-id="7cb44-123">К примеру на исходный набора записей с помощью **Закрыть** не закройте копия.</span><span class="sxs-lookup"><span data-stu-id="7cb44-123">For example, using **Close** on the original recordset doesn't close the clone.</span></span>


> [!NOTE]
> <UL>
> <LI>
> <P><span data-ttu-id="7cb44-124">Закрытие набора записей клонированной ожидающие транзакции будет отображено неявные операции <STRONG>отката</STRONG> .</span><span class="sxs-lookup"><span data-stu-id="7cb44-124">Closing a clone recordset within a pending transaction will cause an implicit <STRONG>Rollback</STRONG> operation.</span></span></P>
> <LI>
> <P><span data-ttu-id="7cb44-125">При клонировании объекта <STRONG>набора записей</STRONG> в таблице типа в рабочей области Microsoft Access значение свойства <STRONG><A href="recordset2-index-property-dao.md">Index</A></STRONG> не копируется в новую копию набора записей.</span><span class="sxs-lookup"><span data-stu-id="7cb44-125">When you clone a table-type <STRONG>Recordset</STRONG> object in a Microsoft Access workspace, the <STRONG><A href="recordset2-index-property-dao.md">Index</A></STRONG> property setting is not cloned on the new copy of the recordset.</span></span> <span data-ttu-id="7cb44-126">Необходимо скопировать вручную значение свойства <STRONG>Index</STRONG> .</span><span class="sxs-lookup"><span data-stu-id="7cb44-126">You must copy the <STRONG>Index</STRONG> property setting manually.</span></span></P></LI></UL>



## <a name="example"></a><span data-ttu-id="7cb44-127">Пример</span><span class="sxs-lookup"><span data-stu-id="7cb44-127">Example</span></span>

<span data-ttu-id="7cb44-128">В этом примере используется метод **клонированной** для создания копии набора записей и затем позволяет пользователя положение указателя записи каждой копии независимо друг от друга.</span><span class="sxs-lookup"><span data-stu-id="7cb44-128">This example uses the **Clone** method to create copies of a recordset and then lets the user position the record pointer of each copy independently.</span></span>

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
