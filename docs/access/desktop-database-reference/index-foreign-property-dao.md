---
title: Свойство index. Foreign (DAO)
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
localization_priority: Normal
ms.openlocfilehash: a3c6adfaf9648147a763f997ce2a91aadc4f7637
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32291819"
---
# <a name="indexforeign-property-dao"></a>Свойство index. Foreign (DAO)

**Область применения**: Access 2013, Office 2013

Возвращает значение, которое указывает, представляет ли объект **[index](index-object-dao.md)** внешний ключ в таблице (только для рабочих областей Microsoft Access). .

## <a name="syntax"></a>Синтаксис

*Expression* . Правительства

*Expression (выражение* ) Переменная, представляющая объект **индекса** .

## <a name="remarks"></a>Замечания

Возвращаемое значение — это **логический** тип данных, который возвращает **значение true** , если объект **index** представляет внешний ключ.

Внешний ключ состоит из одного или нескольких полей в иностранной таблице, которые уникально идентифицируют все строки в главной таблице.

Ядро СУБД Microsoft Access создает объект **индекса** для внешней таблицы и задает внешнее свойство при **** создании связи, которая обеспечивает целостность ссылок.

## <a name="example"></a>Пример

В этом примере показано, **** как внешнее свойство может указывать, какие объекты **индекса** **tabledef** являются индексами внешних ключей. Такие индексы создаются ядром СУБД Microsoft Access при создании **отношения** . По умолчанию для индексов внешних ключей используется имя основной таблицы и имя внешней таблицы. Для выполнения этой процедуры требуется функция Фореигнаутпут.

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
