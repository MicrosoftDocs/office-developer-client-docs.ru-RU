---
title: Свойство Index.Foreign (DAO)
TOCTitle: Foreign Property
ms:assetid: 81272436-a506-4b72-fd28-2d68e76d6d9b
ms:mtpsurl: https://msdn.microsoft.com/library/Ff196489(v=office.15)
ms:contentKeyID: 48545943
ms.date: 09/18/2015
mtps_version: v=office.15
f1_keywords:
- dao360.chm1052974
f1_categories:
- Office.Version=v15
ms.openlocfilehash: 878a59d6c844c7c46cf1a38ee6e4ef165d6fca92
ms.sourcegitcommit: d7248f803002b31cf7fc561b03530199a9b0a8fd
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 11/02/2018
ms.locfileid: "25926411"
---
# <a name="indexforeign-property-dao"></a>Свойство Index.Foreign (DAO)

**Применимо к**: Access 2013, Office 2013

Возвращает значение, указывающее, представляет ли объект **[индекса](index-object-dao.md)** внешний ключ в таблице (только для рабочих областей Microsoft Access). .

## <a name="syntax"></a>Синтаксис

*выражение* . Внешний

*выражение* Переменная, которая представляет объект **индекса** .

## <a name="remarks"></a>Примечания

Возвращаемое значение имеет тип данных **Boolean** , которое возвращает **значение True,** Если объект **индекса** представляет внешний ключ.

Внешний ключ состоит из одного или нескольких полей внешней таблицы, которые однозначно идентифицируют все строки в основной таблице.

Ядро базы данных Microsoft Access создает объект **индекса** для таблицы внешнего и задает свойство **внешнего** при создании отношения, которое обеспечивает целостность данных.

## <a name="example"></a>Пример

В этом примере показано, как свойство **внешнего** позволяет определить, какие объекты **индекса** **TableDef** внешнего ключа индексов. Такие индексы создаются ядром СУБД Microsoft Access, при создании **отношения** . Имя по умолчанию для внешнего ключа индексов — это имя основной таблицы, а также имя внешней таблицы. Функция ForeignOutput является обязательным для выполнения этой процедуры.

```vb
    Sub ForeignX() 
     
     Dim dbsNorthwind As Database 
     
     Set dbsNorthwind = OpenDatabase("Northwind.mdb") 
     
     With dbsNorthwind 
     ' Print report on foreign key indexes from two 
     ' TableDef objects and a QueryDef object. 
     ForeignOutput .TableDefs!Products 
     ForeignOutput .TableDefs!Orders 
     ForeignOutput .TableDefs![Order Details] 
     
     .Close 
     End With 
     
    End Sub 
     
    Function ForeignOutput(tdfTemp As TableDef) 
     
     Dim idxLoop As Index 
     
     With tdfTemp 
     Debug.Print "Indexes in " & .Name & " TableDef" 
     ' Enumerate the Indexes collection of the specified 
     ' TableDef object. 
     For Each idxLoop In .Indexes 
     Debug.Print " " & idxLoop.Name 
     Debug.Print " Foreign = " & idxLoop.Foreign 
     Next idxLoop 
     End With 
     
    End Function
```
