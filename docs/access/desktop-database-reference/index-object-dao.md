---
title: Индекс объекта - объекты доступа к данным (DAO)
TOCTitle: Index object
ms:assetid: 92c32cad-ec8a-1243-1d18-83f50b269ecb
ms:mtpsurl: https://msdn.microsoft.com/library/Ff197655(v=office.15)
ms:contentKeyID: 48546380
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: ca0a975017b5c5396d23817716689b37433d8f97
ms.sourcegitcommit: d6695c94415fa47952ee7961a69660abc0904434
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/17/2019
ms.locfileid: "28708916"
---
# <a name="index-object-dao"></a>Объект индекса (DAO)

**Применимо к**: Access 2013, Office 2013

Объекты **индекса** указать порядок записей, доступного из таблицы базы данных и принимаются ли повторяющихся записей, предоставляя эффективного доступа к данным. Для внешних баз данных объекты **индекса** описывают индексов, установленных для внешних таблиц (только для рабочих областей Microsoft Access).

## <a name="remarks"></a>Замечания

Ядро базы данных Microsoft Access использует индексы при его соединяет таблицы и создает объекты **[набора записей](recordset-object-dao.md)** . Индексов определения порядка, в котором объектов **наборов записей** в таблице тип возврата записей, но они не определяют порядок, в котором хранятся записи в таблице базового ядро базы данных Microsoft Access или порядок, в которых любой другой тип **набора записей** Возвращает объект записей.

С помощью объекта **индекса** можно выполнить следующие действия.

- Свойство **необходимо** использовать для определения потребность в **[поле](field-object-dao.md)** объекты в индексе значения, которые не являются пустыми и затем свойство **IgnoreNulls** позволяет определить, имеют ли значения null записи индекса.

- Использование свойств **основной** и **Unique** для определения порядка и уникальности объекта **индекса** .

Ядро базы данных Microsoft Access автоматически сохраняет все индексы базовая таблица. Индексы обновляется каждый раз, когда добавление, изменение или удаление записей из базовой таблицы. После создания базы данных, метод **[CompactDatabase](dbengine-compactdatabase-method-dao.md)** периодически для переноса актуальных статистику индекса.

При доступе к таблице тип объекта **набора записей** , указать порядок записей с помощью свойства **Index** объекта. Этому свойству присвоено значение **свойства Name существующего объекта **индексу** в коллекции **индексов** ** . Эта коллекция содержится объектом **[TableDef](tabledef-object-dao.md)** базового объекта **набора записей** , который заполнение.

> [!NOTE]
> У вас нет для создания индексов для таблицы, но для больших, неиндексированные таблиц, доступ к определенной записи или обработки соединения может занять много времени. С другой стороны слишком много индексов может снизить обновления базы данных как всех индексов таблицы изменен.

Свойство **[атрибуты](field-attributes-property-dao.md)** каждого объекта **поля** в индексе определяет порядок возвращаемых записей и поэтому определяет, какой доступ к методах, используемых для этого индекса.

Каждый объект **поля** в коллекции **полей** **индекс** объекта является компонентом индекса. Чтобы определить новый объект **индекса** , задайте его свойства перед добавлением в коллекцию предоставление объект **индекса** для последующего использования.

> [!NOTE]
> **Свойства Name существующего объекта **индекса** ** можно изменить только в том случае, если значение свойства **[с возможностью записи](connection-updatable-property-dao.md)** , содержащего объект **TableDef** имеет **значение True**.

При установке первичный ключ для таблицы ядро базы данных Microsoft Access автоматически определяет его как основной индекса. Первичный индекс состоит из одного или нескольких полей, которые однозначно идентифицируют все записи в таблице в предопределенном порядке. Так как поле первичного индекса должно быть уникальным, ядро базы данных Microsoft Access автоматически устанавливает свойство **Уникальный** основной **индекс** объекта значение **True**. Если основной индекс состоит из нескольких полей, в каждом поле может содержать повторяющиеся значения, но сочетание значений из всех индексированных полей должно быть уникальным. Первичный индекс состоит из ключа для таблицы и всегда включает в себя все поля первичный ключ.

> [!IMPORTANT]
> Убедитесь, что ваши данные стандарту атрибуты нового индекса. Если индекс требуются уникальные значения, убедитесь, что существует без повторов в существующей записи данных. Если существуют дубликаты, ядро базы данных Microsoft Access не удается создать индекс; Это перехватываемые приводит к ошибке при попытке использовать метод Append на новый индекс.

При создании отношения, которое обеспечивает целостность данных ядро базы данных Microsoft Access автоматически создает индекс с помощью свойства **внешнего** задаются в виде внешнего ключа в ссылающаяся таблица. После установления связи между таблицами, ядро базы данных Microsoft Access не позволяет дополнения или изменения базы данных, нарушают этой связи. Если для свойства **атрибуты** объекта **[связи](relation-object-dao.md)** , чтобы разрешить каскадных обновление и удаление ядро базы данных Microsoft Access обновляет или удаляет записи из связанных таблиц автоматически.

1.  Используйте метод **CreateIndex** для объекта **TableDef** .

2.  Используйте метод **CreateField** на объект **индекса** для создания объекта **поля** для каждого поля (столбца), включаемых в **индекс** объекта.

3.  При необходимости установите свойства **индекса** .

4.  Добавьте объект **поля** в коллекцию **полей** .

5.  Добавьте объект **индекса** в коллекцию **индексов** .

    > [!NOTE]
    > Свойство **Clustered** игнорируется для баз данных, использующих ядро базы данных Microsoft Access, которые не поддерживают кластеризованных индексов.

## <a name="example"></a>Пример

В этом примере создается новый объект **индекса** , добавляет в коллекцию **индексов** сотрудников **TableDef**и затем создается перечисление коллекции **индексов** **TableDef**. И, наконец перечисляются **записей**, сначала с помощью основной **индекса**, а затем используют нового **индекса**. Процедура IndexOutput является обязательным для выполнения этой процедуры.

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

В этом примере используется метод **CreateIndex** для создания двух новых объектов **индекса** и добавляет их в коллекцию **индексов** сотрудников **TableDef** объекта. Затем выполняется перечисление коллекции **индексов** объекта **TableDef** , коллекции **полей** новых объектов **индекса** и коллекции свойств новых объектов **индекса** . Функция CreateIndexOutput является обязательным для выполнения этой процедуры.

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
