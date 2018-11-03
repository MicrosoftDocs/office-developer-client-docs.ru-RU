---
title: Метод Field2.AppendChunk (DAO)
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
ms.openlocfilehash: e5aaab6a79893a66b12216f60c05690c1e806000
ms.sourcegitcommit: 38d0db57580cc5f4a0231c27b1643f8db5431ca3
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 11/02/2018
ms.locfileid: "25937052"
---
# <a name="field2appendchunk-method-dao"></a>Метод Field2.AppendChunk (DAO)

**Применимо к**: Access 2013, Office 2013

Добавление данных из строковое выражение Memo или Long Binary **поле2** объект в **[набора записей](recordset-object-dao.md)**.

## <a name="syntax"></a>Синтаксис

*выражение* . AppendChunk (***Val***)

*выражение* Переменная, которая представляет собой объект- **поле2** .

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
<td><p>Функция Val</p></td>
<td><p>Обязательный</p></td>
<td><p><strong>Variant</strong></p></td>
<td><p>Выражение типа Variant (String подтип) или переменная, содержащая данные необходимо добавить объект <strong>поле2</strong> .</p></td>
</tr>
</tbody>
</table>


## <a name="remarks"></a>Примечания

Методы **AppendChunk** и **GetChunk** для доступа к подмножества данных можно использовать в полей Memo или Long Binary.

Можно также использовать эти методы для экономии места строку при работе с полей Memo и Long Binary. Некоторые операции (например, копирование) включают временных строк. Если строка ограничено, может потребоваться работать с частями поля, а не всего поля.

Если при использовании **AppendChunk**нет текущей записи, возникает ошибка.

> [!NOTE]
> Начальное операция **AppendChunk** (после **[изменения](recordset-edit-method-dao.md)** или **[AddNew](recordset-addnew-method-dao.md)** вызова) будет просто поместить данные в поле перезапись существующих данных. Последующие **AppendChunk** вызывает в пределах того же **Изменение** или сеанса **AddNew** затем будут добавлены в существующих данных.

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
