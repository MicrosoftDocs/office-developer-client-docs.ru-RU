---
title: Recordset2.Edit Method (DAO)
TOCTitle: Edit Method
ms:assetid: 34c51eee-274d-3511-b5e2-cb74e4925ec8
ms:mtpsurl: https://msdn.microsoft.com/library/Ff192452(v=office.15)
ms:contentKeyID: 48544137
ms.date: 09/18/2015
mtps_version: v=office.15
f1_keywords:
- dao360.chm1052869
f1_categories:
- Office.Version=v15
ms.openlocfilehash: 3f55107988002cf5718eac5eb445529f5c4e3e98
ms.sourcegitcommit: c557bbcccf37a6011f89aae1ddd399dfe549d087
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/31/2018
ms.locfileid: "25867778"
---
# <a name="recordset2edit-method-dao"></a>Recordset2.Edit Method (DAO)


**Применимо к**: Access 2013, Office 2013

Копирует текущей записи из обновляемый объект **[набора записей](recordset-object-dao.md)** в буфер копирования для последующего редактирования.

## <a name="syntax"></a>Синтаксис

*выражение* . Изменение

*выражение* Переменная, которая представляет собой объект- **Recordset2** .

## <a name="remarks"></a>Замечания

После использования метода **Edit** изменений, внесенных в текущей записи полей копируются буфера копирования. Внеся необходимые изменения в запись, используйте метод **[Update](recordset2-update-method-dao.md)** для сохранения изменений.

Текущая запись остается текущей после **изменения**.


> [!NOTE]
> <P>Если изменить запись и затем выполнять любые операции, перемещает к другой записи, но не с помощью <STRONG>обновления</STRONG>, изменения не сохраняются без предупреждения. Кроме того при закрытии набора записей или завершение процедуры, которая объявляет <STRONG>записей</STRONG> или родительский объект <STRONG><A href="database-object-dao.md">базы данных</A></STRONG> или <STRONG><A href="connection-object-dao.md">подключения к</A></STRONG> измененной записи удаляется без предупреждения.</P>



Применить **изменения** вызовет ошибку, если:

  - Нет нет текущей записи.

  - Объект **подключения**, **базы данных**или **набора записей** , был открыт только для чтения.

  - Нет поля в записи, обновляемые.

  - **Базы данных** или **набора записей** была открыта в монопольном режиме другим пользователем (Microsoft Access в рабочей области).

  - Другой пользователь заблокировал страницу, содержащую записи (Microsoft Access в рабочей области).

В рабочей области Microsoft Access когда объекта **набора записей** **[LockEdits](recordset2-lockedits-property-dao.md)** задается **значение True** (pessimistically заблокирован) в многопользовательской среде запись остается заблокированным с момента **Изменение** используется до обновления Завершите. Если значение свойства **LockEdits** равно **False** (оптимистичном случае заблокирован), запись блокируется и по сравнению с предварительно измененной записи непосредственно перед обновляется в базе данных. При изменении записи так, как использовать метод **Edit** операции **обновления** происходит сбой с ошибкой во время выполнения при использовании **OpenRecordset** без указания **dbSeeChanges**. По умолчанию базы данных Microsoft Access модуль подключения ODBC, а устанавливаемый драйвер ISAM баз данных всегда использовать оптимистичный блокировки.


> [!NOTE]
> <P>Чтобы добавить, изменить или удалить записи, должен существовать уникальный индекс на запись в источнике данных. В противном случае ошибку «Отказано в доступе» произойдет на вызов метода <STRONG><A href="recordset2-addnew-method-dao.md">AddNew</A></STRONG>, <STRONG><A href="fields-delete-method-dao.md">Удаление</A></STRONG>или <STRONG>Изменение</STRONG> в рабочей области Microsoft Access.</P>



## <a name="example"></a>Пример

В этом примере используется метод **Изменить** для замены текущих данных с указанным именем. Процедура EditName является обязательным для выполнения этой процедуры.

```vb
    Sub EditX() 
     
     Dim dbsNorthwind As Database 
     Dim rstEmployees As Recordset2 
     Dim strOldFirst As String 
     Dim strOldLast As String 
     Dim strFirstName As String 
     Dim strLastName As String 
     
     Set dbsNorthwind = OpenDatabase("Northwind.mdb") 
     Set rstEmployees = _ 
     dbsNorthwind.OpenRecordset("Employees", _ 
     dbOpenDynaset) 
     
     ' Store original data. 
     strOldFirst = rstEmployees!FirstName 
     strOldLast = rstEmployees!LastName 
     
     ' Get new data for record. 
     strFirstName = Trim(InputBox( _ 
     "Enter first name:")) 
     strLastName = Trim(InputBox( _ 
     "Enter last name:")) 
     
     ' Proceed if the user entered something for both fields. 
     If strFirstName <> "" and strLastName <> "" Then 
     ' Update record with new data. 
     EditName rstEmployees, strFirstName, strLastName 
     
     With rstEmployees 
     ' Show old and new data. 
     Debug.Print "Old data: " & strOldFirst & _ 
     " " & strOldLast 
     Debug.Print "New data: " & !FirstName & _ 
     " " & !LastName 
     ' Restore original data because this is a 
     ' demonstration. 
     .Edit 
     !FirstName = strOldFirst 
     !LastName = strOldLast 
     .Update 
     End With 
     
     Else 
     Debug.Print _ 
     "You must input a string for first and last name!" 
     End If 
     
     rstEmployees.Close 
     dbsNorthwind.Close 
     
    End Sub 
     
    Sub EditName(rstTemp As Recordset2, _ 
     strFirst As String, strLast As String) 
     
     ' Make changes to record and set the bookmark to keep 
     ' the same record current. 
     With rstTemp 
     .Edit 
     !FirstName = strFirst 
     !LastName = strLast 
     .Update 
     .Bookmark = .LastModified 
     End With 
     
    End Sub
```
