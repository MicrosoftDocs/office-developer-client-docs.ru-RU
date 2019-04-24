---
title: Метод Workspace. CommitTrans (DAO)
TOCTitle: CommitTrans Method
ms:assetid: e6d129fb-a578-5c79-9c16-6444519f0daf
ms:mtpsurl: https://msdn.microsoft.com/library/Ff835985(v=office.15)
ms:contentKeyID: 48548391
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: 52af229f03b7ea10510f3e580ba2c4e12784e461
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32306036"
---
# <a name="workspacecommittrans-method-dao"></a><span data-ttu-id="cd0ab-102">Метод Workspace. CommitTrans (DAO)</span><span class="sxs-lookup"><span data-stu-id="cd0ab-102">Workspace.CommitTrans method (DAO)</span></span>

<span data-ttu-id="cd0ab-103">**Область применения**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="cd0ab-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="cd0ab-104">Завершает текущую транзакцию и сохраняет изменения.</span><span class="sxs-lookup"><span data-stu-id="cd0ab-104">Ends the current transaction and saves the changes.</span></span>

## <a name="syntax"></a><span data-ttu-id="cd0ab-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="cd0ab-105">Syntax</span></span>

<span data-ttu-id="cd0ab-106">*Expression* . CommitTrans (***Options***)</span><span class="sxs-lookup"><span data-stu-id="cd0ab-106">*expression* .CommitTrans(***Options***)</span></span>

<span data-ttu-id="cd0ab-107">*expression*: переменная, представляющая объект **Workspace**.</span><span class="sxs-lookup"><span data-stu-id="cd0ab-107">*expression* A variable that represents a **Workspace** object.</span></span>

## <a name="parameters"></a><span data-ttu-id="cd0ab-108">Параметры</span><span class="sxs-lookup"><span data-stu-id="cd0ab-108">Parameters</span></span>

<table>
<colgroup>
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="cd0ab-109">Имя</span><span class="sxs-lookup"><span data-stu-id="cd0ab-109">Name</span></span></p></th>
<th><p><span data-ttu-id="cd0ab-110">Обязательно/необязательно</span><span class="sxs-lookup"><span data-stu-id="cd0ab-110">Required/optional</span></span></p></th>
<th><p><span data-ttu-id="cd0ab-111">Тип данных</span><span class="sxs-lookup"><span data-stu-id="cd0ab-111">Data type</span></span></p></th>
<th><p><span data-ttu-id="cd0ab-112">Описание</span><span class="sxs-lookup"><span data-stu-id="cd0ab-112">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="cd0ab-113"><em>Вариант</em></span><span class="sxs-lookup"><span data-stu-id="cd0ab-113"><em>Option</em></span></span></p></td>
<td><p><span data-ttu-id="cd0ab-114">Необязательный</span><span class="sxs-lookup"><span data-stu-id="cd0ab-114">Optional</span></span></p></td>
<td><p><span data-ttu-id="cd0ab-115"><strong>Long</strong></span><span class="sxs-lookup"><span data-stu-id="cd0ab-115"><strong>Long</strong></span></span></p></td>
<td><p><span data-ttu-id="cd0ab-116">В рабочей области Microsoft Access можно включить константу <strong>дбфорцеосфлуш</strong> с <strong>CommitTrans</strong>.</span><span class="sxs-lookup"><span data-stu-id="cd0ab-116">In a Microsoft Access workspace, you can include the <strong>dbForceOSFlush</strong> constant with <strong>CommitTrans</strong>.</span></span> <span data-ttu-id="cd0ab-117">Это заставляет ядро СУБД немедленно очистить все обновления на диске вместо того, чтобы временно кэшировать их.</span><span class="sxs-lookup"><span data-stu-id="cd0ab-117">This forces the database engine to immediately flush all updates to disk, instead of caching them temporarily.</span></span> <span data-ttu-id="cd0ab-118">Если не использовать этот параметр, пользователь может вернуть управление сразу же после того, как приложение вызовет <strong>CommitTrans</strong>, выключите компьютер и не записывает данные на диск.</span><span class="sxs-lookup"><span data-stu-id="cd0ab-118">Without using this option, a user could get control back immediately after the application program calls <strong>CommitTrans</strong>, turn the computer off, and not have the data written to disk.</span></span> <span data-ttu-id="cd0ab-119">Использование этого параметра может повлиять на производительность приложения, но это полезно в тех случаях, когда компьютер может быть выключен до сохранения кэшированных обновлений на диск.</span><span class="sxs-lookup"><span data-stu-id="cd0ab-119">While using this option may affect your application's performance, it is useful in situations where the computer could be shut off before cached updates are saved to disk.</span></span></p></td>
</tr>
</tbody>
</table>


## <a name="remarks"></a><span data-ttu-id="cd0ab-120">Замечания</span><span class="sxs-lookup"><span data-stu-id="cd0ab-120">Remarks</span></span>

<span data-ttu-id="cd0ab-121">Методы транзакции **BeginTrans**, **CommitTrans**и **ROLLBACK** управляют обработкой транзакций во время сеанса, определенного объектом **Workspace** .</span><span class="sxs-lookup"><span data-stu-id="cd0ab-121">The transaction methods **BeginTrans**, **CommitTrans**, and **Rollback** manage transaction processing during a session defined by a **Workspace** object.</span></span> <span data-ttu-id="cd0ab-122">Эти методы используются вместе с объектом **Workspace** , когда необходимо обрабатывать серию изменений, внесенных в базы данных в сеансе, как единое целое.</span><span class="sxs-lookup"><span data-stu-id="cd0ab-122">You use these methods with a **Workspace** object when you want to treat a series of changes made to the databases in a session as one unit.</span></span>

<span data-ttu-id="cd0ab-123">Как правило, транзакции используются для поддержания целостности данных, когда необходимо обновить записи в двух или более таблицах и убедиться в том, что изменения выполнены (зафиксированы) во всех таблицах или нет (выполняется откат).</span><span class="sxs-lookup"><span data-stu-id="cd0ab-123">Typically, you use transactions to maintain the integrity of your data when you must both update records in two or more tables and ensure changes are completed (committed) in all tables or none at all (rolled back).</span></span> <span data-ttu-id="cd0ab-124">Например, если вы переносите деньги из одной учетной записи в другую, вы можете вычесть сумму из единицы и добавить сумму в другую.</span><span class="sxs-lookup"><span data-stu-id="cd0ab-124">For example, if you transfer money from one account to another, you might subtract an amount from one and add the amount to another.</span></span> <span data-ttu-id="cd0ab-125">Если обновление завершается сбоем, учетные записи больше не сбалансированы.</span><span class="sxs-lookup"><span data-stu-id="cd0ab-125">If either update fails, the accounts no longer balance.</span></span> <span data-ttu-id="cd0ab-126">Используйте метод **BeginTrans** перед обновлением первой записи, а затем, если при последующих обновлениях происходит сбой, можно использовать метод **ROLLBACK** для отмены всех обновлений.</span><span class="sxs-lookup"><span data-stu-id="cd0ab-126">Use the **BeginTrans** method before updating the first record, and then, if any subsequent update fails, you can use the **Rollback** method to undo all of the updates.</span></span> <span data-ttu-id="cd0ab-127">Используйте метод **CommitTrans** после успешного обновления последней записи.</span><span class="sxs-lookup"><span data-stu-id="cd0ab-127">Use the **CommitTrans** method after you successfully update the last record.</span></span>

> [!NOTE]
> <span data-ttu-id="cd0ab-128">В пределах одного объекта **Workspace** транзакции всегда являются глобальными для **рабочей области** и не ограничиваются одним **подключением** или объектом **Database** .</span><span class="sxs-lookup"><span data-stu-id="cd0ab-128">Within one **Workspace** object, transactions are always global to the **Workspace** and aren't limited to only one **Connection** or **Database** object.</span></span> <span data-ttu-id="cd0ab-129">Если вы выполняете операции над несколькими подключениями или базами данных в транзакции **рабочей области** , разрешение транзакции (то есть с помощью метода **CommitTrans** или **ROLLBACK** ) влияет на все операции со всеми подключениями и базами данных в этой рабочей области.</span><span class="sxs-lookup"><span data-stu-id="cd0ab-129">If you perform operations on more than one connection or database within a **Workspace** transaction, resolving the transaction (that is, using the **CommitTrans** or **Rollback** method) affects all operations on all connections and databases within that workspace.</span></span>

<span data-ttu-id="cd0ab-130">Если вы используете **CommitTrans**, вы не сможете отменить изменения, внесенные во время этой транзакции, пока транзакция не будет вложена в другую транзакцию, которая откатывается обратно.</span><span class="sxs-lookup"><span data-stu-id="cd0ab-130">After you use **CommitTrans**, you can't undo changes made during that transaction unless the transaction is nested within another transaction that is itself rolled back.</span></span> <span data-ttu-id="cd0ab-131">При вложении транзакций необходимо разрешить текущую транзакцию, прежде чем можно будет разрешить транзакцию на более высоком уровне вложения.</span><span class="sxs-lookup"><span data-stu-id="cd0ab-131">If you nest transactions, you must resolve the current transaction before you can resolve a transaction at a higher level of nesting.</span></span>

<span data-ttu-id="cd0ab-132">Если требуется одновременные транзакции с перекрывающимися невложенными областями, можно создать дополнительные объекты **рабочей области** , которые будут содержать параллельные транзакции.</span><span class="sxs-lookup"><span data-stu-id="cd0ab-132">If you want to have simultaneous transactions with overlapping, non-nested scopes, you can create additional **Workspace** objects to contain the concurrent transactions.</span></span>

<span data-ttu-id="cd0ab-133">Если закрыть объект **Workspace** , не разрешающий все ожидающие транзакции, выполняется автоматический откат транзакций.</span><span class="sxs-lookup"><span data-stu-id="cd0ab-133">If you close a **Workspace** object without resolving any pending transactions, the transactions are automatically rolled back.</span></span>

<span data-ttu-id="cd0ab-134">Если вы используете метод **CommitTrans** или **ROLLBACK** без предварительного использования метода **BeginTrans** , возникнет ошибка.</span><span class="sxs-lookup"><span data-stu-id="cd0ab-134">If you use the **CommitTrans** or **Rollback** method without first using the **BeginTrans** method, an error occurs.</span></span>

<span data-ttu-id="cd0ab-135">Некоторые базы данных ISAM, используемые в рабочей области Microsoft Access, могут не поддерживать транзакции, в \*\*\*\* этом случае свойство Transactions объекта **базы данных** или объекта **Recordset** имеет **значение false**.</span><span class="sxs-lookup"><span data-stu-id="cd0ab-135">Some ISAM databases used in a Microsoft Access workspace may not support transactions, in which case the **Transactions** property of the **Database** object or **Recordset** object is **False**.</span></span> <span data-ttu-id="cd0ab-136">Чтобы убедиться, что база данных поддерживает транзакции, проверьте значение свойства **Transactions** объекта **Database** , прежде чем использовать метод **BeginTrans** .</span><span class="sxs-lookup"><span data-stu-id="cd0ab-136">To make sure the database supports transactions, check the value of the **Transactions** property of the **Database** object before using the **BeginTrans** method.</span></span> <span data-ttu-id="cd0ab-137">Если вы используете объект **Recordset** на основе нескольких баз данных, проверьте свойство Transactions объекта \*\*\*\* **Recordset** .</span><span class="sxs-lookup"><span data-stu-id="cd0ab-137">If you are using a **Recordset** object based on more than one database, check the **Transactions** property of the **Recordset** object.</span></span> 

<span data-ttu-id="cd0ab-138">Если **набор записей** полностью основан на таблицах ядра СУБД Microsoft Access, всегда можно использовать транзакции.</span><span class="sxs-lookup"><span data-stu-id="cd0ab-138">If a **Recordset** is based entirely on Microsoft Access database engine tables, you can always use transactions.</span></span> <span data-ttu-id="cd0ab-139">Однако объекты **Recordset** , основанные на таблицах, созданных другими продуктами баз данных, могут не поддерживать транзакции.</span><span class="sxs-lookup"><span data-stu-id="cd0ab-139">**Recordset** objects based on tables created by other database products, however, may not support transactions.</span></span> <span data-ttu-id="cd0ab-140">Например, нельзя использовать транзакции в **наборе записей** , основанном на таблице Paradox.</span><span class="sxs-lookup"><span data-stu-id="cd0ab-140">For example, you can't use transactions in a **Recordset** based on a Paradox table.</span></span> <span data-ttu-id="cd0ab-141">В этом случае свойство **Transactions** имеет **значение false**.</span><span class="sxs-lookup"><span data-stu-id="cd0ab-141">In this case, the **Transactions** property is **False**.</span></span> <span data-ttu-id="cd0ab-142">Если **база данных** или **набор записей** не поддерживают транзакции, методы игнорируются, и ошибка не возникает.</span><span class="sxs-lookup"><span data-stu-id="cd0ab-142">If the **Database** or **Recordset** doesn't support transactions, the methods are ignored and no error occurs.</span></span>

<span data-ttu-id="cd0ab-143">Нельзя вкладывать транзакции, если доступ к источникам данных ODBC осуществляется с помощью ядра СУБД Microsoft Access.</span><span class="sxs-lookup"><span data-stu-id="cd0ab-143">You can't nest transactions if you are accessing ODBC data sources through the Microsoft Access database engine.</span></span>

<span data-ttu-id="cd0ab-144">В рабочих областях ODBC при использовании **CommitTrans** курсор может стать недействительным.</span><span class="sxs-lookup"><span data-stu-id="cd0ab-144">In ODBC workspaces, when you use **CommitTrans** your cursor may no longer be valid.</span></span> <span data-ttu-id="cd0ab-145">Используйте метод **Requery** для просмотра изменений в наборе **записей**, а также для закрытия и повторного открытия объекта **Recordset**.</span><span class="sxs-lookup"><span data-stu-id="cd0ab-145">Use the **Requery** method to view the changes in the **Recordset**, or close and re-open the **Recordset**.</span></span>

> [!NOTE]
> - <span data-ttu-id="cd0ab-146">Вы часто можете увеличить производительность приложения, разбив операции, требующие доступа к диску, в блоки транзакций.</span><span class="sxs-lookup"><span data-stu-id="cd0ab-146">You can often improve the performance of your application by breaking operations that require disk access into transaction blocks.</span></span> <span data-ttu-id="cd0ab-147">Это приводит к буферизации операций и значительно сокращает количество обращений к диску.</span><span class="sxs-lookup"><span data-stu-id="cd0ab-147">This buffers your operations and may significantly reduce the number of times a disk is accessed.</span></span>
> - <span data-ttu-id="cd0ab-148">В рабочей области Microsoft Access транзакции записываются в файл, сохраненный в каталоге, указанном в переменной среды TEMP на рабочей станции.</span><span class="sxs-lookup"><span data-stu-id="cd0ab-148">In a Microsoft Access workspace, transactions are logged in a file kept in the directory specified by the TEMP environment variable on the workstation.</span></span> <span data-ttu-id="cd0ab-149">Если файл журнала транзакций исчерпал Доступное хранилище на диске TEMP, ядро СУБД запускает ошибку во время выполнения.</span><span class="sxs-lookup"><span data-stu-id="cd0ab-149">If the transaction log file exhausts the available storage on your TEMP drive, the database engine triggers a run-time error.</span></span> <span data-ttu-id="cd0ab-150">На этом шаге при использовании **CommitTrans**зафиксировано неопределенное количество операций, но оставшиеся незавершенные операции теряются и операция должна быть перезапущена.</span><span class="sxs-lookup"><span data-stu-id="cd0ab-150">At this point, if you use **CommitTrans**, an indeterminate number of operations are committed, but the remaining uncompleted operations are lost, and the operation has to be restarted.</span></span> <span data-ttu-id="cd0ab-151">Использование метода **отката** освобождает журнал транзакций и выполняет откат всех операций в транзакции.</span><span class="sxs-lookup"><span data-stu-id="cd0ab-151">Using a **Rollback** method releases the transaction log and rolls back all operations in the transaction.</span></span>
> - <span data-ttu-id="cd0ab-152">Закрытие **набора записей** клонирования в ожидающей транзакции приводит к неявной операции **отката** .</span><span class="sxs-lookup"><span data-stu-id="cd0ab-152">Closing a clone **Recordset** within a pending transaction will cause an implicit **Rollback** operation.</span></span>

## <a name="example"></a><span data-ttu-id="cd0ab-153">Пример</span><span class="sxs-lookup"><span data-stu-id="cd0ab-153">Example</span></span>

<span data-ttu-id="cd0ab-154">В приведенном ниже примере показано, как использовать транзакцию в рабочей области объектов доступа к данным (DAO).</span><span class="sxs-lookup"><span data-stu-id="cd0ab-154">The following example shows how to use a transaction in a Data Access Objects (DAO) workspace.</span></span>

<span data-ttu-id="cd0ab-155">**Пример кода из** [справочника программиста Microsoft Access 2010](https://www.amazon.com/Microsoft-Access-2010-Programmers-Reference/dp/8126528125).</span><span class="sxs-lookup"><span data-stu-id="cd0ab-155">**Sample code provided by** the [Microsoft Access 2010 Programmer’s Reference](https://www.amazon.com/Microsoft-Access-2010-Programmers-Reference/dp/8126528125).</span></span>


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
