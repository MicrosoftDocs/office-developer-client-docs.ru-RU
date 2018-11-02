---
title: Объекты объекта поля - доступ к данным (DAO)
TOCTitle: Field Object
ms:assetid: 47282ce2-9b49-ccf9-ad37-c4bb25cfd037
ms:mtpsurl: https://msdn.microsoft.com/library/Ff193203(v=office.15)
ms:contentKeyID: 48544587
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 644089e9ff4dddf2aed9f767a667cc3d80b6e039
ms.sourcegitcommit: d7248f803002b31cf7fc561b03530199a9b0a8fd
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 11/02/2018
ms.locfileid: "25924570"
---
# <a name="field-object-dao"></a>Объект поля (DAO)

**Применимо к**: Access 2013, Office 2013

Объект **поля** представляет столбец данных с типом данных и общий набор свойств.

## <a name="remarks"></a>Примечания

Коллекции **полей** **индекса**, **QueryDef**, **связь**и **TableDef** объектов содержат спецификаций для полей представляют эти объекты. Коллекция **полей** объекта **набора записей** представляет объекты **поля** в строке данных или в записи. Используйте объекты **поля** в объекте **набора записей** для чтения и задайте значения для полей в текущей записи объекта **набора записей** .

В workspacee Microsoft Access управлять с помощью объекта **поля** , методы и свойства поля. Например можно выполнить следующие действия.

  - Свойство **OrdinalPosition** задает или возвращает порядок представления объекта **поля** в коллекции **полей** .

  - Свойство **значение** поля в объекте **набора записей** или возвращает сохраненных данных.

  - Используйте **AppendChunk** и **GetChunk** методы и **свойства FieldSize** получить или задать значение в поле объекта OLE или Memo объекта **набора записей** .

  - Использование свойств **типа**, **размер**и **атрибуты** для определения типа данных, которые могут храниться в поле.

  - Использование свойства **SourceField** и **Таблица** для определения исходного источника данных.

  - Свойство **ForeignName** задает или возвращает сведения о поле внешнего в объект **связи** .

  - Использование свойств **пустые строки**, **значение по умолчанию**, **необходимых**, **Проверка набора**, **значение**или **сообщение об ошибке** или возвращает условия проверки данных.

  - Свойство **DefaultValue** поля в объекте **TableDef** для установки значения по умолчанию для этого поля, при добавлении новых записей.

Чтобы создать новый объект **поля** в **индексе**, **TableDef**или объект **отношения** , используйте метод **CreateField** .

При получении доступа к объекту **поля** в составе объекта **набора записей** , данные из текущей записи отображается в свойство **Value** объекта **поля** . Для работы с данными в объекте **набора записей** , не ссылки обычно коллекции **полей** напрямую. Вместо этого косвенно ссылки на свойство **Value** объекта **поля** в коллекции **полей** объекта **набора записей** .

Для ссылки на объект **поля** в семействе сайтов, с его порядковый номер или **его свойства Name** , используйте любой из следующих форм синтаксиса:

- **Поля** (0)

- **Поля** («имя»)

- **Поля**\!\[имя\]

С помощью одной синтаксиса форм можно найти в свойство **Value** объекта **поля** , добавьте к коллекции **полей** . Контекст ссылку на поле определяет, будет ли вы ссылаетесь на объект **поля** или свойства **Value** объекта **поля** .

## <a name="example"></a>Пример

В этом примере показано, какие свойства являются допустимыми для объекта **поля** в зависимости от того, где находится **поле** (для примера, коллекции **полей** **TableDef**, коллекции **полей** **QueryDef**и т. д.). Процедура FieldOutput является обязательным для выполнения этой процедуры.

```vb
    Sub FieldX() 
     
     Dim dbsNorthwind As Database 
     Dim rstEmployees As Recordset 
     Dim fldTableDef As Field 
     Dim fldQueryDef As Field 
     Dim fldRecordset As Field 
     Dim fldRelation As Field 
     Dim fldIndex As Field 
     Dim prpLoop As Property 
     
     Set dbsNorthwind = OpenDatabase("Northwind.mdb") 
     Set rstEmployees = _ 
     dbsNorthwind.OpenRecordset("Employees") 
     
     ' Assign a Field object from different Fields 
     ' collections to object variables. 
     Set fldTableDef = _ 
     dbsNorthwind.TableDefs(0).Fields(0) 
     Set fldQueryDef =dbsNorthwind.QueryDefs(0).Fields(0) 
     Set fldRecordset = rstEmployees.Fields(0) 
     Set fldRelation =dbsNorthwind.Relations(0).Fields(0) 
     Set fldIndex = _ 
     dbsNorthwind.TableDefs(0).Indexes(0).Fields(0) 
     
     ' Print report. 
     FieldOutput "TableDef", fldTableDef 
     FieldOutput "QueryDef", fldQueryDef 
     FieldOutput "Recordset", fldRecordset 
     FieldOutput "Relation", fldRelation 
     FieldOutput "Index", fldIndex 
     
     rstEmployees.Close 
     dbsNorthwind.Close 
     
    End Sub 
     
    Sub FieldOutput(strTemp As String, fldTemp As Field) 
     ' Report function for FieldX. 
     
     Dim prpLoop As Property 
     
     Debug.Print "Valid Field properties in " & strTemp 
     
     ' Enumerate Properties collection of passed Field 
     ' object. 
     For Each prpLoop In fldTemp.Properties 
     ' Some properties are invalid in certain 
     ' contexts (the Value property in the Fields 
     ' collection of a TableDef for example). Any 
     ' attempt to use an invalid property will 
     ' trigger an error. 
     On Error Resume Next 
     Debug.Print " " & prpLoop.Name & " = " & _ 
     prpLoop.Value 
     On Error GoTo 0 
     Next prpLoop 
     
    End Sub 
```

<br/>

В этом примере используется метод **CreateField** для создания трех **полей** для нового **TableDef**. Затем отображает свойства объектов **поля** , которые автоматически устанавливаются с помощью метода **CreateField** . (Во время создания **поля** пусты, значения свойств, не отображаются.)

```vb
    Sub CreateFieldX() 
     
     Dim dbsNorthwind As Database 
     Dim tdfNew As TableDef 
     Dim fldLoop As Field 
     Dim prpLoop As Property 
     
     Set dbsNorthwind = OpenDatabase("Northwind.mdb") 
     
     Set tdfNew = dbsNorthwind.CreateTableDef("NewTableDef") 
     
     ' Create and append new Field objects for the new 
     ' TableDef object. 
     With tdfNew 
     ' The CreateField method will set a default Size 
     ' for a new Field object if one is not specified. 
     .Fields.Append .CreateField("TextField", dbText) 
     .Fields.Append .CreateField("IntegerField", dbInteger) 
     .Fields.Append .CreateField("DateField", dbDate) 
     End With 
     
     dbsNorthwind.TableDefs.Append tdfNew 
     
     Debug.Print "Properties of new Fields in " & tdfNew.Name 
     
     ' Enumerate Fields collection to show the properties of 
     ' the new Field objects. 
     For Each fldLoop In tdfNew.Fields 
     Debug.Print " " & fldLoop.Name 
     
     For Each prpLoop In fldLoop.Properties 
     ' Properties that are invalid in the context of 
     ' TableDefs will trigger an error if an attempt 
     ' is made to read their values. 
     On Error Resume Next 
     Debug.Print " " & prpLoop.Name & " - " & _ 
     IIf(prpLoop = "", "[empty]", prpLoop) 
     On Error GoTo 0 
     Next prpLoop 
     
     Next fldLoop 
     
     ' Delete new TableDef because this is a demonstration. 
     dbsNorthwind.TableDefs.Delete tdfNew.Name 
     dbsNorthwind.Close 
     
    End Sub
```
