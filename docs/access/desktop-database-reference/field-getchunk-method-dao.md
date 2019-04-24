---
title: Метод Field. выБлоч (DAO)
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
# <a name="fieldgetchunk-method-dao"></a>Метод Field. выБлоч (DAO)

**Область применения**: Access 2013, Office 2013

Возвращает полностью или часть содержимого объекта **MEMO** или длинного двоичного **** объекта **[field](field-object-dao.md)** в коллекции Fields **[](fields-collection-dao.md)** объекта **[Recordset](recordset-object-dao.md)** .

## <a name="syntax"></a>Синтаксис

*Expression* . ПереФрагмент (***offset***, ***bytes***)

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
<th><p>Обязательно/необязательно</p></th>
<th><p>Тип данных</p></th>
<th><p>Описание</p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><em>Offset</em></p></td>
<td><p>Обязательный</p></td>
<td><p><strong>Long</strong></p></td>
<td><p>Число байтов, которые необходимо пропустить перед началом копирования.</p></td>
</tr>
<tr class="even">
<td><p><em>Числа</em></p></td>
<td><p>Обязательный</p></td>
<td><p><strong>Long</strong></p></td>
<td><p>Число возвращаемых байтов.</p></td>
</tr>
</tbody>
</table>


## <a name="return-value"></a>Возвращаемое значение

Variant

## <a name="remarks"></a>Примечания

Возвращаемые методом GetBytes **** байты присваиваются переменной. Используйте параметрического **блока** , чтобы возвратить часть значения данных за раз. Для повторной сборки частей можно использовать метод **[AppendChunk](field-appendchunk-method-dao.md)** .

Если смещение равно 0, то операция- **блок** начинает копироваться с первого байта поля.

Если нумбитес больше, чем число байтов в поле, то параметр GetBytes **** возвращает фактическое количество оставшихся байтов в поле.

> [!NOTE]
> Используйте поле **MEMO** для текста и разместите двоичные данные только в **длинных двоичных** полях. В противном случае могут возникнуть нежелательные результаты.

## <a name="example"></a>Пример

В этом примере используются методы **AppendChunk** и GetObject для заполнения поля объекта OLE данными из другой записи (32 КБ) за раз. **** В реальном приложении можно использовать такую процедуру, как копирование записи сотрудника (включая фотографию сотрудника) из одной таблицы в другую. В этом примере запись просто копируется обратно в ту же таблицу. Обратите внимание, что все операции с блоками выполняются в рамках одной последовательности с обновлением с помощью метода AddNew.

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
