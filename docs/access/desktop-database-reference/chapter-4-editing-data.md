---
title: 'Chapter 4: Editing Data'
TOCTitle: 'Chapter 4: Editing Data'
ms:assetid: 822b7365-0926-6411-6fb4-30de032570f8
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249563(v=office.15)
ms:contentKeyID: 48545974
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 3c5364a7b9e70c4627a7f5b4e6708542e2c8516f
ms.sourcegitcommit: 19aca09c5812cfb98b68b5d4604dcaa814479df7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/09/2018
ms.locfileid: "25481517"
---
# <a name="chapter-4-editing-data"></a>Chapter 4: Editing Data


**Применимо к**: Access 2013 | Office 2013

Предыдущая двух частях, как описано использование ADO для подключения к источнику данных, выполнения команды, получение результатов в объект **набора записей** и перейдите в рамках **набора записей**. Эта глава посвящена следующей базовые операции ADO: изменение данных.

В этой главе по-прежнему производится при использовании образца **набора записей** , введенные в Глава 3 — с помощью одного важное изменение. Следующий код используется для открытия **набора записей**:

```vb 
 
 . . . 
'BeginEditIntro 
 Dim strSQL As String 
 Dim objRs1 As ADODB.Recordset 
 
 strSQL = "SELECT * FROM Shippers" 
 
 Set objRs1 = New ADODB.Recordset 
 
 objRs1.Open strSQL, GetNewConnection, adOpenStatic, _ 
 adLockBatchOptimistic, adCmdText 
 
 ' Disconnect the Recordset from the Connection object. 
 Set objRs1.ActiveConnection = Nothing 
'EndEditIntro 
 
 
 . . . 
```

Важные изменения в код включает в себя свойства объект **подключения** **CursorLocation** равно **adUseClient** функция GetNewConnection (как показано ниже), который указывает на использование курсор клиента. Дополнительные сведения о различиях между клиентские и серверные курсоры можно [главы 8: Общее представление о курсоры и блокировки](chapter-8-understanding-cursors-and-locks.md).

Настройка **adUseClient** свойства **CursorLocation** перемещает позиции курсора из источника данных (SQL Server, в данном случае) расположение кода клиента (рабочего стола рабочей станции). Этот параметр принудительно ADO для вызова модуля курсор клиента для OLE DB на стороне клиента для создания и управления курсора.

Вы могли также заметить, что параметр **LockType для** метода **Open** изменено на **adLockBatchOptimistic**. Откроется курсор в пакетном режиме. (Поставщик кэширует несколько изменений и записывает их в источнике данных только при вызове метода **UpdateBatch** .) Изменения, внесенные в **набор записей** в базе данных не будут обновляться, пока не будет вызван метод **UpdateBatch** .

Наконец код, приведенный в этой главе используется измененная версия GetNewConnection функции, введенные в Глава 2. Данная версия функции теперь возвращает указатель со стороны клиента. Функция выглядит следующим образом:

```vb 
 
'BeginNewConnection 
Public Function GetNewConnection() As ADODB.Connection 
 Dim objConn1 As ADODB.Connection 
 Set objConn1 = New ADODB.Connection 
 
 strConnStr = "Provider=SQLOLEDB;Initial Catalog=Northwind;" & _ 
 "Data Source=MySrvr;Integrated Security=SSPI;" 
 
 objConn1.ConnectionString = strConnStr 
 objConn1.CursorLocation = adUseClient 
 objConn1.Open 
 
 Set GetNewConnection = objConn1 
End Function 
'EndNewConnection 
```

