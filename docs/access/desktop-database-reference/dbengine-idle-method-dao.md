---
title: Метод DBEngine. Idle (DAO)
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
# <a name="dbengineidle-method-dao"></a>Метод DBEngine. Idle (DAO)

**Область применения**: Access 2013, Office 2013

Приостанавливает обработку данных, позволяя ядру СУБД Microsoft Access выполнять все ожидающие задачи, такие как оптимизация памяти или время ожидания страниц (только для рабочих областей Microsoft Access).

## <a name="syntax"></a>Синтаксис

*Expression* . Бездействие (***действие***)

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
<td><p>Задает действие, которое необходимо выполнить. Может быть одной из констант <strong><a href="idleenum-enumeration-dao.md">идлинум</a></strong> .</p></td>
</tr>
</tbody>
</table>


## <a name="remarks"></a>Примечания

Метод **Idle** позволяет ядру СУБД Microsoft Access выполнять фоновые задачи, которые могут быть не актуальны из-за интенсивной обработки данных. Это часто относится к многозадачным средам, в которых недостаточно времени фоновой обработки для хранения всех записей в текущем **[наборе записей](recordset-object-dao.md)** .

Обычно блокировки чтения удаляются и данные в локальных объектах **набора записей** динамического типа обновляются только в том случае, если не выполняются никакие другие действия (включая перемещение мыши). Если вы периодически используете метод **Idle** , ядро СУБД Microsoft Access может отслеживать задачи фоновой обработки, освобождая ненужные блокировки чтения.

При указании необязательного аргумента **дбрефрешкаче** происходит обновление памяти с использованием только самых актуальных данных из базы данных.

Этот метод не требуется использовать в средах с одним пользователем, если не запущено несколько экземпляров приложения. Метод **Idle** может увеличить производительность в многопользовательской среде, так как она заставляет ядро СУБД записывать данные на диск, освобождая блокировку памяти.


> [!NOTE]
> Кроме того, можно выпустить блокировку чтения, делая операции частью транзакции.

## <a name="example"></a>Пример

В этом примере используется метод **Idle** , обеспечивающий доступ к последним данным, доступным из базы данных, в выходной процедуре. Для выполнения этой процедуры требуется процедура Идлеаутпут.

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

