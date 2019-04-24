---
title: Свойство. Inherited (DAO)
TOCTitle: Inherited Property
ms:assetid: 10e624db-2301-b9be-beca-6e8caccf7274
ms:mtpsurl: https://msdn.microsoft.com/library/Ff845349(v=office.15)
ms:contentKeyID: 48543304
ms.date: 09/18/2015
mtps_version: v=office.15
f1_keywords:
- dao360.chm1052991
f1_categories:
- Office.Version=v15
localization_priority: Normal
ms.openlocfilehash: cf3aef6d04c7d7cc573ec1d6efaca7d5238f5125
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32302928"
---
# <a name="propertyinherited-property-dao"></a>Свойство. Inherited (DAO)


**Область применения**: Access 2013, Office 2013 

Возвращает значение, которое указывает, наследуется ли объект **[Свойства](property-object-dao.md)** из базового объекта.

## <a name="syntax"></a>Синтаксис

*Expression* . Наследуется

*Expression (выражение* ) Переменная, представляющая объект **Property** .

## <a name="remarks"></a>Замечания

Для встроенных объектов **Property** , представляющих собой предопределенные свойства, единственным возможным возвращаемым значением является **false**.

Можно использовать унаследованное **** свойство, чтобы определить, было ли создано пользовательское **свойство** для объекта, к которому он применяется, или же **свойство** было унаследовано от другого объекта. Например, предположим, что вы создаете новое **свойство** для объекта **[QueryDef](querydef-object-dao.md)** , а затем открыли объект **[Recordset](recordset-object-dao.md)** из объекта **QueryDef** . Это новое **свойство** будет частью коллекции **[свойств](properties-collection-dao.md)** объекта **Recordset** , а его унаследованное свойство будет **** иметь значение **true** , так как свойство было создано для объекта **QueryDef** , а не ** Объект Recordset** .

## <a name="example"></a>Пример

В этом примере показано **** , как использовать унаследованное свойство, чтобы определить, был ли создан пользовательский объект **свойства** для объекта **Recordset** или для некоторого базового объекта.

```vb 
Sub InheritedX() 
 
 Dim dbsNorthwind As Database 
 Dim tdfTest As TableDef 
 Dim rstTest As Recordset 
 Dim prpNew As Property 
 Dim prpLoop As Property 
 
 ' Create a new property for a saved TableDef object, then 
 ' open a recordset from that TableDef object. 
 Set dbsNorthwind = OpenDatabase("Northwind.mdb") 
 Set tdfTest = dbsNorthwind.TableDefs(0) 
 Set prpNew = tdfTest.CreateProperty("NewProperty", _ 
 dbBoolean, True) 
 tdfTest.Properties.Append prpNew 
 Set rstTest = tdfTest.OpenRecordset(dbOpenForwardOnly) 
 
 ' Show Name and Inherited property of the new Property 
 ' object in the TableDef. 
 Debug.Print "NewProperty of " & tdfTest.Name & _ 
 " TableDef:" 
 Debug.Print " Inherited = " & _ 
 tdfTest.Properties("NewProperty").Inherited 
 
 ' Show Name and Inherited property of the new Property 
 ' object in the Recordset. 
 Debug.Print "NewProperty of " & rstTest.Name & _ 
 " Recordset:" 
 Debug.Print " Inherited = " & _ 
 rstTest.Properties("NewProperty").Inherited 
 
 ' Delete new TableDef because this is a demonstration. 
 tdfTest.Properties.Delete prpNew.Name 
 dbsNorthwind.Close 
 
End Sub 
 
```

