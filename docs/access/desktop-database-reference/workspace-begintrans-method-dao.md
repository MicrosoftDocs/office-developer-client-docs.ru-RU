---
title: Workspace.BeginTrans Method (DAO)
TOCTitle: BeginTrans Method
ms:assetid: aa7c3bf8-fb08-9360-5998-4bf3f721ecbb
ms:mtpsurl: https://msdn.microsoft.com/library/Ff821457(v=office.15)
ms:contentKeyID: 48546948
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 850868a3a5d9dd0cfda2b2f365e05004fc4b2ffd
ms.sourcegitcommit: c557bbcccf37a6011f89aae1ddd399dfe549d087
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/31/2018
ms.locfileid: "25872626"
---
# <a name="workspacebegintrans-method-dao"></a><span data-ttu-id="00135-102">Workspace.BeginTrans Method (DAO)</span><span class="sxs-lookup"><span data-stu-id="00135-102">Workspace.BeginTrans Method (DAO)</span></span>

<span data-ttu-id="00135-103">**Применимо к**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="00135-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="00135-104">Начало новой транзакции.</span><span class="sxs-lookup"><span data-stu-id="00135-104">Begins a new transaction.</span></span> <span data-ttu-id="00135-105">Чтение и запись **базы данных**.</span><span class="sxs-lookup"><span data-stu-id="00135-105">Read/write **Database**.</span></span>

## <a name="syntax"></a><span data-ttu-id="00135-106">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="00135-106">Syntax</span></span>

<span data-ttu-id="00135-107">*выражение* . BeginTrans</span><span class="sxs-lookup"><span data-stu-id="00135-107">*expression* .BeginTrans</span></span>

<span data-ttu-id="00135-108">*выражение* Переменная, которая представляет собой объект- **рабочей области** .</span><span class="sxs-lookup"><span data-stu-id="00135-108">*expression* A variable that represents a **Workspace** object.</span></span>

## <a name="remarks"></a><span data-ttu-id="00135-109">Замечания</span><span class="sxs-lookup"><span data-stu-id="00135-109">Remarks</span></span>

<span data-ttu-id="00135-110">Методы транзакции **BeginTrans** **CommitTrans**и **отката** управление обработки во время сеанса, определенные с помощью объекта **рабочей области** транзакций.</span><span class="sxs-lookup"><span data-stu-id="00135-110">The transaction methods **BeginTrans**, **CommitTrans**, and **Rollback** manage transaction processing during a session defined by a **Workspace** object.</span></span> <span data-ttu-id="00135-111">Вы можете использовать эти методы с объектом **рабочей области** , когда необходимо рассматривать ряд изменений, внесенных в базы данных в сеансе как одно целое.</span><span class="sxs-lookup"><span data-stu-id="00135-111">You use these methods with a **Workspace** object when you want to treat a series of changes made to the databases in a session as one unit.</span></span>

<span data-ttu-id="00135-112">Как правило использование транзакций для обеспечения целостности данных при необходимо выполнить оба обновления записей в двух или нескольких таблиц и убедитесь, что изменения выполнены (зафиксировано) на все таблицы или нет для всех (откат).</span><span class="sxs-lookup"><span data-stu-id="00135-112">Typically, you use transactions to maintain the integrity of your data when you must both update records in two or more tables and ensure changes are completed (committed) in all tables or none at all (rolled back).</span></span> <span data-ttu-id="00135-113">Например при перемещении деньги из одной учетной записи в другую могут вычесть сумму из одного и добавить сумму в другой.</span><span class="sxs-lookup"><span data-stu-id="00135-113">For example, if you transfer money from one account to another, you might subtract an amount from one and add the amount to another.</span></span> <span data-ttu-id="00135-114">Если либо обновить возникает ошибка, больше не сбалансировать учетные записи.</span><span class="sxs-lookup"><span data-stu-id="00135-114">If either update fails, the accounts no longer balance.</span></span> <span data-ttu-id="00135-115">Используйте метод **BeginTrans** перед обновлением первой записи, и затем, в случае все последующие обновления, можно использовать метод **отката** для отмены всех обновлений.</span><span class="sxs-lookup"><span data-stu-id="00135-115">Use the **BeginTrans** method before updating the first record, and then, if any subsequent update fails, you can use the **Rollback** method to undo all of the updates.</span></span> <span data-ttu-id="00135-116">Используйте метод **CommitTrans** после успешного обновления последней записи.</span><span class="sxs-lookup"><span data-stu-id="00135-116">Use the **CommitTrans** method after you successfully update the last record.</span></span>

> [!NOTE]
> <span data-ttu-id="00135-117">В рамках одного объекта **рабочей области** транзакции всегда являются глобальными для **рабочей области** и не ограничиваются ими только одно **подключение** или объект **базы данных** .</span><span class="sxs-lookup"><span data-stu-id="00135-117">Within one **Workspace** object, transactions are always global to the **Workspace** and aren't limited to only one **Connection** or **Database** object.</span></span> <span data-ttu-id="00135-118">При выполнении операций более одного подключения или базы данных в **рабочей области** транзакции разрешение транзакций (с использованием метода **CommitTrans** или **отката** ) влияет на все операции для всех баз данных и подключений в рабочей области.</span><span class="sxs-lookup"><span data-stu-id="00135-118">If you perform operations on more than one connection or database within a **Workspace** transaction, resolving the transaction (that is, using the **CommitTrans** or **Rollback** method) affects all operations on all connections and databases within that workspace.</span></span>

<span data-ttu-id="00135-119">После использования **CommitTrans**нельзя отменить изменения, внесенные во время транзакции, если только операции, вложенная в другую транзакцию, которая является самой откат.</span><span class="sxs-lookup"><span data-stu-id="00135-119">After you use **CommitTrans**, you can't undo changes made during that transaction unless the transaction is nested within another transaction that is itself rolled back.</span></span> <span data-ttu-id="00135-120">Если вложенные транзакции, необходимо устранить текущей операции можно устранить транзакций на высоком уровне вложения.</span><span class="sxs-lookup"><span data-stu-id="00135-120">If you nest transactions, you must resolve the current transaction before you can resolve a transaction at a higher level of nesting.</span></span>

<span data-ttu-id="00135-121">Если требуется предоставить одновременных операций с перекрывающимися, не вложенных областей, можно создать дополнительные объекты **рабочей области** для хранения одновременных операций.</span><span class="sxs-lookup"><span data-stu-id="00135-121">If you want to have simultaneous transactions with overlapping, non-nested scopes, you can create additional **Workspace** objects to contain the concurrent transactions.</span></span>

<span data-ttu-id="00135-122">Если объект **рабочей области для** закрытия без разрешения все отложенные транзакции, автоматически откат транзакций.</span><span class="sxs-lookup"><span data-stu-id="00135-122">If you close a **Workspace** object without resolving any pending transactions, the transactions are automatically rolled back.</span></span>

<span data-ttu-id="00135-123">Если вы используете **CommitTrans** или метод **отката** без использования метода **BeginTrans** , возникает ошибка.</span><span class="sxs-lookup"><span data-stu-id="00135-123">If you use the **CommitTrans** or **Rollback** method without first using the **BeginTrans** method, an error occurs.</span></span>

<span data-ttu-id="00135-124">Некоторые ISAM баз данных, используемых в рабочей области Microsoft Access могут не поддерживают транзакции, в противном случае свойство **транзакции** объекта **базы данных** или объекта **набора записей** имеет **значение False**.</span><span class="sxs-lookup"><span data-stu-id="00135-124">Some ISAM databases used in a Microsoft Access workspace may not support transactions, in which case the **Transactions** property of the **Database** object or **Recordset** object is **False**.</span></span> <span data-ttu-id="00135-125">Чтобы убедиться в том, что базы данных поддерживает транзакции, проверьте значение свойства **транзакции** объекта **базы данных** перед использованием метода **BeginTrans** .</span><span class="sxs-lookup"><span data-stu-id="00135-125">To make sure the database supports transactions, check the value of the **Transactions** property of the **Database** object before using the **BeginTrans** method.</span></span> <span data-ttu-id="00135-126">При использовании объекта **набора записей** на основе более одной базы данных проверьте свойство **транзакции** объекта **набора записей** .</span><span class="sxs-lookup"><span data-stu-id="00135-126">If you are using a **Recordset** object based on more than one database, check the **Transactions** property of the **Recordset** object.</span></span> 

<span data-ttu-id="00135-127">Если **набор записей** полностью основано на таблиц ядра базы данных Microsoft Access, всегда можно использовать транзакции.</span><span class="sxs-lookup"><span data-stu-id="00135-127">If a **Recordset** is based entirely on Microsoft Access database engine tables, you can always use transactions.</span></span> <span data-ttu-id="00135-128">Объекты **набора записей** на основе таблиц, созданных с другими продуктами баз данных, тем не менее, не поддерживает транзакции.</span><span class="sxs-lookup"><span data-stu-id="00135-128">**Recordset** objects based on tables created by other database products, however, may not support transactions.</span></span> <span data-ttu-id="00135-129">Например нельзя использовать транзакции в **набора записей** на основе таблицы Paradox.</span><span class="sxs-lookup"><span data-stu-id="00135-129">For example, you can't use transactions in a **Recordset** based on a Paradox table.</span></span> <span data-ttu-id="00135-130">В этом случае свойство **транзакции** имеет **значение False**.</span><span class="sxs-lookup"><span data-stu-id="00135-130">In this case, the **Transactions** property is **False**.</span></span> <span data-ttu-id="00135-131">Если **базы данных** или **набора записей** не поддерживает транзакции, игнорируются методы и ошибка не происходит.</span><span class="sxs-lookup"><span data-stu-id="00135-131">If the **Database** or **Recordset** doesn't support transactions, the methods are ignored and no error occurs.</span></span>

<span data-ttu-id="00135-132">При доступе к источникам данных ODBC через ядро базы данных Microsoft Access, вложенных транзакций невозможно.</span><span class="sxs-lookup"><span data-stu-id="00135-132">You can't nest transactions if you are accessing ODBC data sources through the Microsoft Access database engine.</span></span>

<span data-ttu-id="00135-133">В рабочих областях ODBC при использовании **CommitTrans** курсор может перестают быть допустимыми.</span><span class="sxs-lookup"><span data-stu-id="00135-133">In ODBC workspaces, when you use **CommitTrans** your cursor may no longer be valid.</span></span> <span data-ttu-id="00135-134">Используйте метод **повторный запрос** для просмотра изменений в **набор записей**, или закрыть и повторно открыть **набора записей**.</span><span class="sxs-lookup"><span data-stu-id="00135-134">Use the **Requery** method to view the changes in the **Recordset**, or close and re-open the **Recordset**.</span></span>

> [!NOTE]
> - <span data-ttu-id="00135-135">Часто можно повысить производительность приложения, устраняя операции, требующие доступа к диску на блоки транзакций.</span><span class="sxs-lookup"><span data-stu-id="00135-135">You can often improve the performance of your application by breaking operations that require disk access into transaction blocks.</span></span> <span data-ttu-id="00135-136">Это буферов операции, а также может значительно сократить количество отправок диску.</span><span class="sxs-lookup"><span data-stu-id="00135-136">This buffers your operations and may significantly reduce the number of times a disk is accessed.</span></span>
> - <span data-ttu-id="00135-137">В рабочей области Microsoft Access операций записи в файл, сохраняются в папке, указанной в переменной среды TEMP на рабочей станции.</span><span class="sxs-lookup"><span data-stu-id="00135-137">In a Microsoft Access workspace, transactions are logged in a file kept in the directory specified by the TEMP environment variable on the workstation.</span></span> <span data-ttu-id="00135-138">Если файл журнала транзакций выполнит доступные хранилища на диске временных файлов, компонент database engine вызывает ошибку времени выполнения.</span><span class="sxs-lookup"><span data-stu-id="00135-138">If the transaction log file exhausts the available storage on your TEMP drive, the database engine triggers a run-time error.</span></span> <span data-ttu-id="00135-139">На этом этапе при использовании **CommitTrans**количестве операций фиксируются, но оставшиеся незавершенных операций не сохраняются, и операция должна быть перезапущена.</span><span class="sxs-lookup"><span data-stu-id="00135-139">At this point, if you use **CommitTrans**, an indeterminate number of operations are committed, but the remaining uncompleted operations are lost, and the operation has to be restarted.</span></span> <span data-ttu-id="00135-140">С помощью метода **отката** освобождает журнала транзакций и выполняет откат всех операций в транзакции.</span><span class="sxs-lookup"><span data-stu-id="00135-140">Using a **Rollback** method releases the transaction log and rolls back all operations in the transaction.</span></span>
> - <span data-ttu-id="00135-141">Закрытие клонированной **записей** в ожидающие транзакции будет отображено неявные операции **отката** .</span><span class="sxs-lookup"><span data-stu-id="00135-141">Closing a clone **Recordset** within a pending transaction will cause an implicit **Rollback** operation.</span></span>

## <a name="example"></a><span data-ttu-id="00135-142">Пример</span><span class="sxs-lookup"><span data-stu-id="00135-142">Example</span></span>

<span data-ttu-id="00135-143">Следующем примере показано, как использовать транзакции в рабочую область для объектов доступа к данным (DAO).</span><span class="sxs-lookup"><span data-stu-id="00135-143">The following example shows how to use a transaction in a Data Access Objects (DAO) workspace.</span></span>

<span data-ttu-id="00135-144">**Пример кода предоставлен** [Справочник программиста Microsoft Access 2010](https://www.amazon.com/Microsoft-Access-2010-Programmers-Reference/dp/8126528125).</span><span class="sxs-lookup"><span data-stu-id="00135-144">**Sample code provided by** the [Microsoft Access 2010 Programmer’s Reference](https://www.amazon.com/Microsoft-Access-2010-Programmers-Reference/dp/8126528125).</span></span>

```vb
    Public Sub TransferFunds()
        Dim wrk As DAO.Workspace
        Dim dbC As DAO.Database
        Dim dbX As DAO.Database
        
        Set wrk = DBEngine(0)
        Set dbC = CurrentDb
        Set dbX = wrk.OpenDatabase("e:\books\acc2007vba\myDB.accdb")
        
        On Error GoTo trans_Err
        
        'Begin the transaction
        
        wrk.BeginTrans
        
        'Withdraw funds from one account table
        dbC.Execute "INSERT INTO tblAccounts ( Amount, Txn, TxnDate ) SELECT -20, 'DEBIT', Date()", dbFailOnError
    
        'Deposit funds into another account table
        dbX.Execute "INSERT INTO tblAccounts ( Amount, Txn, TxnDate ) SELECT 20, 'CREDIT', Date()", dbFailOnError
        
        'Commit the transaction
        wrk.CommitTrans dbForceOSFlush
        
    trans_Exit:
        'Clean up
        wrk.Close
        Set dbC = Nothing
        Set dbX = Nothing
        Set wrk = Nothing
        Exit Sub
        
    trans_Err:
        'Roll back the transaction
        wrk.Rollback
        Resume trans_Exit
        
    End Sub
```
