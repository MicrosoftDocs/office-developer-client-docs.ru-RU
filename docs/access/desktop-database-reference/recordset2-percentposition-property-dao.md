---
title: Свойство Recordset2.PercentPosition (DAO)
TOCTitle: PercentPosition Property
ms:assetid: 830a7d26-6817-233f-ce24-80b572c1c100
ms:mtpsurl: https://msdn.microsoft.com/library/Ff196732(v=office.15)
ms:contentKeyID: 48545996
ms.date: 09/18/2015
mtps_version: v=office.15
f1_keywords:
- dao360.chm1052973
f1_categories:
- Office.Version=v15
ms.openlocfilehash: 316dd9e8b430ba0dbb741bc1af81517749d84f77
ms.sourcegitcommit: d7248f803002b31cf7fc561b03530199a9b0a8fd
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 11/02/2018
ms.locfileid: "25921889"
---
# <a name="recordset2percentposition-property-dao"></a><span data-ttu-id="09742-102">Свойство Recordset2.PercentPosition (DAO)</span><span class="sxs-lookup"><span data-stu-id="09742-102">Recordset2.PercentPosition property (DAO)</span></span>


<span data-ttu-id="09742-103">**Применимо к**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="09742-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="09742-104">Задает или возвращает значение, указывающее, приблизительно, например расположение текущей записи в объекте **[набора записей](recordset-object-dao.md)** на основе процента записей в **набора записей**.</span><span class="sxs-lookup"><span data-stu-id="09742-104">Sets or returns a value indicating the approximate location of the current record in the **[Recordset](recordset-object-dao.md)** object based on a percentage of the records in the **Recordset**.</span></span>

## <a name="syntax"></a><span data-ttu-id="09742-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="09742-105">Syntax</span></span>

<span data-ttu-id="09742-106">*выражение* . PercentPosition</span><span class="sxs-lookup"><span data-stu-id="09742-106">*expression* .PercentPosition</span></span>

<span data-ttu-id="09742-107">*выражение* Переменная, которая представляет собой объект- **Recordset2** .</span><span class="sxs-lookup"><span data-stu-id="09742-107">*expression* A variable that represents a **Recordset2** object.</span></span>

## <a name="remarks"></a><span data-ttu-id="09742-108">Примечания</span><span class="sxs-lookup"><span data-stu-id="09742-108">Remarks</span></span>

<span data-ttu-id="09742-109">Чтобы указать или изменить приблизительно, например положения текущей записи в объекте **набора записей** , можно проверить или задайте для свойства **PercentPosition** .</span><span class="sxs-lookup"><span data-stu-id="09742-109">To indicate or change the approximate position of the current record in a **Recordset** object, you can check or set the **PercentPosition** property.</span></span> <span data-ttu-id="09742-110">При работе с объектом **набора записей** добавляющий или моментальный снимок непосредственно из базовой таблицы заполните путем перемещения к последнему записи, прежде чем задать или свойство **PercentPosition** объекта **набора записей** .</span><span class="sxs-lookup"><span data-stu-id="09742-110">When working with a dynaset- or snapshot-type **Recordset** object opened directly from a base table, first populate the **Recordset** object by moving to the last record before you set or check the **PercentPosition** property.</span></span> <span data-ttu-id="09742-111">Если использовать свойство **PercentPosition** до полностью заполнения объекта **набора записей** , величину перемещения задается число записей, доступны как указано значение свойства **[RecordCount](recordset2-recordcount-property-dao.md)** .</span><span class="sxs-lookup"><span data-stu-id="09742-111">If you use the **PercentPosition** property before fully populating the **Recordset** object, the amount of movement is relative to the number of records accessed as indicated by the **[RecordCount](recordset2-recordcount-property-dao.md)** property setting.</span></span> <span data-ttu-id="09742-112">К последнему можно перемещать записи с помощью метода **[MoveLast](recordset2-movelast-method-dao.md)** .</span><span class="sxs-lookup"><span data-stu-id="09742-112">You can move to the last record by using the **[MoveLast](recordset2-movelast-method-dao.md)** method.</span></span>


> [!NOTE]
> <P><span data-ttu-id="09742-113">С помощью свойства <STRONG>PercentPosition</STRONG> для перемещения что текущей записи к определенной записи в объекте <STRONG>набора записей</STRONG> не recommended?the <STRONG><A href="recordset2-bookmark-property-dao.md">закладку</A></STRONG> свойство лучше всего подходит для этой задачи.</span><span class="sxs-lookup"><span data-stu-id="09742-113">Using the <STRONG>PercentPosition</STRONG> property to move the current record to a specific record in a <STRONG>Recordset</STRONG> object isn't recommended?the <STRONG><A href="recordset2-bookmark-property-dao.md">Bookmark</A></STRONG> property is better suited for this task.</span></span></P>



<span data-ttu-id="09742-114">После **PercentPosition** свойству присвоено значение, записи в приблизительно, например позиции, соответствующее значение, становится текущей и свойство **PercentPosition** сбрасывается в значение, которое отражает приблизительно, например положение текущего запись.</span><span class="sxs-lookup"><span data-stu-id="09742-114">Once you set the **PercentPosition** property to a value, the record at the approximate position corresponding to that value becomes current, and the **PercentPosition** property is reset to a value that reflects the approximate position of the current record.</span></span> <span data-ttu-id="09742-115">Например если объекта **набора записей** содержит только пять записей и присвойте ему значение свойства **PercentPosition** для 77, значение, возвращенное свойством **PercentPosition** может быть 80, не 77.</span><span class="sxs-lookup"><span data-stu-id="09742-115">For example, if your **Recordset** object contains only five records, and you set its **PercentPosition** property value to 77, the value returned from the **PercentPosition** property may be 80, not 77.</span></span>

<span data-ttu-id="09742-116">Свойство **PercentPosition** применяется ко всем типам объектов **наборов записей** , за исключением объекты **набора записей** прямого — только — тип или **набора записей** открывается из запросов к серверу для удаленной баз данных.</span><span class="sxs-lookup"><span data-stu-id="09742-116">The **PercentPosition** property applies to all types of **Recordset** objects except for forward–only–type **Recordset** objects or **Recordset** objects opened from pass-through queries against remote databases.</span></span>

<span data-ttu-id="09742-117">Свойство **PercentPosition** с полосы прокрутки на форме или текстовое поле для указания расположения текущей записи в объекте **набора записей** .</span><span class="sxs-lookup"><span data-stu-id="09742-117">You can use the **PercentPosition** property with a scroll bar on a form or text box to indicate the location of the current record in a **Recordset** object.</span></span>

## <a name="example"></a><span data-ttu-id="09742-118">Пример</span><span class="sxs-lookup"><span data-stu-id="09742-118">Example</span></span>

<span data-ttu-id="09742-119">В этом примере используется свойство **PercentPosition** для отображения положения указатель текущей записи с начала **набора записей**.</span><span class="sxs-lookup"><span data-stu-id="09742-119">This example uses the **PercentPosition** property to show the position of the current record pointer relative to the beginning of the **Recordset**.</span></span>

```vb
    Sub PercentPositionX() 
     
     Dim dbsNorthwind As Database 
     Dim rstProducts As Recordset2 
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
