---
title: Метод field2. AppendChunk (DAO)
TOCTitle: AppendChunk Method
ms:assetid: 540cd02d-1fc6-81d1-ac08-1e3df72a7208
ms:mtpsurl: https://msdn.microsoft.com/library/Ff194088(v=office.15)
ms:contentKeyID: 48544886
ms.date: 09/18/2015
mtps_version: v=office.15
f1_keywords:
- dao360.chm1052867
f1_categories:
- Office.Version=v15
localization_priority: Normal
ms.openlocfilehash: fda1ab5a3e339d951225f4f43ab4275cce2cdb80
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32292883"
---
# <a name="field2appendchunk-method-dao"></a>Метод field2. AppendChunk (DAO)

**Область применения**: Access 2013, Office 2013

Добавляет данные из строкового выражения в объект MEMO или большой двоичный объект **field2** в **[наборе записей](recordset-object-dao.md)**.

## <a name="syntax"></a>Синтаксис

*Expression* . AppendChunk (***Val***)

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
<td><p><em>Val</em></p></td>
<td><p>Обязательный</p></td>
<td><p><strong>Variant</strong></p></td>
<td><p>Выражение типа Variant (String подтип) или переменная, содержащая данные, которые необходимо добавить в объект <strong>field2</strong> .</p></td>
</tr>
</tbody>
</table>


## <a name="remarks"></a>Примечания

Вы можете использовать методы **AppendChunk** и **,** чтобы получить доступ к подмножествам данных в поле MEMO или длинном двоичном поле.

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
