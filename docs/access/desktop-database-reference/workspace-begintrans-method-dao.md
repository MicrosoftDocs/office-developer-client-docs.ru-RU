---
title: Метод Workspace.BeginTrans (DAO)
TOCTitle: BeginTrans Method
ms:assetid: aa7c3bf8-fb08-9360-5998-4bf3f721ecbb
ms:mtpsurl: https://msdn.microsoft.com/library/Ff821457(v=office.15)
ms:contentKeyID: 48546948
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: c143d91c3dfe786c3245c2b67768c57379869e75
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32302550"
---
# <a name="workspacebegintrans-method-dao"></a><span data-ttu-id="b5659-102">Метод Workspace.BeginTrans (DAO)</span><span class="sxs-lookup"><span data-stu-id="b5659-102">Workspace.BeginTrans method (DAO)</span></span>

<span data-ttu-id="b5659-103">**Область применения**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="b5659-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="b5659-104">Начинается новая транзакция.</span><span class="sxs-lookup"><span data-stu-id="b5659-104">Begins a new transaction.</span></span> <span data-ttu-id="b5659-105">База данных чтения и **записи**.</span><span class="sxs-lookup"><span data-stu-id="b5659-105">Read/write **Database**.</span></span>

## <a name="syntax"></a><span data-ttu-id="b5659-106">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="b5659-106">Syntax</span></span>

<span data-ttu-id="b5659-107">*выражения* . BeginTrans</span><span class="sxs-lookup"><span data-stu-id="b5659-107">*expression* .BeginTrans</span></span>

<span data-ttu-id="b5659-108">*expression*: переменная, представляющая объект **Workspace**.</span><span class="sxs-lookup"><span data-stu-id="b5659-108">*expression* A variable that represents a **Workspace** object.</span></span>

## <a name="remarks"></a><span data-ttu-id="b5659-109">Примечания</span><span class="sxs-lookup"><span data-stu-id="b5659-109">Remarks</span></span>

<span data-ttu-id="b5659-110">Методы транзакций **BeginTrans,** **CommitTrans** и **Rollback** управляют обработкой транзакций во время сеанса, определенного объектом **Рабочей** области.</span><span class="sxs-lookup"><span data-stu-id="b5659-110">The transaction methods **BeginTrans**, **CommitTrans**, and **Rollback** manage transaction processing during a session defined by a **Workspace** object.</span></span> <span data-ttu-id="b5659-111">Эти методы используются с объектом **Workspace,** когда необходимо рассматривать ряд изменений, внесенных в базы данных в сеансе, как одно целое.</span><span class="sxs-lookup"><span data-stu-id="b5659-111">You use these methods with a **Workspace** object when you want to treat a series of changes made to the databases in a session as one unit.</span></span>

<span data-ttu-id="b5659-112">Как правило, транзакции используются для поддержания целостности данных, когда необходимо обновлять записи в двух или более таблицах и обеспечивать, чтобы изменения были завершены (зафиксированы) во всех таблицах или вообще нет (откат).</span><span class="sxs-lookup"><span data-stu-id="b5659-112">Typically, you use transactions to maintain the integrity of your data when you must both update records in two or more tables and ensure changes are completed (committed) in all tables or none at all (rolled back).</span></span> <span data-ttu-id="b5659-113">Например, при переводе денег с одной учетной записи на другую можно вычесть сумму из одной и добавить ее в другую.</span><span class="sxs-lookup"><span data-stu-id="b5659-113">For example, if you transfer money from one account to another, you might subtract an amount from one and add the amount to another.</span></span> <span data-ttu-id="b5659-114">Если обновление не удается, учетные записи перестают балансировать.</span><span class="sxs-lookup"><span data-stu-id="b5659-114">If either update fails, the accounts no longer balance.</span></span> <span data-ttu-id="b5659-115">Используйте метод **BeginTrans** перед обновлением первой записи, а затем, если любое последующее обновление сбой, вы можете использовать метод **отката,** чтобы отменить все обновления.</span><span class="sxs-lookup"><span data-stu-id="b5659-115">Use the **BeginTrans** method before updating the first record, and then, if any subsequent update fails, you can use the **Rollback** method to undo all of the updates.</span></span> <span data-ttu-id="b5659-116">Используйте метод **CommitTrans** после успешного обновления последней записи.</span><span class="sxs-lookup"><span data-stu-id="b5659-116">Use the **CommitTrans** method after you successfully update the last record.</span></span>

> [!NOTE]
> <span data-ttu-id="b5659-117">В одном **объекте Workspace** транзакции всегда являются глобальными для **рабочей** области и не ограничиваются только одним объектом **Подключения** или **Базы данных.**</span><span class="sxs-lookup"><span data-stu-id="b5659-117">Within one **Workspace** object, transactions are always global to the **Workspace** and aren't limited to only one **Connection** or **Database** object.</span></span> <span data-ttu-id="b5659-118">Если вы выполняете операции по более чем одному подключению или базе данных в транзакции **Workspace,** решение транзакции (то есть с помощью метода **CommitTrans** или **Rollback)** влияет на все операции на всех подключениях и базах данных в этом рабочем пространстве.</span><span class="sxs-lookup"><span data-stu-id="b5659-118">If you perform operations on more than one connection or database within a **Workspace** transaction, resolving the transaction (that is, using the **CommitTrans** or **Rollback** method) affects all operations on all connections and databases within that workspace.</span></span>

<span data-ttu-id="b5659-119">После использования **CommitTrans** нельзя отменить изменения, внесенные во время этой транзакции, если транзакция не будет вложена в другую транзакцию, которая сама откатится.</span><span class="sxs-lookup"><span data-stu-id="b5659-119">After you use **CommitTrans**, you can't undo changes made during that transaction unless the transaction is nested within another transaction that is itself rolled back.</span></span> <span data-ttu-id="b5659-120">При вложении транзакций необходимо решить текущую транзакцию, прежде чем разрешить транзакцию на более высоком уровне вложения.</span><span class="sxs-lookup"><span data-stu-id="b5659-120">If you nest transactions, you must resolve the current transaction before you can resolve a transaction at a higher level of nesting.</span></span>

<span data-ttu-id="b5659-121">Если вы хотите иметь одновременные транзакции с перекрывающимися, не вложенными областьми, можно создать дополнительные объекты **Workspace,** чтобы содержать одновременные транзакции.</span><span class="sxs-lookup"><span data-stu-id="b5659-121">If you want to have simultaneous transactions with overlapping, non-nested scopes, you can create additional **Workspace** objects to contain the concurrent transactions.</span></span>

<span data-ttu-id="b5659-122">Если вы закрываете **объект Workspace** без разрешения каких-либо ожидающих транзакций, транзакции автоматически откатываются обратно.</span><span class="sxs-lookup"><span data-stu-id="b5659-122">If you close a **Workspace** object without resolving any pending transactions, the transactions are automatically rolled back.</span></span>

<span data-ttu-id="b5659-123">Если вы используете метод **CommitTrans или** **Rollback** без использования метода **BeginTrans,** возникает ошибка.</span><span class="sxs-lookup"><span data-stu-id="b5659-123">If you use the **CommitTrans** or **Rollback** method without first using the **BeginTrans** method, an error occurs.</span></span>

<span data-ttu-id="b5659-124">Некоторые базы данных ISAM, используемые в рабочей области Microsoft Access, могут не поддерживать транзакции, в этом случае свойство **Transactions** объекта **Database** или **объекта Recordset** является **false**.</span><span class="sxs-lookup"><span data-stu-id="b5659-124">Some ISAM databases used in a Microsoft Access workspace may not support transactions, in which case the **Transactions** property of the **Database** object or **Recordset** object is **False**.</span></span> <span data-ttu-id="b5659-125">Чтобы убедиться, что база данных поддерживает транзакции, перед использованием метода **BeginTrans** проверьте значение свойства **Transactions** объекта **Database.**</span><span class="sxs-lookup"><span data-stu-id="b5659-125">To make sure the database supports transactions, check the value of the **Transactions** property of the **Database** object before using the **BeginTrans** method.</span></span> <span data-ttu-id="b5659-126">Если вы используете объект **Recordset** на основе более чем одной базы данных, проверьте свойство **Transactions** объекта **Recordset.**</span><span class="sxs-lookup"><span data-stu-id="b5659-126">If you are using a **Recordset** object based on more than one database, check the **Transactions** property of the **Recordset** object.</span></span> 

<span data-ttu-id="b5659-127">Если набор **recordset** полностью основан на таблицах баз данных Microsoft Access, всегда можно использовать транзакции.</span><span class="sxs-lookup"><span data-stu-id="b5659-127">If a **Recordset** is based entirely on Microsoft Access database engine tables, you can always use transactions.</span></span> <span data-ttu-id="b5659-128">**Однако объекты recordset** на основе таблиц, созданных другими продуктами базы данных, могут не поддерживать транзакции.</span><span class="sxs-lookup"><span data-stu-id="b5659-128">**Recordset** objects based on tables created by other database products, however, may not support transactions.</span></span> <span data-ttu-id="b5659-129">Например, вы не можете использовать транзакции в **наборе recordset** на основе таблицы Paradox.</span><span class="sxs-lookup"><span data-stu-id="b5659-129">For example, you can't use transactions in a **Recordset** based on a Paradox table.</span></span> <span data-ttu-id="b5659-130">В этом случае свойство **Transactions** является **false**.</span><span class="sxs-lookup"><span data-stu-id="b5659-130">In this case, the **Transactions** property is **False**.</span></span> <span data-ttu-id="b5659-131">Если **база данных** или **набор записей** не поддерживают транзакции, методы игнорируются и ошибки не происходят.</span><span class="sxs-lookup"><span data-stu-id="b5659-131">If the **Database** or **Recordset** doesn't support transactions, the methods are ignored and no error occurs.</span></span>

<span data-ttu-id="b5659-132">Вы не можете вложенные транзакции, если вы имеете доступ к источникам данных ODBC с помощью двигателя базы данных Microsoft Access.</span><span class="sxs-lookup"><span data-stu-id="b5659-132">You can't nest transactions if you are accessing ODBC data sources through the Microsoft Access database engine.</span></span>

<span data-ttu-id="b5659-133">В рабочей области ODBC при использовании **CommitTrans** курсор может перестать быть допустимым.</span><span class="sxs-lookup"><span data-stu-id="b5659-133">In ODBC workspaces, when you use **CommitTrans** your cursor may no longer be valid.</span></span> <span data-ttu-id="b5659-134">Используйте метод **Requery** для просмотра изменений в **Наборе записей** или закрытия и повторного **открытия наборов записей.**</span><span class="sxs-lookup"><span data-stu-id="b5659-134">Use the **Requery** method to view the changes in the **Recordset**, or close and re-open the **Recordset**.</span></span>

> [!NOTE]
> - <span data-ttu-id="b5659-135">Вы часто можете повысить производительность приложения, разбивая операции, которые требуют доступа к диску в блоки транзакций.</span><span class="sxs-lookup"><span data-stu-id="b5659-135">You can often improve the performance of your application by breaking operations that require disk access into transaction blocks.</span></span> <span data-ttu-id="b5659-136">Это буферит операции и может значительно сократить количество случаев доступа к диску.</span><span class="sxs-lookup"><span data-stu-id="b5659-136">This buffers your operations and may significantly reduce the number of times a disk is accessed.</span></span>
> - <span data-ttu-id="b5659-137">В рабочей области Microsoft Access транзакции регистрируются в файле, который хранится в каталоге, указанном переменной среды TEMP на рабочей станции.</span><span class="sxs-lookup"><span data-stu-id="b5659-137">In a Microsoft Access workspace, transactions are logged in a file kept in the directory specified by the TEMP environment variable on the workstation.</span></span> <span data-ttu-id="b5659-138">Если файл журнала транзакций исчерпает доступное хранилище на диске TEMP, двигатель базы данных вызывает ошибку во время запуска.</span><span class="sxs-lookup"><span data-stu-id="b5659-138">If the transaction log file exhausts the available storage on your TEMP drive, the database engine triggers a run-time error.</span></span> <span data-ttu-id="b5659-139">На этом этапе при использовании **CommitTrans** совершается неопределяемая численность операций, но остальные незавершенные операции теряются, и операция должна быть перезапущена.</span><span class="sxs-lookup"><span data-stu-id="b5659-139">At this point, if you use **CommitTrans**, an indeterminate number of operations are committed, but the remaining uncompleted operations are lost, and the operation has to be restarted.</span></span> <span data-ttu-id="b5659-140">Метод **отката** освобождает журнал транзакций и откатит все операции в транзакции.</span><span class="sxs-lookup"><span data-stu-id="b5659-140">Using a **Rollback** method releases the transaction log and rolls back all operations in the transaction.</span></span>
> - <span data-ttu-id="b5659-141">Закрытие клона **Recordset в** ожидаемой транзакции приведет к неявной операции **отката.**</span><span class="sxs-lookup"><span data-stu-id="b5659-141">Closing a clone **Recordset** within a pending transaction will cause an implicit **Rollback** operation.</span></span>

## <a name="example"></a><span data-ttu-id="b5659-142">Пример</span><span class="sxs-lookup"><span data-stu-id="b5659-142">Example</span></span>

<span data-ttu-id="b5659-143">В следующем примере показано, как использовать транзакцию в рабочей области объектов доступа к данным (DAO).</span><span class="sxs-lookup"><span data-stu-id="b5659-143">The following example shows how to use a transaction in a Data Access Objects (DAO) workspace.</span></span>

<span data-ttu-id="b5659-144">**Пример кода из** [справочника программиста Microsoft Access 2010](https://www.amazon.com/Microsoft-Access-2010-Programmers-Reference/dp/8126528125).</span><span class="sxs-lookup"><span data-stu-id="b5659-144">**Sample code provided by** the [Microsoft Access 2010 Programmer’s Reference](https://www.amazon.com/Microsoft-Access-2010-Programmers-Reference/dp/8126528125).</span></span>

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
