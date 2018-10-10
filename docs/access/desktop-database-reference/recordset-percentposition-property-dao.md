---
title: Recordset.PercentPosition Property (DAO)
TOCTitle: PercentPosition Property
ms:assetid: aebbda44-ed72-7a6c-0cd5-28c8997d4d96
ms:mtpsurl: https://msdn.microsoft.com/library/Ff821751(v=office.15)
ms:contentKeyID: 48547077
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 5793d2b73e424726e91cf3bbb54b09db59123b92
ms.sourcegitcommit: 19aca09c5812cfb98b68b5d4604dcaa814479df7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/09/2018
ms.locfileid: "25481339"
---
# <a name="recordsetpercentposition-property-dao"></a><span data-ttu-id="6f16d-102">Recordset.PercentPosition Property (DAO)</span><span class="sxs-lookup"><span data-stu-id="6f16d-102">Recordset.PercentPosition Property (DAO)</span></span>


<span data-ttu-id="6f16d-103">**Применимо к**: Access 2013 | Office 2013</span><span class="sxs-lookup"><span data-stu-id="6f16d-103">**Applies to**: Access 2013 | Office 2013</span></span>

<span data-ttu-id="6f16d-104">Задает или возвращает значение, указывающее, приблизительно, например расположение текущей записи в объекте **[набора записей](recordset-object-dao.md)** на основе процента записей в **набора записей**.</span><span class="sxs-lookup"><span data-stu-id="6f16d-104">Sets or returns a value indicating the approximate location of the current record in the **[Recordset](recordset-object-dao.md)** object based on a percentage of the records in the **Recordset**.</span></span>

## <a name="syntax"></a><span data-ttu-id="6f16d-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="6f16d-105">Syntax</span></span>

<span data-ttu-id="6f16d-106">*выражение* . PercentPosition</span><span class="sxs-lookup"><span data-stu-id="6f16d-106">*expression* .PercentPosition</span></span>

<span data-ttu-id="6f16d-107">*выражение* Переменная, которая представляет собой объект **набора записей** .</span><span class="sxs-lookup"><span data-stu-id="6f16d-107">*expression* A variable that represents a **Recordset** object.</span></span>

## <a name="remarks"></a><span data-ttu-id="6f16d-108">Замечания</span><span class="sxs-lookup"><span data-stu-id="6f16d-108">Remarks</span></span>

<span data-ttu-id="6f16d-109">Чтобы указать или изменить приблизительно, например положения текущей записи в объекте **набора записей** , можно проверить или задайте для свойства **PercentPosition** .</span><span class="sxs-lookup"><span data-stu-id="6f16d-109">To indicate or change the approximate position of the current record in a **Recordset** object, you can check or set the **PercentPosition** property.</span></span> <span data-ttu-id="6f16d-110">При работе с объектом **набора записей** добавляющий или моментальный снимок непосредственно из базовой таблицы заполните путем перемещения к последнему записи, прежде чем задать или свойство **PercentPosition** объекта **набора записей** .</span><span class="sxs-lookup"><span data-stu-id="6f16d-110">When working with a dynaset- or snapshot-type **Recordset** object opened directly from a base table, first populate the **Recordset** object by moving to the last record before you set or check the **PercentPosition** property.</span></span> <span data-ttu-id="6f16d-111">Если использовать свойство **PercentPosition** до полностью заполнения объекта **набора записей** , величину перемещения задается число записей, доступны как указано значение свойства **[RecordCount](recordset-recordcount-property-dao.md)** .</span><span class="sxs-lookup"><span data-stu-id="6f16d-111">If you use the **PercentPosition** property before fully populating the **Recordset** object, the amount of movement is relative to the number of records accessed as indicated by the **[RecordCount](recordset-recordcount-property-dao.md)** property setting.</span></span> <span data-ttu-id="6f16d-112">К последнему можно перемещать записи с помощью метода **[MoveLast](recordset-movelast-method-dao.md)** .</span><span class="sxs-lookup"><span data-stu-id="6f16d-112">You can move to the last record by using the **[MoveLast](recordset-movelast-method-dao.md)** method.</span></span>


> [!NOTE]
> <P><span data-ttu-id="6f16d-113">С помощью свойства <STRONG>PercentPosition</STRONG> для перемещения что текущей записи к определенной записи в объекте <STRONG>набора записей</STRONG> не recommended?the <STRONG><A href="recordset-bookmark-property-dao.md">закладку</A></STRONG> свойство лучше всего подходит для этой задачи.</span><span class="sxs-lookup"><span data-stu-id="6f16d-113">Using the <STRONG>PercentPosition</STRONG> property to move the current record to a specific record in a <STRONG>Recordset</STRONG> object isn't recommended?the <STRONG><A href="recordset-bookmark-property-dao.md">Bookmark</A></STRONG> property is better suited for this task.</span></span></P>



<span data-ttu-id="6f16d-114">После **PercentPosition** свойству присвоено значение, записи в приблизительно, например позиции, соответствующее значение, становится текущей и свойство **PercentPosition** сбрасывается в значение, которое отражает приблизительно, например положение текущего запись.</span><span class="sxs-lookup"><span data-stu-id="6f16d-114">Once you set the **PercentPosition** property to a value, the record at the approximate position corresponding to that value becomes current, and the **PercentPosition** property is reset to a value that reflects the approximate position of the current record.</span></span> <span data-ttu-id="6f16d-115">Например если объекта **набора записей** содержит только пять записей и присвойте ему значение свойства **PercentPosition** для 77, значение, возвращенное свойством **PercentPosition** может быть 80, не 77.</span><span class="sxs-lookup"><span data-stu-id="6f16d-115">For example, if your **Recordset** object contains only five records, and you set its **PercentPosition** property value to 77, the value returned from the **PercentPosition** property may be 80, not 77.</span></span>

<span data-ttu-id="6f16d-116">Свойство **PercentPosition** применяется ко всем типам объектов **наборов записей** , за исключением объекты **набора записей** прямого — только — тип или **набора записей** открывается из запросов к серверу для удаленной баз данных.</span><span class="sxs-lookup"><span data-stu-id="6f16d-116">The **PercentPosition** property applies to all types of **Recordset** objects except for forward–only–type **Recordset** objects or **Recordset** objects opened from pass-through queries against remote databases.</span></span>

<span data-ttu-id="6f16d-117">Свойство **PercentPosition** с полосы прокрутки на форме или текстовое поле для указания расположения текущей записи в объекте **набора записей** .</span><span class="sxs-lookup"><span data-stu-id="6f16d-117">You can use the **PercentPosition** property with a scroll bar on a form or text box to indicate the location of the current record in a **Recordset** object.</span></span>

## <a name="example"></a><span data-ttu-id="6f16d-118">Пример</span><span class="sxs-lookup"><span data-stu-id="6f16d-118">Example</span></span>

<span data-ttu-id="6f16d-119">В этом примере используется свойство **PercentPosition** для отображения положения указатель текущей записи с начала **набора записей**.</span><span class="sxs-lookup"><span data-stu-id="6f16d-119">This example uses the **PercentPosition** property to show the position of the current record pointer relative to the beginning of the **Recordset**.</span></span>

```vb
    Sub PercentPositionX() 
     
     Dim dbsNorthwind As Database 
     Dim rstProducts As Recordset 
     Dim strFind As String 
     Dim strMessage As String 
     
     Set dbsNorthwind = OpenDatabase("Northwind.mdb") 
     ' PercentPosition only works with dynasets or snapshots. 
     Set rstProducts = dbsNorthwind.OpenRecordset( _ 
     "SELECT ProductName FROM Products " & _ 
     "ORDER BY ProductName", dbOpenSnapshot) 
     
     With rstProducts 
     ' Populate the Recordset. 
     .MoveLast 
     .MoveFirst 
     
     Do While True 
     ' Show current record information and ask user 
     ' for input. 
     strMessage = "Product: " & !ProductName & vbCr & _ 
     "The record pointer is " & _ 
     Format(.PercentPosition, "##0.0") & _ 
     "% from the " & vbCr & _ 
     "beginning of the Recordset." & vbCr & _ 
     "Please enter a character search string " & _ 
     "for a product name." 
     strFind = Trim(InputBox(strMessage)) 
     If strFind = "" Then Exit Do 
     
     ' Try to find a record matching the search string. 
     .FindFirst "ProductName >= '" & strFind & "'" 
     If .NoMatch Then .MoveLast 
     Loop 
     
     .Close 
     End With 
     
     dbsNorthwind.Close 
     
    End Sub
```
