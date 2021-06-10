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

Задает или возвращает значение, которое указывает, представляет ли объект **[Index](index-object-dao.md)** уникальный (ключевой) индекс для таблицы (только в рабочей области Microsoft Access).

## <a name="syntax"></a>Синтаксис

*выражения* . Уникальный

*выражение* Переменная, представляюная объект **Index.**

## <a name="remarks"></a>Примечания

Этот параметр свойства считыв или записывай до тех пор, пока объект не будет примыкать к коллекции, после чего он будет только для чтения.

Уникальный индекс состоит из одного или нескольких полей, логически упорядочив все записи в таблице в уникальном заранее определенном порядке. Если индекс состоит из одного поля, значения в этом поле должны быть уникальными для всей таблицы. Если индекс состоит из нескольких полей, каждое поле может содержать дублирующие значения, но каждая комбинация значений из всех проиндексированные поля должна быть уникальной.

Если уникальные **[](index-primary-property-dao.md)** и первичные свойства объекта **Index** задают  **true,** индекс является уникальным и первичным: он однозначно определяет все записи в таблице в заранее определенном логическом порядке. Если свойство **Primary** настроено на **False,** индекс является вторичным индексом. Вторичные индексы (как ключевые, так и неконкретные) логически упорядочивали записи в заранее заранее определенном порядке без использования в качестве идентификатора для записей в таблице.

> [!NOTE]
> - Вам не нужно создавать индексы для таблиц, но в больших, неиндексуальных таблицах доступ к определенной записи может занять много времени.
> - Записи, извлеченные из таблиц без индексов, возвращаются без определенной последовательности.
> - Свойство **[Атрибуты](field-attributes-property-dao.md)** каждого объекта **[Field](field-object-dao.md)** в объекте **Index** определяет порядок записей и, следовательно, определяет методы доступа, которые необходимо использовать для этого **объекта Index.**
> - Уникальный индекс помогает оптимизировать поиск записей.
> - Индексы не влияют на физический порядок базовой таблицы; Индексы влияют только на то, как записи доступны объекту **[Recordset](recordset-object-dao.md)** в таблице, когда выбран определенный индекс или когда в движке базы данных Microsoft Access создаются объекты **Recordset.**

## <a name="example"></a>Пример

В этом примере **уникальное** свойство нового объекта **Index** определяется как **True** и придает индекс коллекции **Indexes** таблицы Employees. Далее в нем огосвидетельна коллекция **Индексов** **TableDef** и коллекция **свойств** каждого **индекса.** Новый индекс **разрешает** только одну запись с определенной комбинацией Country, LastName и FirstName в **TableDef.**

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
