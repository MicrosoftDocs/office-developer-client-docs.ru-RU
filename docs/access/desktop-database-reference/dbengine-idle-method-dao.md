---
title: DBEngine.Idle Method (DAO)
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
ms.openlocfilehash: 50e445339251bb2d35f700c1fa3860c246ec70d4
ms.sourcegitcommit: c557bbcccf37a6011f89aae1ddd399dfe549d087
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/31/2018
ms.locfileid: "25882352"
---
# <a name="dbengineidle-method-dao"></a>DBEngine.Idle Method (DAO)


**Применимо к**: Access 2013, Office 2013


Выполняется приостановка обработки данных, позволяя ядро базы данных Microsoft Access завершить все ожидающие задач, таких как оптимизации памяти или время ожидания страницы (только для рабочих областей Microsoft Access).

## <a name="syntax"></a>Синтаксис

*выражение* . Простоя (***Действие***)

*выражение* Переменная, которая представляет собой объект- **DBEngine** .

### <a name="parameters"></a>Параметры

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
<th><p>Обязательный или необязательный</p></th>
<th><p>Тип данных</p></th>
<th><p>Описание</p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p>Действие</p></td>
<td><p>Необязательный</p></td>
<td><p><strong>Variant</strong></p></td>
<td><p>Указывает действие, которое выполняется. Может быть <strong><a href="idleenum-enumeration-dao.md">IdleEnum</a></strong> констант.</p></td>
</tr>
</tbody>
</table>


## <a name="remarks"></a>Замечания

Метод **Idle** позволяет ядро базы данных Microsoft Access для выполнения фоновых задач, могут не соответствовать действительности из-за процесс обработки данных. Это особенно актуально в многопользовательской, многозадачных средах, которые не являются достаточно фоновую обработку времени хранения для всех записей в наборе **[записей](recordset-object-dao.md)** текущей.

Как правило доступ на чтение блокировки удаляются и данных в локальной добавляющий **набора записей** объекты обновляются только в том случае, если возникают никаких других действий (в том числе движения мыши). При использовании метода **Idle** периодически ядро базы данных Microsoft Access можно захватить на фоновую обработку задачи освободить ненужные чтение блокировки.

Указание аргумент необязательный **dbRefreshCache** обновляет памяти с последних данных из базы данных.

Используйте этот метод в средах отдельного пользователя, если не запущено несколько экземпляров приложения не требуется. Метод **Idle** может повысить производительность в многопользовательской среде, так как принудительно ядро базы данных для записи данных на диск, освобождения блокировок на память.


> [!NOTE]
> Можно также запустить блокировки чтения, сделав операции часть транзакции.

## <a name="example"></a>Пример

В этом примере используется метод **Idle** , чтобы убедиться, что процедуру вывода обращается к последнему данных, которые доступны из базы данных. Процедура IdleOutput является обязательным для выполнения этой процедуры.

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

