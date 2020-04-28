---
title: Свойство Recordset2. PercentPosition (DAO)
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
localization_priority: Normal
ms.openlocfilehash: 7b0a086004d987a73e6dfb18fe5f919c239fb66c
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32307226"
---
# <a name="recordset2percentposition-property-dao"></a><span data-ttu-id="6495b-102">Свойство Recordset2. PercentPosition (DAO)</span><span class="sxs-lookup"><span data-stu-id="6495b-102">Recordset2.PercentPosition property (DAO)</span></span>

<span data-ttu-id="6495b-103">**Область применения**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="6495b-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="6495b-104">Задает или возвращает значение, определяющее приблизительное место текущей записи в объекте **[Recordset](recordset-object-dao.md)** на основе процента записей в **Recordset**.</span><span class="sxs-lookup"><span data-stu-id="6495b-104">Sets or returns a value indicating the approximate location of the current record in the **[Recordset](recordset-object-dao.md)** object based on a percentage of the records in the **Recordset**.</span></span>

## <a name="syntax"></a><span data-ttu-id="6495b-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="6495b-105">Syntax</span></span>

<span data-ttu-id="6495b-106">*Expression* . PercentPosition</span><span class="sxs-lookup"><span data-stu-id="6495b-106">*expression* .PercentPosition</span></span>

<span data-ttu-id="6495b-107">*Expression (выражение* ) Переменная, представляющая объект **Recordset2** .</span><span class="sxs-lookup"><span data-stu-id="6495b-107">*expression* A variable that represents a **Recordset2** object.</span></span>

## <a name="remarks"></a><span data-ttu-id="6495b-108">Примечания</span><span class="sxs-lookup"><span data-stu-id="6495b-108">Remarks</span></span>

<span data-ttu-id="6495b-109">Чтобы указать или изменить приближенное положение текущей записи в объекте **Recordset** , можно проверить или задать свойство **PercentPosition** .</span><span class="sxs-lookup"><span data-stu-id="6495b-109">To indicate or change the approximate position of the current record in a **Recordset** object, you can check or set the **PercentPosition** property.</span></span> <span data-ttu-id="6495b-110">При работе с объект **Recordset** типа динамического подмножества или моментального снимка, Открытый непосредственно из базовой таблицы, сначала заполните объект **Recordset** , переместив на последнюю запись, прежде чем вы задаете или проверяете свойство **PercentPosition** .</span><span class="sxs-lookup"><span data-stu-id="6495b-110">When working with a dynaset- or snapshot-type **Recordset** object opened directly from a base table, first populate the **Recordset** object by moving to the last record before you set or check the **PercentPosition** property.</span></span> <span data-ttu-id="6495b-111">Если вы используете свойство **PercentPosition** перед полным заполнением объекта **Recordset** , объем передвижения определяется относительно количества записей, доступ к которым можно получить, как указано в параметре свойства **[RecordCount](recordset2-recordcount-property-dao.md)** .</span><span class="sxs-lookup"><span data-stu-id="6495b-111">If you use the **PercentPosition** property before fully populating the **Recordset** object, the amount of movement is relative to the number of records accessed as indicated by the **[RecordCount](recordset2-recordcount-property-dao.md)** property setting.</span></span> <span data-ttu-id="6495b-112">Вы можете перейти к последней записи с помощью метода **[MoveLast](recordset2-movelast-method-dao.md)** .</span><span class="sxs-lookup"><span data-stu-id="6495b-112">You can move to the last record by using the **[MoveLast](recordset2-movelast-method-dao.md)** method.</span></span>

> [!NOTE]
> <span data-ttu-id="6495b-113">Использование свойства **PercentPosition** для перемещения текущей записи в определенную запись в объекте **Recordset** не рекомендуется.</span><span class="sxs-lookup"><span data-stu-id="6495b-113">Using the **PercentPosition** property to move the current record to a specific record in a **Recordset** object isn't recommended.</span></span> <span data-ttu-id="6495b-114">Свойство **[Bookmark](recordset2-bookmark-property-dao.md)** лучше подходит для этой задачи.</span><span class="sxs-lookup"><span data-stu-id="6495b-114">The **[Bookmark](recordset2-bookmark-property-dao.md)** property is better suited for this task.</span></span>

<span data-ttu-id="6495b-115">Когда для свойства **PercentPosition** задано значение, запись в приближенной позиции, соответствующая этому значению, становится текущей, и свойство **PercentPosition** сбрасывается в значение, отражающее приближенное положение текущей записи.</span><span class="sxs-lookup"><span data-stu-id="6495b-115">Once you set the **PercentPosition** property to a value, the record at the approximate position corresponding to that value becomes current, and the **PercentPosition** property is reset to a value that reflects the approximate position of the current record.</span></span> <span data-ttu-id="6495b-116">Например, если объект **Recordset** содержит только пять записей и для свойства **PercentPosition** задано значение 77, то значение, возвращаемое свойством **PercentPosition** , может быть равно 80, а не 77.</span><span class="sxs-lookup"><span data-stu-id="6495b-116">For example, if your **Recordset** object contains only five records, and you set its **PercentPosition** property value to 77, the value returned from the **PercentPosition** property may be 80, not 77.</span></span>

<span data-ttu-id="6495b-117">Свойство **PercentPosition** применяется ко всем типам объектов **Recordset** , за исключением однонаправленных объектов **Recordset** и объектов **Recordset** , открытых из запросов к удаленным базам данных.</span><span class="sxs-lookup"><span data-stu-id="6495b-117">The **PercentPosition** property applies to all types of **Recordset** objects except for forward–only–type **Recordset** objects or **Recordset** objects opened from pass-through queries against remote databases.</span></span>

<span data-ttu-id="6495b-118">Свойство **PercentPosition** можно использовать с полосой прокрутки формы или текстового поля, чтобы указать расположение текущей записи в объекте **Recordset** .</span><span class="sxs-lookup"><span data-stu-id="6495b-118">You can use the **PercentPosition** property with a scroll bar on a form or text box to indicate the location of the current record in a **Recordset** object.</span></span>

## <a name="example"></a><span data-ttu-id="6495b-119">Пример</span><span class="sxs-lookup"><span data-stu-id="6495b-119">Example</span></span>

<span data-ttu-id="6495b-120">В этом примере используется свойство **PercentPosition** для отображения положения указателя текущей записи относительно начала **набора записей**.</span><span class="sxs-lookup"><span data-stu-id="6495b-120">This example uses the **PercentPosition** property to show the position of the current record pointer relative to the beginning of the **Recordset**.</span></span>

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
