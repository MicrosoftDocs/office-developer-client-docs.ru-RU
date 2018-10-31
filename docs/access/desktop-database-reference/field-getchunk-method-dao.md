---
title: Field.GetChunk Method (DAO)
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
ms.openlocfilehash: 691b4d0b18b31c4c4a40f73e232a1829101913f1
ms.sourcegitcommit: 801b1b54786f7b0e5b0d35466e7ae8d1e840b26f
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/31/2018
ms.locfileid: "25863278"
---
# <a name="fieldgetchunk-method-dao"></a>Field.GetChunk Method (DAO)


**Применимо к**: Access 2013 | Office 2013

Возвращает все или часть содержимого объекта **Memo** или **Long Binary** **[поле](field-object-dao.md)** в коллекции **[полей](fields-collection-dao.md)** объекта **[набора записей](recordset-object-dao.md)** .

## <a name="syntax"></a>Синтаксис

*выражение* . Методы GetChunk (***смещение***, ***в байтах***)

*выражение* Переменная, которая представляет собой объект- **поля** .

### <a name="parameters"></a>Параметры

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
<th><p>Обязательный или необязательный</p></th>
<th><p>Тип данных</p></th>
<th><p>Описание</p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p>Offset</p></td>
<td><p>Обязательный</p></td>
<td><p><strong>Длинный</strong></p></td>
<td><p>Число байтов, пропустите перед начинается копирование.</p></td>
</tr>
<tr class="even">
<td><p>Байт</p></td>
<td><p>Обязательный</p></td>
<td><p><strong>Длинный</strong></p></td>
<td><p>Число байтов, которые необходимо вернуть.</p></td>
</tr>
</tbody>
</table>


<<<<<<< HEAD
### <a name="return-value"></a>Возвращаемое значение
=======
### <a name="return-value"></a>Возвращаемое значение
>>>>>>> образец

Variant

## <a name="remarks"></a>Замечания

Байт, возвращаемых **GetChunk** назначаются переменной. Используйте **GetChunk** для возврата значения данных за раз. Метод **[AppendChunk](field-appendchunk-method-dao.md)** воссоздать компоненты.

Если смещение равно 0, **GetChunk** начинает копировать из первого байта ответа от поля.

Если numbytes больше, чем число байтов в поле, **GetChunk** возвращает фактическое число байтов оставшихся в соответствующем поле.


> [!NOTE]
> Используйте поле **Memo** для текста и поместить двоичные данные только в **Длинный двоичные** поля. В противном случае это приведет к нежелательным результатам.



## <a name="example"></a>Пример

В этом примере использует методы **AppendChunk** и **GetChunk** для заполнения поле объекта OLE с данными из другой записи 32 КБ за раз. В реальном приложении один может использовать процедуру следующим образом для копирования запись сотрудника (включая фотографию сотрудника) из одной таблицы в другую. В этом примере запись просто копируется обратно в одной таблицы. Обратите внимание, что все операции блока выполняется в рамках одного последовательность обновления AddNew.

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
