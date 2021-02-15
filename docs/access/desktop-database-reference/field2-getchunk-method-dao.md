---
title: Метод Field2.GetChunk (DAO)
TOCTitle: GetChunk method
ms:assetid: 5d3a66c0-8216-d701-0a91-b79fbbc822b8
ms:mtpsurl: https://msdn.microsoft.com/library/Ff194600(v=office.15)
ms:contentKeyID: 48545101
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: 6a4b850658ca4ab36b0d4f4cbed7266d39b4ff8d
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32292778"
---
# <a name="field2getchunk-method-dao"></a>Метод Field2.GetChunk (DAO)

**Область применения**: Access 2013, Office 2013

Возвращает все или часть содержимого объекта **Memo** или **Long BinaryField2** в коллекции **[Fields](fields-collection-dao.md)** объекта **[Recordset.](recordset-object-dao.md)**

## <a name="syntax"></a>Синтаксис

*выражение .* GetChunk(***Offset***, ***Bytes***)

*expression* — переменная, представляющая объект **Field2**.

## <a name="parameters"></a>Параметры

<table>
<colgroup>
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
</colgroup>
<thead>
<tr class="header">
<th><p>Имя</p></th>
<th><p>Обязательный/необязательный</p></th>
<th><p>Тип данных</p></th>
<th><p>Описание</p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><em>Offset</em></p></td>
<td><p>Обязательный</p></td>
<td><p><strong>Long</strong></p></td>
<td><p>Количество пропуститых до начала копирования вбавок.</p></td>
</tr>
<tr class="even">
<td><p><em>Bytes</em></p></td>
<td><p>Обязательный</p></td>
<td><p><strong>Long</strong></p></td>
<td><p>Количество возвращаемого количества ветвей.</p></td>
</tr>
</tbody>
</table>


## <a name="return-value"></a>Возвращаемое значение

Variant

## <a name="remarks"></a>Примечания

Возвращаемая **GetChunk** величина вбавляет в переменную. Используйте **GetChunk** для возврата части общего значения данных за раз. Вы можете использовать метод **[AppendChunk](field-appendchunk-method-dao.md)** для повторной разборки фрагментов.

Если смещение 0, **GetChunk** начинает копировать из первого byte поля.

Если количество оставшихся в поле больше количества, **GetChunk** возвращает фактическое количество оставшихся в поле.

> [!NOTE]
> Используйте поле **Memo** для текста и поместите двоичные данные только в **длинные двоичные** поля. В противном случае это приведет к нежелательным результатам.

## <a name="example"></a>Пример

В этом примере используются методы **AppendChunk** и **GetChunk** для заполнения поля объекта OLE данными из другой записи по 32K одновременно. В реальном приложении можно использовать процедуру, похожую на эту, для копирования записи сотрудника (включая фотографию сотрудника) из одной таблицы в другую. В этом примере запись просто копируется обратно в ту же таблицу. Обратите внимание, что все манипуляции с блоками происходит в одной AddNew-Update последовательности.

```vb
    Sub AppendChunkX() 
     
     Dim dbsNorthwind As Database 
     Dim rstEmployees As Recordset 
     Dim rstEmployees2 As Recordset 
     
     Set dbsNorthwind = OpenDatabase("Northwind.mdb") 
     
     ' Open two recordsets from the Employees table. 
     Set rstEmployees = _ 
     dbsNorthwind.OpenRecordset("Employees", _ 
     dbOpenDynaset) 
     Set rstEmployees2 = rstEmployees.Clone 
     
     ' Add a new record to the first Recordset and copy the 
     ' data from a record in the second Recordset. 
     With rstEmployees 
     .AddNew 
     !FirstName = rstEmployees2!FirstName 
     !LastName = rstEmployees2!LastName 
     CopyLargeField rstEmployees2!Photo, !Photo 
     .Update 
     
     ' Delete new record because this is a demonstration. 
     .Bookmark = .LastModified 
     .Delete 
     .Close 
     End With 
     
     rstEmployees2.Close 
     dbsNorthwind.Close 
     
    End Sub 
     
    Function CopyLargeField(fldSource As Field2, _ 
     fldDestination As Field2) 
     
     ' Set size of chunk in bytes. 
     Const conChunkSize = 32768 
     
     Dim lngOffset As Long 
     Dim lngTotalSize As Long 
     Dim strChunk As String 
     
     ' Copy the photo from one Recordset to the other in 32K 
     ' chunks until the entire field is copied. 
     lngTotalSize = fldSource.FieldSize 
     Do While lngOffset < lngTotalSize 
     strChunk = fldSource.GetChunk(lngOffset, conChunkSize) 
     fldDestination.AppendChunk strChunk 
     lngOffset = lngOffset + conChunkSize 
     Loop 
     
    End Function
```
