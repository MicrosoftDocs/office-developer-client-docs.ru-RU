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
ms.sourcegitcommit: d6695c94415fa47952ee7961a69660abc0904434
ms.translationtype: Auto
ms.contentlocale: ru-RU
ms.lasthandoff: 01/17/2019
ms.locfileid: "28699347"
---
# <a name="recordset2addnew-method-dao"></a>Метод Recordset2.AddNew (DAO)

**Применимо к**: Access 2013, Office 2013
 
Создает новую запись для объекта обновляемых **Recordset2** .

## <a name="syntax"></a>Синтаксис

*выражение* . AddNew

*выражение* Переменная, которая представляет собой объект- **Recordset2** .

## <a name="remarks"></a>Замечания

Используйте метод **AddNew** создает и добавляет новую запись в объекте **Recordset2** с именем, набора записей. Этого метода можно задать полей значения по умолчанию, и если нет значения по умолчанию не заданы, задает поля значение Null (значения по умолчанию для типа таблицы **Recordset2**).

После изменения новую запись, используйте метод **[Update](recordset2-update-method-dao.md)** чтобы сохранить изменения и добавления записи **Recordset2**. Без изменений в базе данных только при вызове метода **Update** .

> [!NOTE]
> Если выдача **AddNew** и затем выполнять любые операции, перемещает к другой записи, но без использования **обновления**, изменения не сохраняются без предупреждения. Кроме того Если закрыть **Recordset2** или закончить процедуру, которая объявляет **Recordset2** или объект **[базы данных](database-object-dao.md)** , новую запись удаляется без предупреждения.

> [!NOTE]
> При использовании **AddNew** в рабочей области Microsoft Access и имеет ядро базы данных для создания новой страницы для хранения текущей записи, блокировка страницы жесткой. Если новую запись помещается в существующей страницы, страницы блокировки оптимистичный.

Если запись вашего **Recordset2**еще не перемещен к последнему, записи, добавленные базовые таблицы для других процессов могут быть включены, если они размещены за пределы текущей записи. При добавлении записи для собственного **Recordset2**тем не менее, запись будет отображаться в **Recordset2** и включенных в базовой таблице, где он становится видимым для всех новых объектов **Recordset2** .

Положение новую запись зависит от типа **Recordset2**.

- В объекте **Recordset2** добавляющий записи вставляется в конце **набора записей**, независимо от того, сортировки или упорядочивания правил, которые использовались при открытии **набора записей** .

- В объекте **Recordset2** тип таблицы, чьи свойства **[индекса](recordset2-index-property-dao.md)** возвращаются записи в их местом в порядок сортировки. Если вы еще не настроили свойство **Index** , новые записи возвращаются в конце **набора записей**.

Записи, которая была текущей, прежде чем использовать **AddNew** остается текущей. Если вы хотите сделать новую запись текущей, можно задать свойства **[Bookmark](recordset2-bookmark-property-dao.md)** закладку, определяемую средством настройки свойства **[LastModified](recordset2-lastmodified-property-dao.md)** .

> [!NOTE]
> Чтобы добавить, изменить или удалить записи, должен существовать уникальный индекс на запись в источнике данных. В противном случае ошибку «Отказано в доступе» произойдет на вызов метода **AddNew**, **Удаление**или **Изменение** в рабочей области Microsoft Access.

## <a name="example"></a>Пример

В этом примере используется метод **AddNew** , чтобы создать новую запись с указанным именем. Функция AddName является обязательным для выполнения этой процедуры.

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
