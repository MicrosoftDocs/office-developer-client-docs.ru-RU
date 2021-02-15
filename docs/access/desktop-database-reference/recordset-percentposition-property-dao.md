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

*выражение .* PercentPosition

*expression*: переменная, представляющая объект **Recordset**.

## <a name="remarks"></a>Примечания

Чтобы указать или изменить приблизительное положение текущей записи в объекте **Recordset,** можно проверить или установить **свойство PercentPosition.** При работе с объектом **Recordset** типа dynaset или моментальный снимок, открытым непосредственно из базовой таблицы, сначала заполняйте объект **Recordset,** переходя к последней записи, прежде чем устанавливать или проверять свойство **PercentPosition.** Если вы используете свойство **PercentPosition** перед полностью заполнением объекта **Recordset,** то объем перемещения относительно количества записей, к ним можно получить доступ, как указано в параметре свойства **[RecordCount.](recordset-recordcount-property-dao.md)** Вы можете перейти к последней записи с помощью метода **[MoveLast.](recordset-movelast-method-dao.md)**

> [!NOTE]
> Не рекомендуется **использовать свойство PercentPosition** для перемещения текущей записи в определенную запись в **объекте Recordset.** Свойство **[Bookmark](recordset-bookmark-property-dao.md)** лучше подходит для этой задачи.

После того как вы установите для свойства **PercentPosition** значение, запись в приблизительном положении, соответствующем этому значению, становится текущей, а свойство **PercentPosition** сбрасывается до значения, которое отражает приблизительное положение текущей записи. Например, если объект **Recordset** содержит только пять записей, а для свойства **PercentPosition** установлено значение 77, значение, возвращенное свойством **PercentPosition,** может быть 80, а не 77.

Свойство **PercentPosition** применяется ко всем типам объектов **Recordset,** за исключением объектов **Recordset** с однонастройным типом или объектов **Recordset,** открытых в сквозных запросах к удаленным базам данных.

Вы можете использовать свойство **PercentPosition** со ролем прокрутки в форме или текстовом поле, чтобы указать расположение текущей записи в **объекте Recordset.**

## <a name="example"></a>Пример

В этом примере свойство **PercentPosition** используется для показа положения указателя текущей записи относительно начала **объекта Recordset.**

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
