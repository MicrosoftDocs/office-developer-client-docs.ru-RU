---
title: Свойство Recordset2. Transactions (DAO)
TOCTitle: Transactions Property
ms:assetid: f2169565-f782-4089-0e4b-bc5d58d37db5
ms:mtpsurl: https://msdn.microsoft.com/library/Ff836614(v=office.15)
ms:contentKeyID: 48548642
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: 58610ee87e61a8b342955107c2ba2b690e610c8b
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32309244"
---
# <a name="recordset2transactions-property-dao"></a>Свойство Recordset2. Transactions (DAO)


**Область применения**: Access 2013, Office 2013

Возвращает значение, которое указывает на то, поддерживает ли объект транзакций. Только для чтения, **Boolean**.

## <a name="syntax"></a>Синтаксис

*Expression* . Транзакций

*Expression (выражение* ) Переменная, представляющая объект **Recordset2** .

## <a name="remarks"></a>Замечания

В рабочей области Microsoft Access можно также использовать свойство Transactions **** с объектами **Recordset** типа динамического подмножества или таблицы. Объекты **[Recordset](recordset-object-dao.md)** для типа моментального снимка и прямого прямого доступа — всегда возвращают **значение false**.

Если **набор записей** динамического типа или табличного типа основан на таблице ядра СУБД Microsoft Access, свойство Transactions имеет **** **значение true** , и вы можете использовать транзакции. Другие ядра СУБД могут не поддерживать транзакции. Например, нельзя использовать транзакции в объекте **Recordset** типа динамического подмножества на основе таблицы Paradox.

Проверьте свойство **Transactions** перед использованием метода **[BeginTrans](dbengine-begintrans-method-dao.md)** объекта **Recordset** объекта **[Workspace](workspace-object-dao.md)** , чтобы убедиться в том, что транзакции поддерживаются. Использование методов **BeginTrans**, **CommitTrans**и **ROLLBACK** для неподдерживаемого объекта не оказывает никакого действия.

## <a name="example"></a>Пример

В этом примере показано **** свойство Transactions в рабочей области Microsoft Access.

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

