---
title: Свойство Recordset2.Transactions (DAO)
TOCTitle: Transactions Property
ms:assetid: f2169565-f782-4089-0e4b-bc5d58d37db5
ms:mtpsurl: https://msdn.microsoft.com/library/Ff836614(v=office.15)
ms:contentKeyID: 48548642
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: 58610ee87e61a8b342955107c2ba2b690e610c8b
ms.sourcegitcommit: d6695c94415fa47952ee7961a69660abc0904434
ms.translationtype: Auto
ms.contentlocale: ru-RU
ms.lasthandoff: 01/17/2019
ms.locfileid: "28713872"
---
# <a name="recordset2transactions-property-dao"></a>Свойство Recordset2.Transactions (DAO)


**Применимо к**: Access 2013, Office 2013

Возвращает значение, указывающее, поддерживает ли объект транзакции. Только для чтения, **Boolean**.

## <a name="syntax"></a>Синтаксис

*выражение* . Транзакции

*выражение* Переменная, которая представляет собой объект- **Recordset2** .

## <a name="remarks"></a>Замечания

В рабочей области Microsoft Access можно также свойство **транзакции** с или таблице добавляющий объекты **набора записей** . Моментальный снимок и прямого — только – **[набора записей](recordset-object-dao.md)** объекты типа всегда возвращает **значение False**.

Если динамический набор - или -таблицей **набора записей** на основании таблица ядра базы данных Microsoft Access, свойство **транзакции** имеет **значение True** , и могут использоваться транзакции. Другие модули базы данных могут не поддерживать транзакции. К примеру нельзя использовать транзакции в объект типа динамического **набора записей** , на основе таблицы Paradox.

Проверьте свойство **транзакций** перед убедитесь в том, что транзакции поддерживаются с помощью метода **[BeginTrans](dbengine-begintrans-method-dao.md)** объекта **[рабочей области для](workspace-object-dao.md)** объекта **набора записей** . С помощью методов **BeginTrans**, **CommitTrans**или **отката** неподдерживаемый объект не оказывает влияния.

## <a name="example"></a>Пример

В этом примере демонстрируется свойство **транзакции** в рабочих областях Microsoft Access.

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

