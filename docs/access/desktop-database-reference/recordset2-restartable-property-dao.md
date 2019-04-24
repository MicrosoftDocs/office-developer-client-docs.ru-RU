---
title: Свойство Recordset2. restarted (DAO)
TOCTitle: Restartable Property
ms:assetid: 9b1c40f8-5a33-2527-a7b6-bef4cb991d7e
ms:mtpsurl: https://msdn.microsoft.com/library/Ff198019(v=office.15)
ms:contentKeyID: 48546560
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: 873911ff8475a0b37f3f67d9cb2c01afc577487d
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32309092"
---
# <a name="recordset2restartable-property-dao"></a>Свойство Recordset2. restarted (DAO)


**Область применения**: Access 2013, Office 2013

Возвращает значение, которое указывает на то, поддерживает ли объект **[Recordset](recordset-object-dao.md)** метод **[Requery](recordset2-requery-method-dao.md)**, который повторно выполняет запрос, на котором основан объект **Recordset**.

## <a name="syntax"></a>Синтаксис

*Expression* . Перезапускаемой

*Expression (выражение* ) Переменная, представляющая объект **Recordset2** .

## <a name="remarks"></a>Замечания

Объект **Recordset** табличного типа всегда возвращает **значение false**.

Проверьте свойство **** restarted перед использованием метода Restart объекта **Recordset** . **** Если свойство restarted объекта имеет значение **false**, используйте метод **[OpenRecordset](connection-openrecordset-method-dao.md)** базового объекта **[QueryDef](querydef-object-dao.md)** , чтобы повторно выполнить запрос. ****

## <a name="example"></a>Пример

В этом примере показано **** свойство restarted с различными объектами **Recordset** .

```vb
    Sub RestartableX()
    
       Dim dbsNorthwind As Database
       Dim rstTemp As Recordset2
    
       Set dbsNorthwind = OpenDatabase("Northwind.mdb")
    
       With dbsNorthwind
          ' Open a table-type Recordset and print its 
          ' Restartable property.
          Set rstTemp = .OpenRecordset("Employees", dbOpenTable)
          Debug.Print _
             "Table-type recordset from Employees table"
          Debug.Print "  Restartable = " & rstTemp.Restartable
          rstTemp.Close
    
          ' Open a Recordset from an SQL statement and print its 
          ' Restartable property.
          Set rstTemp = _
             .OpenRecordset("SELECT * FROM Employees")
          Debug.Print "Recordset based on SQL statement"
          Debug.Print "  Restartable = " & rstTemp.Restartable
          rstTemp.Close
    
          ' Open a Recordset from a saved QueryDef object and 
          ' print its Restartable property.
          Set rstTemp = .OpenRecordset("Current Product List")
          Debug.Print _
             "Recordset based on permanent QueryDef (" & _
             rstTemp.Name & ")"
          Debug.Print "  Restartable = " & rstTemp.Restartable
          rstTemp.Close
    
          .Close
       End With
    
    End Sub
```
