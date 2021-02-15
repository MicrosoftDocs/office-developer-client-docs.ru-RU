---
title: Свойство Recordset.Transactions (DAO)
TOCTitle: Transactions Property
ms:assetid: 7830c056-8d6a-7942-7993-aa04b29cd77f
ms:mtpsurl: https://msdn.microsoft.com/library/Ff196110(v=office.15)
ms:contentKeyID: 48545746
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: b23568e0830ef07e58119d02c4d221dad4b1d015
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32307597"
---
# <a name="recordsettransactions-property-dao"></a>Свойство Recordset.Transactions (DAO)


**Область применения**: Access 2013, Office 2013

Возвращает значение, которое указывает на то, поддерживает ли объект транзакций. Только для чтения, **Boolean**.

## <a name="syntax"></a>Синтаксис

*выражение .* Транзакции

*expression*: переменная, представляющая объект **Recordset**.

## <a name="remarks"></a>Примечания

В рабочей области Microsoft Access можно также использовать свойство **Transactions** с объектами Recordset типа dynaset или **table.** Объекты **[Recordset](recordset-object-dao.md)** типа "моментальный снимок" и "только вперед" всегда возвращают **false.**

Если набор записей типа "dynaset" или "table" основан на таблице ядров баз данных Microsoft Access, свойство **Transactions** имеет свойство **True,** и вы можете использовать транзакции.  Другие движки баз данных могут не поддерживать транзакции. Например, нельзя использовать транзакции в объекте **Recordset** типа dynaset на основе таблицы Paradox.

Проверьте свойство **Transactions** перед использованием метода **[BeginTrans](dbengine-begintrans-method-dao.md)** в объекте **[Workspace](workspace-object-dao.md)** объекта **Recordset,** чтобы убедиться, что транзакции поддерживаются. Использование **методов BeginTrans,** **CommitTrans** или **Rollback** для неподтверченного объекта не оказывает влияния.

## <a name="example"></a>Пример

В этом примере показано свойство **Transactions** в рабочей области Microsoft Access.

```vb 
Sub TransactionsX() 
 
 Dim wrkAcc As Workspace 
 Dim dbsNorthwind As Database 
 Dim conPubs As Connection 
 Dim rstTemp As Recordset 
 
 Set wrkAcc = CreateWorkspace("", "admin", "", dbUseJet) 
 Set dbsNorthwind = wrkAcc.OpenDatabase("Northwind.mdb") 
 
 ' Open two different Recordset objects and display the 
 ' Transactions property of each. 
 
 Debug.Print "Opening Microsoft Access table-type " & _ 
 "recordset..." 
 Set rstTemp = dbsNorthwind.OpenRecordset( _ 
 "Employees", dbOpenTable) 
 Debug.Print " Transactions = " & rstTemp.Transactions 
 
 Debug.Print "Opening forward-only-type " & _ 
 "recordset where the source is an SQL statement..." 
 Set rstTemp = dbsNorthwind.OpenRecordset( _ 
 "SELECT * FROM Employees", dbOpenForwardOnly) 
 Debug.Print " Transactions = " & rstTemp.Transactions 
 
 rstTemp.Close 
 dbsNorthwind.Close 
 conPubs.Close 
 wrkAcc.Close 
End Sub 
 
```

