---
title: Глава 4. Редактирование данных
TOCTitle: 'Chapter 4: Editing Data'
ms:assetid: 822b7365-0926-6411-6fb4-30de032570f8
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249563(v=office.15)
ms:contentKeyID: 48545974
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: a484cef1e04ce84c30d823a2ac7783008651e77d
ms.sourcegitcommit: c557bbcccf37a6011f89aae1ddd399dfe549d087
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/31/2018
ms.locfileid: "25875793"
---
# <a name="chapter-4-editing-data"></a><span data-ttu-id="ef46b-102">Глава 4. Редактирование данных</span><span class="sxs-lookup"><span data-stu-id="ef46b-102">Chapter 4: Editing Data</span></span>


<span data-ttu-id="ef46b-103">**Применимо к**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="ef46b-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="ef46b-104">Предыдущая двух частях, как описано использование ADO для подключения к источнику данных, выполнения команды, получение результатов в объект **набора записей** и перейдите в рамках **набора записей**.</span><span class="sxs-lookup"><span data-stu-id="ef46b-104">The preceding two chapters explained how use ADO to connect to a data source, execute a command, get the results in a **Recordset** object, and navigate within the **Recordset**.</span></span> <span data-ttu-id="ef46b-105">Эта глава посвящена следующей базовые операции ADO: изменение данных.</span><span class="sxs-lookup"><span data-stu-id="ef46b-105">This chapter focuses on the next fundamental ADO operation: editing data.</span></span>

<span data-ttu-id="ef46b-106">В этой главе по-прежнему производится при использовании образца **набора записей** , введенные в Глава 3 — с помощью одного важное изменение.</span><span class="sxs-lookup"><span data-stu-id="ef46b-106">This chapter continues to use the sample **Recordset** introduced in Chapter 3 — with one important change.</span></span> <span data-ttu-id="ef46b-107">Следующий код используется для открытия **набора записей**:</span><span class="sxs-lookup"><span data-stu-id="ef46b-107">The following code is used to open the **Recordset**:</span></span>

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

<span data-ttu-id="ef46b-108">Важные изменения в код включает в себя свойства объект **подключения** **CursorLocation** равно **adUseClient** функция GetNewConnection (как показано ниже), который указывает на использование курсор клиента.</span><span class="sxs-lookup"><span data-stu-id="ef46b-108">The important change to the code involves setting the **Connection** object's **CursorLocation** property equal to **adUseClient** in the GetNewConnection function (shown below), which indicates the use of a client cursor.</span></span> <span data-ttu-id="ef46b-109">Дополнительные сведения о различиях между клиентские и серверные курсоры можно [главы 8: Общее представление о курсоры и блокировки](chapter-8-understanding-cursors-and-locks.md).</span><span class="sxs-lookup"><span data-stu-id="ef46b-109">For more information about the differences between client-side and server-side cursors, see [Chapter 8: Understanding Cursors and Locks](chapter-8-understanding-cursors-and-locks.md).</span></span>

<span data-ttu-id="ef46b-110">Настройка **adUseClient** свойства **CursorLocation** перемещает позиции курсора из источника данных (SQL Server, в данном случае) расположение кода клиента (рабочего стола рабочей станции).</span><span class="sxs-lookup"><span data-stu-id="ef46b-110">The **CursorLocation** property's **adUseClient** setting moves the location of the cursor from the data source (the SQL Server, in this case) to the location of the client code (the desktop workstation).</span></span> <span data-ttu-id="ef46b-111">Этот параметр принудительно ADO для вызова модуля курсор клиента для OLE DB на стороне клиента для создания и управления курсора.</span><span class="sxs-lookup"><span data-stu-id="ef46b-111">This setting forces ADO to invoke the Client Cursor Engine for OLE DB on the client in order to create and manage the cursor.</span></span>

<span data-ttu-id="ef46b-112">Вы могли также заметить, что параметр **LockType для** метода **Open** изменено на **adLockBatchOptimistic**.</span><span class="sxs-lookup"><span data-stu-id="ef46b-112">You might also have noticed that the **LockType** parameter of the **Open** method changed to **adLockBatchOptimistic**.</span></span> <span data-ttu-id="ef46b-113">Откроется курсор в пакетном режиме.</span><span class="sxs-lookup"><span data-stu-id="ef46b-113">This opens the cursor in batch mode.</span></span> <span data-ttu-id="ef46b-114">(Поставщик кэширует несколько изменений и записывает их в источнике данных только при вызове метода **UpdateBatch** .) Изменения, внесенные в **набор записей** в базе данных не будут обновляться, пока не будет вызван метод **UpdateBatch** .</span><span class="sxs-lookup"><span data-stu-id="ef46b-114">(The provider caches multiple changes and writes them to the underlying data source only when you call the **UpdateBatch** method.) Changes made to the **Recordset** will not be updated in the database until the **UpdateBatch** method is called.</span></span>

<span data-ttu-id="ef46b-115">Наконец код, приведенный в этой главе используется измененная версия GetNewConnection функции, введенные в Глава 2.</span><span class="sxs-lookup"><span data-stu-id="ef46b-115">Finally, the code in this chapter uses a modified version of the GetNewConnection function, introduced in Chapter 2.</span></span> <span data-ttu-id="ef46b-116">Данная версия функции теперь возвращает указатель со стороны клиента.</span><span class="sxs-lookup"><span data-stu-id="ef46b-116">This version of the function now returns a client-side cursor.</span></span> <span data-ttu-id="ef46b-117">Функция выглядит следующим образом:</span><span class="sxs-lookup"><span data-stu-id="ef46b-117">The function looks like this:</span></span>

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

<span data-ttu-id="ef46b-118">В этой главе рассматриваются следующие темы:</span><span class="sxs-lookup"><span data-stu-id="ef46b-118">This chapter covers the following topics:</span></span>

- [<span data-ttu-id="ef46b-119">Редактирование существующих записей</span><span class="sxs-lookup"><span data-stu-id="ef46b-119">Editing Existing Records</span></span>](editing-existing-records.md)

- [<span data-ttu-id="ef46b-120">Определение поддерживаемых возможностей</span><span class="sxs-lookup"><span data-stu-id="ef46b-120">Determining What is Supported</span></span>](determining-what-is-supported.md)

- [<span data-ttu-id="ef46b-121">Удаление записей с помощью метода Delete</span><span class="sxs-lookup"><span data-stu-id="ef46b-121">Deleting Records Using the Delete Method</span></span>](deleting-records-using-the-delete-method.md)

- [<span data-ttu-id="ef46b-122">Альтернативы: использование операторов SQL</span><span class="sxs-lookup"><span data-stu-id="ef46b-122">Alternatives: Using SQL Statements</span></span>](alternatives-using-sql-statements.md)

- [<span data-ttu-id="ef46b-123">Adding Records (ADO)</span><span class="sxs-lookup"><span data-stu-id="ef46b-123">Adding Records (ADO)</span></span>](adding-records.md)