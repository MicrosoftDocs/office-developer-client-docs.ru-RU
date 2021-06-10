---
title: Объект Index — объекты доступа к данным (DAO)
TOCTitle: Index object
ms:assetid: 92c32cad-ec8a-1243-1d18-83f50b269ecb
ms:mtpsurl: https://msdn.microsoft.com/library/Ff197655(v=office.15)
ms:contentKeyID: 48546380
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: ca0a975017b5c5396d23817716689b37433d8f97
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32291770"
---
# <a name="index-object-dao"></a>Объект Index (DAO)

**Область применения**: Access 2013, Office 2013

**Объекты** index указывают порядок записей, доступных из таблиц баз данных, и принимаются ли дублирующиеся записи, обеспечивая эффективный доступ к данным. Для внешних баз данных **объекты Index** описывают индексы, установленные для внешних таблиц (только для рабочей области Microsoft Access).

## <a name="remarks"></a>Примечания

Двигатель базы данных Microsoft Access использует индексы при присоединении к таблицам и создании объектов **[Recordset.](recordset-object-dao.md)** Индексы определяют порядок, в котором объекты **Recordset** таблицы возвращают записи, но не определяют порядок, в котором движок базы данных Microsoft Access хранит записи в базовой таблице или порядок, в котором любой другой тип объекта **Recordset** возвращает записи.

С **объектом Index** можно:

- Используйте свойство **Required,** чтобы определить, требуются ли объекты **[Field](field-object-dao.md)** в индексе значения, которые не являются Null, а затем используйте свойство **IgnoreNulls,** чтобы определить, имеют ли значения null записи индекса.

- Для определения  порядка и уникальности объекта Index используйте свойства **Primary** и **Unique.**

Двигатель базы данных Microsoft Access автоматически поддерживает все индексы базовой таблицы. Он обновляет индексы при добавлении, изменении или удалении записей из базовой таблицы. После создания базы данных периодически используйте метод **[CompactDatabase,](dbengine-compactdatabase-method-dao.md)** чтобы привести статистику индексов в нужное время.

При доступе к объекту **Recordset** типа таблицы указывается порядок записей с помощью свойства **Index** объекта. Установите это свойство в **параметре Свойства Name** существующего **объекта Index** в коллекции **Indexes.** Эта коллекция содержится **[объектом TableDef,](tabledef-object-dao.md)** который является объектом **Recordset,** который заполняется.

> [!NOTE]
> Не нужно создавать индексы для таблицы, но для больших неиндексуальных таблиц доступ к определенной записи или присоединению к обработке может занять много времени. И наоборот, слишком большое количество индексов может замедлить обновление базы данных по мере изменения каждого из индексов таблицы.

Свойство **[Атрибуты](field-attributes-property-dao.md)** каждого объекта **Field** в индексе определяет порядок возвращаемой записи и, следовательно, определяет, какие методы доступа использовать для этого индекса.

Каждый объект **Field** в коллекции **Fields** объекта **Index** является компонентом индекса. Чтобы определить новый **объект Index,** установите его свойства перед его приложением в коллекцию, сделав объект **Index** доступным для последующего использования.

> [!NOTE]
> Параметр свойства **Name** существующего объекта **Index** можно изменить только в том случае, если параметр **[Updatable](connection-updatable-property-dao.md)** свойства содержащегося объекта **TableDef** **является True**.

При наборе основного ключа для таблицы двигатель базы данных Microsoft Access автоматически определяет его как основной индекс. Основной индекс состоит из одного или нескольких полей, которые однозначно идентифицируют все записи в таблице в заранее определенном порядке. Так как основное поле индекса должно быть уникальным,  двигатель базы данных Microsoft Access автоматически задает уникальное свойство основного объекта **Index** **true**. Если основной индекс состоит из нескольких полей, каждое поле может содержать дублирующие значения, но сочетание значений из всех проиндексированные поля должно быть уникальным. Основной индекс состоит из ключа для таблицы и всегда состоит из тех же полей, что и основной ключ.

> [!IMPORTANT]
> Убедитесь, что данные соответствуют атрибутам нового индекса. Если индекс требует уникальных значений, убедитесь, что в существующих записях данных нет дубликатов. Если существуют дубликаты, то механизм базы данных Microsoft Access не может создать индекс; результаты ошибок, которые можно найти при попытке использовать метод Append в новом индексе.

При создании связи, которая обеспечивает целостность ссылок, двигатель базы данных Microsoft Access автоматически создает индекс с свойством **Foreign,** задающийся в качестве иностранного ключа в таблице ссылок. После того как вы установили отношение таблицы, двигатель базы данных Microsoft Access предотвращает добавления или изменения в базу данных, нарушающие эти отношения. Если вы установите свойство **Атрибуты** объекта **[Relation](relation-object-dao.md)** для допуска каскадных обновлений и каскадных удалений, двигатель базы данных Microsoft Access автоматически обновляет или удаляет записи в связанных таблицах.

1.  Используйте метод **CreateIndex** на **объекте TableDef.**

2.  Используйте метод **CreateField** на **объекте Index,** чтобы создать объект **Field** для каждого поля (столбца), который будет включен в **объект Index.**

3.  Установите **свойства Index** по мере необходимости.

4.  Приложение объекта **Field** к коллекции **Fields.**

5.  Привяжи **объект Index** к коллекции **Indexes.**

    > [!NOTE]
    > Свойство **Clustered** игнорируется для баз данных, которые используют движок базы данных Microsoft Access, который не поддерживает кластерные индексы.

## <a name="example"></a>Пример

В этом примере создается новый объект **Index,** он примыкает к коллекции **Indexes** **tableDef** для сотрудников, а затем включает коллекцию **Индексов** **TableDef**. Наконец, он записи, сначала с помощью основного **индекса,** а затем с помощью нового **индекса**. Для запуска этой процедуры требуется процедура IndexOutput.

```vb
    Sub IndexObjectX() 
     
     Dim dbsNorthwind As Database 
     Dim tdfEmployees As TableDef 
     Dim idxNew As Index 
     Dim idxLoop As Index 
     Dim rstEmployees As Recordset 
     
     Set dbsNorthwind = OpenDatabase("Northwind.mdb") 
     Set tdfEmployees = dbsNorthwind!Employees 
     
     With tdfEmployees 
     ' Create new index, create and append Field 
     ' objects to its Fields collection. 
     Set idxNew = .CreateIndex("NewIndex") 
     
     With idxNew 
     .Fields.Append .CreateField("Country") 
     .Fields.Append .CreateField("LastName") 
     .Fields.Append .CreateField("FirstName") 
     End With 
     
     ' Add new Index object to the Indexes collection 
     ' of the Employees table collection. 
     .Indexes.Append idxNew 
     .Indexes.Refresh 
     
     Debug.Print .Indexes.Count & " Indexes in " & _ 
     .Name & " TableDef" 
     
     ' Enumerate Indexes collection of Employees 
     ' table. 
     For Each idxLoop In .Indexes 
     Debug.Print " " & idxLoop.Name 
     Next idxLoop 
     
     Set rstEmployees = _ 
     dbsNorthwind.OpenRecordset("Employees") 
     
     ' Print report using old and new indexes. 
     IndexOutput rstEmployees, "PrimaryKey" 
     IndexOutput rstEmployees, idxNew.Name 
     rstEmployees.Close 
     
     ' Delete new Index because this is a 
     ' demonstration. 
     .Indexes.Delete idxNew.Name 
     End With 
     
     dbsNorthwind.Close 
     
    End Sub 
     
    Sub IndexOutput(rstTemp As Recordset, _ 
     strIndex As String) 
     ' Report function for FieldX. 
     
     With rstTemp 
     ' Set the index. 
     .Index = strIndex 
     .MoveFirst 
     Debug.Print "Recordset = " & .Name & _ 
     ", Index = " & .Index 
     Debug.Print " EmployeeID - Country - Name" 
     
     ' Enumerate the recordset using the specified 
     ' index. 
     Do While Not .EOF 
     Debug.Print " " & !EmployeeID & " - " & _ 
     !Country & " - " & !LastName & ", " & !FirstName 
     .MoveNext 
     Loop 
     
     End With 
     
    End Sub 
```

<br/>

В этом примере метод **CreateIndex** создает два новых объекта **Index** и затем привносим их в коллекцию **Indexes** объекта **Employees TableDef.** Затем он включает коллекцию **Indexes** объекта **TableDef,**  коллекцию Поля новых объектов **Index** и коллекцию Свойств новых объектов **Index.** Для запуска этой процедуры требуется функция CreateIndexOutput.

```vb
    Sub CreateIndexX() 
     
     Dim dbsNorthwind As Database 
     Dim tdfEmployees As TableDef 
     Dim idxCountry As Index 
     Dim idxFirstName As Index 
     Dim idxLoop As Index 
     
     Set dbsNorthwind = OpenDatabase("Northwind.mdb") 
     Set tdfEmployees = dbsNorthwind!Employees 
     
     With tdfEmployees 
     ' Create first Index object, create and append Field 
     ' objects to the Index object, and then append the 
     ' Index object to the Indexes collection of the 
     ' TableDef. 
     Set idxCountry = .CreateIndex("CountryIndex") 
     With idxCountry 
     .Fields.Append .CreateField("Country") 
     .Fields.Append .CreateField("LastName") 
     .Fields.Append .CreateField("FirstName") 
     End With 
     .Indexes.Append idxCountry 
     
     ' Create second Index object, create and append Field 
     ' objects to the Index object, and then append the 
     ' Index object to the Indexes collection of the 
     ' TableDef. 
     Set idxFirstName = .CreateIndex 
     With idxFirstName 
     .Name = "FirstNameIndex" 
     .Fields.Append .CreateField("FirstName") 
     .Fields.Append .CreateField("LastName") 
     End With 
     .Indexes.Append idxFirstName 
     
     ' Refresh collection so that you can access new Index 
     ' objects. 
     .Indexes.Refresh 
     
     Debug.Print .Indexes.Count & " Indexes in " & _ 
     .Name & " TableDef" 
     
     ' Enumerate Indexes collection. 
     For Each idxLoop In .Indexes 
     Debug.Print " " & idxLoop.Name 
     Next idxLoop 
     
     ' Print report. 
     CreateIndexOutput idxCountry 
     CreateIndexOutput idxFirstName 
     
     ' Delete new Index objects because this is a 
     ' demonstration. 
     .Indexes.Delete idxCountry.Name 
     .Indexes.Delete idxFirstName.Name 
     End With 
     
     dbsNorthwind.Close 
     
    End Sub 
     
    Function CreateIndexOutput(idxTemp As Index) 
     
     Dim fldLoop As Field 
     Dim prpLoop As Property 
     
     With idxTemp 
     ' Enumerate Fields collection of Index object. 
     Debug.Print "Fields in " & .Name 
     For Each fldLoop In .Fields 
     Debug.Print " " & fldLoop.Name 
     Next fldLoop 
     
     ' Enumerate Properties collection of Index object. 
     Debug.Print "Properties of " & .Name 
     For Each prpLoop In .Properties 
     Debug.Print " " & prpLoop.Name & " - " & _ 
     IIf(prpLoop = "", "[empty]", prpLoop) 
     Next prpLoop 
     End With 
     
    End Function
```
