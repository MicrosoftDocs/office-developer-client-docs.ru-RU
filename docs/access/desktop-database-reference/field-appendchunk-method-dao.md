---
title: Метод Field. AppendChunk (DAO)
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
# <a name="fieldappendchunk-method-dao"></a>Метод Field. AppendChunk (DAO)

**Область применения**: Access 2013, Office 2013

Добавляет данные из строкового выражения в объект MEMO или длинного двоичного **[поля](field-object-dao.md)** в **[наборе записей](recordset-object-dao.md)**.

## <a name="syntax"></a>Синтаксис

*Expression* . AppendChunk (***Val***)

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
<td><p>Обязательный</p></td>
<td><p><strong>Variant</strong></p></td>
<td><p>Выражение типа Variant (String подтип) или переменная, содержащие данные, которые требуется добавить в объект <strong>field</strong> .</p></td>
</tr>
</tbody>
</table>


## <a name="remarks"></a>Примечания

Вы можете использовать методы **AppendChunk** и **[,](field-getchunk-method-dao.md)** чтобы получить доступ к подмножествам данных в поле MEMO или длинном двоичном поле.

Вы также можете использовать эти методы для экономии пространства строк при работе с полями MEMO и длинных двоичных полей. Некоторые операции (например, копирование) включают временные строки. Если пространство строк ограничено, может потребоваться работа с фрагментами поля, а не с полем целиком.

Если при использовании **AppendChunk**отсутствует текущая запись, возникает ошибка.

> [!NOTE]
> Начальная операция **AppendChunk** (после вызова метода **[Edit](recordset-edit-method-dao.md)** или **[AddNew](recordset-addnew-method-dao.md)** ) просто поместит данные в поле, перезаписывая существующие данные. Последующие вызовы **AppendChunk** в рамках одного сеанса **редактирования** или **AddNew** будут добавляться к существующим данным.

## <a name="example"></a>Пример

В этом примере **используются методы** **AppendChunk** и GetObject для заполнения поля объекта OLE данными из другой записи (32 КБ) за раз. В реальном приложении можно использовать такую процедуру, как копирование записи сотрудника (включая фотографию сотрудника) из одной таблицы в другую. В этом примере запись просто копируется обратно в ту же таблицу. Обратите внимание, что все операции с блоками выполняются в рамках одной последовательности с обновлением с помощью метода AddNew.

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
