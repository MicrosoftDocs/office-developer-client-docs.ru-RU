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
# <a name="recordsetpercentposition-property-dao"></a>Свойство Recordset.PercentPosition (DAO)

**Область применения**: Access 2013, Office 2013

Задает или возвращает значение, определяющее приблизительное место текущей записи в объекте **[Recordset](recordset-object-dao.md)** на основе процента записей в **Recordset**.

## <a name="syntax"></a>Синтаксис

*выражения* . PercentPosition

*expression*: переменная, представляющая объект **Recordset**.

## <a name="remarks"></a>Примечания

Чтобы указать или изменить приблизительное положение текущей записи в объекте **Recordset,** можно проверить или установить **свойство PercentPosition.** При работе с объектом **Recordset** dynaset или snapshot-type, открытым непосредственно из базовой таблицы, сначала заполняйте объект **Recordset,** перед тем как установить или проверить свойство **PercentPosition.** Если вы используете свойство **PercentPosition,** прежде чем полностью заполнить объект **Recordset,** объем перемещения относительно количества записей, доступных по указанию параметра **[Свойства RecordCount.](recordset-recordcount-property-dao.md)** Вы можете перейти к последней записи с помощью метода **[MoveLast.](recordset-movelast-method-dao.md)**

> [!NOTE]
> Использование свойства **PercentPosition** для перемещения текущей записи к определенной записи в **объекте Recordset** не рекомендуется. Свойство **[Bookmark](recordset-bookmark-property-dao.md)** лучше подходит для этой задачи.

После заложения свойства **PercentPosition** значение записи в приблизительном расположении, соответствующем этому значению, становится текущим, а свойство **PercentPosition** сбрасывается до значения, отражаемого приблизительное положение текущей записи. Например, если объект **Recordset** содержит только пять записей, а значение свойства **PercentPosition** — 77, значение, возвращенное из свойства **PercentPosition,** может быть 80, а не 77.

Свойство **PercentPosition** применяется ко всем типам объектов **Recordset,** за исключением объектов Recordset только для форвардного типа или объектов **Recordset,** открытых из сквозных запросов удаленных баз данных. 

Свойство **PercentPosition** можно использовать с помощью панели прокрутки на форме или текстовом поле, чтобы указать расположение текущей записи в **объекте Recordset.**

## <a name="example"></a>Пример

В этом примере свойство **PercentPosition** показывает положение текущего указателя записи относительно начала **наборов записей.**

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
