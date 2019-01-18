---
title: Метод Workspace.CommitTrans (DAO)
TOCTitle: CommitTrans Method
ms:assetid: e6d129fb-a578-5c79-9c16-6444519f0daf
ms:mtpsurl: https://msdn.microsoft.com/library/Ff835985(v=office.15)
ms:contentKeyID: 48548391
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: 52af229f03b7ea10510f3e580ba2c4e12784e461
ms.sourcegitcommit: d6695c94415fa47952ee7961a69660abc0904434
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/17/2019
ms.locfileid: "28712325"
---
# <a name="workspacecommittrans-method-dao"></a><span data-ttu-id="d6e0f-102">Метод Workspace.CommitTrans (DAO)</span><span class="sxs-lookup"><span data-stu-id="d6e0f-102">Workspace.CommitTrans method (DAO)</span></span>

<span data-ttu-id="d6e0f-103">**Применимо к**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="d6e0f-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="d6e0f-104">Завершает текущий транзакций и сохраняет изменения.</span><span class="sxs-lookup"><span data-stu-id="d6e0f-104">Ends the current transaction and saves the changes.</span></span>

## <a name="syntax"></a><span data-ttu-id="d6e0f-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="d6e0f-105">Syntax</span></span>

<span data-ttu-id="d6e0f-106">*выражение* . CommitTrans (***Параметры***)</span><span class="sxs-lookup"><span data-stu-id="d6e0f-106">*expression* .CommitTrans(***Options***)</span></span>

<span data-ttu-id="d6e0f-107">*выражение* Переменная, которая представляет собой объект- **рабочей области** .</span><span class="sxs-lookup"><span data-stu-id="d6e0f-107">*expression* A variable that represents a **Workspace** object.</span></span>

## <a name="parameters"></a><span data-ttu-id="d6e0f-108">Параметры</span><span class="sxs-lookup"><span data-stu-id="d6e0f-108">Parameters</span></span>

<table>
<colgroup>
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="d6e0f-109">Имя</span><span class="sxs-lookup"><span data-stu-id="d6e0f-109">Name</span></span></p></th>
<th><p><span data-ttu-id="d6e0f-110">Обязательный или необязательный</span><span class="sxs-lookup"><span data-stu-id="d6e0f-110">Required/optional</span></span></p></th>
<th><p><span data-ttu-id="d6e0f-111">Тип данных</span><span class="sxs-lookup"><span data-stu-id="d6e0f-111">Data type</span></span></p></th>
<th><p><span data-ttu-id="d6e0f-112">Описание</span><span class="sxs-lookup"><span data-stu-id="d6e0f-112">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="d6e0f-113"><em>Option</em></span><span class="sxs-lookup"><span data-stu-id="d6e0f-113"><em>Option</em></span></span></p></td>
<td><p><span data-ttu-id="d6e0f-114">Необязательный</span><span class="sxs-lookup"><span data-stu-id="d6e0f-114">Optional</span></span></p></td>
<td><p><span data-ttu-id="d6e0f-115"><strong>Long</strong></span><span class="sxs-lookup"><span data-stu-id="d6e0f-115"><strong>Long</strong></span></span></p></td>
<td><p><span data-ttu-id="d6e0f-116">В рабочей области для Microsoft Access можно включить константы <strong>dbForceOSFlush</strong> с <strong>CommitTrans</strong>.</span><span class="sxs-lookup"><span data-stu-id="d6e0f-116">In a Microsoft Access workspace, you can include the <strong>dbForceOSFlush</strong> constant with <strong>CommitTrans</strong>.</span></span> <span data-ttu-id="d6e0f-117">Это заставляет СУБД немедленно очистить все обновления на диске, вместо кэширование их временно.</span><span class="sxs-lookup"><span data-stu-id="d6e0f-117">This forces the database engine to immediately flush all updates to disk, instead of caching them temporarily.</span></span> <span data-ttu-id="d6e0f-118">Без этого параметра, пользователь может get управления обратно сразу же после программа приложение вызывает <strong>CommitTrans</strong>включить компьютере отключена и не обновлять данные записываются на диск.</span><span class="sxs-lookup"><span data-stu-id="d6e0f-118">Without using this option, a user could get control back immediately after the application program calls <strong>CommitTrans</strong>, turn the computer off, and not have the data written to disk.</span></span> <span data-ttu-id="d6e0f-119">При использовании этого параметра может повлиять на производительность приложения, будет полезно в ситуациях, где компьютер может отключен перед кэшированные обновления сохраняются на диске.</span><span class="sxs-lookup"><span data-stu-id="d6e0f-119">While using this option may affect your application's performance, it is useful in situations where the computer could be shut off before cached updates are saved to disk.</span></span></p></td>
</tr>
</tbody>
</table>


## <a name="remarks"></a><span data-ttu-id="d6e0f-120">Замечания</span><span class="sxs-lookup"><span data-stu-id="d6e0f-120">Remarks</span></span>

<span data-ttu-id="d6e0f-121">Методы транзакции **BeginTrans** **CommitTrans**и **отката** управление обработки во время сеанса, определенные с помощью объекта **рабочей области** транзакций.</span><span class="sxs-lookup"><span data-stu-id="d6e0f-121">The transaction methods **BeginTrans**, **CommitTrans**, and **Rollback** manage transaction processing during a session defined by a **Workspace** object.</span></span> <span data-ttu-id="d6e0f-122">Вы можете использовать эти методы с объектом **рабочей области** , когда необходимо рассматривать ряд изменений, внесенных в базы данных в сеансе как одно целое.</span><span class="sxs-lookup"><span data-stu-id="d6e0f-122">You use these methods with a **Workspace** object when you want to treat a series of changes made to the databases in a session as one unit.</span></span>

<span data-ttu-id="d6e0f-123">Как правило использование транзакций для обеспечения целостности данных при необходимо выполнить оба обновления записей в двух или нескольких таблиц и убедитесь, что изменения выполнены (зафиксировано) на все таблицы или нет для всех (откат).</span><span class="sxs-lookup"><span data-stu-id="d6e0f-123">Typically, you use transactions to maintain the integrity of your data when you must both update records in two or more tables and ensure changes are completed (committed) in all tables or none at all (rolled back).</span></span> <span data-ttu-id="d6e0f-124">Например при перемещении деньги из одной учетной записи в другую могут вычесть сумму из одного и добавить сумму в другой.</span><span class="sxs-lookup"><span data-stu-id="d6e0f-124">For example, if you transfer money from one account to another, you might subtract an amount from one and add the amount to another.</span></span> <span data-ttu-id="d6e0f-125">Если либо обновить возникает ошибка, больше не сбалансировать учетные записи.</span><span class="sxs-lookup"><span data-stu-id="d6e0f-125">If either update fails, the accounts no longer balance.</span></span> <span data-ttu-id="d6e0f-126">Используйте метод **BeginTrans** перед обновлением первой записи, и затем, в случае все последующие обновления, можно использовать метод **отката** для отмены всех обновлений.</span><span class="sxs-lookup"><span data-stu-id="d6e0f-126">Use the **BeginTrans** method before updating the first record, and then, if any subsequent update fails, you can use the **Rollback** method to undo all of the updates.</span></span> <span data-ttu-id="d6e0f-127">Используйте метод **CommitTrans** после успешного обновления последней записи.</span><span class="sxs-lookup"><span data-stu-id="d6e0f-127">Use the **CommitTrans** method after you successfully update the last record.</span></span>

> [!NOTE]
> <span data-ttu-id="d6e0f-128">В рамках одного объекта **рабочей области** транзакции всегда являются глобальными для **рабочей области** и не ограничиваются ими только одно **подключение** или объект **базы данных** .</span><span class="sxs-lookup"><span data-stu-id="d6e0f-128">Within one **Workspace** object, transactions are always global to the **Workspace** and aren't limited to only one **Connection** or **Database** object.</span></span> <span data-ttu-id="d6e0f-129">При выполнении операций более одного подключения или базы данных в **рабочей области** транзакции разрешение транзакций (с использованием метода **CommitTrans** или **отката** ) влияет на все операции для всех баз данных и подключений в рабочей области.</span><span class="sxs-lookup"><span data-stu-id="d6e0f-129">If you perform operations on more than one connection or database within a **Workspace** transaction, resolving the transaction (that is, using the **CommitTrans** or **Rollback** method) affects all operations on all connections and databases within that workspace.</span></span>

<span data-ttu-id="d6e0f-130">После использования **CommitTrans**нельзя отменить изменения, внесенные во время транзакции, если только операции, вложенная в другую транзакцию, которая является самой откат.</span><span class="sxs-lookup"><span data-stu-id="d6e0f-130">After you use **CommitTrans**, you can't undo changes made during that transaction unless the transaction is nested within another transaction that is itself rolled back.</span></span> <span data-ttu-id="d6e0f-131">Если вложенные транзакции, необходимо устранить текущей операции можно устранить транзакций на высоком уровне вложения.</span><span class="sxs-lookup"><span data-stu-id="d6e0f-131">If you nest transactions, you must resolve the current transaction before you can resolve a transaction at a higher level of nesting.</span></span>

<span data-ttu-id="d6e0f-132">Если требуется предоставить одновременных операций с перекрывающимися, не вложенных областей, можно создать дополнительные объекты **рабочей области** для хранения одновременных операций.</span><span class="sxs-lookup"><span data-stu-id="d6e0f-132">If you want to have simultaneous transactions with overlapping, non-nested scopes, you can create additional **Workspace** objects to contain the concurrent transactions.</span></span>

<span data-ttu-id="d6e0f-133">Если объект **рабочей области для** закрытия без разрешения все отложенные транзакции, автоматически откат транзакций.</span><span class="sxs-lookup"><span data-stu-id="d6e0f-133">If you close a **Workspace** object without resolving any pending transactions, the transactions are automatically rolled back.</span></span>

<span data-ttu-id="d6e0f-134">Если вы используете **CommitTrans** или метод **отката** без использования метода **BeginTrans** , возникает ошибка.</span><span class="sxs-lookup"><span data-stu-id="d6e0f-134">If you use the **CommitTrans** or **Rollback** method without first using the **BeginTrans** method, an error occurs.</span></span>

<span data-ttu-id="d6e0f-135">Некоторые ISAM баз данных, используемых в рабочей области Microsoft Access могут не поддерживают транзакции, в противном случае свойство **транзакции** объекта **базы данных** или объекта **набора записей** имеет **значение False**.</span><span class="sxs-lookup"><span data-stu-id="d6e0f-135">Some ISAM databases used in a Microsoft Access workspace may not support transactions, in which case the **Transactions** property of the **Database** object or **Recordset** object is **False**.</span></span> <span data-ttu-id="d6e0f-136">Чтобы убедиться в том, что базы данных поддерживает транзакции, проверьте значение свойства **транзакции** объекта **базы данных** перед использованием метода **BeginTrans** .</span><span class="sxs-lookup"><span data-stu-id="d6e0f-136">To make sure the database supports transactions, check the value of the **Transactions** property of the **Database** object before using the **BeginTrans** method.</span></span> <span data-ttu-id="d6e0f-137">При использовании объекта **набора записей** на основе более одной базы данных проверьте свойство **транзакции** объекта **набора записей** .</span><span class="sxs-lookup"><span data-stu-id="d6e0f-137">If you are using a **Recordset** object based on more than one database, check the **Transactions** property of the **Recordset** object.</span></span> 

<span data-ttu-id="d6e0f-138">Если **набор записей** полностью основано на таблиц ядра базы данных Microsoft Access, всегда можно использовать транзакции.</span><span class="sxs-lookup"><span data-stu-id="d6e0f-138">If a **Recordset** is based entirely on Microsoft Access database engine tables, you can always use transactions.</span></span> <span data-ttu-id="d6e0f-139">Объекты **набора записей** на основе таблиц, созданных с другими продуктами баз данных, тем не менее, не поддерживает транзакции.</span><span class="sxs-lookup"><span data-stu-id="d6e0f-139">**Recordset** objects based on tables created by other database products, however, may not support transactions.</span></span> <span data-ttu-id="d6e0f-140">Например нельзя использовать транзакции в **набора записей** на основе таблицы Paradox.</span><span class="sxs-lookup"><span data-stu-id="d6e0f-140">For example, you can't use transactions in a **Recordset** based on a Paradox table.</span></span> <span data-ttu-id="d6e0f-141">В этом случае свойство **транзакции** имеет **значение False**.</span><span class="sxs-lookup"><span data-stu-id="d6e0f-141">In this case, the **Transactions** property is **False**.</span></span> <span data-ttu-id="d6e0f-142">Если **базы данных** или **набора записей** не поддерживает транзакции, игнорируются методы и ошибка не происходит.</span><span class="sxs-lookup"><span data-stu-id="d6e0f-142">If the **Database** or **Recordset** doesn't support transactions, the methods are ignored and no error occurs.</span></span>

<span data-ttu-id="d6e0f-143">При доступе к источникам данных ODBC через ядро базы данных Microsoft Access, вложенных транзакций невозможно.</span><span class="sxs-lookup"><span data-stu-id="d6e0f-143">You can't nest transactions if you are accessing ODBC data sources through the Microsoft Access database engine.</span></span>

<span data-ttu-id="d6e0f-144">В рабочих областях ODBC при использовании **CommitTrans** курсор может перестают быть допустимыми.</span><span class="sxs-lookup"><span data-stu-id="d6e0f-144">In ODBC workspaces, when you use **CommitTrans** your cursor may no longer be valid.</span></span> <span data-ttu-id="d6e0f-145">Используйте метод **повторный запрос** для просмотра изменений в **набор записей**, или закрыть и повторно открыть **набора записей**.</span><span class="sxs-lookup"><span data-stu-id="d6e0f-145">Use the **Requery** method to view the changes in the **Recordset**, or close and re-open the **Recordset**.</span></span>

> [!NOTE]
> - <span data-ttu-id="d6e0f-146">Часто можно повысить производительность приложения, устраняя операции, требующие доступа к диску на блоки транзакций.</span><span class="sxs-lookup"><span data-stu-id="d6e0f-146">You can often improve the performance of your application by breaking operations that require disk access into transaction blocks.</span></span> <span data-ttu-id="d6e0f-147">Это буферов операции, а также может значительно сократить количество отправок диску.</span><span class="sxs-lookup"><span data-stu-id="d6e0f-147">This buffers your operations and may significantly reduce the number of times a disk is accessed.</span></span>
> - <span data-ttu-id="d6e0f-148">В рабочей области Microsoft Access операций записи в файл, сохраняются в папке, указанной в переменной среды TEMP на рабочей станции.</span><span class="sxs-lookup"><span data-stu-id="d6e0f-148">In a Microsoft Access workspace, transactions are logged in a file kept in the directory specified by the TEMP environment variable on the workstation.</span></span> <span data-ttu-id="d6e0f-149">Если файл журнала транзакций выполнит доступные хранилища на диске временных файлов, компонент database engine вызывает ошибку времени выполнения.</span><span class="sxs-lookup"><span data-stu-id="d6e0f-149">If the transaction log file exhausts the available storage on your TEMP drive, the database engine triggers a run-time error.</span></span> <span data-ttu-id="d6e0f-150">На этом этапе при использовании **CommitTrans**количестве операций фиксируются, но оставшиеся незавершенных операций не сохраняются, и операция должна быть перезапущена.</span><span class="sxs-lookup"><span data-stu-id="d6e0f-150">At this point, if you use **CommitTrans**, an indeterminate number of operations are committed, but the remaining uncompleted operations are lost, and the operation has to be restarted.</span></span> <span data-ttu-id="d6e0f-151">С помощью метода **отката** освобождает журнала транзакций и выполняет откат всех операций в транзакции.</span><span class="sxs-lookup"><span data-stu-id="d6e0f-151">Using a **Rollback** method releases the transaction log and rolls back all operations in the transaction.</span></span>
> - <span data-ttu-id="d6e0f-152">Закрытие клонированной **записей** в ожидающие транзакции будет отображено неявные операции **отката** .</span><span class="sxs-lookup"><span data-stu-id="d6e0f-152">Closing a clone **Recordset** within a pending transaction will cause an implicit **Rollback** operation.</span></span>

## <a name="example"></a><span data-ttu-id="d6e0f-153">Пример</span><span class="sxs-lookup"><span data-stu-id="d6e0f-153">Example</span></span>

<span data-ttu-id="d6e0f-154">Следующем примере показано, как использовать транзакции в рабочую область для объектов доступа к данным (DAO).</span><span class="sxs-lookup"><span data-stu-id="d6e0f-154">The following example shows how to use a transaction in a Data Access Objects (DAO) workspace.</span></span>

<span data-ttu-id="d6e0f-155">**Пример кода предоставлен** [Справочник программиста Microsoft Access 2010](https://www.amazon.com/Microsoft-Access-2010-Programmers-Reference/dp/8126528125).</span><span class="sxs-lookup"><span data-stu-id="d6e0f-155">**Sample code provided by** the [Microsoft Access 2010 Programmer’s Reference](https://www.amazon.com/Microsoft-Access-2010-Programmers-Reference/dp/8126528125).</span></span>


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
