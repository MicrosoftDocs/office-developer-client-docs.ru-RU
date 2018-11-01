---
title: Index.Unique Property (DAO)
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
ms.openlocfilehash: 877be95d2cd65b020946f125714e0229650d5ec5
ms.sourcegitcommit: c557bbcccf37a6011f89aae1ddd399dfe549d087
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/31/2018
ms.locfileid: "25871887"
---
# <a name="indexunique-property-dao"></a>Index.Unique Property (DAO)

**Применимо к**: Access 2013, Office 2013

Задает или возвращает значение, указывающее, представляет ли объект **[индекса](index-object-dao.md)** уникальный индекс (основные) для таблицы (только для рабочих областей Microsoft Access).

## <a name="syntax"></a>Синтаксис

*выражение* . Уникальный

*выражение* Переменная, которая представляет объект **индекса** .

## <a name="remarks"></a>Замечания

Значение этого свойства — чтение и запись, пока объект добавляется к коллекции, после чего он доступен только для чтения.

Уникальный индекс состоит из одного или нескольких полей, логически Упорядочить все записи в таблице в порядке уникальный, предварительно заданных. Если индекс состоит из одного поля, значения в этом поле должно быть уникальным для всей таблицы. Если индекс состоит из нескольких полей, в каждом поле может содержать повторяющиеся значения, но каждый сочетание значений из всех индексированных полей должно быть уникальным.

Если как **Уникальный** , так и **[основной](index-primary-property-dao.md)** **индекс** объекта задано значение **True**, индекс уникальное и основной: однозначно определяет все записи в таблице в порядке, предварительно определенные, логических. Если **основной** свойство имеет значение **False**, индекс находится вторичного индекса. Вторичные индексы (ключевые и неключевые) логически упорядочить записи в предопределенном порядке без служат в качестве идентификатора для записей в таблице.


> [!NOTE]
> <UL>
> <LI>
> <P>У вас нет для создания индексов для таблиц, но в крупных, неиндексированные таблиц, доступ к определенной записи может уйти много времени.</P>
> <LI>
> <P>Записей, полученных из таблицы без индексов возвращаются в определенной последовательности.</P>
> <LI>
> <P>Свойство <STRONG><A href="field-attributes-property-dao.md">атрибуты</A></STRONG> каждого объекта <STRONG><A href="field-object-dao.md">поля</A></STRONG> в объекте <STRONG>индекса</STRONG> определяет порядок записей и следовательно определяет методы доступа для этого объекта <STRONG>индекса</STRONG> .</P>
> <LI>
> <P>Уникальный индекс помогает оптимизировать поиск записей.</P>
> <LI>
> <P>Индексы не влияют на физический порядок влияние индексов базовая таблица, как только записи обращением объекта <STRONG><A href="recordset-object-dao.md">набора записей</A></STRONG> в таблице тип при выборе определенного индекса или когда ядро базы данных Microsoft Access создает объекты <STRONG>набора записей</STRONG> .</P></LI></UL>



## <a name="example"></a>Пример

В этом примере задается свойство **Уникальный** **индекс** объекта значение **True**и добавляет индекс коллекции **индексов** таблицы «Сотрудники». Затем выполняется перечисление коллекции **индексов** **TableDef** и коллекции **свойств** каждого **индекса**. Новый **индекс** только позволит одна запись с конкретной комбинации страны, LastName и FirstName в **TableDef**.

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
