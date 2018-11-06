---
title: Свойство Recordset2.index (DAO)
TOCTitle: Index Property
ms:assetid: 614bdf53-aca3-25ef-a23c-50095b345d20
ms:mtpsurl: https://msdn.microsoft.com/library/Ff194872(v=office.15)
ms:contentKeyID: 48545209
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 034fd349f140e931d1a5f654dfb275854aa2b78d
ms.sourcegitcommit: 1dd744993ecb4bed241ace874ad26edaef1778b8
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 11/06/2018
ms.locfileid: "25998982"
---
# <a name="recordset2index-property-dao"></a>Свойство Recordset2.index (DAO)

**Применимо к**: Access 2013, Office 2013

Задает или возвращает значение, указывающее имя текущего объекта **[индекса](index-object-dao.md)** в таблице тип объекта **[набора записей](recordset-object-dao.md)** (только для рабочих областей Microsoft Access).

## <a name="syntax"></a>Синтаксис

*выражение* . Индекс

*выражение* Переменная, которая представляет собой объект- **Recordset2** .

## <a name="remarks"></a>Примечания

Записи в базовые таблицы не сохраняются в любом порядке. Свойство **Index** изменяет порядок записей, возвращенных из базы данных; он не влияет на порядок, в котором хранятся записи.

Указанный объект **индекса** уже должны быть определены. Если значение свойства **Index** объекта **индекса** , не существует или свойства **Index** не задано, при использовании метода **[Seek](recordset2-seek-method-dao.md)** , то перехватываемые возникает ошибка.

Проверьте коллекцию **индексов** **TableDef** объекта, чтобы определить, какие объекты **индекса** доступны для объектов тип таблицы **записей** , создаваемых с помощью этого объекта **TableDef** .

Можно создать новый индекс для таблицы путем создания объекта **индекса** , установка ее свойств, добавления в коллекцию **индексов** базового объекта **TableDef** и повторно открыть объекта **набора записей** .

Возвращенный объект **набора записей** в таблице типа записи могут быть упорядочены только с помощью индексов, определенных для базового объекта **TableDef** . Чтобы отсортировать записи в некоторые другие порядке, можно открыть динамический набор –, моментальный снимок – или объекта **набора записей** прямого — только — тип с помощью инструкции SQL с предложение ORDER BY.

> [!NOTE]
> - У вас нет для создания индексов для таблиц. С большой, неиндексированные таблиц доступ к определенной записи или создание объекта **набора записей** может занять много времени. С другой стороны, создание слишком много индексов замедляет работу обновления, добавлять и удалять операции, так как все индексы обновляются автоматически.
> - Чтение из таблицы без индексов записи возвращаются в определенной последовательности.
> - Свойство **[атрибуты](field-attributes-property-dao.md)** каждого объекта **[поля](field-object-dao.md)** в объекте **индекса** определяет порядок записей и следовательно определяет методы доступа для этого индекса.
> - Уникальный индекс помогает оптимизировать поиск записей.
> - Индексы не влияют на физический порядок базовый tableindexes определяют, как только записи обращением объекта **набора записей** в таблице тип при выборе определенного индекса или при открытии **набора записей** .

## <a name="example"></a>Пример

В этом примере используется свойство **индекса** Установка другой записи заказов для табличного типа **набора записей**.

```vb
    Sub IndexPropertyX() 
     
       Dim dbsNorthwind As Database 
       Dim tdfEmployees As TableDef 
       Dim rstEmployees As Recordset2 
       Dim idxLoop As Index 
     
       Set dbsNorthwind = OpenDatabase("Northwind.mdb") 
       Set rstEmployees = _ 
          dbsNorthwind.OpenRecordset("Employees") 
       Set tdfEmployees = dbsNorthwind.TableDefs!Employees 
     
       With rstEmployees 
     
          ' Enumerate Indexes collection of Employees table. 
          For Each idxLoop In tdfEmployees.Indexes 
             .Index = idxLoop.Name 
             Debug.Print "Index = " & .Index 
             Debug.Print "  EmployeeID - PostalCode - Name" 
             .MoveFirst 
     
             ' Enumerate Recordset to show the order of records. 
             Do While Not .EOF 
                Debug.Print "    " & !EmployeeID & " - " & _ 
                   !PostalCode & " - " & !FirstName & " " & _ 
                   !LastName 
                .MoveNext 
             Loop 
     
          Next idxLoop 
     
          .Close 
       End With 
     
       dbsNorthwind.Close 
     
    End Sub 
```

<br/>

В этом примере демонстрируется использование метода **Seek** , позволяя пользователю выполнять поиск по идентификатору продукта.

```vb
    Sub SeekX() 
     
       Dim dbsNorthwind As Database 
       Dim rstProducts As Recordset2 
       Dim intFirst As Integer 
       Dim intLast As Integer 
       Dim strMessage As String 
       Dim strSeek As String 
       Dim varBookmark As Variant 
     
       Set dbsNorthwind = OpenDatabase("Northwind.mdb") 
       ' You must open a table-type Recordset to use an index,  
       ' and hence the Seek method. 
       Set rstProducts = _ 
          dbsNorthwind.OpenRecordset("Products", dbOpenTable) 
     
       With rstProducts 
          ' Set the index. 
          .Index = "PrimaryKey" 
     
          ' Get the lowest and highest product IDs. 
          .MoveLast 
          intLast = !ProductID 
          .MoveFirst 
          intFirst = !ProductID 
     
          Do While True 
             ' Display current record information and ask user  
             ' for ID number. 
             strMessage = "Product ID: " & !ProductID & vbCr & _ 
                "Name: " & !ProductName & vbCr & vbCr & _ 
                "Enter a product ID between " & intFirst & _ 
                " and " & intLast & "." 
             strSeek = InputBox(strMessage) 
     
             If strSeek = "" Then Exit Do 
     
             ' Store current bookmark in case the Seek fails. 
             varBookmark = .Bookmark 
     
             .Seek "=", Val(strSeek) 
     
             ' Return to the current record if the Seek fails. 
             If .NoMatch Then 
                MsgBox "ID not found!" 
                .Bookmark = varBookmark 
             End If 
          Loop 
     
          .Close 
       End With 
     
       dbsNorthwind.Close 
     
    End Sub
```
