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
# <a name="chapter-4-editing-data"></a><span data-ttu-id="0eb12-102">Глава 4. Редактирование данных</span><span class="sxs-lookup"><span data-stu-id="0eb12-102">Chapter 4: Editing data</span></span>

<span data-ttu-id="0eb12-103">**Область применения**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="0eb12-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="0eb12-104">В предыдущих двух главах объяснялись, как использовать ADO для подключения к источнику данных, выполнения команды, получения результатов в **объекте Recordset** и навигации в **recordset**.</span><span class="sxs-lookup"><span data-stu-id="0eb12-104">The preceding two chapters explained how use ADO to connect to a data source, execute a command, get the results in a **Recordset** object, and navigate within the **Recordset**.</span></span> <span data-ttu-id="0eb12-105">В этой главе основное внимание уделяется следующей фундаментальной операции ADO: редактированию данных.</span><span class="sxs-lookup"><span data-stu-id="0eb12-105">This chapter focuses on the next fundamental ADO operation: editing data.</span></span>

<span data-ttu-id="0eb12-106">В этой главе по-прежнему используется пример **Набор записей,** введенный в главе 3, с одним важным изменением.</span><span class="sxs-lookup"><span data-stu-id="0eb12-106">This chapter continues to use the sample **Recordset** introduced in Chapter 3 — with one important change.</span></span> <span data-ttu-id="0eb12-107">Для открытия наборов записей используется следующий **код:**</span><span class="sxs-lookup"><span data-stu-id="0eb12-107">The following code is used to open the **Recordset**:</span></span>

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

<span data-ttu-id="0eb12-108">Важное изменение кода включает  в себя установку свойства **CursorLocation** объекта Подключения, равное **adUseClient** в функции GetNewConnection (показано ниже), что указывает на использование курсора клиента.</span><span class="sxs-lookup"><span data-stu-id="0eb12-108">The important change to the code involves setting the **Connection** object's **CursorLocation** property equal to **adUseClient** in the GetNewConnection function (shown below), which indicates the use of a client cursor.</span></span> <span data-ttu-id="0eb12-109">Дополнительные сведения о различиях между курсорами на стороне клиента и сервера см. в главе [8. Понимание курсоров и блокировки.](chapter-8-understanding-cursors-and-locks.md)</span><span class="sxs-lookup"><span data-stu-id="0eb12-109">For more information about the differences between client-side and server-side cursors, see [Chapter 8: Understanding Cursors and Locks](chapter-8-understanding-cursors-and-locks.md).</span></span>

<span data-ttu-id="0eb12-110">Параметр **adUseClient** свойства **CursorLocation** перемещает расположение курсора из источника данных (в данном случае SQL Server) в расположение клиентского кода (рабочей станции рабочего стола).</span><span class="sxs-lookup"><span data-stu-id="0eb12-110">The **CursorLocation** property's **adUseClient** setting moves the location of the cursor from the data source (the SQL Server, in this case) to the location of the client code (the desktop workstation).</span></span> <span data-ttu-id="0eb12-111">Этот параметр заставляет ADO вызывать клиентский cursor Engine для OLE DB для клиента для создания и управления курсором.</span><span class="sxs-lookup"><span data-stu-id="0eb12-111">This setting forces ADO to invoke the Client Cursor Engine for OLE DB on the client in order to create and manage the cursor.</span></span>

<span data-ttu-id="0eb12-112">Возможно, вы также заметили, что параметр **LockType** метода **Open** изменен на **adLockBatchOptimistic**.</span><span class="sxs-lookup"><span data-stu-id="0eb12-112">You might also have noticed that the **LockType** parameter of the **Open** method changed to **adLockBatchOptimistic**.</span></span> <span data-ttu-id="0eb12-113">Это открывает курсор в пакетном режиме.</span><span class="sxs-lookup"><span data-stu-id="0eb12-113">This opens the cursor in batch mode.</span></span> <span data-ttu-id="0eb12-114">(Поставщик записывает несколько изменений и записывает их в исходный источник данных только при вызове метода **UpdateBatch.)** Изменения, внесенные в **Набор записей,** не будут обновляться в базе данных до тех пор, пока не будет вызван метод **UpdateBatch.**</span><span class="sxs-lookup"><span data-stu-id="0eb12-114">(The provider caches multiple changes and writes them to the underlying data source only when you call the **UpdateBatch** method.) Changes made to the **Recordset** will not be updated in the database until the **UpdateBatch** method is called.</span></span>

<span data-ttu-id="0eb12-115">Наконец, код в этой главе использует измененную версию функции GetNewConnection, представленную в главе 2.</span><span class="sxs-lookup"><span data-stu-id="0eb12-115">Finally, the code in this chapter uses a modified version of the GetNewConnection function, introduced in Chapter 2.</span></span> <span data-ttu-id="0eb12-116">Эта версия функции возвращает курсор на стороне клиента.</span><span class="sxs-lookup"><span data-stu-id="0eb12-116">This version of the function now returns a client-side cursor.</span></span> <span data-ttu-id="0eb12-117">Функция выглядит так:</span><span class="sxs-lookup"><span data-stu-id="0eb12-117">The function looks like this:</span></span>

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

<span data-ttu-id="0eb12-118">В этой главе освещают следующие темы:</span><span class="sxs-lookup"><span data-stu-id="0eb12-118">This chapter covers the following topics:</span></span>

- [<span data-ttu-id="0eb12-119">Редактирование существующих записей</span><span class="sxs-lookup"><span data-stu-id="0eb12-119">Editing existing records</span></span>](editing-existing-records.md)
- [<span data-ttu-id="0eb12-120">Определение поддерживаемых возможностей</span><span class="sxs-lookup"><span data-stu-id="0eb12-120">Determining what is supported</span></span>](determining-what-is-supported.md)
- [<span data-ttu-id="0eb12-121">Удаление записей с помощью метода Delete</span><span class="sxs-lookup"><span data-stu-id="0eb12-121">Deleting records using the Delete method</span></span>](deleting-records-using-the-delete-method.md)
- [<span data-ttu-id="0eb12-122">Альтернативы: использование SQL отчетов</span><span class="sxs-lookup"><span data-stu-id="0eb12-122">Alternatives: using SQL statements</span></span>](alternatives-using-sql-statements.md)
- [<span data-ttu-id="0eb12-123">Добавление записей (ADO)</span><span class="sxs-lookup"><span data-stu-id="0eb12-123">Adding records (ADO)</span></span>](adding-records.md)
