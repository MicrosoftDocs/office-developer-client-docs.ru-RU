---
title: Свойство Index.Unique (DAO)
TOCTitle: Unique Property
ms:assetid: a4486da5-8a1a-b4fc-0e07-e65cd2e726f6
ms:mtpsurl: https://msdn.microsoft.com/library/Ff821087(v=office.15)
ms:contentKeyID: 48546809
ms.date: 09/18/2015
mtps_version: v=office.15
f1_keywords:
- dao360.chm1052990
f1_categories:
- Office.Version=v15
localization_priority: Normal
ms.openlocfilehash: 5c94200245b4736ad244cb37beec617a98d6c367
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32291694"
---
# <a name="indexunique-property-dao"></a>Свойство Index.Unique (DAO)

**Область применения**: Access 2013, Office 2013

Задает или возвращает значение, которое указывает, представляет ли объект **[Index](index-object-dao.md)** уникальный индекс (ключ) для таблицы (только для рабочей области Microsoft Access).

## <a name="syntax"></a>Синтаксис

*выражение .* Уникальный

*выражение* Переменная, представляюная объект **Index.**

## <a name="remarks"></a>Заметки

Этот параметр свойства считывать и записывать, пока объект не будет appended в коллекцию, после чего он будет только для чтения.

Уникальный индекс состоит из одного или нескольких полей, логически упорядочив все записи в таблице в уникальном предопределеном порядке. Если индекс состоит из одного поля, значения в этом поле должны быть уникальными для всей таблицы. Если индекс состоит из нескольких полей, каждое поле может содержать повторяющиеся значения, но каждая комбинация значений из всех индексных полей должна быть уникальной.

Если для свойств **Unique** и **[Primary](index-primary-property-dao.md)** объекта **Index** за установлено **true,** индекс является уникальным и первичным: он уникальным образом идентифицирует все записи в таблице в предопределеном логическом порядке. Если свойство **Primary** имеет значение **False,** индекс является дополнительным индексом. Дополнительные индексы (как ключевые, так и нестрогие) логически упорядочивание записей в предварительно определенном порядке без использования в качестве идентификатора для записей в таблице.

> [!NOTE]
> - Создавать индексы для таблиц не нужно, но в больших неиндексных таблицах доступ к определенной записи может занять много времени.
> - Записи, полученные из таблиц без индексов, не возвращаются в определенной последовательности.
> - Свойство **[Attributes](field-attributes-property-dao.md)** каждого **[объекта Field](field-object-dao.md)** в объекте **Index** определяет порядок записей и, следовательно, определяет методы доступа для этого объекта **Index.**
> - Уникальный индекс помогает оптимизировать поиск записей.
> - Индексы не влияют на физический порядок базовой таблицы; индексы влияют только на то, как записи доступны объекту **[Recordset](recordset-object-dao.md)** типа таблицы при выбранном индексе или при создании объектов **Recordset** ядром базы данных Microsoft Access.

## <a name="example"></a>Пример

В этом примере свойству **Unique** нового объекта **Index** задано свойство **True,** а затем к коллекции **Indexes** таблицы Employees (Сотрудники) прилагается индекс. Затем он нумерирует коллекцию **Indexes** **объекта TableDef** и коллекцию **свойств** каждого **индекса.** Новый индекс **разрешает** только одну запись с определенным сочетанием Country, LastName и FirstName в **TableDef.**

```vb
    Sub UniqueX() 
     
       Dim dbsNorthwind As Database 
       Dim tdfEmployees As TableDef 
       Dim idxNew As Index 
       Dim idxLoop As Index 
       Dim prpLoop As Property 
     
       Set dbsNorthwind = OpenDatabase("Northwind.mdb") 
       Set tdfEmployees = dbsNorthwind!Employees 
     
       With tdfEmployees 
          ' Create and append new Index object to the Indexes  
          ' collection of the Employees table. 
          Set idxNew = .CreateIndex("NewIndex") 
     
          With idxNew 
             .Fields.Append .CreateField("Country") 
             .Fields.Append .CreateField("LastName") 
             .Fields.Append .CreateField("FirstName") 
             .Unique = True 
          End With 
     
          .Indexes.Append idxNew 
          .Indexes.Refresh 
     
          Debug.Print .Indexes.Count & " Indexes in " & _ 
             .Name & " TableDef" 
     
          ' Enumerate Indexes collection of Employees table. 
          For Each idxLoop In .Indexes 
             Debug.Print "  " & idxLoop.Name 
     
             ' Enumerate Properties collection of each Index  
             ' object. 
             For Each prpLoop In idxLoop.Properties 
                Debug.Print "    " & prpLoop.Name & _ 
                   " = " & IIf(prpLoop = "", "[empty]", prpLoop) 
             Next prpLoop 
     
          Next idxLoop 
     
          ' Delete new Index because this is a demonstration. 
          .Indexes.Delete idxNew.Name 
       End With 
     
       dbsNorthwind.Close 
     
    End Sub
```
