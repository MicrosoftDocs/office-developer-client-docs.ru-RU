---
title: Метод Recordset.AddNew (DAO)
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
localization_priority: Priority
ms.openlocfilehash: 79c8691fcea7cf04bac7d6cd05711730b510e215
ms.sourcegitcommit: d6695c94415fa47952ee7961a69660abc0904434
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/17/2019
ms.locfileid: "28703946"
---
# <a name="recordsetaddnew-method-dao"></a>Метод Recordset.AddNew (DAO)

**Область применения**: Access 2013, Office 2013

Создает новую запись для обновляемого объекта **[Recordset](recordset-object-dao.md)**.

## <a name="syntax"></a>Синтаксис

*expression* .AddNew

*expression* — переменная, которая представляет объект **Recordset**.

## <a name="remarks"></a>Примечания

Метод **AddNew** используется для создания и добавления новой записи в объекте **Recordset** с именем набора записей. Этот метод задает значения по умолчанию для полей, а если значения по умолчанию не указаны, он задает для полей значение Null (значения по умолчанию, указанные для **Recordset** табличного типа).

Изменив новую запись, используйте метод **[Update](recordset-update-method-dao.md)**, чтобы сохранить изменения и добавить запись в объект **Recordset**. В базу данных не будут внесены никакие изменения, пока вы не вызовете метод **Update**.

> [!NOTE]
> Если вызвать метод **AddNew**, а затем выполнить какую-либо операцию, переходящую к другой записи, но без использования метода **Update**, то изменения будут потеряны без предупреждения. Кроме того, если закрыть объект **Recordset** или завершить процедуру, которая объявляет объект **Recordset** или его объект **[Database](database-object-dao.md)**, то новая запись удаляется без предупреждения.

> [!NOTE]
> Если вы используете метод **AddNew** в рабочей области Microsoft Access, а ядру СУБД нужно создать новую страницу для хранения текущей записи, то используется пессимистическая блокировка страницы. Если новую запись можно разместить на имеющейся странице, то используется оптимистическая блокировка.

Если вы не перешли к последней записи в объекте **Recordset**, то записи, добавленные к базовым таблицам другими процессами, могут быть включены, если они находятся за пределами текущей записи. Однако если добавить запись к собственному объекту **Recordset**, то запись будет видна в объекте **Recordset** и включена в базовую таблицу, где она становится видна всем новым объектам **Recordset**.

Расположение новой записи зависит от типа объекта **Recordset**:

- Если объект **Recordset** является динамическим подмножеством данных, то записи вставляются в конце объекта **Recordset** независимо от правил сортировки и упорядочения, которые действовали во время открытия объекта **Recordset**.

- В табличном объекте **Recordset**, для которого задано свойство **[Index](recordset-index-property-dao.md)**, записи возвращаются в надлежащем месте в порядке сортировки. Если свойство **Index** не задано, новые записи возвращаются в конце объекта **Recordset**.

Запись, которая была текущей до использования метода **AddNew**, остается текущей. Если вам нужно сделать новую запись текущей, вы можете указать в свойстве **[Bookmark](recordset-bookmark-property-dao.md)** закладку, определяемую значением свойства **[LastModified](recordset-lastmodified-property-dao.md)**.

> [!NOTE]
> Чтобы запись можно было добавить, изменить или удалить, в базовом источнике данных должен быть указан ее уникальный индекс. Если это не так, при вызове метода **AddNew**, **Delete** или **Edit** возникнет ошибка "Отказано в разрешении" в рабочей области Microsoft Access.

## <a name="example"></a>Пример

В этом примере используется метод **AddNew**, чтобы создать запись с указанным именем. Функция AddName необходима для запуска этой процедуры.

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
