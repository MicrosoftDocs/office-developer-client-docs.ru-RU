---
title: Метод Field.AppendChunk (DAO)
TOCTitle: AppendChunk Method
ms:assetid: f98c6862-fecf-06cb-a7c0-42b0d3150a06
ms:mtpsurl: https://msdn.microsoft.com/library/Ff837014(v=office.15)
ms:contentKeyID: 48548819
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: b1ce1c359582194ce87dfaf4f409be4303486e09
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32293170"
---
# <a name="fieldappendchunk-method-dao"></a>Метод Field.AppendChunk (DAO)

**Область применения**: Access 2013, Office 2013

Appends data from a string expression to a Memo or Long Binary **[Field](field-object-dao.md)** object in a **[Recordset](recordset-object-dao.md)**.

## <a name="syntax"></a>Синтаксис

*выражение .* AppendChunk(***Val***)

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
<td><p><em>Val</em></p></td>
<td><p>Обязательно</p></td>
<td><p><strong>Variant</strong></p></td>
<td><p>Выражение Variant (строка подтипа) или переменная, содержащая данные, которые необходимо применить к <strong>объекту Field.</strong></p></td>
</tr>
</tbody>
</table>


## <a name="remarks"></a>Заметки

Вы можете использовать методы **AppendChunk** и **[GetChunk](field-getchunk-method-dao.md)** для доступа к подмесям данных в поле Memo или Long Binary.

Эти методы также можно использовать для экономии строковых пространств при работе с полями Memo и Long Binary. Некоторые операции (например, копирование) включают временные строки. Если строковая область ограничена, может потребоваться работать с блоками поля, а не с всем полем.

Если при использовании **AppendChunk** нет текущей записи, возникает ошибка.

> [!NOTE]
> Первоначальная операция **AppendChunk** (после вызова **[Edit](recordset-edit-method-dao.md)** или **[AddNew)](recordset-addnew-method-dao.md)** просто поместите данные в поле, переописав все существующие данные. Последующие **вызовы AppendChunk** в рамках одного и того же сеанса **Edit** или **AddNew** затем добавляются к существующим данным.

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
