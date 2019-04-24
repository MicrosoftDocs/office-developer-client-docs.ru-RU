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

В предыдущих главах поясняется, как использовать ADO для подключения к источнику данных, выполнения команды, получения результатов в объекте **Recordset** и перехода в пределах **набора записей**. В этой главе рассказывается о следующей фундаментальной операции ADO: Редактирование данных.

В этой главе показано, как использовать пример **набора записей** , представленный в главе 3, с одним существенным изменением. Для открытия объекта **Recordset**используется следующий код:

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

Важное изменение кода заключается в установке свойства **CursorLocation** объекта **Connection** равным **адусеклиент** в функции жетневконнектион (показанной ниже), которая указывает на использование клиентского курсора. Дополнительные сведения о различиях между клиентскими и серверными курсорами приведены в [главе 8: Общие сведения о курсорах и блокировках](chapter-8-understanding-cursors-and-locks.md).

Параметр **адусеклиент** свойства **CursorLocation** перемещает расположение курсора из источника данных (в данном случае — SQL Server) в расположение клиентского кода (настольной рабочей станции). Этот параметр заставляет ADO вызывать модуль клиентского курсора для OLE DB на клиенте для создания курсора и управления им.

Вы также можете заметить, что параметр **LockType** метода **Open** изменился на **адлоккбатчоптимистик**. Курсор откроется в пакетном режиме. (Поставщик кэширует несколько изменений и записывает их в базовый источник данных только при вызове метода **UpdateBatch** .) Изменения, внесенные в **набор записей** , не будут обновлены в базе данных, пока не будет вызван метод **UpdateBatch** .

Наконец, код в этой главе использует модифицированную версию функции Жетневконнектион, которая приведена в главе 2. Теперь эта версия функции возвращает курсор на стороне клиента. Функция выглядит следующим образом:

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

В этой главе рассматриваются следующие темы:

- [Редактирование существующих записей](editing-existing-records.md)
- [Определение поддерживаемых возможностей](determining-what-is-supported.md)
- [Удаление записей с помощью метода Delete](deleting-records-using-the-delete-method.md)
- [Альтернативы: использование операторов SQL](alternatives-using-sql-statements.md)
- [Добавление записей (ADO)](adding-records.md)
