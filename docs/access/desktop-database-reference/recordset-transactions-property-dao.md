---
title: Recordset.Transactions Property (DAO)
TOCTitle: Transactions Property
ms:assetid: 7830c056-8d6a-7942-7993-aa04b29cd77f
ms:mtpsurl: https://msdn.microsoft.com/library/Ff196110(v=office.15)
ms:contentKeyID: 48545746
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: c3b34f8f027b2e70ada94c6d15584cf25a4aec1c
ms.sourcegitcommit: c557bbcccf37a6011f89aae1ddd399dfe549d087
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/31/2018
ms.locfileid: "25873294"
---
# <a name="recordsettransactions-property-dao"></a>Recordset.Transactions Property (DAO)


**Применимо к**: Access 2013, Office 2013

Возвращает значение, указывающее, поддерживает ли объект транзакции. Только для чтения, **Boolean**.

## <a name="syntax"></a>Синтаксис

*выражение* . Транзакции

*выражение* Переменная, которая представляет собой объект **набора записей** .

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

