---
title: Свойство Recordset2.Index (DAO)
TOCTitle: Index Property
ms:assetid: 614bdf53-aca3-25ef-a23c-50095b345d20
ms:mtpsurl: https://msdn.microsoft.com/library/Ff194872(v=office.15)
ms:contentKeyID: 48545209
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: 05a29ff9dbe720fe7c5539639b20e0abdc3c587b
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32307303"
---
# <a name="recordset2index-property-dao"></a>Свойство Recordset2.Index (DAO)

**Область применения**: Access 2013, Office 2013

Задает или возвращает значение, которое указывает имя текущего объекта **[Index](index-object-dao.md)** в объекта **[Recordset](recordset-object-dao.md)** табличного типа (только для рабочих областей Microsoft Access).

## <a name="syntax"></a>Синтаксис

*expression* .Index

*выражение* Переменная, представляюная объект **Recordset2.**

## <a name="remarks"></a>Комментарии

Записи в базовых таблицах не хранятся в определенном порядке. Настройка свойства **Index** изменяет порядок записей, возвращаемых из базы данных; оно не влияет на порядок, в котором хранятся записи.

Указанный объект **Index** уже должен быть определен. Если вы задаете свойство **Index** для объекта **Index**, который не существует, или если свойство **Index** не задано при использовании метода **[Seek](recordset2-seek-method-dao.md)**, возникает перехватываемая ошибка.

Ознакомьтесь с коллекцией **Indexes** объекта **TableDef**, чтобы определить, что объекты **Index** доступны для объектов **Recordset** табличного типа, созданных на основе объекта **TableDef**.

Вы можете создать новый индекс для таблицы, создав новый объект **Index**, задав его свойства, добавив его в коллекцию **Indexes** базового объекта **TableDef** и повторно открыв объект **Recordset**.

Записи, возвращаемые из объекта **Recordset** табличного типа, можно упорядочить только по индексам, заданным для базового объекта **TableDef**. Чтобы отсортировать записи в другом порядке, можно открыть объект **Recordset** типа dynaset, мгновенный снимок или однонаправленный с помощью оператора SQL с предложением ORDER BY.

> [!NOTE]
> - Вам не нужно создавать индексы для таблиц. Для больших, неиндексированных таблиц доступ к определенной записи или создание объекта **Recordset** может занять много времени. С другой стороны, создание слишком большого количества индексов замедляет обновление, добавление и удаление, так как все индексы автоматически обновляются.
> - Записи, считываемые из таблиц без индексов, возвращаются без определенной последовательности.
> - Свойство **[Attributes](field-attributes-property-dao.md)** каждого объекта **[Field](field-object-dao.md)** в объекте **Index** определяет порядок записей и соответственно определяет техники доступа для использования этого индекса.
> - Уникальный индекс помогает оптимизировать поиск записей.
> - Индексы не влияют на физический порядок базового tableindexes, а влияют только на то, как записи будут доступны объекту **Recordset** типа таблицы при выборе определенного индекса или при открывлении **Recordset.**

## <a name="example"></a>Пример

В этом примере используется свойство **Index** для установки другого порядка записей для объекта **Recordset** табличного типа.

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

В этом примере показан метод **Seek**, позволяющий пользователю выполнить поиск продукта на основании на номере идентификатора.

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
