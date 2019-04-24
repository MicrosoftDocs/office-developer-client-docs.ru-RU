---
title: Метод Recordset2. Edit (DAO)
TOCTitle: Edit method
ms:assetid: 34c51eee-274d-3511-b5e2-cb74e4925ec8
ms:mtpsurl: https://msdn.microsoft.com/library/Ff192452(v=office.15)
ms:contentKeyID: 48544137
ms.date: 09/18/2015
mtps_version: v=office.15
f1_keywords:
- dao360.chm1052869
f1_categories:
- Office.Version=v15
localization_priority: Normal
ms.openlocfilehash: 2742b6558c555673937666ea7d27cae1a54fdf73
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32309438"
---
# <a name="recordset2edit-method-dao"></a>Метод Recordset2. Edit (DAO)

**Область применения**: Access 2013, Office 2013

Копирует текущую запись с обновляемым объектом **[Recordset](recordset-object-dao.md)** в буфер обмена для последующего редактирования.

## <a name="syntax"></a>Синтаксис

*Expression* . Правка

*Expression (выражение* ) Переменная, представляющая объект **Recordset2** .

## <a name="remarks"></a>Замечания

После использования метода **Edit** изменения, внесенные в поля текущей записи, копируются в буфер копирования. После внесения требуемых изменений в запись используйте метод **[Update](recordset2-update-method-dao.md)** , чтобы сохранить изменения.

Текущая запись остается текущей, после того как вы используете **Edit**.

> [!NOTE]
> Если изменить запись и затем выполнить любую операцию, которая перемещается в другую запись, но без предварительного **обновления**, изменения будут потеряны без предупреждения. Кроме того, если закрывать набор записей или завершать процедуру, в которой объявляется **набор записей** или родительский объект **[базы данных](database-object-dao.md)** или **[подключения](connection-object-dao.md)** , отредактированная запись удаляется без предупреждения.

При использовании метода **Edit** выдается сообщение об ошибке, если:

- Нет текущей записи.

- Объект **подключения**, **базы данных**или объекта **Recordset** открыт только для чтения.

- Поля в записи не обновляются.

- **База данных** или **набор записей** были открыты для монопольного использования другим пользователем (рабочей областью Microsoft Access).

- Другой пользователь заблокировал страницу, содержащую запись (Рабочая область Microsoft Access).

В рабочей области Microsoft Access, когда значение свойства **[LockEdits](recordset2-lockedits-property-dao.md)** объекта **Recordset** (пессимистикалли заблокировано) в многопользовательской среде, запись остается заблокированной, пока не будет установлено обновление. **** **** заполнить. Если для свойства **LockEdits** задано **значение false** (оптимистикалли заблокировано), запись блокируется и сравнивается с предварительно измененной записью непосредственно перед ее обновлением в базе данных. Если после использования метода **Edit** запись изменилась, операция **обновления** завершается с ошибкой во время выполнения, если вы используете **OpenRecordset** без указания **дбсичанжес**. По умолчанию ODBC и устанавливаемые базы данных ISAM, подключенные к ядру СУБД Microsoft Access, всегда используют оптимистическую блокировку.

> [!NOTE]
> Чтобы запись можно было добавить, изменить или удалить, в базовом источнике данных должен быть указан ее уникальный индекс. В противном случае при вызове метода **[AddNew](recordset2-addnew-method-dao.md)**, **[Delete](fields-delete-method-dao.md)** или **Edit** в рабочей области Microsoft Access произойдет ошибка "отказано в разрешении".

## <a name="example"></a>Пример

В этом примере с помощью метода **Edit** заменяются текущие данные с указанным именем. Для выполнения этой процедуры требуется процедура Едитнаме.

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
