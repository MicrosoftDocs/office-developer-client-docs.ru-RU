---
title: Метод DBEngine.CommitTrans (DAO)
TOCTitle: CommitTrans Method
ms:assetid: 0c9d345f-13ff-7fe6-789d-fbdb43fa54b8
ms:mtpsurl: https://msdn.microsoft.com/library/Ff845171(v=office.15)
ms:contentKeyID: 48543197
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: 75918ac4da32020214d9e58d866c5def169eede3
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32294389"
---
# <a name="dbenginecommittrans-method-dao"></a><span data-ttu-id="fbc20-102">Метод DBEngine.CommitTrans (DAO)</span><span class="sxs-lookup"><span data-stu-id="fbc20-102">DBEngine.CommitTrans method (DAO)</span></span>


<span data-ttu-id="fbc20-103">**Область применения**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="fbc20-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="fbc20-104">Завершает текущую транзакцию и сохраняет изменения.</span><span class="sxs-lookup"><span data-stu-id="fbc20-104">Ends the current transaction and saves the changes.</span></span>

## <a name="syntax"></a><span data-ttu-id="fbc20-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="fbc20-105">Syntax</span></span>

<span data-ttu-id="fbc20-106">*выражения* . ***CommitTrans(Option)***</span><span class="sxs-lookup"><span data-stu-id="fbc20-106">*expression* .CommitTrans(***Option***)</span></span>

<span data-ttu-id="fbc20-107">*expression*: переменная, представляющая объект **DBEngine**.</span><span class="sxs-lookup"><span data-stu-id="fbc20-107">*expression* A variable that represents a **DBEngine** object.</span></span>

## <a name="parameters"></a><span data-ttu-id="fbc20-108">Параметры</span><span class="sxs-lookup"><span data-stu-id="fbc20-108">Parameters</span></span>

<table>
<colgroup>
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="fbc20-109">Имя</span><span class="sxs-lookup"><span data-stu-id="fbc20-109">Name</span></span></p></th>
<th><p><span data-ttu-id="fbc20-110">Обязательный/необязательный</span><span class="sxs-lookup"><span data-stu-id="fbc20-110">Required/optional</span></span></p></th>
<th><p><span data-ttu-id="fbc20-111">Тип данных</span><span class="sxs-lookup"><span data-stu-id="fbc20-111">Data type</span></span></p></th>
<th><p><span data-ttu-id="fbc20-112">Описание</span><span class="sxs-lookup"><span data-stu-id="fbc20-112">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="fbc20-113"><em>Option</em></span><span class="sxs-lookup"><span data-stu-id="fbc20-113"><em>Option</em></span></span></p></td>
<td><p><span data-ttu-id="fbc20-114">Необязательный</span><span class="sxs-lookup"><span data-stu-id="fbc20-114">Optional</span></span></p></td>
<td><p><span data-ttu-id="fbc20-115"><strong>Long</strong></span><span class="sxs-lookup"><span data-stu-id="fbc20-115"><strong>Long</strong></span></span></p></td>
<td><p><span data-ttu-id="fbc20-116">В рабочей области Microsoft Access можно включить константу <strong>dbForceOSFlush</strong> с <strong>CommitTrans.</strong></span><span class="sxs-lookup"><span data-stu-id="fbc20-116">In a Microsoft Access workspace, you can include the <strong>dbForceOSFlush</strong> constant with <strong>CommitTrans</strong>.</span></span> <span data-ttu-id="fbc20-117">Это заставляет двигатель базы данных немедленно смывать все обновления на диск, а не временно кэшывать их.</span><span class="sxs-lookup"><span data-stu-id="fbc20-117">This forces the database engine to immediately flush all updates to disk, instead of caching them temporarily.</span></span> <span data-ttu-id="fbc20-118">Не используя этот параметр, пользователь может получить контроль сразу после вызова программы приложения <strong>CommitTrans,</strong>отключить компьютер и не иметь данные, написанные на диск.</span><span class="sxs-lookup"><span data-stu-id="fbc20-118">Without using this option, a user could get control back immediately after the application program calls <strong>CommitTrans</strong>, turn the computer off, and not have the data written to disk.</span></span> <span data-ttu-id="fbc20-119">Использование этого параметра может повлиять на производительность приложения, но оно полезно в ситуациях, когда компьютер можно отключить перед тем, как кэшировали обновления, сохраненные на диске.</span><span class="sxs-lookup"><span data-stu-id="fbc20-119">While using this option may affect your application's performance, it is useful in situations where the computer could be shut off before cached updates are saved to disk.</span></span></p></td>
</tr>
</tbody>
</table>


## <a name="remarks"></a><span data-ttu-id="fbc20-120">Примечания</span><span class="sxs-lookup"><span data-stu-id="fbc20-120">Remarks</span></span>

<span data-ttu-id="fbc20-121">Методы транзакций **BeginTrans,** **CommitTrans** и **Rollback** управляют обработкой транзакций во время сеанса, определенного объектом **Рабочей** области.</span><span class="sxs-lookup"><span data-stu-id="fbc20-121">The transaction methods **BeginTrans**, **CommitTrans**, and **Rollback** manage transaction processing during a session defined by a **Workspace** object.</span></span> <span data-ttu-id="fbc20-122">Эти методы используются с объектом **Workspace,** когда необходимо рассматривать ряд изменений, внесенных в базы данных в сеансе, как одно целое.</span><span class="sxs-lookup"><span data-stu-id="fbc20-122">You use these methods with a **Workspace** object when you want to treat a series of changes made to the databases in a session as one unit.</span></span>

<span data-ttu-id="fbc20-123">Как правило, транзакции используются для поддержания целостности данных, когда необходимо обновлять записи в двух или более таблицах и обеспечивать, чтобы изменения были завершены (зафиксированы) во всех таблицах или вообще нет (откат).</span><span class="sxs-lookup"><span data-stu-id="fbc20-123">Typically, you use transactions to maintain the integrity of your data when you must both update records in two or more tables and ensure changes are completed (committed) in all tables or none at all (rolled back).</span></span> <span data-ttu-id="fbc20-124">Например, при переводе денег с одной учетной записи на другую можно вычесть сумму из одной и добавить ее в другую.</span><span class="sxs-lookup"><span data-stu-id="fbc20-124">For example, if you transfer money from one account to another, you might subtract an amount from one and add the amount to another.</span></span> <span data-ttu-id="fbc20-125">Если обновление не удается, учетные записи перестают балансировать.</span><span class="sxs-lookup"><span data-stu-id="fbc20-125">If either update fails, the accounts no longer balance.</span></span> <span data-ttu-id="fbc20-126">Используйте метод **BeginTrans** перед обновлением первой записи, а затем, если любое последующее обновление сбой, вы можете использовать метод **отката,** чтобы отменить все обновления.</span><span class="sxs-lookup"><span data-stu-id="fbc20-126">Use the **BeginTrans** method before updating the first record, and then, if any subsequent update fails, you can use the **Rollback** method to undo all of the updates.</span></span> <span data-ttu-id="fbc20-127">Используйте метод **CommitTrans** после успешного обновления последней записи.</span><span class="sxs-lookup"><span data-stu-id="fbc20-127">Use the **CommitTrans** method after you successfully update the last record.</span></span>

> [!NOTE]
> <span data-ttu-id="fbc20-128">В одном **объекте Workspace** транзакции всегда являются глобальными для **рабочей** области и не ограничиваются только одним объектом **Подключения** или **Базы данных.**</span><span class="sxs-lookup"><span data-stu-id="fbc20-128">Within one **Workspace** object, transactions are always global to the **Workspace** and aren't limited to only one **Connection** or **Database** object.</span></span> <span data-ttu-id="fbc20-129">Если вы выполняете операции по более чем одному подключению или базе данных в транзакции **Workspace,** решение транзакции (то есть с помощью метода **CommitTrans** или **Rollback)** влияет на все операции на всех подключениях и базах данных в этом рабочем пространстве.</span><span class="sxs-lookup"><span data-stu-id="fbc20-129">If you perform operations on more than one connection or database within a **Workspace** transaction, resolving the transaction (that is, using the **CommitTrans** or **Rollback** method) affects all operations on all connections and databases within that workspace.</span></span>

<span data-ttu-id="fbc20-130">После использования **CommitTrans** нельзя отменить изменения, внесенные во время этой транзакции, если транзакция не будет вложена в другую транзакцию, которая сама откатится.</span><span class="sxs-lookup"><span data-stu-id="fbc20-130">After you use **CommitTrans**, you can't undo changes made during that transaction unless the transaction is nested within another transaction that is itself rolled back.</span></span> <span data-ttu-id="fbc20-131">При вложении транзакций необходимо решить текущую транзакцию, прежде чем разрешить транзакцию на более высоком уровне вложения.</span><span class="sxs-lookup"><span data-stu-id="fbc20-131">If you nest transactions, you must resolve the current transaction before you can resolve a transaction at a higher level of nesting.</span></span>

<span data-ttu-id="fbc20-132">Если вы хотите иметь одновременные транзакции с перекрывающимися, не вложенными областьми, можно создать дополнительные объекты **Workspace,** чтобы содержать одновременные транзакции.</span><span class="sxs-lookup"><span data-stu-id="fbc20-132">If you want to have simultaneous transactions with overlapping, non-nested scopes, you can create additional **Workspace** objects to contain the concurrent transactions.</span></span>

<span data-ttu-id="fbc20-133">Если вы закрываете **объект Workspace** без разрешения каких-либо ожидающих транзакций, транзакции автоматически откатываются обратно.</span><span class="sxs-lookup"><span data-stu-id="fbc20-133">If you close a **Workspace** object without resolving any pending transactions, the transactions are automatically rolled back.</span></span>

<span data-ttu-id="fbc20-134">Если вы используете метод **CommitTrans или** **Rollback** без использования метода **BeginTrans,** возникает ошибка.</span><span class="sxs-lookup"><span data-stu-id="fbc20-134">If you use the **CommitTrans** or **Rollback** method without first using the **BeginTrans** method, an error occurs.</span></span>

<span data-ttu-id="fbc20-135">Некоторые базы данных ISAM, используемые в рабочей области Microsoft Access, могут не поддерживать транзакции, в этом случае свойство **Transactions** объекта **Database** или **объекта Recordset** является **false**.</span><span class="sxs-lookup"><span data-stu-id="fbc20-135">Some ISAM databases used in a Microsoft Access workspace may not support transactions, in which case the **Transactions** property of the **Database** object or **Recordset** object is **False**.</span></span> <span data-ttu-id="fbc20-136">Чтобы убедиться, что база данных поддерживает транзакции, перед использованием метода **BeginTrans** проверьте значение свойства **Transactions** объекта **Database.**</span><span class="sxs-lookup"><span data-stu-id="fbc20-136">To make sure the database supports transactions, check the value of the **Transactions** property of the **Database** object before using the **BeginTrans** method.</span></span> <span data-ttu-id="fbc20-137">Если вы используете объект **Recordset** на основе более чем одной базы данных, проверьте свойство **Transactions** объекта **Recordset.**</span><span class="sxs-lookup"><span data-stu-id="fbc20-137">If you are using a **Recordset** object based on more than one database, check the **Transactions** property of the **Recordset** object.</span></span> <span data-ttu-id="fbc20-138">Если набор **recordset** полностью основан на таблицах баз данных Microsoft Access, всегда можно использовать транзакции.</span><span class="sxs-lookup"><span data-stu-id="fbc20-138">If a **Recordset** is based entirely on Microsoft Access database engine tables, you can always use transactions.</span></span> <span data-ttu-id="fbc20-139">**Однако объекты recordset** на основе таблиц, созданных другими продуктами базы данных, могут не поддерживать транзакции.</span><span class="sxs-lookup"><span data-stu-id="fbc20-139">**Recordset** objects based on tables created by other database products, however, may not support transactions.</span></span> <span data-ttu-id="fbc20-140">Например, вы не можете использовать транзакции в **наборе recordset** на основе таблицы Paradox.</span><span class="sxs-lookup"><span data-stu-id="fbc20-140">For example, you can't use transactions in a **Recordset** based on a Paradox table.</span></span> <span data-ttu-id="fbc20-141">В этом случае свойство **Transactions** является **false**.</span><span class="sxs-lookup"><span data-stu-id="fbc20-141">In this case, the **Transactions** property is **False**.</span></span> <span data-ttu-id="fbc20-142">Если **база данных** или **набор записей** не поддерживают транзакции, методы игнорируются и ошибки не происходят.</span><span class="sxs-lookup"><span data-stu-id="fbc20-142">If the **Database** or **Recordset** doesn't support transactions, the methods are ignored and no error occurs.</span></span>

<span data-ttu-id="fbc20-143">Вы не можете вложенные транзакции, если вы имеете доступ к источникам данных ODBC с помощью двигателя базы данных Microsoft Access.</span><span class="sxs-lookup"><span data-stu-id="fbc20-143">You can't nest transactions if you are accessing ODBC data sources through the Microsoft Access database engine.</span></span>

<span data-ttu-id="fbc20-144">В рабочей области ODBC при использовании **CommitTrans** курсор может перестать быть допустимым.</span><span class="sxs-lookup"><span data-stu-id="fbc20-144">In ODBC workspaces, when you use **CommitTrans** your cursor may no longer be valid.</span></span> <span data-ttu-id="fbc20-145">Используйте метод **Requery** для просмотра изменений в **Наборе записей** или закрытия и повторного **открытия наборов записей.**</span><span class="sxs-lookup"><span data-stu-id="fbc20-145">Use the **Requery** method to view the changes in the **Recordset**, or close and re-open the **Recordset**.</span></span>


> [!NOTE]
> - <span data-ttu-id="fbc20-146">Вы часто можете повысить производительность приложения, разбивая операции, которые требуют доступа к диску в блоки транзакций.</span><span class="sxs-lookup"><span data-stu-id="fbc20-146">You can often improve the performance of your application by breaking operations that require disk access into transaction blocks.</span></span> <span data-ttu-id="fbc20-147">Это буферит операции и может значительно сократить количество случаев доступа к диску.</span><span class="sxs-lookup"><span data-stu-id="fbc20-147">This buffers your operations and may significantly reduce the number of times a disk is accessed.</span></span>
> - <span data-ttu-id="fbc20-148">В рабочей области Microsoft Access транзакции регистрируются в файле, который хранится в каталоге, указанном переменной среды TEMP на рабочей станции.</span><span class="sxs-lookup"><span data-stu-id="fbc20-148">In a Microsoft Access workspace, transactions are logged in a file kept in the directory specified by the TEMP environment variable on the workstation.</span></span> <span data-ttu-id="fbc20-149">Если файл журнала транзакций исчерпает доступное хранилище на диске TEMP, двигатель базы данных вызывает ошибку во время запуска.</span><span class="sxs-lookup"><span data-stu-id="fbc20-149">If the transaction log file exhausts the available storage on your TEMP drive, the database engine triggers a run-time error.</span></span> <span data-ttu-id="fbc20-150">На этом этапе при использовании **CommitTrans** совершается неопределяемая численность операций, но остальные незавершенные операции теряются, и операция должна быть перезапущена.</span><span class="sxs-lookup"><span data-stu-id="fbc20-150">At this point, if you use **CommitTrans**, an indeterminate number of operations are committed, but the remaining uncompleted operations are lost, and the operation has to be restarted.</span></span> <span data-ttu-id="fbc20-151">Метод **отката** освобождает журнал транзакций и откатит все операции в транзакции.</span><span class="sxs-lookup"><span data-stu-id="fbc20-151">Using a **Rollback** method releases the transaction log and rolls back all operations in the transaction.</span></span>
> - <span data-ttu-id="fbc20-152">Закрытие клона **Recordset в** ожидаемой транзакции приведет к неявной операции **отката.**</span><span class="sxs-lookup"><span data-stu-id="fbc20-152">Closing a clone **Recordset** within a pending transaction will cause an implicit **Rollback** operation.</span></span>


