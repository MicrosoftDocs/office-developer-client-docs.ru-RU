---
title: Свойство Property.Inherited (DAO)
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
ms.openlocfilehash: 56f0153748a6d5cc7dd8e6b15dbae93fb638a381
ms.sourcegitcommit: d7248f803002b31cf7fc561b03530199a9b0a8fd
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 11/02/2018
ms.locfileid: "25927160"
---
# <a name="propertyinherited-property-dao"></a>Свойство Property.Inherited (DAO)


**Применимо к**: Access 2013, Office 2013 

Возвращает значение, указывающее, является ли объект **[Свойства](property-object-dao.md)** наследуется из базового объекта.

## <a name="syntax"></a>Синтаксис

*выражение* . Унаследованные

*выражение* Переменная, которая представляет собой объект- **свойство** .

## <a name="remarks"></a>Примечания

Для встроенных **свойств** объектов, которые представляют предварительно определенные свойства единственными возможными возвращаемое значение — **значение False**.

Чтобы определить, был ли создан пользовательских **свойств** для объекта, его можно применить, можно использовать свойство **Inherited** или ли **свойство** наследующего от другого объекта. Предположим, например, создание нового **Свойства** для объекта **[QueryDef](querydef-object-dao.md)** и откройте объект **[набора записей](recordset-object-dao.md)** из объекта **QueryDef** . Это новое **свойство** будет частью коллекции **[свойств](properties-collection-dao.md)** объекта **набора записей** и его свойство **Inherited** будет присвоено **значение True,** так как свойство был создан для объекта **QueryDef** не ** Набор записей** объекта.

## <a name="example"></a>Пример

В этом примере свойство **Inherited** используется для определения, был ли создан объект пользовательские **Свойства** для объекта **набора записей** или для некоторых базового объекта.

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

