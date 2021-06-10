---
title: Метод DBEngine.Idle (DAO)
TOCTitle: Idle Method
ms:assetid: c90b565e-626e-139d-102a-0386601ce0c8
ms:mtpsurl: https://msdn.microsoft.com/library/Ff823202(v=office.15)
ms:contentKeyID: 48547666
ms.date: 09/18/2015
mtps_version: v=office.15
f1_keywords:
- dao360.chm1052978
f1_categories:
- Office.Version=v15
localization_priority: Normal
ms.openlocfilehash: 7a84e3cc4b35886a12b2e6b4cf92b7483fea293a
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32294332"
---
# <a name="dbengineidle-method-dao"></a>Метод DBEngine.Idle (DAO)

**Область применения**: Access 2013, Office 2013

Приостанавливать обработку данных, позволяя движку базы данных Microsoft Access выполнять любые ожидающие задачи, такие как оптимизация памяти или время ожидания страниц (только в рабочей области Microsoft Access).

## <a name="syntax"></a>Синтаксис

*выражения* . Idle ***(Action)***

*expression*: переменная, представляющая объект **DBEngine**.

## <a name="parameters"></a>Параметры

<table>
<colgroup>
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
</colgroup>
<thead>
<tr class="header">
<th><p>Имя</p></th>
<th><p>Обязательный/необязательный</p></th>
<th><p>Тип данных</p></th>
<th><p>Описание</p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><em>Action</em></p></td>
<td><p>Необязательный</p></td>
<td><p><strong>Variant</strong></p></td>
<td><p>Указывает действие, необходимое для принятия. Может быть одной из <strong><a href="idleenum-enumeration-dao.md">констант IdleEnum.</a></strong></p></td>
</tr>
</tbody>
</table>


## <a name="remarks"></a>Примечания

Метод **Idle** позволяет механизму базы данных Microsoft Access выполнять фоновые задачи, которые могут быть не в курсе из-за интенсивной обработки данных. Это часто верно в многоядерных многозадачных средах, где не хватает времени фоновой обработки, чтобы сохранить все записи в течение **[Recordset.](recordset-object-dao.md)**

Обычно блоки чтения удаляются, а данные в локальных объектах **recordset** типа dynaset обновляются только в том случае, если не происходит никаких других действий (в том числе движений мыши). Если вы периодически используете метод **Idle,** то двигатель базы данных Microsoft Access может догнать задачи обработки фона, выпустив нежелательные блокировки чтения.

Указание необязательного **аргумента dbRefreshCache** обновляет память только с самыми актуальными данными из базы данных.

Этот метод не требуется использовать в средах с одним пользователем, если не запущено несколько экземпляров приложения. Метод **Idle** может повысить производительность в многоуровневой среде, так как заставляет двигатель базы данных записывать данные на диск, выпуская блокировки в памяти.


> [!NOTE]
> Кроме того, можно освободить блокировки чтения, сделав операции частью транзакции.

## <a name="example"></a>Пример

В этом примере метод **Idle** используется для обеспечения доступа к самым актуальным данным из базы данных. Процедура IdleOutput необходима для запуска этой процедуры.

```vb 
Sub IdleX() 
 
 Dim dbsNorthwind As Database 
 Dim strCountry As String 
 Dim strSQL As String 
 Dim rstOrders As Recordset 
 
 Set dbsNorthwind = OpenDatabase("Northwind.mdb") 
 
 ' Get name of country from user and build SQL statement 
 ' with it. 
 strCountry = Trim(InputBox("Enter country:")) 
 strSQL = "SELECT * FROM Orders WHERE ShipCountry = '" & _ 
 strCountry & "' ORDER BY OrderID" 
 
 ' Open Recordset object with SQL statement. 
 Set rstOrders = dbsNorthwind.OpenRecordset(strSQL) 
 
 ' Display contents of Recordset object. 
 IdleOutput rstOrders, strCountry 
 
 rstOrders.Close 
 dbsNorthwind.Close 
 
End Sub 
 
Sub IdleOutput(rstTemp As Recordset, strTemp As String) 
 
 ' Call the Idle method to release unneeded locks, force 
 ' pending writes, and refresh the memory with the current 
 ' data in the .mdb file. 
 DBEngine.Idle dbRefreshCache 
 
 ' Enumerate the Recordset object. 
 With rstTemp 
 Debug.Print "Orders from " & strTemp & ":" 
 Debug.Print , "OrderID", "CustomerID", "OrderDate" 
 Do While Not .EOF 
 Debug.Print , !OrderID, !CustomerID, !OrderDate 
 .MoveNext 
 Loop 
 End With 
 
End Sub 
 
```

