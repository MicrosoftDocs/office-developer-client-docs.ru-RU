---
title: Метод Recordset.Clone (DAO)
TOCTitle: Clone Method
ms:assetid: 50cbc011-7e72-4dee-488d-96e681618e8e
ms:mtpsurl: https://msdn.microsoft.com/library/Ff193824(v=office.15)
ms:contentKeyID: 48544802
ms.date: 09/18/2015
mtps_version: v=office.15
f1_keywords:
- dao360.chm1052909
f1_categories:
- Office.Version=v15
localization_priority: Priority
ms.openlocfilehash: ecc5592893c1caee16f0a00687ce50f68b05e9c7
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32300660"
---
# <a name="recordsetclone-method-dao"></a><span data-ttu-id="00341-102">Метод Recordset.Clone (DAO)</span><span class="sxs-lookup"><span data-stu-id="00341-102">Recordset.Clone method (DAO)</span></span>

<span data-ttu-id="00341-103">**Область применения**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="00341-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="00341-104">Создает дубликат объекта **[Recordset](recordset-object-dao.md)**, который ссылается на исходный объект **Recordset**.</span><span class="sxs-lookup"><span data-stu-id="00341-104">Creates a duplicate **[Recordset](recordset-object-dao.md)** object that refers to the original **Recordset** object.</span></span>

## <a name="syntax"></a><span data-ttu-id="00341-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="00341-105">Syntax</span></span>

<span data-ttu-id="00341-106">*expression* .Clone</span><span class="sxs-lookup"><span data-stu-id="00341-106">*expression* .Clone</span></span>

<span data-ttu-id="00341-107">*expression*: переменная, представляющая объект **Recordset**.</span><span class="sxs-lookup"><span data-stu-id="00341-107">*expression* A variable that represents a **Recordset** object.</span></span>

## <a name="return-value"></a><span data-ttu-id="00341-108">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="00341-108">Return value</span></span>

<span data-ttu-id="00341-109">Recordset</span><span class="sxs-lookup"><span data-stu-id="00341-109">Recordset</span></span>

## <a name="remarks"></a><span data-ttu-id="00341-110">Примечания</span><span class="sxs-lookup"><span data-stu-id="00341-110">Remarks</span></span>

<span data-ttu-id="00341-111">Метод **Clone** используется для создания нескольких дублированных объектов **Recordset**.</span><span class="sxs-lookup"><span data-stu-id="00341-111">Use the **Clone** method to create multiple, duplicate **Recordset** objects.</span></span> <span data-ttu-id="00341-112">У каждого объекта **Recordset** есть собственная текущая запись.</span><span class="sxs-lookup"><span data-stu-id="00341-112">Each **Recordset** can have its own current record.</span></span> <span data-ttu-id="00341-113">Сам по себе метод **Clone** не меняет данные в объектах и их базовых структурах.</span><span class="sxs-lookup"><span data-stu-id="00341-113">Using **Clone** by itself doesn't change the data in the objects or in their underlying structures.</span></span> <span data-ttu-id="00341-114">Благодаря методу **Clone** вы можете использовать одни и те же закладки в нескольких объектах **Recordset**, так как их закладки взаимозаменяемы.</span><span class="sxs-lookup"><span data-stu-id="00341-114">When you use the **Clone** method, you can share bookmarks between two or more **Recordset** objects because their bookmarks are interchangeable.</span></span>

<span data-ttu-id="00341-115">Вы можете использовать метод **Clone**, если с объектом **Recordset** нужно выполнить операцию, требующую нескольких текущих записей.</span><span class="sxs-lookup"><span data-stu-id="00341-115">You can use the **Clone** method when you want to perform an operation on a **Recordset** that requires multiple current records.</span></span> <span data-ttu-id="00341-116">Это быстрее и эффективнее, чем открытие второго объекта **Recordset**.</span><span class="sxs-lookup"><span data-stu-id="00341-116">This is faster and more efficient than opening a second **Recordset**.</span></span> <span data-ttu-id="00341-117">При создании объекта **Recordset** с помощью метода **Clone** изначально отсутствует текущая запись.</span><span class="sxs-lookup"><span data-stu-id="00341-117">When you create a **Recordset** with the **Clone** method, it initially lacks a current record.</span></span> <span data-ttu-id="00341-118">Чтобы сделать запись текущей перед использованием клона объекта **Recordset**, необходимо задать свойство **[Bookmark](recordset-bookmark-property-dao.md)** или использовать один из методов **[Move](recordset-movefirst-method-dao.md)**, один из методов **[Find](recordset-findfirst-method-dao.md)** или метод **[Seek](recordset-seek-method-dao.md)**.</span><span class="sxs-lookup"><span data-stu-id="00341-118">To make a record current before you use the **Recordset** clone, you must set the **[Bookmark](recordset-bookmark-property-dao.md)** property or use one of the **[Move](recordset-movefirst-method-dao.md)** methods, one of the **[Find](recordset-findfirst-method-dao.md)** methods, or the **[Seek](recordset-seek-method-dao.md)** method.</span></span>

<span data-ttu-id="00341-119">Использование метода **[Close](connection-close-method-dao.md)** для исходного или дублированного объекта не влияет на другой объект.</span><span class="sxs-lookup"><span data-stu-id="00341-119">Using the **[Close](connection-close-method-dao.md)** method on either the original or duplicate object doesn't affect the other object.</span></span> <span data-ttu-id="00341-120">Например, при использовании метода **Close** для исходного объекта **Recordset** клон не закрывается.</span><span class="sxs-lookup"><span data-stu-id="00341-120">For example, using **Close** on the original **Recordset** doesn't close the clone.</span></span>

> [!NOTE]
> - <span data-ttu-id="00341-121">Закрытие клонированного набора записей в транзакции, ожидающей обработки, приведет к выполнению неявной операции **Rollback**.</span><span class="sxs-lookup"><span data-stu-id="00341-121">Closing a clone recordset within a pending transaction will cause an implicit **Rollback** operation.</span></span>
> - <span data-ttu-id="00341-122">При клонировании объекта **Recordset** табличного типа в рабочей области Microsoft Access значение свойства **[Index](recordset2-index-property-dao.md)** не клонируется в новую копию набора записей.</span><span class="sxs-lookup"><span data-stu-id="00341-122">When you clone a table-type **Recordset** object in a Microsoft Access workspace, the **[Index](recordset2-index-property-dao.md)** property setting is not cloned on the new copy of the recordset.</span></span> <span data-ttu-id="00341-123">Значение свойства **Index** следует копировать вручную.</span><span class="sxs-lookup"><span data-stu-id="00341-123">You must copy the **Index** property setting manually.</span></span>

## <a name="example"></a><span data-ttu-id="00341-124">Пример</span><span class="sxs-lookup"><span data-stu-id="00341-124">Example</span></span>

<span data-ttu-id="00341-125">В этом примере используется метод **Clone**, чтобы создать копии объекта **Recordset**, после чего пользователь может разместить указатели записей для каждой копии независимо друг от друга.</span><span class="sxs-lookup"><span data-stu-id="00341-125">This example uses the **Clone** method to create copies of a **Recordset** and then lets the user position the record pointer of each copy independently.</span></span>

```vb
    Sub CloneX() 
     
       Dim dbsNorthwind As Database 
       Dim arstProducts(1 To 3) As Recordset 
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
