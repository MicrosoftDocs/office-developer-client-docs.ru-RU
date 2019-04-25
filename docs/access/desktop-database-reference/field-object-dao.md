---
title: Объект Field — объекты DAO
TOCTitle: Field Object
ms:assetid: 47282ce2-9b49-ccf9-ad37-c4bb25cfd037
ms:mtpsurl: https://msdn.microsoft.com/library/Ff193203(v=office.15)
ms:contentKeyID: 48544587
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Priority
ms.openlocfilehash: c58896fb0d0a5c5a28844fdd3a6df922dd587f32
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32293044"
---
# <a name="field-object-dao"></a>Объект Field (DAO)

**Область применения**: Access 2013, Office 2013

Объект **Field** представляет столбец данных с общим типом данных и общим набором свойств.

## <a name="remarks"></a>Примечания

Коллекции **Fields** объектов **Index**, **QueryDef**, **Relation** и **TableDef** содержат спецификации для полей, представляемых этими объектами. Коллекция **Fields** объекта **Recordset** представляет объекты **Field** в строке данных или в записи. Объекты **Field** в объекте **Recordset** используются для чтения и задания значений для полей в текущей записи объекта **Recordset**.

В рабочей области Microsoft Access управление полем выполняется с помощью объекта **Field** и его методов и свойств. Например, вы можете:

  - Использовать свойство **OrdinalPosition**, чтобы задать или вернуть порядок представления объекта **Field** в коллекции **Fields**.

  - Использовать свойство **Value** поля в объекте **Recordset**, чтобы задать или вернуть сохраняемые данные.

  - Использовать методы **AppendChunk** и **GetChunk**, а также свойство **FieldSize**, чтобы получить или задать значение в объекте OLE или поле Memo объекта **Recordset**.

  - Использовать свойства **Type**, **Size** и **Attributes**, чтобы определить тип данных, которые могут храниться в поле.

  - Использовать свойства **SourceField** и **SourceTable**, чтобы определить исходный источник данных.

  - Использовать свойство **ForeignName**, чтобы задать или получить сведения о внешнем поле в объекте **Relation**.

  - Использовать свойства **AllowZeroLength**, **DefaultValue**, **Required**, **ValidateOnSet**, **ValidationRule** или **ValidationText**, чтобы задать или вернуть условия проверки.

  - Использовать свойство **DefaultValue** поля в объекте **TableDef**, чтобы задать значение по умолчанию для этого поля при добавлении новых записей.

Чтобы создать новый объект **Field** в объектах **Index**, **TableDef** или **Relation**, используйте метод **CreateField**.

При доступе к объекту **Field**, входящему в объект **Recordset**, данные из текущей записи отображаются в свойстве **Value** объекта **Field**. Чтобы управлять данными в объекте **Recordset**, обычно не используется прямая ссылка на коллекцию **Fields**; вместо этого используется косвенная ссылка на свойство **Value** объекта **Field** в коллекции **Fields** объекта **Recordset**.

Чтобы сослаться на объект **Field** в коллекции по его порядковому номеру или по его свойству**Name**, используйте любую из указанных ниже синтаксических форм.

- **Fields**(0)

- **Fields**("name")

- **Fields**\!\[name\]

С помощью этих синтаксических форм можно также ссылаться на свойство **Value** созданного объекта **Field**, добавляемого в коллекцию **Fields**. Контекст ссылки на поле определяет, ссылаетесь ли вы на объект **Field** или свойство **Value** объекта **Field**.

## <a name="example"></a>Пример

В этом примере показано, какие свойства допустимы для объекта **Field** в зависимости от расположения объекта **Field** (например, в коллекции **Fields** объекта **TableDef**, коллекции **Fields** объекта **QueryDef** и т. д.). Процедура FieldOutput является обязательной для запуска этой процедуры.

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

В этом примере используется метод **CreateField** для создания трех объектов **Field** для нового объекта **TableDef**. После этого отображаются свойства этих объектов **Field**, автоматически устанавливаемые методом **CreateField**. (Свойства, у которых отсутствуют значения во время создания объекта **Field**, не отображаются.)

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
