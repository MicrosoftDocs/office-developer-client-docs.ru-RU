---
title: Метод Field.GetChunk (DAO)
TOCTitle: GetChunk Method
ms:assetid: b8984e79-54f7-8052-85a3-d12033daf7a1
ms:mtpsurl: https://msdn.microsoft.com/library/Ff822448(v=office.15)
ms:contentKeyID: 48547328
ms.date: 09/18/2015
mtps_version: v=office.15
f1_keywords:
- dao360.chm1052871
f1_categories:
- Office.Version=v15
localization_priority: Normal
ms.openlocfilehash: c7eabceb1f7c130e349428aeb6b2dc079fe4319d
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32293100"
---
# <a name="fieldgetchunk-method-dao"></a>Метод Field.GetChunk (DAO)

**Область применения**: Access 2013, Office 2013

Возвращает все или часть содержимого объекта **Memo** или **Long Binary** **[Field](field-object-dao.md)** в коллекции **[Fields](fields-collection-dao.md)** объекта **[Recordset.](recordset-object-dao.md)**

## <a name="syntax"></a>Синтаксис

*выражение .* GetChunk(***Offset***, ***Bytes***)

*выражение*: переменная, представляющая объект **Field**.

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
<td><p>Количество пропущенных перед началом копирования количеством пропусков.</p></td>
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

Возвращаемая **GetChunk** величина вбавляет в переменную. Используйте **GetChunk** для возврата части общего значения данных за раз. Для повторной разборки фрагментов можно использовать метод **[AppendChunk.](field-appendchunk-method-dao.md)**

Если смещение 0, **GetChunk** начинает копировать из первого byte поля.

Если количество оставшихся в поле больше количества, **GetChunk** возвращает фактическое количество оставшихся в поле.

> [!NOTE]
> Используйте поле **Memo** для текста и поместите двоичные данные только в **длинные двоичные** поля. В противном случае это приведет к нежелательным результатам.

## <a name="example"></a>Пример

В этом примере используются методы **AppendChunk** и **GetChunk** для заполнения поля объекта OLE данными из другой записи 32K одновременно. В реальном приложении можно использовать процедуру, похожую на эту, для копирования записи сотрудника (включая фотографию сотрудника) из одной таблицы в другую. В этом примере запись просто копируется обратно в ту же таблицу. Обратите внимание, что все манипуляции с блоками происходит в одной AddNew-Update последовательности.

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
     
    Function CopyLargeField(fldSource As Field, _ 
     fldDestination As Field) 
     
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
