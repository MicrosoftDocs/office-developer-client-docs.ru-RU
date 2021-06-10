---
title: Глава 4. Редактирование данных
TOCTitle: 'Chapter 4: Editing data'
ms:assetid: 822b7365-0926-6411-6fb4-30de032570f8
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249563(v=office.15)
ms:contentKeyID: 48545974
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: b954cf8b730a74fb7e630fbafb96c046491c6f46
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32296439"
---
# <a name="chapter-4-editing-data"></a>Глава 4. Редактирование данных

**Область применения**: Access 2013, Office 2013

В предыдущих двух главах объяснялись, как использовать ADO для подключения к источнику данных, выполнения команды, получения результатов в **объекте Recordset** и навигации в **recordset**. В этой главе основное внимание уделяется следующей фундаментальной операции ADO: редактированию данных.

В этой главе по-прежнему используется пример **Набор записей,** введенный в главе 3, с одним важным изменением. Для открытия наборов записей используется следующий **код:**

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

Важное изменение кода включает  в себя установку свойства **CursorLocation** объекта Подключения, равное **adUseClient** в функции GetNewConnection (показано ниже), что указывает на использование курсора клиента. Дополнительные сведения о различиях между курсорами на стороне клиента и сервера см. в главе [8. Понимание курсоров и блокировки.](chapter-8-understanding-cursors-and-locks.md)

Параметр **adUseClient** свойства **CursorLocation** перемещает расположение курсора из источника данных (в данном случае SQL Server) в расположение клиентского кода (рабочей станции рабочего стола). Этот параметр заставляет ADO вызывать клиентский cursor Engine для OLE DB для клиента для создания и управления курсором.

Возможно, вы также заметили, что параметр **LockType** метода **Open** изменен на **adLockBatchOptimistic**. Это открывает курсор в пакетном режиме. (Поставщик записывает несколько изменений и записывает их в исходный источник данных только при вызове метода **UpdateBatch.)** Изменения, внесенные в **Набор записей,** не будут обновляться в базе данных до тех пор, пока не будет вызван метод **UpdateBatch.**

Наконец, код в этой главе использует измененную версию функции GetNewConnection, представленную в главе 2. Эта версия функции возвращает курсор на стороне клиента. Функция выглядит так:

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

В этой главе освещают следующие темы:

- [Редактирование существующих записей](editing-existing-records.md)
- [Определение поддерживаемых возможностей](determining-what-is-supported.md)
- [Удаление записей с помощью метода Delete](deleting-records-using-the-delete-method.md)
- [Альтернативы: использование SQL отчетов](alternatives-using-sql-statements.md)
- [Добавление записей (ADO)](adding-records.md)
