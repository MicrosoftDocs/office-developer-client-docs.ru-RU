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
localization_priority: Normal
ms.openlocfilehash: 7b0a086004d987a73e6dfb18fe5f919c239fb66c
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32307226"
---
# <a name="recordset2percentposition-property-dao"></a>Свойство Recordset2.PercentPosition (DAO)

**Область применения**: Access 2013, Office 2013

Задает или возвращает значение, определяющее приблизительное место текущей записи в объекте **[Recordset](recordset-object-dao.md)** на основе процента записей в **Recordset**.

## <a name="syntax"></a>Синтаксис

*выражение .* PercentPosition

*выражение* Переменная, представляюная объект **Recordset2.**

## <a name="remarks"></a>Заметки

Чтобы указать или изменить приблизительное положение текущей записи в объекте **Recordset,** можно проверить или установить **свойство PercentPosition.** При работе с объектом **Recordset** типа dynaset или моментальный снимок, открытым непосредственно из базовой таблицы, сначала заполняйте объект **Recordset,** переходя к последней записи, прежде чем устанавливать или проверять свойство **PercentPosition.** Если вы используете свойство **PercentPosition** перед полностью заполнением объекта **Recordset,** то объем перемещения относительно количества записей, к ним можно получить доступ, как указано в параметре свойства **[RecordCount.](recordset2-recordcount-property-dao.md)** Вы можете перейти к последней записи с помощью метода **[MoveLast.](recordset2-movelast-method-dao.md)**

> [!NOTE]
> Не рекомендуется **использовать свойство PercentPosition** для перемещения текущей записи в определенную запись в **объекте Recordset.** Свойство **[Bookmark](recordset2-bookmark-property-dao.md)** лучше подходит для этой задачи.

После того как вы установите для свойства **PercentPosition** значение, запись в приблизительном положении, соответствующем этому значению, становится текущей, а свойство **PercentPosition** сбрасывается до значения, которое отражает приблизительное положение текущей записи. Например, если объект **Recordset** содержит только пять записей, а для свойства **PercentPosition** установлено значение 77, значение, возвращенное свойством **PercentPosition,** может быть 80, а не 77.

Свойство **PercentPosition** применяется ко всем типам объектов **Recordset,** за исключением объектов **Recordset** с однонастройным типом или объектов **Recordset,** открытых в сквозных запросах к удаленным базам данных.

Вы можете использовать свойство **PercentPosition** со ролем прокрутки в форме или текстовом поле, чтобы указать расположение текущей записи в **объекте Recordset.**

## <a name="example"></a>Пример

В этом примере свойство **PercentPosition** используется для показа положения указателя текущей записи относительно начала **объекта Recordset.**

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
