---
title: Объект index — объекты доступа к данным (DAO)
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
# <a name="index-object-dao"></a>Объект index (DAO)

**Область применения**: Access 2013, Office 2013

Объект **index** указывает порядок записей, доступ к которым осуществляется из таблиц базы данных, а также сведения о том, принимаются ли повторяющиеся записи, что обеспечивает эффективный доступ к данным. Для внешних баз данных объекты **index** описывают индексы, установленные для внешних таблиц (только для рабочих областей Microsoft Access).

## <a name="remarks"></a>Замечания

Ядро СУБД Microsoft Access использует индексы при присоединении таблиц и создании объектов **[Recordset](recordset-object-dao.md)** . Индексы определяют порядок, в котором объекты **Recordset** табличного типа возвращают записи, но не определяют порядок, в котором ядро СУБД Microsoft Access хранит записи в базовой таблице, или порядок, в котором любой другой тип **набора записей** объект возвращает записи.

С помощью объекта **index** можно выполнять следующие действия:

- Используйте свойство **Required** , чтобы определить, требуются ли для объектов **[field](field-object-dao.md)** в индексе значения, которые не равны NULL, а затем используйте свойство **игноренуллс** , чтобы определить, имеют ли значения NULL элементы индекса.

- Используйте свойства **PRIMARY** и **UNIQUE** для определения порядка и уникальности объекта **index** .

Ядро СУБД Microsoft Access автоматически обслуживает все индексы базовых таблиц. Он обновляет индексы при каждом добавлении, изменении или удалении записей из базовой таблицы. Когда вы создадите базу данных, используйте метод **[CompactDatabase](dbengine-compactdatabase-method-dao.md)** периодически для получения статистики индекса в актуальном состоянии.

При доступе к объекту **Recordset** табличного типа необходимо указать порядок записей с помощью свойства **index** объекта. ПриСвойте этому свойству значение свойства **Name** существующего **индекса** в коллекции **indexes** . Эта коллекция находится в объекте **[tabledef](tabledef-object-dao.md)** , базовом объекте **Recordset** , который вы заполняете.

> [!NOTE]
> Вам не нужно создавать индексы для таблицы, но для больших неиндексированных таблиц доступ к определенной записи или обработка соединений может занять длительное время. С другой стороны, наличие слишком большого количества индексов может замедлить обновление базы данных по мере уточнения каждого индекса таблицы.

Свойство **[Attributes](field-attributes-property-dao.md)** каждого объекта **field** в индексе определяет порядок возврата записей и, соответственно, определяет методы доступа, которые необходимо использовать для этого индекса.

Каждый объект **field** в коллекции **Fields** объекта **index** является компонентом индекса. Чтобы определить новый объект **index** , задайте его свойства перед добавлением в коллекцию, сделав объект **индекса** доступным для последующего использования.

> [!NOTE]
> Значение свойства **Name** существующего **индекса** можно изменить только в том случае, если значение свойства **[обновляемого](connection-updatable-property-dao.md)** объекта **tabledef** равно **true**.

При задании первичного ключа для таблицы ядро СУБД Microsoft Access автоматически определяет его как первичный индекс. Первичный индекс состоит из одного или нескольких полей, которые уникально идентифицируют все записи в таблице в предварительно заданном порядке. Так как поле основного индекса должно быть уникальным, ядро СУБД Microsoft Access автоматически устанавливает **значение true**для свойства **UNIQUE** объекта основного **индекса** . Если первичный индекс состоит из нескольких полей, каждое поле может содержать повторяющиеся значения, но комбинация значений из всех индексированных полей должна быть уникальной. Первичный индекс состоит из ключа для таблицы и всегда состоит из тех же полей, что и первичный ключ.

> [!IMPORTANT]
> Убедитесь, что данные соответствуют атрибутам нового индекса. Если для индекса требуются уникальные значения, убедитесь, что в существующих записях данных нет дубликатов. Если дубликаты существуют, ядро СУБД Microsoft Access не может создать индекс; При попытке использовать метод Append для нового индекса возникает перехватываемая ошибка.

При создании связи, которая применяет целостность ссылок, ядро СУБД Microsoft Access автоматически создает индекс с **внешним** свойством, установленным в качестве внешнего ключа в ссылающейся таблице. После установления связи таблицы ядро СУБД Microsoft Access предотвращает добавление или изменение базы данных, которая нарушает эту связь. Если задать для свойства **Attributes** объекта **[relation](relation-object-dao.md)** разрешение каскадных обновлений и каскадных удаленИй, ядро СУБД Microsoft Access обновляет или удаляет записи в связанных таблицах автоматически.

1.  Используйте метод **креатеиндекс** для объекта **tabledef** .

2.  Используйте метод **CreateField** для объекта **index** , чтобы создать объект **field** для каждого поля (столбца), включаемого в объект **index** .

3.  Задайте свойства **индекса** по мере необходимости.

4.  Добавьте объект **field** в коллекцию **Fields** .

5.  Добавьте объект **index** в коллекцию **indexes** .

    > [!NOTE]
    > Свойство **Clustered** игнорируется для баз данных, использующих ядро СУБД Microsoft Access, которое не поддерживает кластеризованные индексы.

## <a name="example"></a>Пример

В этом примере создается новый объект **index** , который добавляется в коллекцию **indexes** для Employees **tabledef**, а затем перечисляет коллекцию **indexes** объекта **tabledef**. Наконец, он перечисляет **набор записей**, сначала используя первичный **индекс**, а затем с помощью нового **индекса**. Для выполнения этой процедуры требуется процедура Индексаутпут.

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

В этом примере используется метод **креатеиндекс** для создания двух новых объектов **индекса** , а затем они добавляются в коллекцию **indexes** объекта Employees **tabledef** . Затем выполняется перечисление **** коллекции индексов объекта **tabledef** , коллекции **Fields** новых объектов **index** и коллекции свойств новых объектов **index** . Для выполнения этой процедуры требуется функция Креатеиндексаутпут.

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
