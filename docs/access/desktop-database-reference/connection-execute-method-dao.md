---
title: Connection.Execute Method (DAO)
TOCTitle: Execute Method
ms:assetid: d6140d4e-fa14-6455-525e-49d8aab3dff7
ms:mtpsurl: https://msdn.microsoft.com/library/Ff835040(v=office.15)
ms:contentKeyID: 48547978
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: fd7d0ec92643a8a177134e19ea3e40983efdbb11
ms.sourcegitcommit: c557bbcccf37a6011f89aae1ddd399dfe549d087
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 11/01/2018
ms.locfileid: "25891200"
---
# <a name="connectionexecute-method-dao"></a><span data-ttu-id="52d50-102">Connection.Execute Method (DAO)</span><span class="sxs-lookup"><span data-stu-id="52d50-102">Connection.Execute Method (DAO)</span></span>


<span data-ttu-id="52d50-103">**Применимо к**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="52d50-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="52d50-104">Запуск запроса или выполняет инструкции SQL на указанный объект.</span><span class="sxs-lookup"><span data-stu-id="52d50-104">Runs an action query or executes an SQL statement on the specified object.</span></span>

## <a name="syntax"></a><span data-ttu-id="52d50-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="52d50-105">Syntax</span></span>

<span data-ttu-id="52d50-106">*выражение* . Выполнение (***запроса***, ***Параметры***)</span><span class="sxs-lookup"><span data-stu-id="52d50-106">*expression* .Execute(***Query***, ***Options***)</span></span>

<span data-ttu-id="52d50-107">*выражение* Переменная, которая содержит объект **подключения** .</span><span class="sxs-lookup"><span data-stu-id="52d50-107">*expression* A variable that represents a **Connection** object.</span></span>

### <a name="parameters"></a><span data-ttu-id="52d50-108">Параметры</span><span class="sxs-lookup"><span data-stu-id="52d50-108">Parameters</span></span>

<table>
<colgroup>
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="52d50-109">Имя</span><span class="sxs-lookup"><span data-stu-id="52d50-109">Name</span></span></p></th>
<th><p><span data-ttu-id="52d50-110">Обязательный или необязательный</span><span class="sxs-lookup"><span data-stu-id="52d50-110">Required/Optional</span></span></p></th>
<th><p><span data-ttu-id="52d50-111">Тип данных</span><span class="sxs-lookup"><span data-stu-id="52d50-111">Data Type</span></span></p></th>
<th><p><span data-ttu-id="52d50-112">Описание</span><span class="sxs-lookup"><span data-stu-id="52d50-112">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="52d50-113">Query</span><span class="sxs-lookup"><span data-stu-id="52d50-113">Query</span></span></p></td>
<td><p><span data-ttu-id="52d50-114">Обязательный</span><span class="sxs-lookup"><span data-stu-id="52d50-114">Required</span></span></p></td>
<td><p><span data-ttu-id="52d50-115"><strong>Строка</strong></span><span class="sxs-lookup"><span data-stu-id="52d50-115"><strong>String</strong></span></span></p></td>
<td><p><span data-ttu-id="52d50-116"><strong>Строка</strong> , которая является значение свойства <strong>Name</strong> объекта <strong>QueryDef</strong> или инструкции SQL.</span><span class="sxs-lookup"><span data-stu-id="52d50-116">A <strong>String</strong> that is an SQL statement or the <strong>Name</strong> property value of a <strong>QueryDef</strong> object.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="52d50-117">Options</span><span class="sxs-lookup"><span data-stu-id="52d50-117">Options</span></span></p></td>
<td><p><span data-ttu-id="52d50-118">Необязательный</span><span class="sxs-lookup"><span data-stu-id="52d50-118">Optional</span></span></p></td>
<td><p><span data-ttu-id="52d50-119"><strong>Variant</strong></span><span class="sxs-lookup"><span data-stu-id="52d50-119"><strong>Variant</strong></span></span></p></td>
<td><p><span data-ttu-id="52d50-120">Константа или сочетание констант, который определяет характеристики целостности данных запроса, как указано в настройки.</span><span class="sxs-lookup"><span data-stu-id="52d50-120">A constant or combination of constants that determines the data integrity characteristics of the query, as specified in Settings.</span></span></p></td>
</tr>
</tbody>
</table>


## <a name="remarks"></a><span data-ttu-id="52d50-121">Замечания</span><span class="sxs-lookup"><span data-stu-id="52d50-121">Remarks</span></span>

<span data-ttu-id="52d50-122">Следующие константы **[RecordsetOptionEnum](recordsetoptionenum-enumeration-dao.md)** можно использовать для доступа к параметрам.</span><span class="sxs-lookup"><span data-stu-id="52d50-122">You can use the following **[RecordsetOptionEnum](recordsetoptionenum-enumeration-dao.md)** constants for options.</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="52d50-123">Константа</span><span class="sxs-lookup"><span data-stu-id="52d50-123">Constant</span></span></p></th>
<th><p><span data-ttu-id="52d50-124">Описание</span><span class="sxs-lookup"><span data-stu-id="52d50-124">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="52d50-125"><strong>dbDenyWrite</strong></span><span class="sxs-lookup"><span data-stu-id="52d50-125"><strong>dbDenyWrite</strong></span></span></p></td>
<td><p><span data-ttu-id="52d50-126">Запрещает разрешение на запись другим пользователям (только для рабочих областей Microsoft Access).</span><span class="sxs-lookup"><span data-stu-id="52d50-126">Denies write permission to other users (Microsoft Access workspaces only).</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="52d50-127"><strong>dbInconsistent</strong></span><span class="sxs-lookup"><span data-stu-id="52d50-127"><strong>dbInconsistent</strong></span></span></p></td>
<td><p><span data-ttu-id="52d50-128">(По умолчанию) Выполняет несогласованных обновлений (только для рабочих областей Microsoft Access).</span><span class="sxs-lookup"><span data-stu-id="52d50-128">(Default) Executes inconsistent updates (Microsoft Access workspaces only).</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="52d50-129"><strong>dbConsistent</strong></span><span class="sxs-lookup"><span data-stu-id="52d50-129"><strong>dbConsistent</strong></span></span></p></td>
<td><p><span data-ttu-id="52d50-130">Выполняет согласованности обновлений (только для рабочих областей Microsoft Access).</span><span class="sxs-lookup"><span data-stu-id="52d50-130">Executes consistent updates (Microsoft Access workspaces only).</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="52d50-131"><strong>dbSQLPassThrough</strong></span><span class="sxs-lookup"><span data-stu-id="52d50-131"><strong>dbSQLPassThrough</strong></span></span></p></td>
<td><p><span data-ttu-id="52d50-132">Выполняет запрос к серверу.</span><span class="sxs-lookup"><span data-stu-id="52d50-132">Executes an SQL pass-through query.</span></span> <span data-ttu-id="52d50-133">Если этот параметр передает инструкции SQL к базе данных ODBC для обработки (только для рабочих областей Microsoft Access).</span><span class="sxs-lookup"><span data-stu-id="52d50-133">Setting this option passes the SQL statement to an ODBC database for processing (Microsoft Access workspaces only).</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="52d50-134"><strong>dbFailOnError</strong></span><span class="sxs-lookup"><span data-stu-id="52d50-134"><strong>dbFailOnError</strong></span></span></p></td>
<td><p><span data-ttu-id="52d50-135">Откат обновления при возникновении ошибки (только для рабочих областей Microsoft Access).</span><span class="sxs-lookup"><span data-stu-id="52d50-135">Rolls back updates if an error occurs (Microsoft Access workspaces only).</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="52d50-136"><strong>dbSeeChanges</strong></span><span class="sxs-lookup"><span data-stu-id="52d50-136"><strong>dbSeeChanges</strong></span></span></p></td>
<td><p><span data-ttu-id="52d50-137">Создает ошибку времени выполнения, если другой пользователь изменение данных, редактировании (только для рабочих областей Microsoft Access).</span><span class="sxs-lookup"><span data-stu-id="52d50-137">Generates a run-time error if another user is changing data you are editing (Microsoft Access workspaces only).</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="52d50-138"><strong>dbRunAsync</strong></span><span class="sxs-lookup"><span data-stu-id="52d50-138"><strong>dbRunAsync</strong></span></span></p></td>
<td><p><span data-ttu-id="52d50-139">Выполняет асинхронный запрос (только объекты технология ODBCDirect подключения и QueryDef).</span><span class="sxs-lookup"><span data-stu-id="52d50-139">Executes the query asynchronously (ODBCDirect Connection and QueryDef objects only).</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="52d50-140"><strong>dbExecDirect</strong></span><span class="sxs-lookup"><span data-stu-id="52d50-140"><strong>dbExecDirect</strong></span></span></p></td>
<td><p><span data-ttu-id="52d50-141">Выполняет оператор без первого вызова функции SQLPrepare ODBC API (только объекты технология ODBCDirect подключения и QueryDef).</span><span class="sxs-lookup"><span data-stu-id="52d50-141">Executes the statement without first calling SQLPrepare ODBC API function (ODBCDirect Connection and QueryDef objects only).</span></span></p></td>
</tr>
</tbody>
</table>

> [!NOTE]
> <span data-ttu-id="52d50-142">Рабочие области технология ODBCDirect не поддерживаются в Microsoft Access 2013.</span><span class="sxs-lookup"><span data-stu-id="52d50-142">ODBCDirect workspaces are not supported in Microsoft Access 2013.</span></span> <span data-ttu-id="52d50-143">Использование ADO, если вы хотите получить доступ к внешним источникам данных без использования ядро базы данных Microsoft Access.</span><span class="sxs-lookup"><span data-stu-id="52d50-143">Use ADO if you want to access external data sources without using the Microsoft Access database engine.</span></span>

> [!NOTE]
> <span data-ttu-id="52d50-144">Константы **dbConsistent** и **dbInconsistent** являются взаимоисключающими.</span><span class="sxs-lookup"><span data-stu-id="52d50-144">The constants **dbConsistent** and **dbInconsistent** are mutually exclusive.</span></span> <span data-ttu-id="52d50-145">Можно использовать одно или другое, но не оба в экземпляре **OpenRecordset**.</span><span class="sxs-lookup"><span data-stu-id="52d50-145">You can use one or the other, but not both in a given instance of **OpenRecordset**.</span></span> <span data-ttu-id="52d50-146">С помощью **dbConsistent** и **dbInconsistent** приводит к ошибке.</span><span class="sxs-lookup"><span data-stu-id="52d50-146">Using both **dbConsistent** and **dbInconsistent** causes an error.</span></span>

<span data-ttu-id="52d50-147">Метод **Execute** действителен только для запросов.</span><span class="sxs-lookup"><span data-stu-id="52d50-147">The **Execute** method is valid only for action queries.</span></span> <span data-ttu-id="52d50-148">Если вы используете **Execute** с запрос другого типа, возникает ошибка.</span><span class="sxs-lookup"><span data-stu-id="52d50-148">If you use **Execute** with another type of query, an error occurs.</span></span> <span data-ttu-id="52d50-149">Поскольку запрос не возвращает все записи, **выполнение** не возвращает **набор записей**.</span><span class="sxs-lookup"><span data-stu-id="52d50-149">Because an action query doesn't return any records, **Execute** doesn't return a **Recordset**.</span></span> <span data-ttu-id="52d50-150">(Выполнение запроса к серверу в рабочей области технология ODBCDirect не возвращает ошибку при **записей** не возвращаются.)</span><span class="sxs-lookup"><span data-stu-id="52d50-150">(Executing an SQL pass-through query in an ODBCDirect workspace will not return an error if a **Recordset** isn't returned.)</span></span>

<span data-ttu-id="52d50-151">Используйте свойство **RecordsAffected** объекта **подключения**, **базы данных**или **QueryDef** для определения количества записей, влияет на последнюю метод **Execute** .</span><span class="sxs-lookup"><span data-stu-id="52d50-151">Use the **RecordsAffected** property of the **Connection**, **Database**, or **QueryDef** object to determine the number of records affected by the most recent **Execute** method.</span></span> <span data-ttu-id="52d50-152">Например **RecordsAffected** содержит число записей удален, обновляется или вставляется при выполнении запроса.</span><span class="sxs-lookup"><span data-stu-id="52d50-152">For example, **RecordsAffected** contains the number of records deleted, updated, or inserted when executing an action query.</span></span> <span data-ttu-id="52d50-153">При использовании метода **Execute** для выполнения запроса, свойство **RecordsAffected** объекта **QueryDef** присваивается количество записей.</span><span class="sxs-lookup"><span data-stu-id="52d50-153">When you use the **Execute** method to run a query, the **RecordsAffected** property of the **QueryDef** object is set to the number of records affected.</span></span>

<span data-ttu-id="52d50-154">В рабочей области Microsoft Access, если предоставить синтаксически правильные инструкции SQL и имеют соответствующие разрешения метода **Execute** не ошибка — даже в том случае, если не одной строки можно изменить или удалить.</span><span class="sxs-lookup"><span data-stu-id="52d50-154">In a Microsoft Access workspace, if you provide a syntactically correct SQL statement and have the appropriate permissions, the **Execute** method won't fail — even if not a single row can be modified or deleted.</span></span> <span data-ttu-id="52d50-155">Таким образом всегда используйте параметр **dbFailOnError** , при использовании метода **Execute** для запуска и обновления или удаления запроса.</span><span class="sxs-lookup"><span data-stu-id="52d50-155">Therefore, always use the **dbFailOnError** option when using the **Execute** method to run an update or delete query.</span></span> <span data-ttu-id="52d50-156">Этот параметр, возникает ошибка времени выполнения и выполняет откат всех изменений успешно Если никакой из записей влияет на блокируется и не может быть обновлении или удалении.</span><span class="sxs-lookup"><span data-stu-id="52d50-156">This option generates a run-time error and rolls back all successful changes if any of the records affected are locked and can't be updated or deleted.</span></span>

<span data-ttu-id="52d50-157">В более ранних версиях ядра базы данных Microsoft Jet SQL операторы автоматически были внедрены в неявные транзакции.</span><span class="sxs-lookup"><span data-stu-id="52d50-157">In earlier versions of the Microsoft Jet database engine, SQL statements were automatically embedded in implicit transactions.</span></span> <span data-ttu-id="52d50-158">Если не удалось выполнить инструкции, с **dbFailOnError** , всей оператор будет выполнен откат.</span><span class="sxs-lookup"><span data-stu-id="52d50-158">If part of a statement executed with **dbFailOnError** failed, the entire statement would be rolled back.</span></span> <span data-ttu-id="52d50-159">В целях повышения производительности эти неявные транзакции были удалены, начиная с версии 3.5.</span><span class="sxs-lookup"><span data-stu-id="52d50-159">To improve performance, these implicit transactions were removed starting with version 3.5.</span></span> <span data-ttu-id="52d50-160">При обновлении старых кода DAO, необходимо принять во внимание использование явных транзакций вокруг **выполнение** инструкций.</span><span class="sxs-lookup"><span data-stu-id="52d50-160">If you are updating older DAO code, be sure to consider using explicit transactions around **Execute** statements.</span></span>

<span data-ttu-id="52d50-161">Для достижения наилучшей производительности в рабочую область для Microsoft Access, особенно в многопользовательской среде вложить метода **Execute** внутри транзакции.</span><span class="sxs-lookup"><span data-stu-id="52d50-161">For best performance in a Microsoft Access workspace, especially in a multiuser environment, nest the **Execute** method inside a transaction.</span></span> <span data-ttu-id="52d50-162">Используйте метод **BeginTrans** на текущий объект **рабочей области** , а затем используйте метод **Execute** и завершения транзакции с помощью метода **CommitTrans** в **рабочей области**.</span><span class="sxs-lookup"><span data-stu-id="52d50-162">Use the **BeginTrans** method on the current **Workspace** object, then use the **Execute** method, and complete the transaction by using the **CommitTrans** method on the **Workspace**.</span></span> <span data-ttu-id="52d50-163">Это сохраняет изменения на диске и освобождает любые блокировки во время выполнения запроса.</span><span class="sxs-lookup"><span data-stu-id="52d50-163">This saves changes on disk and frees any locks placed while the query is running.</span></span>

