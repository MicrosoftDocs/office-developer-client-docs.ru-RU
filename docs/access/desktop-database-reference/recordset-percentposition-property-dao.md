---
title: Свойство Recordset.PercentPosition (DAO)
TOCTitle: PercentPosition Property
ms:assetid: aebbda44-ed72-7a6c-0cd5-28c8997d4d96
ms:mtpsurl: https://msdn.microsoft.com/library/Ff821751(v=office.15)
ms:contentKeyID: 48547077
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: 118b93641184eed367cd5f0f00a15a13ff28cd58
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32300167"
---
# <a name="recordsetpercentposition-property-dao"></a><span data-ttu-id="b9a71-102">Свойство Recordset.PercentPosition (DAO)</span><span class="sxs-lookup"><span data-stu-id="b9a71-102">Recordset.PercentPosition property (DAO)</span></span>

<span data-ttu-id="b9a71-103">**Область применения**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="b9a71-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="b9a71-104">Задает или возвращает значение, определяющее приблизительное место текущей записи в объекте **[Recordset](recordset-object-dao.md)** на основе процента записей в **Recordset**.</span><span class="sxs-lookup"><span data-stu-id="b9a71-104">Sets or returns a value indicating the approximate location of the current record in the **[Recordset](recordset-object-dao.md)** object based on a percentage of the records in the **Recordset**.</span></span>

## <a name="syntax"></a><span data-ttu-id="b9a71-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="b9a71-105">Syntax</span></span>

<span data-ttu-id="b9a71-106">*выражение .* PercentPosition</span><span class="sxs-lookup"><span data-stu-id="b9a71-106">*expression* .PercentPosition</span></span>

<span data-ttu-id="b9a71-107">*expression*: переменная, представляющая объект **Recordset**.</span><span class="sxs-lookup"><span data-stu-id="b9a71-107">*expression* A variable that represents a **Recordset** object.</span></span>

## <a name="remarks"></a><span data-ttu-id="b9a71-108">Примечания</span><span class="sxs-lookup"><span data-stu-id="b9a71-108">Remarks</span></span>

<span data-ttu-id="b9a71-109">Чтобы указать или изменить приблизительное положение текущей записи в объекте **Recordset,** можно проверить или установить **свойство PercentPosition.**</span><span class="sxs-lookup"><span data-stu-id="b9a71-109">To indicate or change the approximate position of the current record in a **Recordset** object, you can check or set the **PercentPosition** property.</span></span> <span data-ttu-id="b9a71-110">При работе с объектом **Recordset** типа dynaset или моментальный снимок, открытым непосредственно из базовой таблицы, сначала заполняйте объект **Recordset,** переходя к последней записи, прежде чем устанавливать или проверять свойство **PercentPosition.**</span><span class="sxs-lookup"><span data-stu-id="b9a71-110">When working with a dynaset- or snapshot-type **Recordset** object opened directly from a base table, first populate the **Recordset** object by moving to the last record before you set or check the **PercentPosition** property.</span></span> <span data-ttu-id="b9a71-111">Если вы используете свойство **PercentPosition** перед полностью заполнением объекта **Recordset,** то объем перемещения относительно количества записей, к ним можно получить доступ, как указано в параметре свойства **[RecordCount.](recordset-recordcount-property-dao.md)**</span><span class="sxs-lookup"><span data-stu-id="b9a71-111">If you use the **PercentPosition** property before fully populating the **Recordset** object, the amount of movement is relative to the number of records accessed as indicated by the **[RecordCount](recordset-recordcount-property-dao.md)** property setting.</span></span> <span data-ttu-id="b9a71-112">Вы можете перейти к последней записи с помощью метода **[MoveLast.](recordset-movelast-method-dao.md)**</span><span class="sxs-lookup"><span data-stu-id="b9a71-112">You can move to the last record by using the **[MoveLast](recordset-movelast-method-dao.md)** method.</span></span>

> [!NOTE]
> <span data-ttu-id="b9a71-113">Не рекомендуется **использовать свойство PercentPosition** для перемещения текущей записи в определенную запись в **объекте Recordset.**</span><span class="sxs-lookup"><span data-stu-id="b9a71-113">Using the **PercentPosition** property to move the current record to a specific record in a **Recordset** object isn't recommended.</span></span> <span data-ttu-id="b9a71-114">Свойство **[Bookmark](recordset-bookmark-property-dao.md)** лучше подходит для этой задачи.</span><span class="sxs-lookup"><span data-stu-id="b9a71-114">The **[Bookmark](recordset-bookmark-property-dao.md)** property is better suited for this task.</span></span>

<span data-ttu-id="b9a71-115">После того как вы установите для свойства **PercentPosition** значение, запись в приблизительном положении, соответствующем этому значению, становится текущей, а свойство **PercentPosition** сбрасывается до значения, которое отражает приблизительное положение текущей записи.</span><span class="sxs-lookup"><span data-stu-id="b9a71-115">Once you set the **PercentPosition** property to a value, the record at the approximate position corresponding to that value becomes current, and the **PercentPosition** property is reset to a value that reflects the approximate position of the current record.</span></span> <span data-ttu-id="b9a71-116">Например, если объект **Recordset** содержит только пять записей, а для свойства **PercentPosition** установлено значение 77, значение, возвращенное свойством **PercentPosition,** может быть 80, а не 77.</span><span class="sxs-lookup"><span data-stu-id="b9a71-116">For example, if your **Recordset** object contains only five records, and you set its **PercentPosition** property value to 77, the value returned from the **PercentPosition** property may be 80, not 77.</span></span>

<span data-ttu-id="b9a71-117">Свойство **PercentPosition** применяется ко всем типам объектов **Recordset,** за исключением объектов **Recordset** с однонастройным типом или объектов **Recordset,** открытых в сквозных запросах к удаленным базам данных.</span><span class="sxs-lookup"><span data-stu-id="b9a71-117">The **PercentPosition** property applies to all types of **Recordset** objects except for forward–only–type **Recordset** objects or **Recordset** objects opened from pass-through queries against remote databases.</span></span>

<span data-ttu-id="b9a71-118">Вы можете использовать свойство **PercentPosition** со ролем прокрутки в форме или текстовом поле, чтобы указать расположение текущей записи в **объекте Recordset.**</span><span class="sxs-lookup"><span data-stu-id="b9a71-118">You can use the **PercentPosition** property with a scroll bar on a form or text box to indicate the location of the current record in a **Recordset** object.</span></span>

## <a name="example"></a><span data-ttu-id="b9a71-119">Пример</span><span class="sxs-lookup"><span data-stu-id="b9a71-119">Example</span></span>

<span data-ttu-id="b9a71-120">В этом примере свойство **PercentPosition** используется для показа положения указателя текущей записи относительно начала **объекта Recordset.**</span><span class="sxs-lookup"><span data-stu-id="b9a71-120">This example uses the **PercentPosition** property to show the position of the current record pointer relative to the beginning of the **Recordset**.</span></span>

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
