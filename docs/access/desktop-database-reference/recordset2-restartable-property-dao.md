---
title: Recordset2.Restartable Property (DAO)
TOCTitle: Restartable Property
ms:assetid: 9b1c40f8-5a33-2527-a7b6-bef4cb991d7e
ms:mtpsurl: https://msdn.microsoft.com/library/Ff198019(v=office.15)
ms:contentKeyID: 48546560
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 3be986fce66342ec736ebfebcfbc3e615ae57a40
ms.sourcegitcommit: 19aca09c5812cfb98b68b5d4604dcaa814479df7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/09/2018
ms.locfileid: "25481608"
---
# <a name="recordset2restartable-property-dao"></a>Recordset2.Restartable Property (DAO)


**Применимо к**: Access 2013 | Office 2013

Возвращает значение, указывающее, поддерживает ли объект **[набора записей](recordset-object-dao.md)** метод **[повторный запрос](recordset2-requery-method-dao.md)** , который повторно выполняет запрос, на котором основано объекта **набора записей** .

## <a name="syntax"></a>Синтаксис

*выражение* . Перезапускаемое

*выражение* Переменная, которая представляет собой объект- **Recordset2** .

## <a name="remarks"></a>Замечания

Объекты **набора записей** в таблице типа всегда возвращает **значение False**.

Проверьте свойство **Restartable** перед использованием метода **повторный запрос** на объект **набора записей** . Если свойство **Restartable** имеет значение **False**, используйте метод **[OpenRecordset](connection-openrecordset-method-dao.md)** для базового объекта **[QueryDef](querydef-object-dao.md)** повторное выполнение запроса.

## <a name="example"></a>Пример

В этом примере демонстрируется свойство **Restartable** с разных объектов **набора записей** .

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
