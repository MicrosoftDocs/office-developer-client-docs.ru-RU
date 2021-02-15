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
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32306036"
---
# <a name="workspacecommittrans-method-dao"></a><span data-ttu-id="4c05a-102">Метод Workspace.CommitTrans (DAO)</span><span class="sxs-lookup"><span data-stu-id="4c05a-102">Workspace.CommitTrans method (DAO)</span></span>

<span data-ttu-id="4c05a-103">**Область применения**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="4c05a-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="4c05a-104">Завершает текущую транзакцию и сохраняет изменения.</span><span class="sxs-lookup"><span data-stu-id="4c05a-104">Ends the current transaction and saves the changes.</span></span>

## <a name="syntax"></a><span data-ttu-id="4c05a-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="4c05a-105">Syntax</span></span>

<span data-ttu-id="4c05a-106">*выражение .* CommitTrans(***Options***)</span><span class="sxs-lookup"><span data-stu-id="4c05a-106">*expression* .CommitTrans(***Options***)</span></span>

<span data-ttu-id="4c05a-107">*expression*: переменная, представляющая объект **Workspace**.</span><span class="sxs-lookup"><span data-stu-id="4c05a-107">*expression* A variable that represents a **Workspace** object.</span></span>

## <a name="parameters"></a><span data-ttu-id="4c05a-108">Параметры</span><span class="sxs-lookup"><span data-stu-id="4c05a-108">Parameters</span></span>

<table>
<colgroup>
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="4c05a-109">Имя</span><span class="sxs-lookup"><span data-stu-id="4c05a-109">Name</span></span></p></th>
<th><p><span data-ttu-id="4c05a-110">Обязательный/необязательный</span><span class="sxs-lookup"><span data-stu-id="4c05a-110">Required/optional</span></span></p></th>
<th><p><span data-ttu-id="4c05a-111">Тип данных</span><span class="sxs-lookup"><span data-stu-id="4c05a-111">Data type</span></span></p></th>
<th><p><span data-ttu-id="4c05a-112">Описание</span><span class="sxs-lookup"><span data-stu-id="4c05a-112">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="4c05a-113"><em>Option</em></span><span class="sxs-lookup"><span data-stu-id="4c05a-113"><em>Option</em></span></span></p></td>
<td><p><span data-ttu-id="4c05a-114">Необязательный</span><span class="sxs-lookup"><span data-stu-id="4c05a-114">Optional</span></span></p></td>
<td><p><span data-ttu-id="4c05a-115"><strong>Long</strong></span><span class="sxs-lookup"><span data-stu-id="4c05a-115"><strong>Long</strong></span></span></p></td>
<td><p><span data-ttu-id="4c05a-116">В рабочей области Microsoft Access можно включить константу <strong>dbForceOSFlush</strong> с <strong>CommitTrans.</strong></span><span class="sxs-lookup"><span data-stu-id="4c05a-116">In a Microsoft Access workspace, you can include the <strong>dbForceOSFlush</strong> constant with <strong>CommitTrans</strong>.</span></span> <span data-ttu-id="4c05a-117">Это заставляет яд баз данных немедленно очистить все обновления на диск, а не кэшвать их временно.</span><span class="sxs-lookup"><span data-stu-id="4c05a-117">This forces the database engine to immediately flush all updates to disk, instead of caching them temporarily.</span></span> <span data-ttu-id="4c05a-118">Без использования этого параметра пользователь может получить контроль непосредственно после того, как программа приложения вызывает <strong>CommitTrans,</strong>отключит компьютер и данные не будут записаны на диск.</span><span class="sxs-lookup"><span data-stu-id="4c05a-118">Without using this option, a user could get control back immediately after the application program calls <strong>CommitTrans</strong>, turn the computer off, and not have the data written to disk.</span></span> <span data-ttu-id="4c05a-119">Хотя использование этого параметра может повлиять на производительность приложения, оно полезно в ситуациях, когда компьютер может быть отключен до снесения кэшных обновлений на диск.</span><span class="sxs-lookup"><span data-stu-id="4c05a-119">While using this option may affect your application's performance, it is useful in situations where the computer could be shut off before cached updates are saved to disk.</span></span></p></td>
</tr>
</tbody>
</table>


## <a name="remarks"></a><span data-ttu-id="4c05a-120">Заметки</span><span class="sxs-lookup"><span data-stu-id="4c05a-120">Remarks</span></span>

<span data-ttu-id="4c05a-121">Методы транзакций **BeginTrans,** **CommitTrans** и **Rollback** управляют обработкой транзакций во время сеанса, определенного **объектом Рабочей** области.</span><span class="sxs-lookup"><span data-stu-id="4c05a-121">The transaction methods **BeginTrans**, **CommitTrans**, and **Rollback** manage transaction processing during a session defined by a **Workspace** object.</span></span> <span data-ttu-id="4c05a-122">Эти методы используются с объектом **Workspace,** если необходимо рассматривать ряд изменений, внесенных в базы данных в сеансе, как одно целое.</span><span class="sxs-lookup"><span data-stu-id="4c05a-122">You use these methods with a **Workspace** object when you want to treat a series of changes made to the databases in a session as one unit.</span></span>

<span data-ttu-id="4c05a-123">Как правило, транзакции используются для поддержания целостности данных, когда необходимо обновить записи в двух или более таблицах и убедиться, что изменения завершены (зафиксированы) во всех таблицах или вообще нет (откат).</span><span class="sxs-lookup"><span data-stu-id="4c05a-123">Typically, you use transactions to maintain the integrity of your data when you must both update records in two or more tables and ensure changes are completed (committed) in all tables or none at all (rolled back).</span></span> <span data-ttu-id="4c05a-124">Например, если вы переводите деньги с одной учетной записи на другую, вы можете вычитать сумму из одной учетной записи и добавить ее в другую.</span><span class="sxs-lookup"><span data-stu-id="4c05a-124">For example, if you transfer money from one account to another, you might subtract an amount from one and add the amount to another.</span></span> <span data-ttu-id="4c05a-125">Если обновление не удастся, учетные записи перестают балансировать.</span><span class="sxs-lookup"><span data-stu-id="4c05a-125">If either update fails, the accounts no longer balance.</span></span> <span data-ttu-id="4c05a-126">Используйте метод **BeginTrans** перед обновлением первой записи, а затем, если последующее обновление не удастся, вы можете отменить все обновления с помощью метода **Rollback.**</span><span class="sxs-lookup"><span data-stu-id="4c05a-126">Use the **BeginTrans** method before updating the first record, and then, if any subsequent update fails, you can use the **Rollback** method to undo all of the updates.</span></span> <span data-ttu-id="4c05a-127">Используйте метод **CommitTrans** после успешного обновления последней записи.</span><span class="sxs-lookup"><span data-stu-id="4c05a-127">Use the **CommitTrans** method after you successfully update the last record.</span></span>

> [!NOTE]
> <span data-ttu-id="4c05a-128">В одном **объекте Workspace** транзакции всегда являются глобальными для **рабочей** области и не ограничиваются только одним объектом **Connection** или **Database.**</span><span class="sxs-lookup"><span data-stu-id="4c05a-128">Within one **Workspace** object, transactions are always global to the **Workspace** and aren't limited to only one **Connection** or **Database** object.</span></span> <span data-ttu-id="4c05a-129">Если вы выполняете операции с более чем одним подключением или базой данных в транзакции **Рабочей** области, разрешение транзакции (то есть с помощью метода **CommitTrans** или **Rollback)** влияет на все операции со всеми подключениями и базами данных в этой рабочей области.</span><span class="sxs-lookup"><span data-stu-id="4c05a-129">If you perform operations on more than one connection or database within a **Workspace** transaction, resolving the transaction (that is, using the **CommitTrans** or **Rollback** method) affects all operations on all connections and databases within that workspace.</span></span>

<span data-ttu-id="4c05a-130">После использования **CommitTrans** вы не сможете отменить изменения, внесенные во время этой транзакции, если транзакция не вложена в другую транзакцию, которая была отката.</span><span class="sxs-lookup"><span data-stu-id="4c05a-130">After you use **CommitTrans**, you can't undo changes made during that transaction unless the transaction is nested within another transaction that is itself rolled back.</span></span> <span data-ttu-id="4c05a-131">Если вы вложены транзакции, необходимо разрешить текущую транзакцию, прежде чем разрешать транзакцию на более высоком уровне вложенности.</span><span class="sxs-lookup"><span data-stu-id="4c05a-131">If you nest transactions, you must resolve the current transaction before you can resolve a transaction at a higher level of nesting.</span></span>

<span data-ttu-id="4c05a-132">Если вы хотите иметь одновременные транзакции с перекрывающимися, не вложенными областью, можно создать дополнительные объекты **Рабочей** области, содержащие параллельные транзакции.</span><span class="sxs-lookup"><span data-stu-id="4c05a-132">If you want to have simultaneous transactions with overlapping, non-nested scopes, you can create additional **Workspace** objects to contain the concurrent transactions.</span></span>

<span data-ttu-id="4c05a-133">При закрытии **объекта Workspace** без разрешения ожидающих транзакций транзакции автоматически откатываются.</span><span class="sxs-lookup"><span data-stu-id="4c05a-133">If you close a **Workspace** object without resolving any pending transactions, the transactions are automatically rolled back.</span></span>

<span data-ttu-id="4c05a-134">Если вы используете метод **CommitTrans** или **Rollback** без использования метода **BeginTrans,** возникает ошибка.</span><span class="sxs-lookup"><span data-stu-id="4c05a-134">If you use the **CommitTrans** or **Rollback** method without first using the **BeginTrans** method, an error occurs.</span></span>

<span data-ttu-id="4c05a-135">Некоторые базы данных ISAM, используемые в рабочей области Microsoft Access, могут не поддерживать транзакции, в этом случае свойство **Transactions** объекта **Database** или **Объекта Recordset** имеет свойство **False.**</span><span class="sxs-lookup"><span data-stu-id="4c05a-135">Some ISAM databases used in a Microsoft Access workspace may not support transactions, in which case the **Transactions** property of the **Database** object or **Recordset** object is **False**.</span></span> <span data-ttu-id="4c05a-136">Чтобы убедиться, что база данных поддерживает транзакции, проверьте значение свойства **Transactions** объекта **Database** перед использованием метода **BeginTrans.**</span><span class="sxs-lookup"><span data-stu-id="4c05a-136">To make sure the database supports transactions, check the value of the **Transactions** property of the **Database** object before using the **BeginTrans** method.</span></span> <span data-ttu-id="4c05a-137">Если вы используете объект **Recordset на** основе более чем одной базы данных, проверьте свойство **Transactions** объекта **Recordset.**</span><span class="sxs-lookup"><span data-stu-id="4c05a-137">If you are using a **Recordset** object based on more than one database, check the **Transactions** property of the **Recordset** object.</span></span> 

<span data-ttu-id="4c05a-138">Если набор **recordset** полностью основан на таблицах ядров баз данных Microsoft Access, всегда можно использовать транзакции.</span><span class="sxs-lookup"><span data-stu-id="4c05a-138">If a **Recordset** is based entirely on Microsoft Access database engine tables, you can always use transactions.</span></span> <span data-ttu-id="4c05a-139">**Однако объекты наборов** записей, основанные на таблицах, созданных другими продуктами базы данных, могут не поддерживать транзакции.</span><span class="sxs-lookup"><span data-stu-id="4c05a-139">**Recordset** objects based on tables created by other database products, however, may not support transactions.</span></span> <span data-ttu-id="4c05a-140">Например, вы не можете использовать транзакции в наборе **записей** на основе таблицы Paradox.</span><span class="sxs-lookup"><span data-stu-id="4c05a-140">For example, you can't use transactions in a **Recordset** based on a Paradox table.</span></span> <span data-ttu-id="4c05a-141">В этом случае свойство **Transactions** имеет свойство **False.**</span><span class="sxs-lookup"><span data-stu-id="4c05a-141">In this case, the **Transactions** property is **False**.</span></span> <span data-ttu-id="4c05a-142">Если база **данных** или **набор записей** не поддерживают транзакции, методы игнорируются и ошибки не возникают.</span><span class="sxs-lookup"><span data-stu-id="4c05a-142">If the **Database** or **Recordset** doesn't support transactions, the methods are ignored and no error occurs.</span></span>

<span data-ttu-id="4c05a-143">При доступе к источникам данных ODBC с помощью яда базы данных Microsoft Access нельзя вложенные транзакции.</span><span class="sxs-lookup"><span data-stu-id="4c05a-143">You can't nest transactions if you are accessing ODBC data sources through the Microsoft Access database engine.</span></span>

<span data-ttu-id="4c05a-144">В ODBC workspaces, when you use **CommitTrans** your cursor may no longer be valid.</span><span class="sxs-lookup"><span data-stu-id="4c05a-144">In ODBC workspaces, when you use **CommitTrans** your cursor may no longer be valid.</span></span> <span data-ttu-id="4c05a-145">Используйте метод **Requery** для просмотра изменений в наборе **записей** или закрытия и повторного **открытия recordset.**</span><span class="sxs-lookup"><span data-stu-id="4c05a-145">Use the **Requery** method to view the changes in the **Recordset**, or close and re-open the **Recordset**.</span></span>

> [!NOTE]
> - <span data-ttu-id="4c05a-146">Часто производительность приложения можно повысить, разорвав операции, которые требуют доступа к диску, в блоки транзакций.</span><span class="sxs-lookup"><span data-stu-id="4c05a-146">You can often improve the performance of your application by breaking operations that require disk access into transaction blocks.</span></span> <span data-ttu-id="4c05a-147">Это буферит ваши операции и может значительно сократить количество операций доступа к диску.</span><span class="sxs-lookup"><span data-stu-id="4c05a-147">This buffers your operations and may significantly reduce the number of times a disk is accessed.</span></span>
> - <span data-ttu-id="4c05a-148">В рабочей области Microsoft Access транзакции регистрируются в файле, который хранится в каталоге, указанном переменной среды TEMP на рабочей станции.</span><span class="sxs-lookup"><span data-stu-id="4c05a-148">In a Microsoft Access workspace, transactions are logged in a file kept in the directory specified by the TEMP environment variable on the workstation.</span></span> <span data-ttu-id="4c05a-149">Если файл журнала транзакций исчерпает доступное хранилище на диске TEMP, обдвижка базы данных инициирует ошибку времени запуска.</span><span class="sxs-lookup"><span data-stu-id="4c05a-149">If the transaction log file exhausts the available storage on your TEMP drive, the database engine triggers a run-time error.</span></span> <span data-ttu-id="4c05a-150">На этом этапе, если вы используете **CommitTrans,** будет фиксироваться неопределяемого количества операций, но остальные невыполненные операции будут потеряны, и операцию необходимо перезапустить.</span><span class="sxs-lookup"><span data-stu-id="4c05a-150">At this point, if you use **CommitTrans**, an indeterminate number of operations are committed, but the remaining uncompleted operations are lost, and the operation has to be restarted.</span></span> <span data-ttu-id="4c05a-151">Использование метода **отката** освобождает журнал транзакций и откатит все операции в транзакции.</span><span class="sxs-lookup"><span data-stu-id="4c05a-151">Using a **Rollback** method releases the transaction log and rolls back all operations in the transaction.</span></span>
> - <span data-ttu-id="4c05a-152">Закрытие клона **recordset в** ожидающих транзакциях приведет к неявной операции **отката.**</span><span class="sxs-lookup"><span data-stu-id="4c05a-152">Closing a clone **Recordset** within a pending transaction will cause an implicit **Rollback** operation.</span></span>

## <a name="example"></a><span data-ttu-id="4c05a-153">Пример</span><span class="sxs-lookup"><span data-stu-id="4c05a-153">Example</span></span>

<span data-ttu-id="4c05a-154">В следующем примере показано, как использовать транзакцию в рабочей области объектов доступа к данным (DAO).</span><span class="sxs-lookup"><span data-stu-id="4c05a-154">The following example shows how to use a transaction in a Data Access Objects (DAO) workspace.</span></span>

<span data-ttu-id="4c05a-155">**Пример кода из** [справочника программиста Microsoft Access 2010](https://www.amazon.com/Microsoft-Access-2010-Programmers-Reference/dp/8126528125).</span><span class="sxs-lookup"><span data-stu-id="4c05a-155">**Sample code provided by** the [Microsoft Access 2010 Programmer’s Reference](https://www.amazon.com/Microsoft-Access-2010-Programmers-Reference/dp/8126528125).</span></span>


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
