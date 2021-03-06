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
localization_priority: Normal
ms.openlocfilehash: a3c6adfaf9648147a763f997ce2a91aadc4f7637
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32291819"
---
# <a name="indexforeign-property-dao"></a>Свойство Index.Foreign (DAO)

**Область применения**: Access 2013, Office 2013

Возвращает значение, которое указывает, представляет ли объект **[Index](index-object-dao.md)** иностранный ключ в таблице (только в рабочей области Microsoft Access). .

## <a name="syntax"></a>Синтаксис

*выражения* . Foreign

*выражение* Переменная, представляюная объект **Index.**

## <a name="remarks"></a>Примечания

Возвращаемая величина — это тип **данных Boolean,** который возвращает **True,** если объект **Index** представляет иностранный ключ.

Иностранный ключ состоит из одного или нескольких полей в иностранной таблице, которые однозначно определяют все строки в основной таблице.

Двигатель базы данных Microsoft Access создает объект **Index** для иностранной таблицы и задает свойство **Foreign** при создании отношения, которое обеспечивает целостность ссылок.

## <a name="example"></a>Пример

В этом примере показано, как **свойство Foreign** может указывать, какие объекты **Index** в **TableDef** являются иностранными ключевыми индексами. Такие индексы создаются с помощью двигателя базы данных Microsoft Access, когда **создается отношение.** По умолчанию для индексов внешних ключевых элементов имя основной таблицы плюс имя иностранной таблицы. Для запуска этой процедуры требуется функция ForeignOutput.

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
