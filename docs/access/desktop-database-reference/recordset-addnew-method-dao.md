---
title: Recordset.AddNew Method (DAO)
TOCTitle: AddNew Method
ms:assetid: 18cb35f6-8652-fb20-2460-3d13fae39d23
ms:mtpsurl: https://msdn.microsoft.com/library/Ff845624(v=office.15)
ms:contentKeyID: 48543483
ms.date: 09/18/2015
mtps_version: v=office.15
f1_keywords:
- dao360.chm1052883
f1_categories:
- Office.Version=v15
ms.openlocfilehash: 8aee4e63959beca98e96d04d14f817b2b6a30e7c
ms.sourcegitcommit: 19aca09c5812cfb98b68b5d4604dcaa814479df7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/09/2018
ms.locfileid: "25481870"
---
# <a name="recordsetaddnew-method-dao"></a>Recordset.AddNew Method (DAO)


**Применимо к**: Access 2013 | Office 2013

Создает новую запись для обновляемых объекта **[набора записей](recordset-object-dao.md)** .

## <a name="syntax"></a>Синтаксис

*выражение* . AddNew

*выражение* Переменная, которая представляет собой объект **набора записей** .

## <a name="remarks"></a>Замечания

Используйте метод **AddNew** для создания и добавления новой записи в объекте **набора записей** с именем, набора записей. Этого метода можно задать полей значения по умолчанию, и если нет значения по умолчанию не заданы, задает поля значение Null (значения по умолчанию, заданные для табличного типа **записей**).

После изменения новую запись, используйте метод **[Update](recordset-update-method-dao.md)** чтобы сохранить изменения и добавления записи **набора записей**. Без изменений в базе данных только при вызове метода **Update** .


> [!NOTE]
> <P>Если выдача <STRONG>AddNew</STRONG> и затем выполнять любые операции, перемещает к другой записи, но без использования <STRONG>обновления</STRONG>, изменения не сохраняются без предупреждения. Кроме того при закрытии <STRONG>набора записей</STRONG> или закончить процедуру, которая объявляет <STRONG>записей</STRONG> или объект <STRONG><A href="database-object-dao.md">базы данных</A></STRONG> новую запись удаляется без предупреждения.</P>




> [!NOTE]
> <P>При использовании <STRONG>AddNew</STRONG> в рабочей области Microsoft Access и имеет ядро базы данных для создания новой страницы для хранения текущей записи, блокировка страницы жесткой. Если новую запись помещается в существующей страницы, страницы блокировки оптимистичный.</P>



Если еще не к последнему перемещен записи из набора **записей**, записи, добавленные базовые таблицы для других процессов могут быть включены, если они размещены за пределы текущей записи. При добавлении записи для собственных **записей**тем не менее, запись будет отображаться в **набор записей** и включенных в базовой таблице, где он становится видимым для всех новых объектов **набора записей** .

Положение новую запись зависит от типа **набора записей**.

  - В объект **набора записей** добавляющий записи вставляются в конце **набора записей**, независимо от того, сортировки или упорядочивания правил, которые использовались при открытии **набора записей** .

  - В объекте **набора записей** тип таблицы, чьи свойства **[индекса](recordset-index-property-dao.md)** возвращаются записи в их местом в порядок сортировки. Если вы еще не настроили свойство **Index** , новые записи возвращаются в конце **набора записей**.

Записи, которая была текущей, прежде чем использовать **AddNew** остается текущей. Если вы хотите сделать новую запись текущей, можно задать свойства **[Bookmark](recordset-bookmark-property-dao.md)** закладку, определяемую средством настройки свойства **[LastModified](recordset-lastmodified-property-dao.md)** .


> [!NOTE]
> <P>Чтобы добавить, изменить или удалить записи, должен существовать уникальный индекс на запись в источнике данных. В противном случае ошибку «Отказано в доступе» произойдет на вызов метода <STRONG>AddNew</STRONG>, <STRONG>Удаление</STRONG>или <STRONG>Изменение</STRONG> в рабочей области Microsoft Access.</P>



## <a name="example"></a>Пример

В этом примере используется метод **AddNew** , чтобы создать новую запись с указанным именем. Функция AddName является обязательным для выполнения этой процедуры.

```vb
    Sub AddNewX() 
     
     Dim dbsNorthwind As Database 
     Dim rstEmployees As Recordset 
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
     
    Function AddName(rstTemp As Recordset, _ 
     strFirst As String, strLast As String) 
     
     ' Adds a new record to a Recordset using the data passed 
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
