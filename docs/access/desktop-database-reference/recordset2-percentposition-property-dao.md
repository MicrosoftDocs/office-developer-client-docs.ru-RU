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
ms.openlocfilehash: 7cf5a0e0a9d0cf3d3cd5ce2b89dc287b41c72f74
ms.sourcegitcommit: 1dd744993ecb4bed241ace874ad26edaef1778b8
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 11/06/2018
ms.locfileid: "25998800"
---
# <a name="recordset2percentposition-property-dao"></a>Свойство Recordset2.PercentPosition (DAO)

**Применимо к**: Access 2013, Office 2013

Задает или возвращает значение, указывающее, приблизительно, например расположение текущей записи в объекте **[набора записей](recordset-object-dao.md)** на основе процента записей в **набора записей**.

## <a name="syntax"></a>Синтаксис

*выражение* . PercentPosition

*выражение* Переменная, которая представляет собой объект- **Recordset2** .

## <a name="remarks"></a>Примечания

Чтобы указать или изменить приблизительно, например положения текущей записи в объекте **набора записей** , можно проверить или задайте для свойства **PercentPosition** . При работе с объектом **набора записей** добавляющий или моментальный снимок непосредственно из базовой таблицы заполните путем перемещения к последнему записи, прежде чем задать или свойство **PercentPosition** объекта **набора записей** . Если использовать свойство **PercentPosition** до полностью заполнения объекта **набора записей** , величину перемещения задается число записей, доступны как указано значение свойства **[RecordCount](recordset2-recordcount-property-dao.md)** . К последнему можно перемещать записи с помощью метода **[MoveLast](recordset2-movelast-method-dao.md)** .

> [!NOTE]
> Не рекомендуется использовать свойство **PercentPosition** Перемещение текущей записи к определенной записи в объекте **набора записей** . Свойство **[закладку](recordset2-bookmark-property-dao.md)** лучше всего подходит для этой задачи.

После **PercentPosition** свойству присвоено значение, записи в приблизительно, например позиции, соответствующее значение, становится текущей и свойство **PercentPosition** сбрасывается в значение, которое отражает приблизительно, например положение текущего запись. Например если объекта **набора записей** содержит только пять записей и присвойте ему значение свойства **PercentPosition** для 77, значение, возвращенное свойством **PercentPosition** может быть 80, не 77.

Свойство **PercentPosition** применяется ко всем типам объектов **наборов записей** , за исключением объекты **набора записей** прямого — только — тип или **набора записей** открывается из запросов к серверу для удаленной баз данных.

Свойство **PercentPosition** с полосы прокрутки на форме или текстовое поле для указания расположения текущей записи в объекте **набора записей** .

## <a name="example"></a>Пример

В этом примере используется свойство **PercentPosition** для отображения положения указатель текущей записи с начала **набора записей**.

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
