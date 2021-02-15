---
title: Свойство Recordset.Restartable (DAO)
TOCTitle: Restartable Property
ms:assetid: 00def49d-ea7e-6cd5-2f4a-914a1ddcdd51
ms:mtpsurl: https://msdn.microsoft.com/library/Ff844737(v=office.15)
ms:contentKeyID: 48542919
ms.date: 09/18/2015
mtps_version: v=office.15
f1_keywords:
- dao360.chm1052926
f1_categories:
- Office.Version=v15
localization_priority: Normal
ms.openlocfilehash: 5142d0d47be37ca8c2e1c6b89462c05b7d41d302
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32307576"
---
# <a name="recordsetrestartable-property-dao"></a>Свойство Recordset.Restartable (DAO)


**Область применения**: Access 2013, Office 2013

Возвращает значение, которое указывает на то, поддерживает ли объект **[Recordset](recordset-object-dao.md)** метод **[Requery](recordset-requery-method-dao.md)**, который повторно выполняет запрос, на котором основан объект **Recordset**.

## <a name="syntax"></a>Синтаксис

*выражение .* Перезапуск

*expression*: переменная, представляющая объект **Recordset**.

## <a name="remarks"></a>Примечания

Объекты **Recordset табли с типом** таблицы всегда возвращают **false.**

Проверьте свойство **Restartable** перед использованием метода **Requery** в **объекте Recordset.** Если свойство **Restartable** объекта имеет свойство **False,** используйте метод **[OpenRecordset](connection-openrecordset-method-dao.md)** в основном объекте **[QueryDef](querydef-object-dao.md)** для повторного выполнения запроса.

## <a name="example"></a>Пример

В этом примере показано свойство **Restartable** с различными **объектами Recordset.**

```vb
    Sub RestartableX() 
     
     Dim dbsNorthwind As Database 
     Dim rstTemp As Recordset 
     
     Set dbsNorthwind = OpenDatabase("Northwind.mdb") 
     
     With dbsNorthwind 
     ' Open a table-type Recordset and print its 
     ' Restartable property. 
     Set rstTemp = .OpenRecordset("Employees", dbOpenTable) 
     Debug.Print _ 
     "Table-type recordset from Employees table" 
     Debug.Print " Restartable = " & rstTemp.Restartable 
     rstTemp.Close 
     
     ' Open a Recordset from an SQL statement and print its 
     ' Restartable property. 
     Set rstTemp = _ 
     .OpenRecordset("SELECT * FROM Employees") 
     Debug.Print "Recordset based on SQL statement" 
     Debug.Print " Restartable = " & rstTemp.Restartable 
     rstTemp.Close 
     
     ' Open a Recordset from a saved QueryDef object and 
     ' print its Restartable property. 
     Set rstTemp = .OpenRecordset("Current Product List") 
     Debug.Print _ 
     "Recordset based on permanent QueryDef (" & _ 
     rstTemp.Name & ")" 
     Debug.Print " Restartable = " & rstTemp.Restartable 
     rstTemp.Close 
     
     .Close 
     End With 
     
    End Sub
```
