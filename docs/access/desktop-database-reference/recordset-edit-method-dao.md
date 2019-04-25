---
title: Метод Recordset.Edit (DAO)
TOCTitle: Edit Method
ms:assetid: a64d601b-f446-da40-0020-b99110a72872
ms:mtpsurl: https://msdn.microsoft.com/library/Ff821175(v=office.15)
ms:contentKeyID: 48546850
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Priority
ms.openlocfilehash: 82dc6e175c7168d5c1b042e85dce7b77aa96b575
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32300541"
---
# <a name="recordsetedit-method-dao"></a>Метод Recordset.Edit (DAO)

**Область применения**: Access 2013, Office 2013

Копирует текущую запись с обновляемым объектом **[Recordset](recordset-object-dao.md)** в буфер обмена для последующего редактирования.

## <a name="syntax"></a>Синтаксис

*выражение* .Edit

*выражение*: переменная, представляющая объект **Recordset**.

## <a name="remarks"></a>Примечания

После использования метода **Edit** изменения, внесенные в поля текущей записи, копируются в буфер обмена. После внесения нужных изменений в запись используйте метод **[Update](recordset-update-method-dao.md)**, чтобы сохранить изменения.

После использования метода **Edit** текущая запись остается текущей.

> [!NOTE]
> Если изменить запись, а затем выполнить какую-либо операцию, переходящую к другой записи, но без предварительного использования метода **Update**, изменения будут потеряны без предупреждения. Кроме того, если закрыть набор записей или завершить процедуру, которая объявляет объект **Recordset** или родительский объект **[Database](database-object-dao.md)** или **[Connection](connection-object-dao.md)**, измененная запись удаляется без предупреждения.

Использование метода **Edit** вызывает ошибку, если:

- Отсутствует текущая запись.

- Объект **Connection**, **Database** или **Recordset** был открыт только для чтения.

- В записи нет обновляемых полей.

- Объект **Database** или **Recordset** был открыт для монопольного использования другим пользователем (рабочая область Microsoft Access).

- Другой пользователь заблокировал страницу, содержащую запись (рабочая область Microsoft Access).

Если в рабочей области Microsoft Access свойству **[LockEdits](recordset-lockedits-property-dao.md)** объекта **Recordset** задано значение **True** (пессимистичная блокировка) в многопользовательской среде, запись останется заблокированной с момента использования метода **Edit** до завершения обновления. Если свойству **LockEdits** задано значение **False** (оптимистичная блокировка), запись заблокирована и сравнивается с состоянием записи до изменения непосредственно перед обновлением в базе данных. Если запись была изменена после использования метода **Edit**, операция **Update** завершается ошибкой во время выполнения, если используется **OpenRecordset** без указания **dbSeeChanges**. По умолчанию в ODBC с подключением к ядру СУБД Microsoft Access и устанавливаемых базах данных ISAM всегда используется оптимистичная блокировка.

> [!NOTE]
> Чтобы запись можно было добавить, изменить или удалить, в базовом источнике данных должен быть указан ее уникальный индекс. Если это не так, при вызове метода **[AddNew](recordset-addnew-method-dao.md)**, **[Delete](fields-delete-method-dao.md)** или **Edit** возникнет ошибка "Отказано в разрешении" в рабочей области Microsoft Access.

## <a name="example"></a>Пример

В этом примере используется метод **Edit** для замены текущих данных указанным именем. Процедура EditName является обязательной для запуска этой процедуры.

```vb
    Sub EditX() 
     
     Dim dbsNorthwind As Database 
     Dim rstEmployees As Recordset 
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
     
    Sub EditName(rstTemp As Recordset, _ 
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
