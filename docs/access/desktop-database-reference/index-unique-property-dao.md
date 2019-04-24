---
title: Свойство index. Unique (DAO)
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
# <a name="indexunique-property-dao"></a>Свойство index. Unique (DAO)

**Область применения**: Access 2013, Office 2013

Задает или возвращает значение, указывающее, представляет ли объект **[индекса](index-object-dao.md)** уникальный (ключ) индекс для таблицы (только для рабочих областей Microsoft Access).

## <a name="syntax"></a>Синтаксис

*Expression* . Уникальный

*Expression (выражение* ) Переменная, представляющая объект **индекса** .

## <a name="remarks"></a>Замечания

Значение этого свойства доступно для чтения и записи до тех пор, пока объект не будет добавлен в коллекцию, после чего он доступен только для чтения.

Уникальный индекс состоит из одного или нескольких полей, которые логически упорядочивают все записи в таблице в уникальном, предварительно определенном порядке. Если индекс состоит из одного поля, значения в этом поле должны быть уникальными для всей таблицы. Если индекс состоит из нескольких полей, каждое поле может содержать повторяющиеся значения, но каждая комбинация значений из всех индексируемых полей должна быть уникальной.

Если для свойств **UNIQUE** и **[PRIMARY](index-primary-property-dao.md)** объекта **index** задано значение **true**, то индекс является уникальным и основным: он однозначно определяет все записи в таблице в предварительно определенном логическом порядке. Если для свойства **PRIMARY** задано значение **false**, то индекс является вторичным индексом. Вторичные индексы (ключевые и неключевые) логически упорядочивают записи в предварительно заданном порядке, не прибегая к идентификатору записей в таблице.

> [!NOTE]
> - Не нужно создавать индексы для таблиц, но в больших неиндексированных таблицах доступ к определенной записи может занять много времени.
> - Записи, извлеченные из таблиц без индексов, возвращаются без определенной последовательности.
> - Свойство **[Attributes](field-attributes-property-dao.md)** каждого объекта **[field](field-object-dao.md)** в объекте **index** определяет порядок записей и, соответственно, определяет способы доступа, которые необходимо использовать для этого объекта **индекса** .
> - Уникальный индекс помогает оптимизировать поиск записей.
> - Индексы не влияют на физический порядок базовых таблиц; индексы влияют только на то, как доступ к записям осуществляется с помощью объекта **[Recordset](recordset-object-dao.md)** табличного типа при выборе определенного индекса или при создании ядром СУБД Microsoft Access объектов **Recordset** .

## <a name="example"></a>Пример

В этом примере для свойства **UNIQUE** нового объекта **index** устанавливается **значение true**, а индекс добавляется в коллекцию **indexes** таблицы Employees. Затем выполняется перечисление **** коллекции индексов объектов **tabledef** и коллекции **свойств** каждого **индекса**. Новый **индекс** позволяет только одной записи с определенным сочетанием страны, LastName и FirstName в **tabledef**.

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
