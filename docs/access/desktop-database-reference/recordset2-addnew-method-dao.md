---
title: Метод Recordset2.AddNew (DAO)
TOCTitle: AddNew Method
ms:assetid: 25c7d207-185c-943b-405e-b138ffb8b3e2
ms:mtpsurl: https://msdn.microsoft.com/library/Ff191874(v=office.15)
ms:contentKeyID: 48543792
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: 49a69b5e8603e72faaba480ea9069d3668bd6de1
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32307499"
---
# <a name="recordset2addnew-method-dao"></a>Метод Recordset2.AddNew (DAO)

**Область применения**: Access 2013, Office 2013
 
Создает новую запись для объекта **Recordset2** с возможностью его создания.

## <a name="syntax"></a>Синтаксис

*expression* .AddNew

*выражение* Переменная, представляюная объект **Recordset2.**

## <a name="remarks"></a>Заметки

Используйте метод **AddNew** для создания и добавления новой записи в объект **Recordset2** с именем по набору записей. Этот метод устанавливает для полей значения по умолчанию, и если значения по умолчанию не указаны, он устанавливает для полей значение NULL (значения по умолчанию, заданные для типа таблицы **Recordset2).**

После изменения новой записи используйте метод **[Update,](recordset2-update-method-dao.md)** чтобы сохранить изменения и добавить запись в **Recordset2.** В базу данных не будут внесены никакие изменения, пока вы не вызовете метод **Update**.

> [!NOTE]
> Если вызвать метод **AddNew**, а затем выполнить какую-либо операцию, переходящую к другой записи, но без использования метода **Update**, то изменения будут потеряны без предупреждения. Кроме того, при закрытии **объекта Recordset2** или завершении процедуры, в которой объявляется **объект Recordset2** или его **[база](database-object-dao.md)** данных, новая запись удаляется без предупреждения.

> [!NOTE]
> Если вы используете метод **AddNew** в рабочей области Microsoft Access, а ядру СУБД нужно создать новую страницу для хранения текущей записи, то используется пессимистическая блокировка страницы. Если новую запись можно разместить на имеющейся странице, то используется оптимистическая блокировка.

Если вы не перешли к последней записи **recordset2,** записи, добавленные в базовые таблицы другими процессами, могут быть включены, если они находятся за пределами текущей записи. Однако если добавить запись в собственный объект **Recordset2,** она будет видна в **Recordset2** и будет включена в таблицу, в которой она станет видимой для любых новых объектов **Recordset2.**

Положение новой записи зависит от типа **Recordset2:**

- В объекте **Recordset2** типа "dynaset" записи вставляются в конце объекта Recordset независимо от правил сортировки или упорядочения, которые влияли на момент открытия объекта **Recordset.** 

- В объекте **Recordset2** таблицы, свойство **[Index](recordset2-index-property-dao.md)** которого установлено, записи возвращаются в надлежащем месте в порядке сортировки. Если свойство **Index** не задано, новые записи возвращаются в конце объекта **Recordset**.

Запись, которая была текущей до использования метода **AddNew**, остается текущей. Если вам нужно сделать новую запись текущей, вы можете указать в свойстве **[Bookmark](recordset2-bookmark-property-dao.md)** закладку, определяемую значением свойства **[LastModified](recordset2-lastmodified-property-dao.md)**.

> [!NOTE]
> Чтобы запись можно было добавить, изменить или удалить, в базовом источнике данных должен быть указан ее уникальный индекс. Если это не так, при вызове метода **AddNew**, **Delete** или **Edit** возникнет ошибка "Отказано в разрешении" в рабочей области Microsoft Access.

## <a name="example"></a>Пример

В этом примере используется метод **AddNew**, чтобы создать запись с указанным именем. Функция AddName необходима для запуска этой процедуры.

```vb
    Sub AddNewX() 
     
     Dim dbsNorthwind As Database 
     Dim rstEmployees As Recordset2 
     Dim strFirstName As String 
     Dim strLastName As String 
     
     Set dbsNorthwind = OpenDatabase("Northwind.mdb") 
     Set rstEmployees = _ 
     dbsNorthwind.OpenRecordset("Employees", dbOpenDynaset) 
     
     ' Get data from the user. 
     strFirstName = Trim(InputBox( _ 
     "Enter first name:")) 
     strLastName = Trim(InputBox( _ 
     "Enter last name:")) 
     
     ' Proceed only if the user actually entered something 
     ' for both the first and last names. 
     If strFirstName <> "" and strLastName <> "" Then 
     
     ' Call the function that adds the record. 
     AddName rstEmployees, strFirstName, strLastName 
     
     ' Show the newly added data. 
     With rstEmployees 
     Debug.Print "New record: " & !FirstName & _ 
     " " & !LastName 
     ' Delete new record because this is a demonstration. 
     .Delete 
     End With 
     
     Else 
     Debug.Print _ 
     "You must input a string for first and last name!" 
     End If 
     
     rstEmployees.Close 
     dbsNorthwind.Close 
     
    End Sub 
     
    Function AddName(rstTemp As Recordset2, _ 
     strFirst As String, strLast As String) 
     
     ' Adds a new record to a recordset using the data passed 
     ' by the calling procedure. The new record is then made 
     ' the current record. 
     With rstTemp 
     .AddNew 
     !FirstName = strFirst 
     !LastName = strLast 
     .Update 
     .Bookmark = .LastModified 
     End With 
     
    End Function
```
